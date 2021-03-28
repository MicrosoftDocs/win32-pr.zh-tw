---
description: 示範如何在 Windows 檔案總管命名空間中的資料夾或專案上接聽 Shell 變更通知。
title: 變更通知監看員範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 02A7C5B4-94F2-4c35-9290-4C816E5CF63A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5d0ac6ccb2dd2328d81b77d03bffc68dfa9a70cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193952"
---
# <a name="change-notify-watcher-sample"></a><span data-ttu-id="cb5cf-103">變更通知監看員範例</span><span class="sxs-lookup"><span data-stu-id="cb5cf-103">Change Notify Watcher Sample</span></span>

<span data-ttu-id="cb5cf-104">示範如何在 Windows 檔案總管命名空間中的資料夾或專案上接聽 Shell 變更通知。</span><span class="sxs-lookup"><span data-stu-id="cb5cf-104">Demonstrates how to listen to Shell change notifications on a folder or item in the Windows Explorer namespace.</span></span>

<span data-ttu-id="cb5cf-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="cb5cf-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="cb5cf-106">需求</span><span class="sxs-lookup"><span data-stu-id="cb5cf-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="cb5cf-107">下載範例</span><span class="sxs-lookup"><span data-stu-id="cb5cf-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="cb5cf-108">建立範例</span><span class="sxs-lookup"><span data-stu-id="cb5cf-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="cb5cf-109">執行範例</span><span class="sxs-lookup"><span data-stu-id="cb5cf-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="cb5cf-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb5cf-110">Requirements</span></span>



| <span data-ttu-id="cb5cf-111">產品</span><span class="sxs-lookup"><span data-stu-id="cb5cf-111">Product</span></span>                                | <span data-ttu-id="cb5cf-112">最小產品版本</span><span class="sxs-lookup"><span data-stu-id="cb5cf-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="cb5cf-113">Windows</span><span class="sxs-lookup"><span data-stu-id="cb5cf-113">Windows</span></span>                                | <span data-ttu-id="cb5cf-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cb5cf-114">Windows Vista</span></span>           |
| <span data-ttu-id="cb5cf-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="cb5cf-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="cb5cf-116">7.0</span><span class="sxs-lookup"><span data-stu-id="cb5cf-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="cb5cf-117">下載範例</span><span class="sxs-lookup"><span data-stu-id="cb5cf-117">Downloading the Sample</span></span>

| <span data-ttu-id="cb5cf-118">Location</span><span class="sxs-lookup"><span data-stu-id="cb5cf-118">Location</span></span>      | <span data-ttu-id="cb5cf-119">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="cb5cf-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb5cf-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="cb5cf-120">GitHub</span></span>  | [<span data-ttu-id="cb5cf-121">ChangeNotifyWatcher 範例</span><span class="sxs-lookup"><span data-stu-id="cb5cf-121">ChangeNotifyWatcher sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ChangeNotifyWatcher) |

## <a name="building-the-sample"></a><span data-ttu-id="cb5cf-122">建立範例</span><span class="sxs-lookup"><span data-stu-id="cb5cf-122">Building the Sample</span></span>

<span data-ttu-id="cb5cf-123">若要從命令提示字元建立範例：</span><span class="sxs-lookup"><span data-stu-id="cb5cf-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="cb5cf-124">開啟 [命令提示字元] 視窗，並流覽至 **ChangeNotifyWatcher** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="cb5cf-124">Open the command prompt window and navigate to the **ChangeNotifyWatcher** project directory.</span></span>
2.  <span data-ttu-id="cb5cf-125">輸入 `msbuild ChangeNotifyWatcher.sln`。</span><span class="sxs-lookup"><span data-stu-id="cb5cf-125">Enter `msbuild ChangeNotifyWatcher.sln`.</span></span>

<span data-ttu-id="cb5cf-126">若要使用 Microsoft Visual Studio (慣用的) 來建立範例：</span><span class="sxs-lookup"><span data-stu-id="cb5cf-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="cb5cf-127">開啟 Windows 檔案總管，然後流覽至 **ChangeNotifyWatcher** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="cb5cf-127">Open Windows Explorer and navigate to the **ChangeNotifyWatcher** project directory.</span></span>
2.  <span data-ttu-id="cb5cf-128">按兩下 ChangeNotifyWatcher .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="cb5cf-128">Double-click the icon for the ChangeNotifyWatcher.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="cb5cf-129">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="cb5cf-129">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="cb5cf-130">執行範例</span><span class="sxs-lookup"><span data-stu-id="cb5cf-130">Running the Sample</span></span>

1.  <span data-ttu-id="cb5cf-131">使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="cb5cf-131">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="cb5cf-132">在命令提示字元處，輸入 `ChangeNotifyWatcher.exe`。</span><span class="sxs-lookup"><span data-stu-id="cb5cf-132">At the command prompt, enter `ChangeNotifyWatcher.exe`.</span></span> <span data-ttu-id="cb5cf-133">或者，從 Windows 檔案總管按兩下 ChangeNotifyWatcher.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="cb5cf-133">Alternatively, from Windows Explorer double-click the icon for ChangeNotifyWatcher.exe.</span></span>
3.  <span data-ttu-id="cb5cf-134">若要示範效果， (AppUserModelIDs 的應用程式使用者模型識別碼) 選取要監看的資料夾，方法是按一下 **[挑選 ...]** ，或從 Windows 檔案總管視窗的資料夾拖放至範例的清單視圖中。</span><span class="sxs-lookup"><span data-stu-id="cb5cf-134">To demonstrate the effect, Application User Model IDs (AppUserModelIDs) select a folder to watch by either clicking **"Pick..."** or by using drag-and-drop on a folder from a Windows Explorer window into the sample's list view.</span></span>

 

 



