I ran docker compose up -d: it's saying my pnpm-lock.yaml is not found because it's in my app folder instead of in the root. My docker file says "COPY pnpm-lock.yaml package.json ./" so it's looking for it. 

how to fix: 
app:
  build: ./app
  in yaml file. or:
  change docker file to "COPY app/package.json app/pnpm-lock.yaml ./"

Why this error occurred
  Docker builds from a “build context.”

If you say:

build: .

Docker only sees files in that directory tree.

