cmake_minimum_required ( VERSION 2.6 )

project ( TP1_medev )

file( GLOB_RECURSE
  source_files
  src/*
)


find_package (OpenSceneGraph 2.0.0 REQUIRED osg osgDB osgUtil osgGA osgViewer)

include_directories (include ${OPENSCENEGRAPH_INCLUDE_DIRS})

add_executable ( TP1_medev ${source_files} )

target_link_libraries (TP1_medev ${OPENSCENEGRAPH_LIBRARIES})