---
title: 桌面應用程式範例
description: 桌面應用程式範例
ms.assetid: 3736dd01-b02f-4056-b19b-0e7cc6c9aa67
keywords:
- Windows Media 裝置管理員，範例
- 裝置管理員，範例
- 桌面應用程式、範例
- Windows Media 裝置管理員，桌面應用程式範例
- 裝置管理員，桌面應用程式範例
- wmdmapp 範例應用程式
- 範例，桌面應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f4008a25ca4448d4d4be7c9f667c5a9e4f08023
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372242"
---
# <a name="sample-desktop-application"></a><span data-ttu-id="c6c71-110">桌面應用程式範例</span><span class="sxs-lookup"><span data-stu-id="c6c71-110">Sample Desktop Application</span></span>

<span data-ttu-id="c6c71-111">Windows Media 裝置管理員隨附一個稱為 wmdmapp 的範例桌面應用程式。</span><span class="sxs-lookup"><span data-stu-id="c6c71-111">The Windows Media Device Manager ships with a sample desktop application called wmdmapp.</span></span> <span data-ttu-id="c6c71-112">此應用程式具有圖形化使用者介面，可讓您流覽連線的裝置、在裝置上建立播放清單，以及將媒體檔案拖曳至裝置。</span><span class="sxs-lookup"><span data-stu-id="c6c71-112">This application has a graphical user interface that allows you to browse connected devices, create playlists on the device, and drag media files to the device.</span></span>

<span data-ttu-id="c6c71-113">這個範例應用程式是由兩個部分所組成：</span><span class="sxs-lookup"><span data-stu-id="c6c71-113">This sample application consists of two pieces:</span></span>

-   <span data-ttu-id="c6c71-114">wmdapp.exe，此可執行檔會顯示視窗並執行大部分的使用者介面和程式的基本功能，以及</span><span class="sxs-lookup"><span data-stu-id="c6c71-114">wmdapp.exe, an executable that displays a window and performs most of the user interface and basic functionality of the program, and</span></span>
-   <span data-ttu-id="c6c71-115">proghelp.dll，此為應用程式執行公用程式函式的 helper DLL。</span><span class="sxs-lookup"><span data-stu-id="c6c71-115">proghelp.dll, a helper DLL that performs utility functions for the application.</span></span> <span data-ttu-id="c6c71-116">您必須在建立專案之後註冊這個 DLL。</span><span class="sxs-lookup"><span data-stu-id="c6c71-116">You must register this DLL after building the project.</span></span>

<span data-ttu-id="c6c71-117">若要編譯範例應用程式，您可以使用 Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="c6c71-117">To compile the sample application, you can use Visual Studio.</span></span> <span data-ttu-id="c6c71-118">下一節將說明如何完成這項操作：</span><span class="sxs-lookup"><span data-stu-id="c6c71-118">The following section describes how this is done:</span></span>

-   [<span data-ttu-id="c6c71-119">使用 Visual Studio 編譯範例應用程式</span><span class="sxs-lookup"><span data-stu-id="c6c71-119">Compiling the Sample Application Using Visual Studio</span></span>](compiling-the-sample-application-using-visual-studio.md)

<span data-ttu-id="c6c71-120">編譯專案之後，請註冊 proghelp.dll 檔案。</span><span class="sxs-lookup"><span data-stu-id="c6c71-120">After compiling the project, register the proghelp.dll file.</span></span> <span data-ttu-id="c6c71-121">若要註冊此 DLL，請開啟命令提示字元，然後流覽至包含此 DLL 的目錄並輸入 `regsvr32 proghelp.dll` 。</span><span class="sxs-lookup"><span data-stu-id="c6c71-121">To register this DLL, open a command prompt and browse to the directory containing this DLL and type `regsvr32 proghelp.dll`.</span></span>

 

 




