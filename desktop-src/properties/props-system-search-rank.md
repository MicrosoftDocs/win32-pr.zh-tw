---
description: 資料列的關聯次序，範圍從0-1000。
ms.assetid: e0c03f6f-4539-4a6b-b58d-161bd985ee0f
title: System. Rank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d23d1c78e5c3807c529fd68b04cc71b6f03300c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998121"
---
# <a name="systemsearchrank"></a><span data-ttu-id="bf21f-103">System. Rank</span><span class="sxs-lookup"><span data-stu-id="bf21f-103">System.Search.Rank</span></span>

<span data-ttu-id="bf21f-104">資料列的關聯次序，範圍從0-1000。</span><span class="sxs-lookup"><span data-stu-id="bf21f-104">Relevance rank of row, with a range from 0-1000.</span></span> <span data-ttu-id="bf21f-105">較大的數位表示較佳的相符專案。</span><span class="sxs-lookup"><span data-stu-id="bf21f-105">Larger numbers mean better matches.</span></span> <span data-ttu-id="bf21f-106">僅限查詢時間;未定義于搜尋架構中。</span><span class="sxs-lookup"><span data-stu-id="bf21f-106">Query-time only; not defined in Search schema.</span></span> <span data-ttu-id="bf21f-107">這個屬性是可抓取但無法搜尋的。</span><span class="sxs-lookup"><span data-stu-id="bf21f-107">This property is retrievable but not searchable.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="bf21f-108">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本</span><span class="sxs-lookup"><span data-stu-id="bf21f-108">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.Rank
   shellPKey = PKEY_Search_Rank
   formatID = 49691C90-7E17-101A-A91C-08002B2ECDA9
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Int32
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="bf21f-109">備註</span><span class="sxs-lookup"><span data-stu-id="bf21f-109">Remarks</span></span>

<span data-ttu-id="bf21f-110">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="bf21f-110">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf21f-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="bf21f-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf21f-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="bf21f-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="bf21f-113">searchInfo</span><span class="sxs-lookup"><span data-stu-id="bf21f-113">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="bf21f-114">labelInfo</span><span class="sxs-lookup"><span data-stu-id="bf21f-114">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="bf21f-115">typeInfo</span><span class="sxs-lookup"><span data-stu-id="bf21f-115">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="bf21f-116">displayInfo</span><span class="sxs-lookup"><span data-stu-id="bf21f-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="bf21f-117">stringFormat</span><span class="sxs-lookup"><span data-stu-id="bf21f-117">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="bf21f-118">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="bf21f-118">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="bf21f-119">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="bf21f-119">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="bf21f-120">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="bf21f-120">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="bf21f-121">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="bf21f-121">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="bf21f-122">drawControl</span><span class="sxs-lookup"><span data-stu-id="bf21f-122">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="bf21f-123">editControl</span><span class="sxs-lookup"><span data-stu-id="bf21f-123">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="bf21f-124">filterControl</span><span class="sxs-lookup"><span data-stu-id="bf21f-124">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="bf21f-125">queryControl</span><span class="sxs-lookup"><span data-stu-id="bf21f-125">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
