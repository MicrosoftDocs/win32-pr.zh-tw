---
description: Windows Search 索引中給定目錄內之專案的專案識別碼。
ms.assetid: 9162e92b-b738-4462-b346-68410f088e95
title: System.servicemodel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd647338102d17e215973c85ea0e5d84c9bbdf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979314"
---
# <a name="systemsearchentryid"></a><span data-ttu-id="3976c-103">System.servicemodel</span><span class="sxs-lookup"><span data-stu-id="3976c-103">System.Search.EntryID</span></span>

<span data-ttu-id="3976c-104">Windows Search 索引中給定目錄內之專案的專案識別碼。</span><span class="sxs-lookup"><span data-stu-id="3976c-104">The entry ID for an item within a given catalog in the Windows Search Index.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="3976c-105">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本</span><span class="sxs-lookup"><span data-stu-id="3976c-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.EntryID
   shellPKey = PKEY_Search_EntryID
   formatID = 49691C90-7E17-101A-A91C-08002B2ECDA9
   propID = 5
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Int32
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="3976c-106">備註</span><span class="sxs-lookup"><span data-stu-id="3976c-106">Remarks</span></span>

<span data-ttu-id="3976c-107">系統會在產生用來查詢索引的 SQL 中使用[EntryID。]()</span><span class="sxs-lookup"><span data-stu-id="3976c-107">[System.Search.EntryID]() is used in the SQL that is generated to query the index.</span></span> <span data-ttu-id="3976c-108">此值不會在一段時間內被視為唯一的，因為它可能會被回收。</span><span class="sxs-lookup"><span data-stu-id="3976c-108">This value is not considered unique over time because it may be recycled.</span></span>

<span data-ttu-id="3976c-109">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="3976c-109">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3976c-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="3976c-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3976c-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="3976c-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="3976c-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="3976c-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="3976c-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="3976c-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="3976c-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="3976c-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="3976c-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="3976c-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="3976c-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="3976c-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="3976c-117">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="3976c-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="3976c-118">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="3976c-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="3976c-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="3976c-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="3976c-120">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="3976c-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="3976c-121">drawControl</span><span class="sxs-lookup"><span data-stu-id="3976c-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="3976c-122">editControl</span><span class="sxs-lookup"><span data-stu-id="3976c-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="3976c-123">filterControl</span><span class="sxs-lookup"><span data-stu-id="3976c-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="3976c-124">queryControl</span><span class="sxs-lookup"><span data-stu-id="3976c-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
