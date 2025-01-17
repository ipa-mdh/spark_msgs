cmake_minimum_required(VERSION 3.5)
project(spark_msgs)

# find_package(ament_cmake REQUIRED)
# find_package(builtin_interfaces REQUIRED)
find_package(rosidl_default_generators REQUIRED)

# ROS messages, services and actions

set(srv_files
	srv/SparkRegistration.srv
)
rosidl_generate_interfaces(${PROJECT_NAME}
	${srv_files}
	# DEPENDENCIES
	# builtin_interfaces
	# geometry_msgs
)

ament_export_dependencies(rosidl_default_runtime)

ament_package()
