# MuJoCo Blocks Stacking Task
**Part of the [MujocoAR](https://github.com/omarrayyann/MujocoAR) package demos**

A MuJoCo simulation environment of a simple blocks stacking task. The simulation includes an operational space controller to handle the movement of the KUKA-iiwa14 arm with a gripper at the end.


<table>
<!--   <tr>
    <th><code>camera_name="whole_view"</code></th>
    <th><code>camera_name="top_view"</code></th>
    <th><code>camera_name="side_view"</code></th>
    <th><code>camera_name="front_view"</code></th>
  </tr> -->
  <tr>
    <td><img src="https://github.com/user-attachments/assets/dbb1dbb7-5dff-4c24-88fb-9f4b8afd7d8b" width="800px" /></td>
    <td><img src="https://github.com/user-attachments/assets/df43bb40-6e58-4e94-8d1c-a4fa90359d65" width="800px" /></td>
    <td><img src="https://github.com/user-attachments/assets/cc605670-4717-47e9-8ea3-7f71493b7cad" width="800px" /></td>
  </tr>
</table>


## MuJoCo AR Setup

```python
# Initializing MuJoCo AR
self.mujocoAR = MujocoARConnector(mujoco_model=self.mjmodel,mujoco_data=self.mjdata)

# Linking a Target Site with the AR Position
self.mujocoAR.link_site(
  name="eef_target",
  scale=3.0,
  position_origin=self.pos_origin,
  rotation_origin=self.rot_origin,
  toggle_fn=lambda: setattr(self, 'grasp', not self.grasp),
)

# Start!
self.mujocoAR.start()
```

## Usage Guide

1. **Clone the repository**:

   ```bash
   git clone https://github.com/omarrayyann/mujoco_blocks_stacking.git
   cd mujoco_blocks_stacking
   
3. **Install MujocoAR and othe Requirements**:
   ```bash
   
   pip install requirements.txt
   
4. **Download the [MuJoCo AR App](https://apps.apple.com/jo/app/past-code/id1551535957) from the App Store.**
   
5. **Run the application**:

   ```bash
   mjpython main.py
   
6. **Enter the IP and Port shown into the app's start screen to start. Make sure to be connected to the same Wi-Fi network as the device. Incase of a latency, I recommend connecting to your phone's hotspot.**

## Author

Omar Rayyan (olr7742@nyu.edu)
