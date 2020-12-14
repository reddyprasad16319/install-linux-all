# install-linux-all
All soft install in linux os 
# update os 
    1  sudo yum update
    2  ls
 # install openjdk   
    3  sudo yum list | grep jdk1.8
    4  sudo yum list | grep jdk
    5  sudo yum install java-1.8.0-openjdk-devel.x86_64
    6  sudo java
    7  sudo java --version
    8  sudo java -version
    9  java c
   10  javac
   11  sudo update-alternatives java
   12  sudo update-alternatives --config java
   13  sudo update-alternatives --config javac
 # Dwnload apache 8  
   
   14  sudo wget https://mirrors.estointernet.in/apache/tomcat/tomcat-8/v8.5.61/bin/apache-tomcat-8.5.61.zip
   15  ls
   16  sudo yum instll unzip
   17  sudo yum install unzip
   18  unzip apache-tomcat-8.5.61.zip
   19  ls
   20  rm -rf apache-tomcat-8.5.61.zip
   21  ls
   22  rm apache-tomcat-8.5.61/ apache8
   23  ls
   24  mv apache-tomcat-8.5.61/ apache8
   25  ls
   26  cd apache8/
   27  ls
   28  cd bin/
   29  ls
   30  ./catalina.sh
   31  chmod o-x catalina.sh
   32  ls
   33  ll
   34  chmod 777 catalina.sh
   35  ls
   36  chmod 777 startup.sh shutdown.sh
   37  ls
   38  ./startup.sh
   39  curl ifconfig.co
   40  ll
   41  cd ..
   42  find / name context.xml
   43  cd -
  # change Context.xml File  
   45  sudo find / -name context.xml
   46  sudo vim /home/ec2-user/apache8/webapps/host-manager/META-INF/context.xml
                       <!--  <Valve className="org.apache.catalina.valves.RemoteAddrValve"
                            allow="127\.\d+\.\d+\.\d+|::1|0:0:0:0:0:0:0:1" />  -->

   47  sudo vim /home/ec2-user/apache8/webapps/manager/META-INF/context.xml
                        <!--  <Valve className="org.apache.catalina.valves.RemoteAddrValve"
                              allow="127\.\d+\.\d+\.\d+|::1|0:0:0:0:0:0:0:1" /> -->

   48  ./shutdown.sh
   49  ./startup.sh
   50  cd ..
   51  ll
   52  cd conf/
   53  ll
   54  sudo vim tomcat-users.xml add below line 
             <role rolename="manager-gui"/>
               <user username="tomcat" password="tomcat" roles="manager-gui"/>

   55  cd ../bin/
   56  ./shutdown.sh
   57  ./startup.sh
   58  sudo vim ../conf/tomcat-users.xml
   59  ./shutdown.sh
   60  ./startup.sh
   61  sudo vim ../conf/tomcat-users.xml
   62  ./shutdown.sh
   63  ./startup.sh
   64  ls
   65  cd ..
   66  ls
   67  cd conf/
   68  ls
 # add port  
   69  sudo vim server.xml 
               change port 9090
   70  cd
   71  cd apache8/bin/
   72  ./shutdown.sh
   73  ./startup.sh
   74  sudo vim  ../conf/server.xml
   75  ./shutdown.sh
   76  ./startup.sh
   77  cd
 # install jenkins   
   
   78  sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
   79  sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
   80  yum install jenkins -y
   81  yum install jenkins -y   yum install jenkins
   82  yum install jenkins
   83  sudo   yum install jenkins
   84  service jenkins start
   85  sudo service jenkins starta
   86  sudo chkconfig jenkins on
   87  sudo service jenkins start
   88  sudo chkconfig jenkins on
   89  sudo cat /var/lib/jenkins/secrets/initialAdminPassword
   

