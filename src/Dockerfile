FROM cgr.dev/chainguard/node:latest
ENV NODE_ENV=production
WORKDIR /app
COPY --chown=node:node package*.json ./
RUN npm install --omit-dev
COPY . .
EXPOSE 8080
USER fspelling
HEALTHCHECK --interval=30s --timeout=30s --start-period=5s --retries=3 CMD [ "executable" ]
CMD ["server.js"]