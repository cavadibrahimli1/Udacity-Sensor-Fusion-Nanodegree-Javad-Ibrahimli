# Lesson 1-1 Intro to Lidar and Point Clouds

### I. Lidar Sensors

LiDAR (Light Detection And Ranging) sends out very short light pulses at different angles across the field of view and receives the photons reflected back from an object. It measures the time difference and determines the distance to the object. Thus, the data can be used to model a 3D environment.

![Velodyne HDL 64 Lidar](./media/velodyne-hdl-64-lidar.png)
Velodyne Lidar

Major Lidar types:
- Rotating lidars: rotating sensors to have a 360-degree of the environment
- Reflecting lidars: using mirrors to scan the laser beams
- Solid-state lidars: using phased array type of principle

- Mount position
    * rooftop: farthest field of view (Up side of the vehicles)
    * front, back and side: coverage for the blindspot of rooftop lidars (In general they are not as strong as rooftops)

- Resolution
    * more layers of laser in the vertical field of view, to avoid an object hiding between the gap of two layers

### II. Point Clouds
![image](https://github.com/cavadibrahimli1/Udacity-Sensor-Fusion-Nanodegree-Javad-Ibrahimli/assets/76445357/cc1c08fa-cbaf-42d9-b1a1-8b920dcc0d03)

A point cloud is a set of all lidar reflection points measured. Each point is one laser beam reflected from an object.

![PCD of a City Block](./media/pcd-of-a-block.png)

- A PCD file contains a list of Point Cloud Data, with every point in the format of `(x, y, z, I)`
    * `(x, y, z)` is the Cartesian coordinates
        + telling us the location of the reflected surface on the object
        + `x` pointing towards the front of the car
        + `y` pointing to the left of the car
        + `z` pointing to the vertical up
    * `I` is the signal strength of the laser related to the reflective properties of the material

![PCD Coordinates](./media/pcd-coordinates.png)

Point Cloud Library (PCL) is an open source library for processing the PCD file. It helps doing filtering, segmentation, and clustering of point clouds, rendering work, etc. Official document is available [HERE](https://pointclouds.org/).

![image](https://github.com/cavadibrahimli1/Udacity-Sensor-Fusion-Nanodegree-Javad-Ibrahimli/assets/76445357/e7d8032f-db70-441a-8980-b97106b7ef28)

