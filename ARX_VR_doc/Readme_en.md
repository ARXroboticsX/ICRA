<h1 style="text-align: center;">VR Remote OpenSource</h1>


<h3 style="text-align: center;">ARX 方舟无限</h3>

<p style="text-align: center;">
  <a href="Readme_zh-cn.md">中文</a> | 
  <a href="Readme_en.md">English</a>
</p>
<hr style="text-align: center;">
<h2 style="text-align: ">🎥 Demo Demonstration</h2>


<p align="center">
  <a href="https://x.com/ARX_Zhang/status/1805712418125021191" target="_blank">
    <img src="./imgs/video_demo.png" alt="Watch the video" style="width: 80%;">
  </a>
</p>
## ℹ️ Instruction

This repository serves as a communication bridge for spatial positioning data between Meta Quest 3/Quest 3S and ARX (Ark Infinite) products.

The following are the product models supported by this repository:

<table style="width: 100%; text-align: center; border-collapse: collapse;">
  <thead>
    <tr>
      <th>🦾 Product Model</th>
      <th>🔗 Repository Link</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>ARX_X5 RoboticArm</td>
      <td><a href="#">https://github.com/ARXroboticsX/ARX_X5</a></td>
    </tr>
    <tr>
      <td>ARX_R5系列 RoboticArm</td>
      <td><a href="#">https://github.com/ARXroboticsX/R5</a></td>
    </tr>
    <tr>
      <td>ARX_LIFT Data Acquisition Platform</td>
      <td><a href="#">https://github.com/ARXroboticsX/LIFT</a></td>
    </tr>
    <tr>
      <td>ARX_X7 Series</td>
      <td><a href="#">https://github.com/ARXroboticsX/X7s</a></td>
    </tr>
  </tbody>
</table>

硬件连接参考 

---


##  1.🖥️Environment

Ubuntu 20.04  ROS Noetic(AMD64 ARM64)
Ubuntu 22.04 ROS Humble(AMD64)
⚠️ **Note:** Additional configuration is required for other operating systems.

### 1.1**📝**VR Preparation

If you are not familiar with Quest 3 or have never used a VR device before, you can refer to the brief [Introduction to Quest 3](熟悉Quest3.md). If possible, we also recommend the [official Meta tutorial](https://www.meta.com/help/quest/1994971530885728/?srsltid=AfmBOopU0puvld0dVfJEg2WYxiXC7Sr_6s5OVvPvYB0qFBsDN2HcEyxA).

You will need to install the APK onto your Meta Quest via SideQuest. For detailed installation steps, please refer to the [Quest 3 APK Installation Guide](Quest3_APK_Install.md)

### 1.2 📝 PC/NUC Preparation

Install the appropriate operating system as described in the test environment section, and download the code corresponding to the product model. Using the ARX_LIFT data acquisition platform (ROS1 version) as an example:

Open a terminal:

```bash
git clone https://github.com/ARXroboticsX/LIFT.git
# Enter ARX_VR_SDK
cd ARX_VR_SDK/ROS
# Run port.sh to install runtime libraries
sudo ./port.sh
```

---

## 2.🟢Launching VR

### 2.1❗ Precautions

1. All personnel should maintain a safe distance from the robotic arm to avoid any potential risks.
2. Before performing real-machine VR teleoperation of the robotic arm, please make sure to carefully read the operation instructions.
3. Before operating the robotic arm, ensure that both the zero-point and the Meta viewpoint are properly reset to avoid accidental operations.

### 2.2 🕹️VR  Operation

After confirming correct hardware connections, allow USB debugging.

[How to control the robotic arm via X5_MR_Control (software)](VR软件操作.md)

### 2.3🖱️电脑NUC操作

```bash
# Enter ARX_VR_SDK
cd ARX_VR_SDK/ROS
# Run port.sh to install runtime libraries
sudo ./ARX_VR.sh
# Follow the instructions in the manual, and view VR output data via topics
source install/setup.bash && ros2 topic echo /ARX_VR_L
source install/setup.bash && ros2 topic echo /ARX_VR_R
```

 ### 2.4 🚪 Exit

Hold the Meta and A/X buttons to reset, then close the VR application and shut down the PC-side program.

# 3.📦Hardware List

*Note: Due to regional differences, links are for reference only.*

<table style="width: 100%; text-align: center; border-collapse: collapse;">
  <thead>
    <tr>
      <th>Name</th>
      <th>Quantity</th>
      <th>Link</th>
      <th>Note</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>ARX Robotic Arm Series</td>
      <td>1</td>
      <td><a href="https://arx-x.com/">Official Website</a></td>
      <td>X5, R5, LIFT, X7S Series</td>
    </tr>
    <tr>
      <td>Meta Quest 3</td>
      <td>1</td>
      <td><a href="https://www.amazon.com/Meta-Quest-128GB-Breakthrough-Reality-3/dp/B0C8VKH1ZH">Amazon</a></td>
      <td>Developer mode required for APK installation</td>
    </tr>
    <tr>
      <td>PC / NUC</td>
      <td>1</td>
      <td></td>
      <td>Ubuntu 20 or Ubuntu 22</td>
    </tr>
    <tr>
      <td>Serial Box</td>
      <td>1</td>
      <td></td>
      <td>Must support USB Type-C serial</td>
    </tr>
    <tr>
      <td>Dual Type-C Data Cables</td>
      <td>2</td>
      <td><a href="https://detail.tmall.com/item.htm?id=601375235325&pisk=gQsT_lYut4v696I9KOznornIRPwHXyXNL1WSmIAil6CdMTHGSEADlnCPwEi07hYvD6OhjCXMfKTfi__M1NAmDiCF6cmDfsqvGT7U3CvGjxpfR1ncSOAGJxKNxNmDs5-Ah_xYZ7quqOWwYnNuZqOu5E-WeIisidTBAnvA-OgiFOWw0IMnGzbCQxKtegkXhIwpAKp-5nT6CeGBTKvsGsO6RX9JUntfGFMBdL9m5d9X1vwpeK9sfc96RB9k3Kg1GnwddBJXcd1XcxvYBBk6BmQyaYmJWzBscmspBealCB6Vn-vBWZB997N5vg89NOOKc7z5C2d6FgNn7LLOMeshnYmDTO_PgL1s17YNhwCpB6VEJpQl_gKCVWoAMTSF9p17D0A1LTbk7GamqUKp6Ej1B5EkJObfDaW3u4XeyabWJirrbOLyOhj6Vul6iwXRDKI4gkCRUM5pd_ZxmIjN6G-GA8gpiaJf4VIl24RsZQpm5JeKuq86LkeNnjxTMdRepQ265qu2opJpZJFIuq8pZpduCI3queih.&pvid=f368dda4-ccb0-462d-93d5-b4ad297fd544&scm=1007.56608.416674.0&skuId=5902303315322&spm=tbpc.boughtlist.repurchaseitem.d1.274c2e8dSONtf4&xxc=home_recommend">TaoBao</a></td>
      <td>USB Type-C cable</td>
    </tr>
  </tbody>
</table>



# 4 🤝Acknowledgements

**[SideQuest](https://github.com/SideQuestVR/SideQuest)**：https://github.com/SideQuestVR/SideQuest

Meta XR All-in-One SDK：https://assetstore.unity.com/packages/tools/integration/meta-xr-all-in-one-sdk

