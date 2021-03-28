---
description: 示範如何建立應用程式的自訂捷徑清單，包括新增自訂分類和工作。
title: 自訂跳躍清單範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 60DEDB01-8F8F-4c25-8FCC-8EAC461A99B7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c20592e508a24985e0f8283993482c7bd61af232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193950"
---
# <a name="custom-jump-list-sample"></a><span data-ttu-id="f530a-103">自訂跳躍清單範例</span><span class="sxs-lookup"><span data-stu-id="f530a-103">Custom Jump List Sample</span></span>

<span data-ttu-id="f530a-104">示範如何建立應用程式的自訂捷徑清單，包括新增自訂分類和工作。</span><span class="sxs-lookup"><span data-stu-id="f530a-104">Demonstrates how to create a custom Jump List for an application, including adding a custom category and tasks.</span></span>

<span data-ttu-id="f530a-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="f530a-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="f530a-106">需求</span><span class="sxs-lookup"><span data-stu-id="f530a-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="f530a-107">下載範例</span><span class="sxs-lookup"><span data-stu-id="f530a-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="f530a-108">建立範例</span><span class="sxs-lookup"><span data-stu-id="f530a-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="f530a-109">執行範例</span><span class="sxs-lookup"><span data-stu-id="f530a-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="f530a-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="f530a-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="f530a-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="f530a-111">Requirements</span></span>



| <span data-ttu-id="f530a-112">產品</span><span class="sxs-lookup"><span data-stu-id="f530a-112">Product</span></span>                                | <span data-ttu-id="f530a-113">最小產品版本</span><span class="sxs-lookup"><span data-stu-id="f530a-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="f530a-114">Windows</span><span class="sxs-lookup"><span data-stu-id="f530a-114">Windows</span></span>                                | <span data-ttu-id="f530a-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f530a-115">Windows 7</span></span>               |
| <span data-ttu-id="f530a-116">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="f530a-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="f530a-117">7.0</span><span class="sxs-lookup"><span data-stu-id="f530a-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="f530a-118">下載範例</span><span class="sxs-lookup"><span data-stu-id="f530a-118">Downloading the Sample</span></span>

| <span data-ttu-id="f530a-119">Location</span><span class="sxs-lookup"><span data-stu-id="f530a-119">Location</span></span>      | <span data-ttu-id="f530a-120">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="f530a-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f530a-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="f530a-121">GitHub</span></span>  | [<span data-ttu-id="f530a-122">CustomJumpList 範例</span><span class="sxs-lookup"><span data-stu-id="f530a-122">CustomJumpList sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CustomJumpList) |

## <a name="building-the-sample"></a><span data-ttu-id="f530a-123">建立範例</span><span class="sxs-lookup"><span data-stu-id="f530a-123">Building the Sample</span></span>

<span data-ttu-id="f530a-124">若要從命令提示字元建立範例：</span><span class="sxs-lookup"><span data-stu-id="f530a-124">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="f530a-125">開啟 [命令提示字元] 視窗，並流覽至 **CustomJumpList** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="f530a-125">Open the command prompt window and navigate to the **CustomJumpList** project directory.</span></span>
2.  <span data-ttu-id="f530a-126">輸入 `msbuild CustomJumpListSample.sln`。</span><span class="sxs-lookup"><span data-stu-id="f530a-126">Enter `msbuild CustomJumpListSample.sln`.</span></span>

<span data-ttu-id="f530a-127">若要使用 Microsoft Visual Studio (慣用的) 來建立範例：</span><span class="sxs-lookup"><span data-stu-id="f530a-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="f530a-128">開啟 Windows 檔案總管，然後流覽至 **CustomJumpList** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="f530a-128">Open Windows Explorer and navigate to the **CustomJumpList** project directory.</span></span>
2.  <span data-ttu-id="f530a-129">按兩下 CustomJumpListSample .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="f530a-129">Double-click the icon for the CustomJumpListSample.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="f530a-130">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="f530a-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="f530a-131">執行範例</span><span class="sxs-lookup"><span data-stu-id="f530a-131">Running the Sample</span></span>

1.  <span data-ttu-id="f530a-132">使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="f530a-132">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="f530a-133">在命令列中，輸入 `CustomJumpListSample.exe` 。</span><span class="sxs-lookup"><span data-stu-id="f530a-133">At the command line, enter `CustomJumpListSample.exe`.</span></span> <span data-ttu-id="f530a-134">或者，從 Windows 檔案總管按兩下 CustomJumpListSample.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="f530a-134">Alternatively, from Windows Explorer double-click the icon for CustomJumpListSample.exe.</span></span>
3.  <span data-ttu-id="f530a-135">在第一次執行此範例時，必須以系統管理員的身分執行，讓它可以安裝必要的檔案類型註冊。</span><span class="sxs-lookup"><span data-stu-id="f530a-135">This sample must be run as an administrator the first time it is run so that it can install the necessary file type registrations.</span></span> <span data-ttu-id="f530a-136">在註冊檔案類型之後，範例可以作為標準使用者來執行。</span><span class="sxs-lookup"><span data-stu-id="f530a-136">After the file types have been registered, the sample can run as a standard user.</span></span>
4.  <span data-ttu-id="f530a-137">從範例應用程式的功能表中選取 [選項]，以查看它們如何影響工作列中的應用程式捷徑清單。</span><span class="sxs-lookup"><span data-stu-id="f530a-137">Select options from the menu in the sample application to see how they affect the application's Jump List in the taskbar.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f530a-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="f530a-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f530a-139">應用程式使用者模型識別碼 (AppUserModelIDs) </span><span class="sxs-lookup"><span data-stu-id="f530a-139">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> </dl>

 

 



