---
description: 示範如何使用 ExplorerCommand 和 ExplorerCommandState 方法來執行 Shell 動詞命令。
title: Explorer 命令動詞範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2310A6AA-EAF9-4d7a-A784-04931BDC2089
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a35662c3df0e0fcddae049ccfaac2d9e3e265ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852188"
---
# <a name="explorer-command-verb-sample"></a><span data-ttu-id="24be5-103">Explorer 命令動詞範例</span><span class="sxs-lookup"><span data-stu-id="24be5-103">Explorer Command Verb Sample</span></span>

<span data-ttu-id="24be5-104">示範如何使用 ExplorerCommand 和 ExplorerCommandState 方法來執行 Shell 動詞命令。</span><span class="sxs-lookup"><span data-stu-id="24be5-104">Demonstrates how to implement a Shell verb using the ExplorerCommand and ExplorerCommandState methods.</span></span>

<span data-ttu-id="24be5-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="24be5-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="24be5-106">需求</span><span class="sxs-lookup"><span data-stu-id="24be5-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="24be5-107">下載範例</span><span class="sxs-lookup"><span data-stu-id="24be5-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="24be5-108">建立範例</span><span class="sxs-lookup"><span data-stu-id="24be5-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="24be5-109">執行範例</span><span class="sxs-lookup"><span data-stu-id="24be5-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="24be5-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="24be5-110">Requirements</span></span>



| <span data-ttu-id="24be5-111">產品</span><span class="sxs-lookup"><span data-stu-id="24be5-111">Product</span></span>                                | <span data-ttu-id="24be5-112">最小產品版本</span><span class="sxs-lookup"><span data-stu-id="24be5-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="24be5-113">Windows</span><span class="sxs-lookup"><span data-stu-id="24be5-113">Windows</span></span>                                | <span data-ttu-id="24be5-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="24be5-114">Windows Vista</span></span>           |
| <span data-ttu-id="24be5-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="24be5-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="24be5-116">7.0</span><span class="sxs-lookup"><span data-stu-id="24be5-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="24be5-117">下載範例</span><span class="sxs-lookup"><span data-stu-id="24be5-117">Downloading the Sample</span></span>

| <span data-ttu-id="24be5-118">Location</span><span class="sxs-lookup"><span data-stu-id="24be5-118">Location</span></span>      | <span data-ttu-id="24be5-119">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="24be5-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24be5-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="24be5-120">GitHub</span></span>  | [<span data-ttu-id="24be5-121">ExplorerCommandVerb 範例</span><span class="sxs-lookup"><span data-stu-id="24be5-121">ExplorerCommandVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExplorerCommandVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="24be5-122">建立範例</span><span class="sxs-lookup"><span data-stu-id="24be5-122">Building the Sample</span></span>

<span data-ttu-id="24be5-123">若要從命令提示字元建立範例：</span><span class="sxs-lookup"><span data-stu-id="24be5-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="24be5-124">開啟 [命令提示字元] 視窗，並流覽至 **ExplorerCommandVerb** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="24be5-124">Open the command prompt window and navigate to the **ExplorerCommandVerb** project directory.</span></span>
2.  <span data-ttu-id="24be5-125">輸入 `msbuild ExplorerCommandVerb.sln`。</span><span class="sxs-lookup"><span data-stu-id="24be5-125">Enter `msbuild ExplorerCommandVerb.sln`.</span></span>

<span data-ttu-id="24be5-126">若要使用 Microsoft Visual Studio (慣用的) 來建立範例：</span><span class="sxs-lookup"><span data-stu-id="24be5-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="24be5-127">開啟 Windows 檔案總管，然後流覽至 **ExplorerCommandVerb** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="24be5-127">Open Windows Explorer and navigate to the **ExplorerCommandVerb** project directory.</span></span>
2.  <span data-ttu-id="24be5-128">按兩下 ExplorerCommandVerb .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="24be5-128">Double-click the icon for the ExplorerCommandVerb.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="24be5-129">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="24be5-129">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="24be5-130">執行範例</span><span class="sxs-lookup"><span data-stu-id="24be5-130">Running the Sample</span></span>

1.  <span data-ttu-id="24be5-131">使用命令提示字元或 Windows 檔案總管，流覽至包含 ExplorerCommandVerb.dll 的目錄。</span><span class="sxs-lookup"><span data-stu-id="24be5-131">Navigate to the directory that contains the ExplorerCommandVerb.dll, using the command prompt or Windows Explorer.</span></span> <span data-ttu-id="24be5-132">請確定您在64位的 Windows 上使用64位的 DLL 檔案。</span><span class="sxs-lookup"><span data-stu-id="24be5-132">Make sure you use the 64-bit DLL file on 64-bit Windows.</span></span>
2.  <span data-ttu-id="24be5-133">在命令列中，輸入 `regsvr32.exe ExplorerCommandVerb.dll` 。</span><span class="sxs-lookup"><span data-stu-id="24be5-133">At the command line, enter `regsvr32.exe ExplorerCommandVerb.dll`.</span></span>
3.  <span data-ttu-id="24be5-134">當您以滑鼠右鍵按一下 .txt 檔案時，內容功能表上會顯示兩個新的動詞命令。</span><span class="sxs-lookup"><span data-stu-id="24be5-134">Two new verbs will be shown on the context menu when you right-click a .txt file.</span></span>

 

 



