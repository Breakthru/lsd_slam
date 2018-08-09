project('lsd_slam', 'cpp')

eigen = dependency('eigen3')
incdir = include_directories('src/')
sophus = include_directories('thirdparty/Sophus')
lsd_slam_core = library('lsd_slam_core', ['src/DataStructures/Frame.cpp'], include_directories: [incdir, sophus], dependencies: [eigen])
