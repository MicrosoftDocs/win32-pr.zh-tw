---
description: PropertyEdit 程式碼範例示範如何將標準屬性名稱轉換成 PROPERTYKEY、將屬性存放區的值設定為專案的值，然後將資料寫回檔案資料流程。
ms.assetid: 5918b4f6-6b6f-4229-8f29-1c41f80b3b02
title: PropertyEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa248b9e86f8ab93cccba3d5d6b169d7e8699dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847815"
---
# <a name="propertyedit"></a><span data-ttu-id="aeece-103">PropertyEdit</span><span class="sxs-lookup"><span data-stu-id="aeece-103">PropertyEdit</span></span>

<span data-ttu-id="aeece-104">PropertyEdit 程式碼範例示範如何將標準屬性名稱轉換成 PROPERTYKEY、將屬性存放區的值設定為專案的值，然後將資料寫回檔案資料流程。</span><span class="sxs-lookup"><span data-stu-id="aeece-104">The PropertyEdit code sample demonstrates how to convert the canonical property name to a PROPERTYKEY, set the value of the property store to that of the item, and write the data back to the file stream.</span></span>

<span data-ttu-id="aeece-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="aeece-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="aeece-106">需求</span><span class="sxs-lookup"><span data-stu-id="aeece-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="aeece-107">下載範例</span><span class="sxs-lookup"><span data-stu-id="aeece-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="aeece-108">建立範例</span><span class="sxs-lookup"><span data-stu-id="aeece-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="aeece-109">執行範例</span><span class="sxs-lookup"><span data-stu-id="aeece-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="aeece-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="aeece-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="aeece-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="aeece-111">Requirements</span></span>



| <span data-ttu-id="aeece-112">產品</span><span class="sxs-lookup"><span data-stu-id="aeece-112">Product</span></span>     | <span data-ttu-id="aeece-113">最小產品版本</span><span class="sxs-lookup"><span data-stu-id="aeece-113">Minimum Product Version</span></span> |
|-------------|-------------------------|
| <span data-ttu-id="aeece-114">Windows</span><span class="sxs-lookup"><span data-stu-id="aeece-114">Windows</span></span>     | <span data-ttu-id="aeece-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="aeece-115">Windows 7</span></span>               |
| <span data-ttu-id="aeece-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="aeece-116">Windows SDK</span></span> | <span data-ttu-id="aeece-117">7.0</span><span class="sxs-lookup"><span data-stu-id="aeece-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="aeece-118">下載範例</span><span class="sxs-lookup"><span data-stu-id="aeece-118">Downloading the Sample</span></span>

<span data-ttu-id="aeece-119">下列位置提供此範例。</span><span class="sxs-lookup"><span data-stu-id="aeece-119">This sample is available in the following locations.</span></span>



| <span data-ttu-id="aeece-120">Location</span><span class="sxs-lookup"><span data-stu-id="aeece-120">Location</span></span>      | <span data-ttu-id="aeece-121">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="aeece-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="aeece-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="aeece-122">GitHub</span></span>  | [<span data-ttu-id="aeece-123">PropertyEdit 範例</span><span class="sxs-lookup"><span data-stu-id="aeece-123">PropertyEdit sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/PropertyEdit)    |



 

 

> [!Note]  
> <span data-ttu-id="aeece-124">針對所有 Windows 版本（包括 Windows 7），建議您直接從 GitHub 下載最新版本的範例。</span><span class="sxs-lookup"><span data-stu-id="aeece-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

 

## <a name="building-the-sample"></a><span data-ttu-id="aeece-125">建立範例</span><span class="sxs-lookup"><span data-stu-id="aeece-125">Building the Sample</span></span>

<span data-ttu-id="aeece-126">若要從命令提示字元建立範例：</span><span class="sxs-lookup"><span data-stu-id="aeece-126">To build the sample from the Command Prompt:</span></span>

1.  <span data-ttu-id="aeece-127">開啟 [命令提示字元] 視窗，並流覽至 **PropertyEdit** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="aeece-127">Open the Command Prompt window and navigate to the **PropertyEdit** project directory.</span></span> 
2.  <span data-ttu-id="aeece-128">輸入 `msbuild PropertyEdit.sln`。</span><span class="sxs-lookup"><span data-stu-id="aeece-128">Enter `msbuild PropertyEdit.sln`.</span></span>

<span data-ttu-id="aeece-129">若要使用 Microsoft Visual Studio (慣用的) 來建立範例：</span><span class="sxs-lookup"><span data-stu-id="aeece-129">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="aeece-130">開啟 Windows 檔案總管，然後流覽至 **PropertyEdit** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="aeece-130">Open Windows Explorer and navigate to the **PropertyEdit** project directory.</span></span>
2.  <span data-ttu-id="aeece-131">按兩下 PropertyEdit .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="aeece-131">Double-click the icon for the PropertyEdit.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="aeece-132">.Sln 副檔名不會顯示在 [預設資料夾設定] 下。</span><span class="sxs-lookup"><span data-stu-id="aeece-132">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="aeece-133">在這種情況下，它可以透過其唯一圖示或其類型描述「Microsoft Visual Studio 解決方案」來識別。</span><span class="sxs-lookup"><span data-stu-id="aeece-133">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="aeece-134">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="aeece-134">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="aeece-135">執行範例</span><span class="sxs-lookup"><span data-stu-id="aeece-135">Running the Sample</span></span>

1.  <span data-ttu-id="aeece-136">使用命令提示字元視窗或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="aeece-136">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2.  <span data-ttu-id="aeece-137">在命令提示字元中，輸入 `PropertyEdit.exe` ，或從 Windows 檔案總管中，按兩下 PropertyEdit.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="aeece-137">At the command prompt, enter `PropertyEdit.exe`, or from Windows Explorer, double-click the icon for PropertyEdit.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aeece-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="aeece-138">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="aeece-139">**概念**</span><span class="sxs-lookup"><span data-stu-id="aeece-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="aeece-140">搜尋程式碼範例</span><span class="sxs-lookup"><span data-stu-id="aeece-140">Search Code Samples</span></span>](-search-samples-ovw.md)
</dt> <dt>

<span data-ttu-id="aeece-141">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="aeece-141">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="aeece-142">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="aeece-142">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> <dt>

[<span data-ttu-id="aeece-143">關於屬性和屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="aeece-143">About Properties and Property Handlers</span></span>](../properties/building-property-handlers-properties.md)
</dt> <dt>

<span data-ttu-id="aeece-144">[屬性描述架構](/previous-versions//cc144127(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="aeece-144">[Property Description Schema](/previous-versions//cc144127(v=vs.85))</span></span>
</dt> </dl>

 

 
