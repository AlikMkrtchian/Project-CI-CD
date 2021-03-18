
# Maven-project CI/CD

 ## 1) Developer sends - git push to test branch.
     1.1 Jenkins see the changes with a webhook and starts building the project.
     1.2 Jenkins via ssh transfer passes the build variable to the specified directory on the Ansible server and runs the playbook command.
     1.3 Ansible uploads the file to the tomcat server via copy.
     
 ## 2) The developer pushes to the master branch
       2.1 Git push the change,Jenkins builds a new build and sends it to the ansible server along with the dockerfile.
       2.2 ansible launches a container and pushes it to dockerhub after ansible went to the docker server and starts a new container.  
 
 
 
 # copyfile.yml = Test 
 
 # create_docker_container = Prod   
 
 ![Images](https://github.com/AlikMkrtchian/Project-CI-CD/blob/master/DeepinScreenshot_Navigator_20210318115825.png)
 
 
 # Test-result 
 
 ![Images](https://github.com/AlikMkrtchian/Project-CI-CD/blob/master/DeepinScreenshot_Navigator_20210318120712.png)
  ![Images](https://github.com/AlikMkrtchian/Project-CI-CD/blob/master/DeepinScreenshot_Navigator_20210318120301.png)
  
  
 # Prod-result
   ![Images](https://github.com/AlikMkrtchian/Project-CI-CD/blob/master/DeepinScreenshot_Navigator_20210318120218.png)
    ![Images](https://github.com/AlikMkrtchian/Project-CI-CD/blob/master/DeepinScreenshot_Navigator_20210318120227.png)
     ![Images](https://github.com/AlikMkrtchian/Project-CI-CD/blob/master/DeepinScreenshot_select-area_20210318124201.pngg)
     
