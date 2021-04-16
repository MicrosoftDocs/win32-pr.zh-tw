---
description: 由容器的所有子專案發出為 TRUE (例如電子郵件或副檔名為 .zip 的壓縮檔案) ，會發出 IsClosedDirectory 為 TRUE。 這可確保子專案包含在搜尋索引中。
ms.assetid: 6da60e89-6956-41f6-8624-063c4d46464d
title: IsFullyContained
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1245f29a2940146a4e5d8f0a392210173be75e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514028"
---
# <a name="systemsearchisfullycontained"></a><span data-ttu-id="78751-104">IsFullyContained</span><span class="sxs-lookup"><span data-stu-id="78751-104">System.Search.IsFullyContained</span></span>

<span data-ttu-id="78751-105">由容器的所有子專案發出為 **true** (例如電子郵件或副檔名為 .zip 的壓縮檔案) ，會發出 [IsClosedDirectory](./props-system-search-iscloseddirectory.md) 為 **true**。</span><span class="sxs-lookup"><span data-stu-id="78751-105">Emitted as **TRUE** by all child items of a container (such as an e-mail or a compressed file with a .zip name extension) that emits [System.Search.IsClosedDirectory](./props-system-search-iscloseddirectory.md) as **TRUE**.</span></span> <span data-ttu-id="78751-106">這可確保子專案包含在搜尋索引中。</span><span class="sxs-lookup"><span data-stu-id="78751-106">This ensures that the child items are included in the search index.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="78751-107">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本</span><span class="sxs-lookup"><span data-stu-id="78751-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.IsFullyContained
   shellPKey = PKEY_Search_IsFullyContained
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 24
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a><span data-ttu-id="78751-108">備註</span><span class="sxs-lookup"><span data-stu-id="78751-108">Remarks</span></span>

<span data-ttu-id="78751-109">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="78751-109">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="78751-110">[IsClosedDirectory](./props-system-search-iscloseddirectory.md)屬性可讓索引子略過容器子專案的列舉，以協助優化索引子的效能。</span><span class="sxs-lookup"><span data-stu-id="78751-110">The [System.Search.IsClosedDirectory](./props-system-search-iscloseddirectory.md) property helps to optimize indexer performance by allowing the indexer to skip the enumeration of a container's child items.</span></span> <span data-ttu-id="78751-111">不過，索引子會將這些子專案標示為未造訪，因此會從索引中刪除。</span><span class="sxs-lookup"><span data-stu-id="78751-111">However, those child items are marked by the indexer as not visited, and as such will be deleted from the index.</span></span> <span data-ttu-id="78751-112">藉由發出 [IsFullyContained]() 為 **TRUE**，就不會從索引中刪除專案（儘管尚未造訪）。</span><span class="sxs-lookup"><span data-stu-id="78751-112">By emitting [System.Search.IsFullyContained]() as **TRUE**, an item is not deleted from the index despite having not been visited.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78751-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="78751-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78751-114">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="78751-114">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="78751-115">searchInfo</span><span class="sxs-lookup"><span data-stu-id="78751-115">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="78751-116">labelInfo</span><span class="sxs-lookup"><span data-stu-id="78751-116">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="78751-117">typeInfo</span><span class="sxs-lookup"><span data-stu-id="78751-117">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="78751-118">displayInfo</span><span class="sxs-lookup"><span data-stu-id="78751-118">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="78751-119">stringFormat</span><span class="sxs-lookup"><span data-stu-id="78751-119">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="78751-120">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="78751-120">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="78751-121">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="78751-121">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="78751-122">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="78751-122">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="78751-123">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="78751-123">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="78751-124">drawControl</span><span class="sxs-lookup"><span data-stu-id="78751-124">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="78751-125">editControl</span><span class="sxs-lookup"><span data-stu-id="78751-125">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="78751-126">filterControl</span><span class="sxs-lookup"><span data-stu-id="78751-126">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="78751-127">queryControl</span><span class="sxs-lookup"><span data-stu-id="78751-127">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
