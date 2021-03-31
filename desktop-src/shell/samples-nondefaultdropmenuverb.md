---
description: 示範如何延伸拖放快捷方式功能表 (有時也稱為內容功能表) 。
title: NonDefaultDropMenuVerb 範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: F19B7561-D280-41df-A829-15960FEB12F8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9d326e012fb78b04fd542f88d49c370e8aeab613
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320148"
---
# <a name="nondefaultdropmenuverb-sample"></a><span data-ttu-id="5ea5e-103">NonDefaultDropMenuVerb 範例</span><span class="sxs-lookup"><span data-stu-id="5ea5e-103">NonDefaultDropMenuVerb Sample</span></span>

<span data-ttu-id="5ea5e-104">示範如何延伸拖放快捷方式功能表 (有時也稱為內容功能表) 。</span><span class="sxs-lookup"><span data-stu-id="5ea5e-104">Demonstrates how to extend the drag-and-drop shortcut menu (sometimes referred to as a context menu).</span></span>

<span data-ttu-id="5ea5e-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="5ea5e-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="5ea5e-106">需求</span><span class="sxs-lookup"><span data-stu-id="5ea5e-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="5ea5e-107">下載範例</span><span class="sxs-lookup"><span data-stu-id="5ea5e-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="5ea5e-108">建立範例</span><span class="sxs-lookup"><span data-stu-id="5ea5e-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="5ea5e-109">執行範例</span><span class="sxs-lookup"><span data-stu-id="5ea5e-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="5ea5e-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ea5e-110">Requirements</span></span>



| <span data-ttu-id="5ea5e-111">產品</span><span class="sxs-lookup"><span data-stu-id="5ea5e-111">Product</span></span>                                | <span data-ttu-id="5ea5e-112">最小產品版本</span><span class="sxs-lookup"><span data-stu-id="5ea5e-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="5ea5e-113">Windows</span><span class="sxs-lookup"><span data-stu-id="5ea5e-113">Windows</span></span>                                | <span data-ttu-id="5ea5e-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ea5e-114">Windows Vista</span></span>           |
| <span data-ttu-id="5ea5e-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="5ea5e-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="5ea5e-116">7.0</span><span class="sxs-lookup"><span data-stu-id="5ea5e-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="5ea5e-117">下載範例</span><span class="sxs-lookup"><span data-stu-id="5ea5e-117">Downloading the Sample</span></span>

| <span data-ttu-id="5ea5e-118">Location</span><span class="sxs-lookup"><span data-stu-id="5ea5e-118">Location</span></span>      | <span data-ttu-id="5ea5e-119">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="5ea5e-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea5e-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="5ea5e-120">GitHub</span></span>  | [<span data-ttu-id="5ea5e-121">NonDefaultDropMenuVerb 範例</span><span class="sxs-lookup"><span data-stu-id="5ea5e-121">NonDefaultDropMenuVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NonDefaultDropMenuVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="5ea5e-122">建立範例</span><span class="sxs-lookup"><span data-stu-id="5ea5e-122">Building the Sample</span></span>

<span data-ttu-id="5ea5e-123">若要從命令提示字元建立範例：</span><span class="sxs-lookup"><span data-stu-id="5ea5e-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="5ea5e-124">開啟 [命令提示字元] 視窗，並流覽至 **NonDefaultDropMenuVerb** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="5ea5e-124">Open the command prompt window and navigate to the **NonDefaultDropMenuVerb** project directory.</span></span>
2.  <span data-ttu-id="5ea5e-125">輸入 `msbuild NonDefaultDropMenuVerb.sln`。</span><span class="sxs-lookup"><span data-stu-id="5ea5e-125">Enter `msbuild NonDefaultDropMenuVerb.sln`.</span></span>

<span data-ttu-id="5ea5e-126">若要使用 Microsoft Visual Studio (慣用的) 來建立範例：</span><span class="sxs-lookup"><span data-stu-id="5ea5e-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="5ea5e-127">開啟 Windows 檔案總管，然後流覽至 **NonDefaultDropMenuVerb** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="5ea5e-127">Open Windows Explorer and navigate to the **NonDefaultDropMenuVerb** project directory.</span></span>
2.  <span data-ttu-id="5ea5e-128">按兩下 NonDefaultDropMenuVerb .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="5ea5e-128">Double-click the icon for the NonDefaultDropMenuVerb.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="5ea5e-129">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="5ea5e-129">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="5ea5e-130">執行範例</span><span class="sxs-lookup"><span data-stu-id="5ea5e-130">Running the Sample</span></span>

1.  <span data-ttu-id="5ea5e-131">使用命令提示字元或 Windows 檔案總管，流覽至包含新 DLL 檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="5ea5e-131">Navigate to the directory that contains the new DLL file, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="5ea5e-132">將 NonDefaultDropMenuVerb.dll 複製到系統目錄 (例如，C： \\ Windows \\ System32) 。</span><span class="sxs-lookup"><span data-stu-id="5ea5e-132">Copy NonDefaultDropMenuVerb.dll to the System directory (for example, C:\\Windows\\System32).</span></span>
3.  <span data-ttu-id="5ea5e-133">在命令提示字元中，輸入 `regedit NonDefaultDropMenuVerb.reg` 。</span><span class="sxs-lookup"><span data-stu-id="5ea5e-133">At a command prompt, enter `regedit NonDefaultDropMenuVerb.reg`.</span></span>
4.  <span data-ttu-id="5ea5e-134">使用滑鼠右鍵將檔案從一個資料夾拖曳到另一個資料夾。</span><span class="sxs-lookup"><span data-stu-id="5ea5e-134">Use the right mouse button to drag a file from one folder to another.</span></span> <span data-ttu-id="5ea5e-135">您將會看到放置作業的其他功能表項目。</span><span class="sxs-lookup"><span data-stu-id="5ea5e-135">You will see additional menu items for the drop operation.</span></span>

 

 



