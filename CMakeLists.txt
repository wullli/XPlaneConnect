# cmake_minimum_required(VERSION <specify CMake version here>)
project(XPlaneConnect)

set(CMAKE_CXX_STANDARD 14)

include_directories(C/playbackExample/src)
include_directories(C/src)
include_directories("TestScripts/C Tests")
include_directories(xpcPlugin)
include_directories(xpcPlugin/SDK/CHeaders/Widgets)
include_directories(xpcPlugin/SDK/CHeaders/Wrappers)
include_directories(xpcPlugin/SDK/CHeaders/XPLM)

add_executable(XPlaneConnect
        C/monitorExample/main.c
        C/playbackExample/src/chrome.c
        C/playbackExample/src/chrome.h
        C/playbackExample/src/main.c
        C/playbackExample/src/playback.c
        C/playbackExample/src/playback.h
        C/src/xplaneConnect.c
        C/src/xplaneConnect.h
        C/xpcExample/xpcExample/src/main.cpp
        MATLAB/+XPlaneConnect/closeUDP.m
        MATLAB/+XPlaneConnect/getCTRL.m
        MATLAB/+XPlaneConnect/getDREFs.m
        MATLAB/+XPlaneConnect/getPOSI.m
        MATLAB/+XPlaneConnect/openUDP.m
        MATLAB/+XPlaneConnect/pauseSim.m
        MATLAB/+XPlaneConnect/readDATA.m
        MATLAB/+XPlaneConnect/selectDATA.m
        MATLAB/+XPlaneConnect/sendCTRL.m
        MATLAB/+XPlaneConnect/sendDATA.m
        MATLAB/+XPlaneConnect/sendDREF.m
        MATLAB/+XPlaneConnect/sendDREFs.m
        MATLAB/+XPlaneConnect/sendPOSI.m
        MATLAB/+XPlaneConnect/sendTEXT.m
        MATLAB/+XPlaneConnect/sendVIEW.m
        MATLAB/+XPlaneConnect/sendWYPT.m
        MATLAB/+XPlaneConnect/setConn.m
        MATLAB/Example/Example.m
        MATLAB/MonitorExample/MonitorExample.m
        MATLAB/PlaybackExample/Playback.m
        MATLAB/PlaybackExample/Record.m
        "TestScripts/C Tests/CtrlTests.h"
        "TestScripts/C Tests/DataTests.h"
        "TestScripts/C Tests/DrefTests.h"
        "TestScripts/C Tests/main.c"
        "TestScripts/C Tests/PosiTests.h"
        "TestScripts/C Tests/SimuTests.h"
        "TestScripts/C Tests/Test.c"
        "TestScripts/C Tests/Test.h"
        "TestScripts/C Tests/TextTests.h"
        "TestScripts/C Tests/UDPTests.h"
        "TestScripts/C Tests/ViewTests.h"
        "TestScripts/C Tests/WyptTests.h"
        "TestScripts/MATLAB Tests/DATATest.m"
        "TestScripts/MATLAB Tests/getCTRLTest.m"
        "TestScripts/MATLAB Tests/getDREFsTest.m"
        "TestScripts/MATLAB Tests/getPOSITest.m"
        "TestScripts/MATLAB Tests/openCloseTest.m"
        "TestScripts/MATLAB Tests/pauseTest.m"
        "TestScripts/MATLAB Tests/sendCTRLTest.m"
        "TestScripts/MATLAB Tests/sendDREFTest.m"
        "TestScripts/MATLAB Tests/sendPOSITest.m"
        "TestScripts/MATLAB Tests/sendTEXTTest.m"
        "TestScripts/MATLAB Tests/sendVIEWTest.m"
        "TestScripts/MATLAB Tests/sendWYPTTest.m"
        "TestScripts/MATLAB Tests/setConnTest.m"
        "TestScripts/MATLAB Tests/tests.m"
        xpcPlugin/SDK/CHeaders/Widgets/XPStandardWidgets.h
        xpcPlugin/SDK/CHeaders/Widgets/XPUIGraphics.h
        xpcPlugin/SDK/CHeaders/Widgets/XPWidgetDefs.h
        xpcPlugin/SDK/CHeaders/Widgets/XPWidgets.h
        xpcPlugin/SDK/CHeaders/Widgets/XPWidgetUtils.h
        xpcPlugin/SDK/CHeaders/Wrappers/XPCBroadcaster.cpp
        xpcPlugin/SDK/CHeaders/Wrappers/XPCBroadcaster.h
        xpcPlugin/SDK/CHeaders/Wrappers/XPCDisplay.cpp
        xpcPlugin/SDK/CHeaders/Wrappers/XPCDisplay.h
        xpcPlugin/SDK/CHeaders/Wrappers/XPCListener.cpp
        xpcPlugin/SDK/CHeaders/Wrappers/XPCListener.h
        xpcPlugin/SDK/CHeaders/Wrappers/XPCProcessing.cpp
        xpcPlugin/SDK/CHeaders/Wrappers/XPCProcessing.h
        xpcPlugin/SDK/CHeaders/Wrappers/XPCWidget.cpp
        xpcPlugin/SDK/CHeaders/Wrappers/XPCWidget.h
        xpcPlugin/SDK/CHeaders/Wrappers/XPCWidgetAttachments.cpp
        xpcPlugin/SDK/CHeaders/Wrappers/XPCWidgetAttachments.h
        xpcPlugin/SDK/CHeaders/XPLM/XPLMCamera.h
        xpcPlugin/SDK/CHeaders/XPLM/XPLMDataAccess.h
        xpcPlugin/SDK/CHeaders/XPLM/XPLMDefs.h
        xpcPlugin/SDK/CHeaders/XPLM/XPLMDisplay.h
        xpcPlugin/SDK/CHeaders/XPLM/XPLMGraphics.h
        xpcPlugin/SDK/CHeaders/XPLM/XPLMMenus.h
        xpcPlugin/SDK/CHeaders/XPLM/XPLMNavigation.h
        xpcPlugin/SDK/CHeaders/XPLM/XPLMPlanes.h
        xpcPlugin/SDK/CHeaders/XPLM/XPLMPlugin.h
        xpcPlugin/SDK/CHeaders/XPLM/XPLMProcessing.h
        xpcPlugin/SDK/CHeaders/XPLM/XPLMScenery.h
        xpcPlugin/SDK/CHeaders/XPLM/XPLMUtilities.h
        xpcPlugin/DataManager.cpp
        xpcPlugin/DataManager.h
        xpcPlugin/Drawing.cpp
        xpcPlugin/Drawing.h
        xpcPlugin/Log.cpp
        xpcPlugin/Log.h
        xpcPlugin/Message.cpp
        xpcPlugin/Message.h
        xpcPlugin/MessageHandlers.cpp
        xpcPlugin/MessageHandlers.h
        xpcPlugin/UDPSocket.cpp
        xpcPlugin/UDPSocket.h
        xpcPlugin/XPCPlugin.cpp)
