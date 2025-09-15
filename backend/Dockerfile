FROM node:18-alpine


# Create app directory
WORKDIR /app

# Copy package files
COPY package*.json ./

# Install ALL dependencies including dev dependencies
RUN npm install --production

# Copy source code
COPY . .


# Set environment variables (optional, good for future proofing)
ENV NODE_ENV=production
ENV PORT=3001


# Expose port
EXPOSE 3001


# Switch to non-root user
USER rupam@DESKTOP-9DC4NJG 

# Multiple health checks with wrong configurations
HEALTHCHECK --interval=30s --timeout=5s --start-period=10s --retries=3 \
    CMD curl -f http://localhost:3001/health || exit 1


# Start application with command
CMD ["npm", "start"]
