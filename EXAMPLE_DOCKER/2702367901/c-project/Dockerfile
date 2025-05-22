# Stage 1: Build
FROM gcc:latest AS build
WORKDIR /app
COPY src/app.c .
RUN gcc -o app app.c

# Stage 2: Runtime
FROM alpine:latest
WORKDIR /app
# Tambahkan library runtime C
RUN apk add --no-cache libc6-compat
COPY --from=build /app/app .
CMD ["./app"]