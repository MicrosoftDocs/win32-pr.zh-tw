---
description: ReserveCost 資料表是選擇性的表格，可讓作者保留任何目錄中的磁碟空間量，而這些目錄相依于元件的安裝狀態。
ms.assetid: 371e72f1-40a2-4ed2-b0ab-33840075ff47
title: ReserveCost 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f593fd11789cd2304385b97e96e50a009fbde0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944478"
---
# <a name="reservecost-table"></a><span data-ttu-id="2329a-103">ReserveCost 資料表</span><span class="sxs-lookup"><span data-stu-id="2329a-103">ReserveCost Table</span></span>

<span data-ttu-id="2329a-104">ReserveCost 資料表是選擇性的表格，可讓作者保留任何目錄中的磁碟空間量，而這些目錄相依于元件的安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="2329a-104">The ReserveCost table is an optional table that allows the author to reserve an amount of disk space in any directory that depends on the installation state of a component.</span></span>

<span data-ttu-id="2329a-105">ReserveCost 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="2329a-105">The ReserveCost table has the following columns.</span></span>



| <span data-ttu-id="2329a-106">Column</span><span class="sxs-lookup"><span data-stu-id="2329a-106">Column</span></span>        | <span data-ttu-id="2329a-107">類型</span><span class="sxs-lookup"><span data-stu-id="2329a-107">Type</span></span>                               | <span data-ttu-id="2329a-108">答案</span><span class="sxs-lookup"><span data-stu-id="2329a-108">Key</span></span> | <span data-ttu-id="2329a-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="2329a-109">Nullable</span></span> |
|---------------|------------------------------------|-----|----------|
| <span data-ttu-id="2329a-110">ReserveKey</span><span class="sxs-lookup"><span data-stu-id="2329a-110">ReserveKey</span></span>    | [<span data-ttu-id="2329a-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="2329a-111">Identifier</span></span>](identifier.md)       | <span data-ttu-id="2329a-112">Y</span><span class="sxs-lookup"><span data-stu-id="2329a-112">Y</span></span>   | <span data-ttu-id="2329a-113">N</span><span class="sxs-lookup"><span data-stu-id="2329a-113">N</span></span>        |
| <span data-ttu-id="2329a-114">元件\_</span><span class="sxs-lookup"><span data-stu-id="2329a-114">Component\_</span></span>   | [<span data-ttu-id="2329a-115">識別碼</span><span class="sxs-lookup"><span data-stu-id="2329a-115">Identifier</span></span>](identifier.md)       | <span data-ttu-id="2329a-116">N</span><span class="sxs-lookup"><span data-stu-id="2329a-116">N</span></span>   | <span data-ttu-id="2329a-117">N</span><span class="sxs-lookup"><span data-stu-id="2329a-117">N</span></span>        |
| <span data-ttu-id="2329a-118">ReserveFolder</span><span class="sxs-lookup"><span data-stu-id="2329a-118">ReserveFolder</span></span> | [<span data-ttu-id="2329a-119">識別碼</span><span class="sxs-lookup"><span data-stu-id="2329a-119">Identifier</span></span>](identifier.md)       | <span data-ttu-id="2329a-120">N</span><span class="sxs-lookup"><span data-stu-id="2329a-120">N</span></span>   | <span data-ttu-id="2329a-121">Y</span><span class="sxs-lookup"><span data-stu-id="2329a-121">Y</span></span>        |
| <span data-ttu-id="2329a-122">ReserveLocal</span><span class="sxs-lookup"><span data-stu-id="2329a-122">ReserveLocal</span></span>  | [<span data-ttu-id="2329a-123">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="2329a-123">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="2329a-124">N</span><span class="sxs-lookup"><span data-stu-id="2329a-124">N</span></span>   | <span data-ttu-id="2329a-125">N</span><span class="sxs-lookup"><span data-stu-id="2329a-125">N</span></span>        |
| <span data-ttu-id="2329a-126">ReserveSource</span><span class="sxs-lookup"><span data-stu-id="2329a-126">ReserveSource</span></span> | [<span data-ttu-id="2329a-127">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="2329a-127">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="2329a-128">N</span><span class="sxs-lookup"><span data-stu-id="2329a-128">N</span></span>   | <span data-ttu-id="2329a-129">N</span><span class="sxs-lookup"><span data-stu-id="2329a-129">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="2329a-130">資料行</span><span class="sxs-lookup"><span data-stu-id="2329a-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="2329a-131"><span id="ReserveKey"></span><span id="reservekey"></span><span id="RESERVEKEY"></span>ReserveKey</span><span class="sxs-lookup"><span data-stu-id="2329a-131"><span id="ReserveKey"></span><span id="reservekey"></span><span id="RESERVEKEY"></span>ReserveKey</span></span>
</dt> <dd>

<span data-ttu-id="2329a-132">可唯一識別 ReserveCost 資料表專案的主鍵。</span><span class="sxs-lookup"><span data-stu-id="2329a-132">Primary key that uniquely identifies a ReserveCost table entry.</span></span>

</dd> <dt>

<span data-ttu-id="2329a-133"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_</span><span class="sxs-lookup"><span data-stu-id="2329a-133"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="2329a-134">[元件](component-table.md)資料表中第一個資料行的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="2329a-134">External key to column one of the [Component](component-table.md) table.</span></span> <span data-ttu-id="2329a-135">如果要安裝此元件，則保留指定的空間量。</span><span class="sxs-lookup"><span data-stu-id="2329a-135">Reserves a specified amount of space if this component is to be installed.</span></span>

</dd> <dt>

<span data-ttu-id="2329a-136"><span id="ReserveFolder"></span><span id="reservefolder"></span><span id="RESERVEFOLDER"></span>ReserveFolder</span><span class="sxs-lookup"><span data-stu-id="2329a-136"><span id="ReserveFolder"></span><span id="reservefolder"></span><span id="RESERVEFOLDER"></span>ReserveFolder</span></span>
</dt> <dd>

<span data-ttu-id="2329a-137">此資料行包含的屬性名稱是目的地目錄的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="2329a-137">This column contains the name of a property that is the full path to the destination directory.</span></span> <span data-ttu-id="2329a-138">這個屬性名稱通常是 [目錄](directory-table.md) 資料表中的目錄名稱，或使用 [Appsearch](appsearch-action.md) 動作所取得之屬性集的名稱。</span><span class="sxs-lookup"><span data-stu-id="2329a-138">This property name is typically the name of a directory in the [Directory](directory-table.md) table or the name of a property set obtained using the [Appsearch](appsearch-action.md) action.</span></span> <span data-ttu-id="2329a-139">這會將 ReserveLocal 或 ReserveSource 中指定的磁碟空間量新增至包含目錄之裝置的磁片區成本。</span><span class="sxs-lookup"><span data-stu-id="2329a-139">This adds the amount of disk space specified in ReserveLocal or ReserveSource to the volume cost of the device containing the directory.</span></span>

</dd> <dt>

<span data-ttu-id="2329a-140"><span id="ReserveLocal"></span><span id="reservelocal"></span><span id="RESERVELOCAL"></span>ReserveLocal</span><span class="sxs-lookup"><span data-stu-id="2329a-140"><span id="ReserveLocal"></span><span id="reservelocal"></span><span id="RESERVELOCAL"></span>ReserveLocal</span></span>
</dt> <dd>

<span data-ttu-id="2329a-141">當連結的元件安裝在本機執行時，所要保留的磁碟空間位元組數目。</span><span class="sxs-lookup"><span data-stu-id="2329a-141">The number of bytes of disk space to reserve if the linked component is installed to run locally.</span></span>

</dd> <dt>

<span data-ttu-id="2329a-142"><span id="ReserveSource"></span><span id="reservesource"></span><span id="RESERVESOURCE"></span>ReserveSource</span><span class="sxs-lookup"><span data-stu-id="2329a-142"><span id="ReserveSource"></span><span id="reservesource"></span><span id="RESERVESOURCE"></span>ReserveSource</span></span>
</dt> <dd>

<span data-ttu-id="2329a-143">當連結的元件安裝成從來源執行時，所要保留的磁碟空間位元組數目。</span><span class="sxs-lookup"><span data-stu-id="2329a-143">The number of bytes of disk space to reserve if the linked component is installed to run from source.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2329a-144">備註</span><span class="sxs-lookup"><span data-stu-id="2329a-144">Remarks</span></span>

<span data-ttu-id="2329a-145">以這種方式保留成本可能適合想要確保在安裝完成之後可使用最少磁碟空間的作者。</span><span class="sxs-lookup"><span data-stu-id="2329a-145">Reserving cost in this way could be useful for authors who want to ensure that a minimum amount of disk space will be available after the installation is completed.</span></span> <span data-ttu-id="2329a-146">例如，此磁碟空間可能會保留給使用者檔或應用程式檔 (例如，只有在安裝之後啟動應用程式時才會建立的索引檔案) 。</span><span class="sxs-lookup"><span data-stu-id="2329a-146">For example, this disk space might be reserved for user documents or for application files (such as index files) that are created only after the application is started following installation.</span></span>

<span data-ttu-id="2329a-147">您可以使用 ReserveCost 資料表來啟用自訂動作，以指定自訂動作可能會安裝之任何檔案、登錄專案或其他專案的大約成本。</span><span class="sxs-lookup"><span data-stu-id="2329a-147">You can use the ReserveCost table to enable custom actions to specify an approximate cost for any files, registry entries, or other items that the custom action might install.</span></span> <span data-ttu-id="2329a-148">將專案加入至 ReserveCost 資料表的自訂動作應該在 [CostInitialize](costinitialize-action.md) 和 [FileCost](filecost-action.md) 動作之間排序。</span><span class="sxs-lookup"><span data-stu-id="2329a-148">Custom actions that add entries to the ReserveCost table should be sequenced between the [CostInitialize](costinitialize-action.md) and [FileCost](filecost-action.md) actions.</span></span> <span data-ttu-id="2329a-149">這是 FileCost 動作的必要專案，可正確地初始化受 ReserveCost 資料表中專案影響的所有元件的成本。</span><span class="sxs-lookup"><span data-stu-id="2329a-149">This is necessary for the FileCost action to correctly initialize the costing of all components affected by entries in the ReserveCost table.</span></span>

## <a name="validation"></a><span data-ttu-id="2329a-150">驗證</span><span class="sxs-lookup"><span data-stu-id="2329a-150">Validation</span></span>

<dl>

[<span data-ttu-id="2329a-151">ICE03</span><span class="sxs-lookup"><span data-stu-id="2329a-151">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="2329a-152">ICE06</span><span class="sxs-lookup"><span data-stu-id="2329a-152">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="2329a-153">ICE32</span><span class="sxs-lookup"><span data-stu-id="2329a-153">ICE32</span></span>](ice32.md)  
</dl>

 

 



