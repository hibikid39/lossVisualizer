# lossVisualizer
visualize losses by tensorboard

# Using
In host, build container.
```
docker build -t [image_name] .
docker run -it --name [container_name] -v $(pwd):/work -p 6006:6006 [image_name]:latest
```
In container, start tensorboard.
```
tensorboard --port 6006 --logdir [log_dir] --host=0.0.0.0
```
Access localhost:6006 by host's browser.
