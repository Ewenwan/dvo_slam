# Dense Visual Odometry and SLAM (dvo_slam)

*NOTE: this is an alpha release APIs and parameters are going to change in near future. No support is provided at this point.*

These packages provide an implementation of the rigid body motion estimation of an RGB-D camera from consecutive images.

这些包提供了来自连续图像的rgb摄像机刚体运动估计的实现。


 *  **dvo_core**
    
    运动估计算法的核心实现。 Core implementation of the motion estimation algorithm. 
    
 *  **dvo_ros**
    
    dvo_core与ROS的集成 Integration of *dvo_core* with ROS.
    
 *  **dvo_slam**
    
    基于 dvo_core的姿态图SLAM系统与ROS集成 Pose graph SLAM system based on *dvo_core* and integration with ROS.
    
 *  **dvo_benchmark**
    
   集成 dvo_slam 和转向 rgb d 基准  Integration of *dvo_slam* with TUM RGB-D benchmark, see http://vision.in.tum.de/data/datasets/rgbd-dataset.
    
 *  **sophus**
    
    strasdat库 Hauke Sophus的ROS包包装器 ROS package wrapper for Hauke Strasdat's Sophus library, see https://github.com/strasdat/Sophus.
    

## 安装 Installation

Checkout the branch for your ROS version into a folder in your `ROS_PACKAGE_PATH` and build the packages with `rosmake`.

在 ROS_PACKAGE_PATH 中将你的ROS版本的分支签入到中，并使用 rosmake 构建包。

 *  ROS Fuerte:
    
    ```bash
    git clone -b fuerte git://github.com/tum-vision/dvo_slam.git
    rosmake dvo_core dvo_ros dvo_slam dvo_benchmark
    ```

## Usage

Estimating the camera trajectory from an RGB-D image stream:

*TODO*

For visualization:

 *  Start RVIZ
 *  Set the *Target Frame* to `/world`
 *  Add an *Interactive Marker* display and set its *Update Topic* to `/dvo_vis/update`
 *  Add a *PointCloud2* display and set its *Topic* to `/dvo_vis/cloud`

The red camera shows the current camera position. The blue camera displays the initial camera position.

    用法
    从rgb图像流估算相机轨迹：

    为了可视化：

    启动 RVIZ
    将目标帧设置为 /world
    添加交互式标记显示并将它的更新主题 /dvo_vis/update
    添加 PointCloud2 显示并将它的主题 /dvo_vis/cloud
    红色摄影机显示当前相机位置。 蓝色摄影机显示初始相机位置。

## Publications

The following publications describe the approach:

 *   **Dense Visual SLAM for RGB-D Cameras** (C. Kerl, J. Sturm, D. Cremers), In Proc. of the Int. Conf. on Intelligent Robot Systems (IROS), 2013.
 *   **Robust Odometry Estimation for RGB-D Cameras** (C. Kerl, J. Sturm, D. Cremers), In Proc. of the IEEE Int. Conf. on Robotics and Automation (ICRA), 2013
 *   **Real-Time Visual Odometry from Dense RGB-D Images** (F. Steinbruecker, J. Sturm, D. Cremers), In Workshop on Live Dense Reconstruction with Moving Cameras at the Intl. Conf. on Computer Vision (ICCV), 2011.

## License

The packages *dvo_core*, *dvo_ros*, *dvo_slam*, and *dvo_benchmark* are licensed under the GNU General Public License Version 3 (GPLv3), see http://www.gnu.org/licenses/gpl.html.

The package *sophus* is licensed under the MIT License, see http://opensource.org/licenses/MIT.
