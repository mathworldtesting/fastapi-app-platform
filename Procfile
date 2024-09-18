# web: This declares a web process type and tells the platform (like Digital Ocean) 
# that this command should be used to start your web server.
# gunicorn: This is the command to start the Gunicorn server.
# -w 4: Sets the number of worker processes to 4. You can also use 2 for most bare usecases or even 1.
# -k uvicorn.workers.UvicornWorker: Specifies the worker class to be Uvicorn workers, suitable for ASGI applications.
# --bind 0.0.0.0:8080: Tells Gunicorn to bind to all public IPs at port 8080.
# --worker-tmp-dir /dev/shm: Sets the temporary directory for workers to /dev/shm.
# app:app: Indicates the Python module (app) and the application object (app) to run.

web: gunicorn -w 2 -k uvicorn.workers.UvicornWorker --bind 0.0.0.0:8080 --worker-tmp-dir /dev/shm app:app
