---
description: 示範如何將專案加入至應用程式的自動捷徑清單，包括在常見和最近類別的顯示之間切換。
title: 自動跳躍清單範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: C33152FE-1322-42f8-A656-3D5FAF4B612D
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ce0b6520163fcb07bb990b7a5a9fe742d976a899
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469368"
---
# <a name="automatic-jump-list-sample"></a><span data-ttu-id="71e5d-103">自動跳躍清單範例</span><span class="sxs-lookup"><span data-stu-id="71e5d-103">Automatic Jump List Sample</span></span>

<span data-ttu-id="71e5d-104">示範如何將專案加入至應用程式的自動捷徑清單，包括在常見和最近類別的顯示之間切換。</span><span class="sxs-lookup"><span data-stu-id="71e5d-104">Demonstrates how to add items to the automatic Jump List for an application, including switching between the display of the Frequent and Recent categories.</span></span>

<span data-ttu-id="71e5d-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="71e5d-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="71e5d-106">需求</span><span class="sxs-lookup"><span data-stu-id="71e5d-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="71e5d-107">下載範例</span><span class="sxs-lookup"><span data-stu-id="71e5d-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="71e5d-108">建立範例</span><span class="sxs-lookup"><span data-stu-id="71e5d-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="71e5d-109">執行範例</span><span class="sxs-lookup"><span data-stu-id="71e5d-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="71e5d-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="71e5d-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="71e5d-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="71e5d-111">Requirements</span></span>



| <span data-ttu-id="71e5d-112">產品</span><span class="sxs-lookup"><span data-stu-id="71e5d-112">Product</span></span>                                | <span data-ttu-id="71e5d-113">最小產品版本</span><span class="sxs-lookup"><span data-stu-id="71e5d-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="71e5d-114">Windows</span><span class="sxs-lookup"><span data-stu-id="71e5d-114">Windows</span></span>                                | <span data-ttu-id="71e5d-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="71e5d-115">Windows 7</span></span>               |
| <span data-ttu-id="71e5d-116">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="71e5d-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="71e5d-117">7.0</span><span class="sxs-lookup"><span data-stu-id="71e5d-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="71e5d-118">下載範例</span><span class="sxs-lookup"><span data-stu-id="71e5d-118">Downloading the Sample</span></span>

| <span data-ttu-id="71e5d-119">Location</span><span class="sxs-lookup"><span data-stu-id="71e5d-119">Location</span></span>      | <span data-ttu-id="71e5d-120">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="71e5d-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71e5d-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="71e5d-121">GitHub</span></span>  | [<span data-ttu-id="71e5d-122">AutomaticJumpList 範例</span><span class="sxs-lookup"><span data-stu-id="71e5d-122">AutomaticJumpList sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AutomaticJumpList) |

## <a name="building-the-sample"></a><span data-ttu-id="71e5d-123">建立範例</span><span class="sxs-lookup"><span data-stu-id="71e5d-123">Building the Sample</span></span>

<span data-ttu-id="71e5d-124">若要從命令提示字元建立範例：</span><span class="sxs-lookup"><span data-stu-id="71e5d-124">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="71e5d-125">開啟 [命令提示字元] 視窗，並流覽至 **AutomaticJumpList** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="71e5d-125">Open the command prompt window and navigate to the **AutomaticJumpList** project directory.</span></span>
2.  <span data-ttu-id="71e5d-126">輸入 `msbuild AutomaticJumpListSample.sln`。</span><span class="sxs-lookup"><span data-stu-id="71e5d-126">Enter `msbuild AutomaticJumpListSample.sln`.</span></span>

<span data-ttu-id="71e5d-127">若要使用 Microsoft Visual Studio (慣用的) 來建立範例：</span><span class="sxs-lookup"><span data-stu-id="71e5d-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="71e5d-128">開啟 Windows 檔案總管，然後流覽至 **AutomaticJumpList** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="71e5d-128">Open Windows Explorer and navigate to the **AutomaticJumpList** project directory.</span></span>
2.  <span data-ttu-id="71e5d-129">按兩下 AutomaticJumpListSample .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="71e5d-129">Double-click the icon for the AutomaticJumpListSample.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="71e5d-130">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="71e5d-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="71e5d-131">執行範例</span><span class="sxs-lookup"><span data-stu-id="71e5d-131">Running the Sample</span></span>

1.  <span data-ttu-id="71e5d-132">使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="71e5d-132">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="71e5d-133">在命令列中，輸入 `AutomaticJumpListSample.exe` 。</span><span class="sxs-lookup"><span data-stu-id="71e5d-133">At the command line, enter `AutomaticJumpListSample.exe`.</span></span> <span data-ttu-id="71e5d-134">或者，從 Windows 檔案總管按兩下 AutomaticJumpListSample.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="71e5d-134">Alternatively, from Windows Explorer double-click the icon for AutomaticJumpListSample.exe.</span></span>
3.  <span data-ttu-id="71e5d-135">在第一次執行此範例時，必須以系統管理員的身分執行，讓它可以安裝必要的檔案類型註冊。</span><span class="sxs-lookup"><span data-stu-id="71e5d-135">This sample must be run as an administrator the first time it is run so that it can install the necessary file type registrations.</span></span> <span data-ttu-id="71e5d-136">在註冊檔案類型之後，範例可以作為標準使用者來執行。</span><span class="sxs-lookup"><span data-stu-id="71e5d-136">After the file types have been registered, the sample can run as a standard user.</span></span>
4.  <span data-ttu-id="71e5d-137">從範例應用程式的功能表中選取選項，包括透過 [ **開啟** ] 對話方塊選取 .txt 或 .doc 檔，以查看它們如何影響工作列中的應用程式捷徑清單。</span><span class="sxs-lookup"><span data-stu-id="71e5d-137">Select options from the menu in the sample application, including the selection of .txt or .doc documents through the **Open** dialog to see how they affect the application's Jump List in the taskbar.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71e5d-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="71e5d-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71e5d-139">應用程式使用者模型識別碼 (AppUserModelIDs) </span><span class="sxs-lookup"><span data-stu-id="71e5d-139">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> </dl>

 

 



