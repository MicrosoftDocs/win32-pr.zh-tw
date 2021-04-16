---
description: CompLocator 資料表包含尋找使用安裝程式設定資料之檔案或目錄所需的資訊。
ms.assetid: 8b527307-51bf-47b3-a0b2-3421cc5278b7
title: CompLocator 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9fcb4a3c4f2e2c6f3ca3c92f6dc7466326bd11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514153"
---
# <a name="complocator-table"></a><span data-ttu-id="e6cce-103">CompLocator 資料表</span><span class="sxs-lookup"><span data-stu-id="e6cce-103">CompLocator Table</span></span>

<span data-ttu-id="e6cce-104">CompLocator 資料表包含尋找使用安裝程式設定資料之檔案或目錄所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="e6cce-104">The CompLocator Table contains the information needed to find a file or directory that is using the installer configuration data.</span></span>

<span data-ttu-id="e6cce-105">CompLocator 資料表包含下列資訊。</span><span class="sxs-lookup"><span data-stu-id="e6cce-105">The CompLocator table contains the following information.</span></span>



| <span data-ttu-id="e6cce-106">Column</span><span class="sxs-lookup"><span data-stu-id="e6cce-106">Column</span></span>      | <span data-ttu-id="e6cce-107">類型</span><span class="sxs-lookup"><span data-stu-id="e6cce-107">Type</span></span>                         | <span data-ttu-id="e6cce-108">答案</span><span class="sxs-lookup"><span data-stu-id="e6cce-108">Key</span></span> | <span data-ttu-id="e6cce-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="e6cce-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="e6cce-110">簽名\_</span><span class="sxs-lookup"><span data-stu-id="e6cce-110">Signature\_</span></span> | [<span data-ttu-id="e6cce-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="e6cce-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="e6cce-112">Y</span><span class="sxs-lookup"><span data-stu-id="e6cce-112">Y</span></span>   | <span data-ttu-id="e6cce-113">N</span><span class="sxs-lookup"><span data-stu-id="e6cce-113">N</span></span>        |
| <span data-ttu-id="e6cce-114">ComponentId</span><span class="sxs-lookup"><span data-stu-id="e6cce-114">ComponentId</span></span> | [<span data-ttu-id="e6cce-115">GUID</span><span class="sxs-lookup"><span data-stu-id="e6cce-115">GUID</span></span>](guid.md)             | <span data-ttu-id="e6cce-116">N</span><span class="sxs-lookup"><span data-stu-id="e6cce-116">N</span></span>   | <span data-ttu-id="e6cce-117">N</span><span class="sxs-lookup"><span data-stu-id="e6cce-117">N</span></span>        |
| <span data-ttu-id="e6cce-118">類型</span><span class="sxs-lookup"><span data-stu-id="e6cce-118">Type</span></span>        | [<span data-ttu-id="e6cce-119">整數</span><span class="sxs-lookup"><span data-stu-id="e6cce-119">Integer</span></span>](integer.md)       | <span data-ttu-id="e6cce-120">N</span><span class="sxs-lookup"><span data-stu-id="e6cce-120">N</span></span>   | <span data-ttu-id="e6cce-121">Y</span><span class="sxs-lookup"><span data-stu-id="e6cce-121">Y</span></span>        |



 

## <a name="column-information"></a><span data-ttu-id="e6cce-122">資料行資訊</span><span class="sxs-lookup"><span data-stu-id="e6cce-122">Column Information</span></span>

<dl> <dt>

<span data-ttu-id="e6cce-123"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>簽名\_</span><span class="sxs-lookup"><span data-stu-id="e6cce-123"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="e6cce-124">此資料行代表唯一的檔案簽章，而且也是簽章 [資料表](signature-table.md)中的外部金鑰。</span><span class="sxs-lookup"><span data-stu-id="e6cce-124">This column represents a unique file signature and is also the external key into the [Signature Table](signature-table.md).</span></span> <span data-ttu-id="e6cce-125">如果簽章資料表中的索引鍵不存在，則會假設搜尋是為了讓 CompLocator 資料表所指向的目錄存在。</span><span class="sxs-lookup"><span data-stu-id="e6cce-125">If the key is absent from the Signature Table, the search is assumed to be for the presence of a directory pointed to by the CompLocator Table.</span></span>

</dd> <dt>

<span data-ttu-id="e6cce-126"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId</span><span class="sxs-lookup"><span data-stu-id="e6cce-126"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId</span></span>
</dt> <dd>

<span data-ttu-id="e6cce-127">元件的元件識別碼，其金鑰路徑會用於搜尋。</span><span class="sxs-lookup"><span data-stu-id="e6cce-127">The component ID of the component whose key path is to be used for the search.</span></span> <span data-ttu-id="e6cce-128">這應該是元件 [資料表](component-table.md)的 [元件] 欄位中所顯示元件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="e6cce-128">This should be the GUID of a component that appears in the ComponentId field of the [Component Table](component-table.md).</span></span> <span data-ttu-id="e6cce-129">它可能是屬於電腦上所安裝之另一個產品之元件的元件識別碼。</span><span class="sxs-lookup"><span data-stu-id="e6cce-129">It may be the component ID of a component belonging to another product installed on the computer.</span></span> <span data-ttu-id="e6cce-130">它不應該是出現在 [PublishComponent 資料表](publishcomponent-table.md)之 [元件] 欄位中的已發行元件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="e6cce-130">It should not be the GUID of a published component appearing in the ComponentId field of the [PublishComponent Table](publishcomponent-table.md).</span></span>

<span data-ttu-id="e6cce-131">若要尋找另一個產品所安裝之檔案的元件識別碼 GUID 值，請移至產品的安裝套件。</span><span class="sxs-lookup"><span data-stu-id="e6cce-131">To find the component ID GUID value for a file installed by another product, go to the installation package of the product.</span></span> <span data-ttu-id="e6cce-132">移至 [檔案] [資料表](file-table.md) ，並尋找包含檔案之檔案識別碼的資料列。</span><span class="sxs-lookup"><span data-stu-id="e6cce-132">Go to the [File Table](file-table.md) and find the row that contains the file identifier for the file.</span></span> <span data-ttu-id="e6cce-133">此資料列的 [元件] 資料 \_ 行包含控制檔案之元件的元件識別碼。</span><span class="sxs-lookup"><span data-stu-id="e6cce-133">The Component\_ column of this row contains the component identifier for the component that controls the file.</span></span> <span data-ttu-id="e6cce-134">移至 [元件資料表](component-table.md) ，並在 [元件] 資料行中尋找包含此元件識別碼的資料列。</span><span class="sxs-lookup"><span data-stu-id="e6cce-134">Go to the [Component table](component-table.md) and find the row that contains this component identifier in the Component column.</span></span> <span data-ttu-id="e6cce-135">此資料列的 [元件識別碼] 資料行包含元件識別碼 GUID。</span><span class="sxs-lookup"><span data-stu-id="e6cce-135">The ComponentId column of this row contains the component ID GUID.</span></span>

</dd> <dt>

<span data-ttu-id="e6cce-136"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>類型</span><span class="sxs-lookup"><span data-stu-id="e6cce-136"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="e6cce-137">布林值，判斷元件的金鑰路徑是否為檔案名或目錄位置。</span><span class="sxs-lookup"><span data-stu-id="e6cce-137">A Boolean value that determines if the key path of the component is a file name or a directory location.</span></span>

<span data-ttu-id="e6cce-138">下表列出有效的值。</span><span class="sxs-lookup"><span data-stu-id="e6cce-138">The following table lists valid values.</span></span> <span data-ttu-id="e6cce-139">如果不存在，則類型會設定為1， (一個) 。</span><span class="sxs-lookup"><span data-stu-id="e6cce-139">If absent, Type is set to be 1 (one).</span></span>



| <span data-ttu-id="e6cce-140">常數</span><span class="sxs-lookup"><span data-stu-id="e6cce-140">Constant</span></span>                      | <span data-ttu-id="e6cce-141">十六進位</span><span class="sxs-lookup"><span data-stu-id="e6cce-141">Hexadecimal</span></span> | <span data-ttu-id="e6cce-142">Decimal</span><span class="sxs-lookup"><span data-stu-id="e6cce-142">Decimal</span></span> | <span data-ttu-id="e6cce-143">Description</span><span class="sxs-lookup"><span data-stu-id="e6cce-143">Description</span></span>              |
|-------------------------------|-------------|---------|--------------------------|
| <span data-ttu-id="e6cce-144">**msidbLocatorTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="e6cce-144">**msidbLocatorTypeDirectory**</span></span> | <span data-ttu-id="e6cce-145">0x000</span><span class="sxs-lookup"><span data-stu-id="e6cce-145">0x000</span></span>       | <span data-ttu-id="e6cce-146">0</span><span class="sxs-lookup"><span data-stu-id="e6cce-146">0</span></span>       | <span data-ttu-id="e6cce-147">金鑰路徑是目錄。</span><span class="sxs-lookup"><span data-stu-id="e6cce-147">Key path is a directory.</span></span> |
| <span data-ttu-id="e6cce-148">**msidbLocatorTypeFileName**</span><span class="sxs-lookup"><span data-stu-id="e6cce-148">**msidbLocatorTypeFileName**</span></span>  | <span data-ttu-id="e6cce-149">0x001</span><span class="sxs-lookup"><span data-stu-id="e6cce-149">0x001</span></span>       | <span data-ttu-id="e6cce-150">1</span><span class="sxs-lookup"><span data-stu-id="e6cce-150">1</span></span>       | <span data-ttu-id="e6cce-151">金鑰路徑是檔案名。</span><span class="sxs-lookup"><span data-stu-id="e6cce-151">Key path is a file name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6cce-152">備註</span><span class="sxs-lookup"><span data-stu-id="e6cce-152">Remarks</span></span>

<span data-ttu-id="e6cce-153">此資料表與 [AppSearch 資料表](appsearch-table.md)搭配使用。</span><span class="sxs-lookup"><span data-stu-id="e6cce-153">This table is used with the [AppSearch Table](appsearch-table.md).</span></span>

<span data-ttu-id="e6cce-154">一般而言，此資料表中的資料行並不會當地語系化。</span><span class="sxs-lookup"><span data-stu-id="e6cce-154">Typically, the columns in this table are not localized.</span></span> <span data-ttu-id="e6cce-155">如果作者決定搜尋多種語言的產品，則每種語言的表格中都可以有個別的專案。</span><span class="sxs-lookup"><span data-stu-id="e6cce-155">If an author decides to search for products in multiple languages, then there can be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="e6cce-156">如需詳細資訊，請參閱 [搜尋現有的應用程式、檔案、登錄專案或 .ini 檔專案](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)。</span><span class="sxs-lookup"><span data-stu-id="e6cce-156">For more information, see [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="e6cce-157">驗證</span><span class="sxs-lookup"><span data-stu-id="e6cce-157">Validation</span></span>

<dl>

[<span data-ttu-id="e6cce-158">ICE03</span><span class="sxs-lookup"><span data-stu-id="e6cce-158">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="e6cce-159">ICE06</span><span class="sxs-lookup"><span data-stu-id="e6cce-159">ICE06</span></span>](ice06.md)  
</dl>

 

 



