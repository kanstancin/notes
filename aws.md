# aws notes
### how to connect jupyter to aws

1. set up Jupyter password
2. set up ssl
3. cd to project folder and run
```bash
jupyter notebook --certfile=~/ssl/mycert.pem --keyfile ~/ssl/mykey.key
```
4. on local machine run
```bash
ssh -i "noodle-finder.pem" -N -f -L 8880:localhost:8888 ubuntu@ec2-52-6-27-139.compute-1.amazonaws.com
```
5. on local machine open in browser
```bash
https://localhost:8880
```