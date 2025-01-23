This is a blog website,developed with Django,using Postgres database and Docker.

In the website,users are able to view,add,delete posts.The 'mod' users can also ban other users.

Steps to run the project:
--  Install docker
--  Clone the code
--  cd into Final_Project folder
--  docker-compose up -d

Now the project should be up and running at localhost:8000

You have to create a superuser,follow the steps to do it:
--  Open a terminal
--  docker ps(a list of the running containers should be appeared) 
--  copy either the container ID or the name of the django container(must be the one with the final_project-web image that is running on 8000 port)
--  docker exec -it <container ID or name> bash(to get access in the container that the application running)
--  python manage.py createsuperuser

Final steps:
--  Login to django admin(localhost:8000/admin with the superuser)
--  Click on groups(one group should be available 'default')
--  In group 'default' give the following permissions(can add post,can view post)
--  Create a new group with the name 'mod' and give all permissions

Now the project should be fully functional. Enjoy!