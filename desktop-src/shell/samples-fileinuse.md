---
description: 示範如何自訂 [使用中的檔案] 對話方塊，以顯示應用程式中目前開啟之檔案的其他資訊和選項。
title: 檔案使用中範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 22EFE7CC-D223-46b3-BD6B-293E3FA0BA01
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 223e0addf201f3526654a17346963b4639e0d215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319347"
---
# <a name="file-is-in-use-sample"></a><span data-ttu-id="a5aee-103">檔案使用中範例</span><span class="sxs-lookup"><span data-stu-id="a5aee-103">File Is In Use Sample</span></span>

<span data-ttu-id="a5aee-104">示範如何自訂 [ **使用中** 的檔案] 對話方塊，以顯示應用程式中目前開啟之檔案的其他資訊和選項。</span><span class="sxs-lookup"><span data-stu-id="a5aee-104">Demonstrates how to customize the **File In Use** dialog to display additional information and options for files that are currently opened in the application.</span></span>

<span data-ttu-id="a5aee-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="a5aee-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="a5aee-106">需求</span><span class="sxs-lookup"><span data-stu-id="a5aee-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="a5aee-107">下載範例</span><span class="sxs-lookup"><span data-stu-id="a5aee-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="a5aee-108">建立範例</span><span class="sxs-lookup"><span data-stu-id="a5aee-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="a5aee-109">執行範例</span><span class="sxs-lookup"><span data-stu-id="a5aee-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="a5aee-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5aee-110">Requirements</span></span>



| <span data-ttu-id="a5aee-111">產品</span><span class="sxs-lookup"><span data-stu-id="a5aee-111">Product</span></span>                                | <span data-ttu-id="a5aee-112">最小產品版本</span><span class="sxs-lookup"><span data-stu-id="a5aee-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="a5aee-113">Windows</span><span class="sxs-lookup"><span data-stu-id="a5aee-113">Windows</span></span>                                | <span data-ttu-id="a5aee-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5aee-114">Windows Vista</span></span>           |
| <span data-ttu-id="a5aee-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="a5aee-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="a5aee-116">6.1</span><span class="sxs-lookup"><span data-stu-id="a5aee-116">6.1</span></span>                     |



 

<span data-ttu-id="a5aee-117">如需其他需求，請參閱 \_ 範例隨附的 IFileIsInUsesample.docx 檔。</span><span class="sxs-lookup"><span data-stu-id="a5aee-117">For additional requirements, see the IFileIsInUse\_sample.docx file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="a5aee-118">下載範例</span><span class="sxs-lookup"><span data-stu-id="a5aee-118">Downloading the Sample</span></span>

| <span data-ttu-id="a5aee-119">Location</span><span class="sxs-lookup"><span data-stu-id="a5aee-119">Location</span></span>      | <span data-ttu-id="a5aee-120">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="a5aee-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5aee-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="a5aee-121">GitHub</span></span>  | [<span data-ttu-id="a5aee-122">FileIsInUse 範例</span><span class="sxs-lookup"><span data-stu-id="a5aee-122">FileIsInUse sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse) |

## <a name="building-the-sample"></a><span data-ttu-id="a5aee-123">建立範例</span><span class="sxs-lookup"><span data-stu-id="a5aee-123">Building the Sample</span></span>

<span data-ttu-id="a5aee-124">若要從命令提示字元視窗建立範例：</span><span class="sxs-lookup"><span data-stu-id="a5aee-124">To build the sample from the Command Prompt window:</span></span>

1.  <span data-ttu-id="a5aee-125">開啟 [命令提示字元] 視窗，並流覽至 **FileIsInUse** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="a5aee-125">Open the Command Prompt window and navigate to the **FileIsInUse** project directory.</span></span>
2.  <span data-ttu-id="a5aee-126">輸入 `msbuild FileIsInUse.sln`。</span><span class="sxs-lookup"><span data-stu-id="a5aee-126">Enter `msbuild FileIsInUse.sln`.</span></span>

<span data-ttu-id="a5aee-127">若要使用 Microsoft Visual Studio (慣用的) 來建立範例：</span><span class="sxs-lookup"><span data-stu-id="a5aee-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="a5aee-128">開啟 Windows 檔案總管，然後流覽至 **FilesInUse** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="a5aee-128">Open Windows Explorer and navigate to the **FilesInUse** project directory.</span></span> <span data-ttu-id="a5aee-129">例如，完整的預設安裝路徑為 `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileIsInUse` 。</span><span class="sxs-lookup"><span data-stu-id="a5aee-129">For example, the full default installation path is `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileIsInUse`.</span></span>
2.  <span data-ttu-id="a5aee-130">按兩下 FileIsInUseSample .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="a5aee-130">Double-click the icon for the FileIsInUseSample.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="a5aee-131">.Sln 副檔名不會顯示在 [預設資料夾設定] 下。</span><span class="sxs-lookup"><span data-stu-id="a5aee-131">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="a5aee-132">在這種情況下，它可以透過其唯一圖示或其類型描述「Microsoft Visual Studio 解決方案」來識別。</span><span class="sxs-lookup"><span data-stu-id="a5aee-132">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="a5aee-133">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="a5aee-133">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="a5aee-134">執行範例</span><span class="sxs-lookup"><span data-stu-id="a5aee-134">Running the Sample</span></span>

1.  <span data-ttu-id="a5aee-135">使用命令提示字元視窗或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="a5aee-135">Navigate to the directory that contains the new executable, using the command prompt window or Windows Explorer.</span></span>
2.  <span data-ttu-id="a5aee-136">在命令提示字元中，輸入 `FileIsInUseSample.exe` ，或從 Windows 檔案總管中，按兩下 FileIsInUseSample.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="a5aee-136">At the command prompt, enter `FileIsInUseSample.exe`, or from Windows Explorer, double-click the icon for FileIsInUseSample.exe.</span></span>

<span data-ttu-id="a5aee-137">如需此程式碼範例的詳細資訊，請參閱 \_ 範例隨附的 IFileIsInUsesample.docx 檔。</span><span class="sxs-lookup"><span data-stu-id="a5aee-137">For detailed information about this code sample, see the IFileIsInUse\_sample.docx file included with the sample.</span></span>

 

 



