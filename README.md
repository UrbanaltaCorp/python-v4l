python-v4l
==========

Ctypes python bindings for Video 4 Linux (v4l)

Based on original work of authors Tamas Kemenczy, Pete Eberlein and Vesselin Petkov for Linux 2.6.34 
[https://launchpad.net/python-v4l2]

### Example Usage

```python
import v4l2
import fcntl
vd = open('/dev/video0', 'rw')
cp = v4l2.v4l2_capability()
fcntl.ioctl(vd, v4l2.VIDIOC_QUERYCAP, cp)
```
    0
```python
cp.driver
```
    'uvcvideo'
```python
cp.card
```
    'USB 2.0 Camera'

