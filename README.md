# amr_description

### 机器人基础信息：
1. **机器人名称**：  amr
2. **机器人类型**（轮式、腿式、飞行器等）：  二轮差速式

### 链接与关节信息：
1. **链接（Link）列表**：
   - 链接名称1：
     - 形状（立方体、圆柱体、球体、STL等）：
     - 尺寸（x, y, z）或几何描述：
     - 质量（kg）：  
     - 质心位置（x, y, z）：  
     - 惯性矩（Ixx, Ixy, Ixz, Iyy, Iyz, Izz）：
     - 视觉模型（颜色或STL路径）：  
     - 碰撞模型（简单形状或STL路径）：  
   - 链接名称2（如果有更多链接，按此格式继续填写）：
     - 形状：
     - 尺寸：
     - 质量：  
     - 质心位置：  
     - 惯性矩：
     - 视觉模型：  
     - 碰撞模型：

2. **关节（Joint）列表**：
   - 关节名称1：
     - 类型（转动关节revolute、滑动关节prismatic、固定关节fixed）：  
     - 父链接名称：  
     - 子链接名称：  
     - 轴方向（x, y, z）：  
     - 运动范围（最小值，最大值）：  
     - 初始位置（位置或角度）：  
   - 关节名称2（按此格式继续填写更多关节）：  
     - 类型：  
     - 父链接名称：  
     - 子链接名称：  
     - 轴方向：  
     - 运动范围：  
     - 初始位置：

### 传感器和执行器：
1. **传感器列表**（如激光雷达、摄像头、IMU等）：
   - 传感器名称1：激光雷达
     - 类型：  
     - 安装位置（链接名称）：  
     - 相对坐标（x, y, z, roll, pitch, yaw）：  
   - 传感器名称2（按此格式继续填写更多传感器）：  
     - 类型：  
     - 安装位置：  
     - 相对坐标：

2. **执行器列表**（如电机等）：
   - 执行器名称1：
     - 类型：  
     - 安装位置（链接名称）：  
     - 相对坐标（x, y, z, roll, pitch, yaw）：  
     - 控制参数（如转矩、速度范围）：  
   - 执行器名称2（按此格式继续填写更多执行器）：  
     - 类型：  
     - 安装位置：  
     - 相对坐标：  
     - 控制参数：

### 颜色和材质：
1. **默认颜色或材质**（如果有）：  

### 物理特性：
1. **摩擦系数**（如地面摩擦、接触摩擦等）：  
2. **碰撞检测要求**（如果有特别需求）：  



为了让AI自动生成一个适用于 ROS Noetic 的 Xacro 文件，提示词应该尽量详细地描述机器人的结构、组件和属性。可以参考以下几点来编写提示词：

1. **机器人整体结构**：描述机器人的外形和部件。包括底盘、车轮、机械臂等。
2. **关节和连杆信息**：如果有机械臂或其他运动部件，描述关节的数量、类型（如旋转、平移）、连杆的长度和连接方式。
3. **传感器和执行器**：说明机器人上有哪些传感器（如激光雷达、IMU、摄像头等）和执行器（如电机），以及它们的安装位置。
4. **物理属性**：包括质量、惯性矩、重心等。
5. **外观描述**：使用哪些几何形状来表示部件（如盒子、圆柱体、球体等），以及它们的尺寸。
6. **坐标系**：每个部件的原点相对于机器人基座的坐标。
7. **运动范围和限制**：如果有关节或轮子，描述它们的运动范围和限制。
8. **使用的参考框架**：例如是否需要引用URDF格式或者是否需要其他特殊包的依赖。
9. **命名规范**：包括命名惯例、层级结构等。

**示例提示词**：
“请为一个四轮差速驱动机器人生成一个Xacro文件，该机器人具备如下特点：机器人底盘为一个长宽高分别为0.5米、0.3米和0.2米的长方体，四个车轮直径为0.1米，前后左右对称分布。车轮通过旋转关节与底盘连接，运动范围为360度。机器人顶部安装有一个RPLiDAR S2激光雷达，距离底盘顶部0.1米。机器人使用ROS Noetic，并且需要定义惯性、摩擦系数和颜色属性。”

如果你有更多具体的需求，也可以在提示词中详细列出这些条件。