# Frontend Build/Run
FROM nginx:alpine

# Install envsubst (included in gettext package)
RUN apk add --no-cache gettext

# Set workdir
WORKDIR /usr/share/nginx/html

# Copy the frontend file
COPY index.html index.template.html

# Default backend URL (can be overridden at runtime)
ENV BACKEND_URL=http://localhost:8080

# Expose port 80
EXPOSE 80

# On startup:
# 1. Replace placeholder in template with ENV variable
# 2. Inject a script tag to set window.BACKEND_URL
# 3. Start Nginx
CMD ["/bin/sh", "-c", "echo \"<script>window.BACKEND_URL='${BACKEND_URL}';</script>$(cat index.template.html)\" > index.html && nginx -g 'daemon off;'"]
