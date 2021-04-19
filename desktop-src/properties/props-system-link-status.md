---
description: 指定是否驗證 TargetParsingPath 中的連結路徑。
ms.assetid: 38c73501-6376-41bb-8ad0-8f94ad42dfc9
title: 系統連結。狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9b4a6b398ba022f9f62a0860262028ced49a55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975061"
---
# <a name="systemlinkstatus"></a><span data-ttu-id="8ce82-103">系統連結。狀態</span><span class="sxs-lookup"><span data-stu-id="8ce82-103">System.Link.Status</span></span>

<span data-ttu-id="8ce82-104">指定是否驗證 [TargetParsingPath](./props-system-link-targetparsingpath.md) 中的連結路徑。</span><span class="sxs-lookup"><span data-stu-id="8ce82-104">Specifies whether the link path in [System.Link.TargetParsingPath](./props-system-link-targetparsingpath.md) is verified.</span></span> <span data-ttu-id="8ce82-105">定義這些值。</span><span class="sxs-lookup"><span data-stu-id="8ce82-105">These values are defined.</span></span>

-   <span data-ttu-id="8ce82-106">**未解析** 的 (預設) </span><span class="sxs-lookup"><span data-stu-id="8ce82-106">**Unresolved** (default)</span></span>
-   <span data-ttu-id="8ce82-107">已解決</span><span class="sxs-lookup"><span data-stu-id="8ce82-107">Resolved</span></span>
-   <span data-ttu-id="8ce82-108">破碎</span><span class="sxs-lookup"><span data-stu-id="8ce82-108">Broken</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="8ce82-109">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="8ce82-109">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Link.Status
   shellPKey = PKEY_Link_Status
   formatID = B9B4B3FC-2B51-4A42-B5D8-324146AFCF25
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Int32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Resolved
            value = 1
            text = Resolved
            defineToken = LINK_STATUS_RESOLVED
         enum
            name = Broken
            value = 2
            text = Broken
            defineToken = LINK_STATUS_BROKEN
```

## <a name="windows-vista"></a><span data-ttu-id="8ce82-110">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8ce82-110">Windows Vista</span></span>

```
propertyDescription
   name = System.Link.Status
   shellPKey = PKEY_Link_Status
   formatID = B9B4B3FC-2B51-4A42-B5D8-324146AFCF25
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Int32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 1
            text = Resolved
            defineName = LINK_STATUS_RESOLVED
         enum
            value = 2
            text = Broken
            defineName = LINK_STATUS_BROKEN
```

## <a name="remarks"></a><span data-ttu-id="8ce82-111">備註</span><span class="sxs-lookup"><span data-stu-id="8ce82-111">Remarks</span></span>

<span data-ttu-id="8ce82-112">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="8ce82-112">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ce82-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="8ce82-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ce82-114">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="8ce82-114">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="8ce82-115">searchInfo</span><span class="sxs-lookup"><span data-stu-id="8ce82-115">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="8ce82-116">labelInfo</span><span class="sxs-lookup"><span data-stu-id="8ce82-116">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="8ce82-117">typeInfo</span><span class="sxs-lookup"><span data-stu-id="8ce82-117">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="8ce82-118">displayInfo</span><span class="sxs-lookup"><span data-stu-id="8ce82-118">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="8ce82-119">stringFormat</span><span class="sxs-lookup"><span data-stu-id="8ce82-119">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="8ce82-120">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="8ce82-120">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="8ce82-121">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="8ce82-121">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="8ce82-122">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="8ce82-122">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="8ce82-123">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="8ce82-123">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="8ce82-124">drawControl</span><span class="sxs-lookup"><span data-stu-id="8ce82-124">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="8ce82-125">editControl</span><span class="sxs-lookup"><span data-stu-id="8ce82-125">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="8ce82-126">filterControl</span><span class="sxs-lookup"><span data-stu-id="8ce82-126">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="8ce82-127">queryControl</span><span class="sxs-lookup"><span data-stu-id="8ce82-127">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
