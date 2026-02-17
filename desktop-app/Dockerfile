# Stage 1: Prepare resources by copying/transforming browser-version files
FROM node:lts-alpine AS prepare

WORKDIR /app

# Copy the entire repo (context is the repo root)
COPY . .

# Run the prepare script to generate desktop-app resources
RUN node desktop-app/prepare.js

# Stage 2: Build Neutralinojs binaries
FROM node:lts-alpine AS build

WORKDIR /app/desktop-app

# Copy only the desktop-app directory with prepared resources
COPY --from=prepare /app/desktop-app .

# Install pinned neu CLI from package.json, then build both embedded + portable
RUN npm install --ignore-scripts && npm run build:all

# Final stage: Export the dist artifacts
FROM alpine:lts

WORKDIR /output

COPY --from=build /app/desktop-app/dist/ .

CMD ["echo", "Build artifacts are in /output. Use 'docker cp' to extract them."]
