FROM alpine:latest

# Install abuild and required dependencies
RUN apk update && \
    apk add --no-cache abuild

# Create a working directory
WORKDIR /build

# Set the cache directory to be owned by the user
RUN chown -R 1000:1000 /var/cache/distfiles

# We'll use a volume mount for the local files
# The actual mounting will be done at runtime with docker run -v

# Switch to non-root user
USER 1000

# Run abuild checksum followed by abuild clean
CMD ["sh", "-c", "abuild checksum && abuild clean"]