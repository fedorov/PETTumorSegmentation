cmake_minimum_required(VERSION 2.8.9)

project(PETTumorSegmentation)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "http://www.slicer.org/slicerWiki/index.php/Documentation/Nightly/Extensions/PETTumorSegmentation")
set(EXTENSION_CATEGORY “Segmentation”)
set(EXTENSION_CONTRIBUTORS “Christian Bauer (University of Iowa), Markus van Tol (University of Iowa)“)
set(EXTENSION_DESCRIPTION “Tumor and lymph node segmentation in PET scans“)
set(EXTENSION_ICONURL "https://raw.githubusercontent.com/chribaue/PETTumorSegmentation/master/PETTumorSegmentation.png")
set(EXTENSION_SCREENSHOTURLS "http://www.slicer.org/slicerWiki/images/0/04/PETTumorSegmentation_Effect_with_models.png")

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(PETTumorSegmentation)
add_subdirectory(PETTumorSegmentationEffect)
## NEXT_MODULE

#-----------------------------------------------------------------------------
#include(${Slicer_EXTENSION_CPACK}) # this is included in the template, but leads to mac build error