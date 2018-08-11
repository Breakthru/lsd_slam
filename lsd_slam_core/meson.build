project('lsd_slam', 'cpp', default_options : ['cpp_std=c++11'])

eigen = dependency('eigen3')
incdir = include_directories('src/')
sophus = include_directories('thirdparty/Sophus')

g2o_inc = include_directories('/Users/marco/Research/build-g2o/usr/local/include')
g2o_lib = meson.get_compiler('cpp').find_library('g2o_core', dirs: '/Users/marco/Research/build-g2o/usr/local/lib/')

lsdslam = library('lsdslam',
['src/DataStructures/Frame.cpp',
'src/DataStructures/FramePoseStruct.cpp',
'src/DataStructures/FrameMemory.cpp',
'src/SlamSystem.cpp',
'src/LiveSLAMWrapper.cpp',
'src/DepthEstimation/DepthMap.cpp',
'src/DepthEstimation/DepthMapPixelHypothesis.cpp',
'src/util/globalFuncs.cpp',
'src/util/SophusUtil.cpp',
'src/util/settings.cpp',
'src/util/Undistorter.cpp',
'src/Tracking/Sim3Tracker.cpp',
'src/Tracking/Relocalizer.cpp',
'src/Tracking/SE3Tracker.cpp',
'src/Tracking/TrackingReference.cpp',
'src/IOWrapper/Timestamp.cpp',
'src/GlobalMapping/FabMap.cpp',
'src/GlobalMapping/KeyFrameGraph.cpp',
'src/GlobalMapping/g2oTypeSim3Sophus.cpp',
'src/GlobalMapping/TrackableKeyFrameSearch.cpp'
],
include_directories: [incdir, sophus, g2o_inc], dependencies: [eigen, g2o_lib])
