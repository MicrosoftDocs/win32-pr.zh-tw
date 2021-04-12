---
description: SFPCatalog 資料表包含 Windows Me 使用的目錄。
ms.assetid: e9dc65a9-4ec9-4310-b03a-a2c38720ca8c
title: SFPCatalog 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fe887644faf6cf0a5cda626bbf757e9f448ef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191602"
---
# <a name="sfpcatalog-table"></a><span data-ttu-id="fdae7-103">SFPCatalog 資料表</span><span class="sxs-lookup"><span data-stu-id="fdae7-103">SFPCatalog Table</span></span>

<span data-ttu-id="fdae7-104">SFPCatalog 資料表包含 Windows Me 使用的目錄。</span><span class="sxs-lookup"><span data-stu-id="fdae7-104">The SFPCatalog table contains the catalogs used by Windows Me.</span></span>

<span data-ttu-id="fdae7-105">SFPCatalog 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="fdae7-105">The SFPCatalog table has the following columns.</span></span>



| <span data-ttu-id="fdae7-106">Column</span><span class="sxs-lookup"><span data-stu-id="fdae7-106">Column</span></span>     | <span data-ttu-id="fdae7-107">類型</span><span class="sxs-lookup"><span data-stu-id="fdae7-107">Type</span></span>                       | <span data-ttu-id="fdae7-108">答案</span><span class="sxs-lookup"><span data-stu-id="fdae7-108">Key</span></span> | <span data-ttu-id="fdae7-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="fdae7-109">Nullable</span></span> |
|------------|----------------------------|-----|----------|
| <span data-ttu-id="fdae7-110">SFPCatalog</span><span class="sxs-lookup"><span data-stu-id="fdae7-110">SFPCatalog</span></span> | [<span data-ttu-id="fdae7-111">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="fdae7-111">Filename</span></span>](filename.md)   | <span data-ttu-id="fdae7-112">Y</span><span class="sxs-lookup"><span data-stu-id="fdae7-112">Y</span></span>   | <span data-ttu-id="fdae7-113">N</span><span class="sxs-lookup"><span data-stu-id="fdae7-113">N</span></span>        |
| <span data-ttu-id="fdae7-114">目錄</span><span class="sxs-lookup"><span data-stu-id="fdae7-114">Catalog</span></span>    | [<span data-ttu-id="fdae7-115">二進位</span><span class="sxs-lookup"><span data-stu-id="fdae7-115">Binary</span></span>](binary.md)       | <span data-ttu-id="fdae7-116">N</span><span class="sxs-lookup"><span data-stu-id="fdae7-116">N</span></span>   | <span data-ttu-id="fdae7-117">N</span><span class="sxs-lookup"><span data-stu-id="fdae7-117">N</span></span>        |
| <span data-ttu-id="fdae7-118">相依性</span><span class="sxs-lookup"><span data-stu-id="fdae7-118">Dependency</span></span> | [<span data-ttu-id="fdae7-119">格式 化</span><span class="sxs-lookup"><span data-stu-id="fdae7-119">Formatted</span></span>](formatted.md) | <span data-ttu-id="fdae7-120">N</span><span class="sxs-lookup"><span data-stu-id="fdae7-120">N</span></span>   | <span data-ttu-id="fdae7-121">Y</span><span class="sxs-lookup"><span data-stu-id="fdae7-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="fdae7-122">資料行</span><span class="sxs-lookup"><span data-stu-id="fdae7-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="fdae7-123"><span id="SFPCatalog"></span><span id="sfpcatalog"></span><span id="SFPCATALOG"></span>SFPCatalog</span><span class="sxs-lookup"><span data-stu-id="fdae7-123"><span id="SFPCatalog"></span><span id="sfpcatalog"></span><span id="SFPCATALOG"></span>SFPCatalog</span></span>
</dt> <dd>

<span data-ttu-id="fdae7-124">目錄的簡短檔案名。</span><span class="sxs-lookup"><span data-stu-id="fdae7-124">The short file name for the catalog.</span></span> <span data-ttu-id="fdae7-125">因為目錄沒有版本，所以在此資料行中指定的目錄可以覆寫具有相同名稱且已安裝在本機系統上的目錄。</span><span class="sxs-lookup"><span data-stu-id="fdae7-125">Because catalogs have no version, the catalog specified in this column can overwrite a catalog that has the same name and is already installed on the local system.</span></span> <span data-ttu-id="fdae7-126">請參閱檔案版本設定主題， [這兩個檔案都沒有版本](neither-file-has-a-version.md)。</span><span class="sxs-lookup"><span data-stu-id="fdae7-126">See the file versioning topic [Neither File Has a Version](neither-file-has-a-version.md).</span></span>

</dd> <dt>

<span data-ttu-id="fdae7-127"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>目錄</span><span class="sxs-lookup"><span data-stu-id="fdae7-127"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span>
</dt> <dd>

<span data-ttu-id="fdae7-128">目錄的二進位資料。</span><span class="sxs-lookup"><span data-stu-id="fdae7-128">Binary data for the catalog.</span></span>

</dd> <dt>

<span data-ttu-id="fdae7-129"><span id="Dependency"></span><span id="dependency"></span><span id="DEPENDENCY"></span>依賴</span><span class="sxs-lookup"><span data-stu-id="fdae7-129"><span id="Dependency"></span><span id="dependency"></span><span id="DEPENDENCY"></span>Dependency</span></span>
</dt> <dd>

<span data-ttu-id="fdae7-130">此欄位中指定的目錄是 SFPCatalog 欄位中指定之相依目錄的父系。</span><span class="sxs-lookup"><span data-stu-id="fdae7-130">The catalog specified in this field is the parent of the dependent catalog specified in the SFPCatalog field.</span></span> <span data-ttu-id="fdae7-131">在 [相依性] 欄位中輸入父目錄的簡短檔案名。</span><span class="sxs-lookup"><span data-stu-id="fdae7-131">Enter the short file name of the parent catalog into the Dependency field.</span></span> <span data-ttu-id="fdae7-132">此欄位是回 SFPCatalog 資料行的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="fdae7-132">This field is a key back into the SFPCatalog column.</span></span> <span data-ttu-id="fdae7-133">相依性相符會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="fdae7-133">The dependency match is case sensitive.</span></span>

<span data-ttu-id="fdae7-134">如果相依性欄位參考此 SFPCatalog 資料表中的另一筆記錄，則會在相依目錄之前安裝父目錄。</span><span class="sxs-lookup"><span data-stu-id="fdae7-134">If the Dependency field references another record in this SFPCatalog table, the parent catalog is installed before the dependent catalog.</span></span>

<span data-ttu-id="fdae7-135">如果相依性欄位參考的父類別目錄不在此資料表的 SFPCatalog 欄位中，而且如果尚未安裝父目錄，則安裝會失敗。</span><span class="sxs-lookup"><span data-stu-id="fdae7-135">If the Dependency field references a parent catalog that is not present in the SFPCatalog field of this table, and if the parent catalog is not already installed, the installation fails.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fdae7-136">備註</span><span class="sxs-lookup"><span data-stu-id="fdae7-136">Remarks</span></span>

<span data-ttu-id="fdae7-137">[InstallSFPCatalogFile 動作](installsfpcatalogfile-action.md)會查詢[Component 資料表](component-table.md)、 [File Table](file-table.md)、 [FileSFPCatalog table](filesfpcatalog-table.md)和 SFPCatalog 資料表。</span><span class="sxs-lookup"><span data-stu-id="fdae7-137">The [InstallSFPCatalogFile action](installsfpcatalogfile-action.md) queries the [Component table](component-table.md), [File table](file-table.md), [FileSFPCatalog table](filesfpcatalog-table.md) and SFPCatalog table.</span></span>

## <a name="validation"></a><span data-ttu-id="fdae7-138">驗證</span><span class="sxs-lookup"><span data-stu-id="fdae7-138">Validation</span></span>

<dl>

[<span data-ttu-id="fdae7-139">ICE03</span><span class="sxs-lookup"><span data-stu-id="fdae7-139">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="fdae7-140">ICE06</span><span class="sxs-lookup"><span data-stu-id="fdae7-140">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="fdae7-141">ICE29</span><span class="sxs-lookup"><span data-stu-id="fdae7-141">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="fdae7-142">ICE32</span><span class="sxs-lookup"><span data-stu-id="fdae7-142">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="fdae7-143">ICE46</span><span class="sxs-lookup"><span data-stu-id="fdae7-143">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="fdae7-144">ICE66</span><span class="sxs-lookup"><span data-stu-id="fdae7-144">ICE66</span></span>](ice66.md)  
</dl>

 

 



