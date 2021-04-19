---
description: ICE76 會確認適用于 Windows Me Windows Installer 套件內的 SFP (WFP) 目錄。 這項 ICE 也會確認 BindImage 資料表中沒有任何檔案參考 SFP 目錄。
ms.assetid: e8b60b11-19ac-4ec4-aa36-a1f7a3ccd6f6
title: ICE76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5beb0157053e9bd3e4bf0d896f52af04a511ac24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972460"
---
# <a name="ice76"></a><span data-ttu-id="c75d8-104">ICE76</span><span class="sxs-lookup"><span data-stu-id="c75d8-104">ICE76</span></span>

<span data-ttu-id="c75d8-105">ICE76 會確認適用于 Windows Me Windows Installer 套件內的 SFP (WFP) 目錄。</span><span class="sxs-lookup"><span data-stu-id="c75d8-105">ICE76 verifies the use of the SFP (WFP) catalog within Windows Installer packages for Windows Me.</span></span> <span data-ttu-id="c75d8-106">這項 ICE 也會確認 BindImage [資料表](bindimage-table.md) 中沒有任何檔案參考 SFP 目錄。</span><span class="sxs-lookup"><span data-stu-id="c75d8-106">This ICE also verifies that no files in the BindImage [table](bindimage-table.md) reference SFP catalogs.</span></span>

<span data-ttu-id="c75d8-107">Windows 檔案保護需要在類別目錄檔案中內嵌的檔案和簽章完全相符。</span><span class="sxs-lookup"><span data-stu-id="c75d8-107">Windows File Protection requires an exact match between the file and the signature embedded in the catalog file.</span></span> <span data-ttu-id="c75d8-108">參考 SFP 類別目錄的檔案不能列在 BindImage 資料表中，因為這些檔案的 [BindImage 動作](bindimage-action.md) 效果與電腦之間的不同。</span><span class="sxs-lookup"><span data-stu-id="c75d8-108">Files that reference a SFP catalog must not be listed in the BindImage table because the effect of the [BindImage action](bindimage-action.md) on these files differs between computers.</span></span> <span data-ttu-id="c75d8-109">SFP 類別目錄所參考的檔案必須位於永久或本機安裝的元件中。</span><span class="sxs-lookup"><span data-stu-id="c75d8-109">Files referenced by SFP catalogs must be in components that are permanent or installed locally.</span></span>

## <a name="result"></a><span data-ttu-id="c75d8-110">結果</span><span class="sxs-lookup"><span data-stu-id="c75d8-110">Result</span></span>

<span data-ttu-id="c75d8-111">ICE76 會將 [BindImage 資料表](bindimage-table.md) 中的每個檔案的錯誤張貼在 [FileSFPCatalog 資料表](filesfpcatalog-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="c75d8-111">ICE76 posts an error for each file in the [BindImage table](bindimage-table.md) that is also in the [FileSFPCatalog table](filesfpcatalog-table.md).</span></span>

<span data-ttu-id="c75d8-112">如果 FileSFPCatalog 資料表中的檔案屬於下列任何 true 的元件，ICE76 會輸出錯誤：</span><span class="sxs-lookup"><span data-stu-id="c75d8-112">ICE76 outputs an error if a file in the FileSFPCatalog table belongs to a component with any of the following true:</span></span>

-   <span data-ttu-id="c75d8-113">**msidbComponentAttributesPermanent** 不會在 [元件資料表](component-table.md)的 [屬性] 資料行中設定。</span><span class="sxs-lookup"><span data-stu-id="c75d8-113">**msidbComponentAttributesPermanent** is not set in the Attributes column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="c75d8-114">**msidbComponentAttributesSourceOnly** 是在元件資料表的 [屬性] 資料行中設定。</span><span class="sxs-lookup"><span data-stu-id="c75d8-114">**msidbComponentAttributesSourceOnly** is set in the Attributes column of the Component table.</span></span>
-   <span data-ttu-id="c75d8-115">**msidbAttributesOptional** 是在元件資料表的 [屬性] 資料行中設定。</span><span class="sxs-lookup"><span data-stu-id="c75d8-115">**msidbAttributesOptional** is set in the Attributes column of the Component table.</span></span>

## <a name="example"></a><span data-ttu-id="c75d8-116">範例</span><span class="sxs-lookup"><span data-stu-id="c75d8-116">Example</span></span>

<span data-ttu-id="c75d8-117">ICE76 會報告此範例的下列錯誤：</span><span class="sxs-lookup"><span data-stu-id="c75d8-117">ICE76 reports the following error for the example:</span></span>

``` syntax
File 'File1' references a SFP catalog. Therefore it cannot be in the BindImage table.
```

<span data-ttu-id="c75d8-118">[FileSFPCatalog 資料表](filesfpcatalog-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="c75d8-118">[FileSFPCatalog Table](filesfpcatalog-table.md) (partial)</span></span>



| <span data-ttu-id="c75d8-119">檔案\_</span><span class="sxs-lookup"><span data-stu-id="c75d8-119">File\_</span></span> | <span data-ttu-id="c75d8-120">SFPCatalog\_</span><span class="sxs-lookup"><span data-stu-id="c75d8-120">SFPCatalog\_</span></span> |
|--------|--------------|
| <span data-ttu-id="c75d8-121">File1</span><span class="sxs-lookup"><span data-stu-id="c75d8-121">File1</span></span>  | <span data-ttu-id="c75d8-122">Catalog1.Cat</span><span class="sxs-lookup"><span data-stu-id="c75d8-122">Catalog1.Cat</span></span> |



 

<span data-ttu-id="c75d8-123">[BindImage 資料表](bindimage-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="c75d8-123">[BindImage Table](bindimage-table.md) (partial)</span></span>



| <span data-ttu-id="c75d8-124">檔案\_</span><span class="sxs-lookup"><span data-stu-id="c75d8-124">File\_</span></span> |
|--------|
| <span data-ttu-id="c75d8-125">File1</span><span class="sxs-lookup"><span data-stu-id="c75d8-125">File1</span></span>  |



 

<span data-ttu-id="c75d8-126">若要修正此問題，請不要在 BindImage 資料表中輸入參考 SFP 目錄的任何檔案。</span><span class="sxs-lookup"><span data-stu-id="c75d8-126">To fix this do not enter any files that reference SFP catalogs into the BindImage table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c75d8-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="c75d8-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c75d8-128">BindImage 資料表</span><span class="sxs-lookup"><span data-stu-id="c75d8-128">BindImage Table</span></span>](bindimage-table.md)
</dt> <dt>

[<span data-ttu-id="c75d8-129">元件資料表</span><span class="sxs-lookup"><span data-stu-id="c75d8-129">Component Table</span></span>](component-table.md)
</dt> <dt>

[<span data-ttu-id="c75d8-130">FileSFPCatalog 資料表</span><span class="sxs-lookup"><span data-stu-id="c75d8-130">FileSFPCatalog Table</span></span>](filesfpcatalog-table.md)
</dt> <dt>

[<span data-ttu-id="c75d8-131">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="c75d8-131">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



