cmake_minimum_required(VERSION 3.8)
project(hector_slam)

set(CMAKE_CXX_STANDARD 11)

set(SOURCE_FILES
        hector_compressed_map_transport/src/map_to_image_node.cpp
        hector_geotiff/include/hector_geotiff/geotiff_writer.h
        hector_geotiff/include/hector_geotiff/map_writer_interface.h
        hector_geotiff/include/hector_geotiff/map_writer_plugin_interface.h
        hector_geotiff/src/geotiff_writer/geotiff_writer.cpp
        hector_geotiff/src/geotiff_node.cpp
        hector_geotiff/src/geotiff_saver.cpp
        hector_geotiff_plugins/src/trajectory_geotiff_plugin.cpp
        hector_imu_attitude_to_tf/src/imu_attitude_to_tf_node.cpp
        hector_imu_tools/src/pose_and_orientation_to_imu_node.cpp
        hector_map_server/src/hector_map_server.cpp
        hector_map_tools/include/hector_map_tools/HectorMapTools.h
        hector_mapping/include/hector_slam_lib/map/GridMap.h
        hector_mapping/include/hector_slam_lib/map/GridMapBase.h
        hector_mapping/include/hector_slam_lib/map/GridMapCacheArray.h
        hector_mapping/include/hector_slam_lib/map/GridMapLogOdds.h
        hector_mapping/include/hector_slam_lib/map/GridMapReflectanceCount.h
        hector_mapping/include/hector_slam_lib/map/GridMapSimpleCount.h
        hector_mapping/include/hector_slam_lib/map/MapDimensionProperties.h
        hector_mapping/include/hector_slam_lib/map/OccGridMapBase.h
        hector_mapping/include/hector_slam_lib/map/OccGridMapUtil.h
        hector_mapping/include/hector_slam_lib/map/OccGridMapUtilConfig.h
        hector_mapping/include/hector_slam_lib/matcher/ScanMatcher.h
        hector_mapping/include/hector_slam_lib/scan/DataPointContainer.h
        hector_mapping/include/hector_slam_lib/slam_main/HectorSlamProcessor.h
        hector_mapping/include/hector_slam_lib/slam_main/MapProcContainer.h
        hector_mapping/include/hector_slam_lib/slam_main/MapRepMultiMap.h
        hector_mapping/include/hector_slam_lib/slam_main/MapRepresentationInterface.h
        hector_mapping/include/hector_slam_lib/slam_main/MapRepSingleMap.h
        hector_mapping/include/hector_slam_lib/util/DrawInterface.h
        hector_mapping/include/hector_slam_lib/util/HectorDebugInfoInterface.h
        hector_mapping/include/hector_slam_lib/util/MapLockerInterface.h
        hector_mapping/include/hector_slam_lib/util/UtilFunctions.h
        hector_mapping/src/HectorDebugInfoProvider.h
        hector_mapping/src/HectorDrawings.h
        hector_mapping/src/HectorMapMutex.h
        hector_mapping/src/HectorMappingRos.cpp
        hector_mapping/src/HectorMappingRos.h
        hector_mapping/src/main.cpp
        hector_mapping/src/main_mapper.cpp
        hector_mapping/src/PoseInfoContainer.cpp
        hector_mapping/src/PoseInfoContainer.h
        hector_marker_drawing/include/hector_marker_drawing/DrawInterface.h
        hector_marker_drawing/include/hector_marker_drawing/HectorDrawings.h
        hector_trajectory_server/src/hector_trajectory_server.cpp)

add_executable(hector_slam ${SOURCE_FILES})