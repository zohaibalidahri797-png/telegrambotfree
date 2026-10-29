The ready-to-serve frontend was extracted from the source ZIP into public/. Netlify publishes that folder directly, without a build command. The original ZIP remains as the source archive. A ZIP committed as a repository file is not automatically extracted for deployment.

The homepage is public/index.html. Existing .html links and extensionless page URLs are supported. Unknown URLs retain a real 404 response using public/404.html.

This configuration deploys the static frontend. The backend API and long-running bot runtime remain separate services. The existing frontend uses demo mode when the backend is unavailable; authentication and real bot operations require a configured backend. No catch-all rule masks missing APIs with HTML responses.
