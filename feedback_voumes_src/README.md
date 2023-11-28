_Build the image_ 

* docker build -t feedback-nodes:volumes .

Run the container on that image in detach mode with autamtic deletion of the container once it stops with volumes to keep the feedbacks files avaliable after killing the container 

* docker run -d --rm -p 3000:80 --name feedback-app -v feedback:/app/feedback -v "/home/amr/Desktop/personal/docker_projects/docker_projects/feedback_voumes_src:/app:ro" -v /app/node_modules -v /app/temp feedback-nodes:volumes