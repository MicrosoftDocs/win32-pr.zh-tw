---
description: 磁片區中的可用空間量（以位元組為單位）。
ms.assetid: 84c85468-d3c2-49bf-b52b-bbd3d9ecb914
title: System.servicemodel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a605cc75dc2b7b36f6d9baf3c293c8bac8323dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849070"
---
# <a name="systemfreespace"></a><span data-ttu-id="4cbc6-103">System.servicemodel</span><span class="sxs-lookup"><span data-stu-id="4cbc6-103">System.FreeSpace</span></span>

<span data-ttu-id="4cbc6-104">磁片區中的可用空間量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="4cbc6-104">The amount of free space in a volume, in bytes.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="4cbc6-105">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="4cbc6-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.FreeSpace
   shellPKey = PKEY_FreeSpace
   formatID = 9B174B35-40FF-11D2-A27E-00C04FC30871
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt64
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = Full
            minValue = 0
            setValue = 0
            text = Full
            defineToken = FREESPACE_FULL
            mnemonics = full
         enumRange
            name = Tiny
            minValue = 1
            setValue = 1
            text = Tiny (0 - 2 GB)
            defineToken = FREESPACE_TINY
            mnemonics = tiny
         enumRange
            name = Small
            minValue = 2147483649
            setValue = 2147483649
            text = Small (2 - 10 GB)
            defineToken = FREESPACE_SMALL
            mnemonics = small
         enumRange
            name = Medium
            minValue = 10737418241
            setValue = 10737418241
            text = Medium (10 - 40 GB)
            defineToken = FREESPACE_MEDIUM
            mnemonics = medium
         enumRange
            name = Large
            minValue = 42949672961
            setValue = 42949672961
            text = Large (40 - 80 GB)
            defineToken = FREESPACE_LARGE
            mnemonics = large
         enumRange
            name = Huge
            minValue = 85899345921
            setValue = 85899345921
            text = Huge (80 - 120 GB)
            defineToken = FREESPACE_HUGE
            mnemonics = huge
         enumRange
            name = Gigantic
            minValue = 137438953473
            setValue = 137438953473
            text = Gigantic (over 120 GB)
            defineToken = FREESPACE_GIGANTIC
            mnemonics = gigantic
```

## <a name="windows-vista"></a><span data-ttu-id="4cbc6-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4cbc6-106">Windows Vista</span></span>

```
propertyDescription
   name = System.FreeSpace
   shellPKey = PKEY_FreeSpace
   formatID = 9B174B35-40FF-11D2-A27E-00C04FC30871
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt64
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            setValue = 0
            text = Zero
            mnemonics = empty
         enumRange
            minValue = 1
            setValue = 1
            text = Tiny (0 - 2 GB)
            mnemonics = tiny
         enumRange
            minValue = 2147483649
            setValue = 2147483649
            text = Small (2 - 10 GB)
            mnemonics = small
         enumRange
            minValue = 10737418241
            setValue = 10737418241
            text = Medium (10 - 40 GB)
            mnemonics = medium
         enumRange
            minValue = 42949672961
            setValue = 42949672961
            text = Large (40 - 80 GB)
            mnemonics = large
         enumRange
            minValue = 85899345921
            setValue = 85899345921
            text = Huge (80 - 120 GB)
            mnemonics = huge
         enumRange
            minValue = 137438953473
            setValue = 137438953473
            text = Gigantic (over 120 GB)
            mnemonics = gigantic
```

## <a name="remarks"></a><span data-ttu-id="4cbc6-107">備註</span><span class="sxs-lookup"><span data-stu-id="4cbc6-107">Remarks</span></span>

<span data-ttu-id="4cbc6-108">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="4cbc6-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4cbc6-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="4cbc6-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cbc6-110">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="4cbc6-110">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="4cbc6-111">searchInfo</span><span class="sxs-lookup"><span data-stu-id="4cbc6-111">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="4cbc6-112">labelInfo</span><span class="sxs-lookup"><span data-stu-id="4cbc6-112">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="4cbc6-113">typeInfo</span><span class="sxs-lookup"><span data-stu-id="4cbc6-113">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="4cbc6-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="4cbc6-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="4cbc6-115">stringFormat</span><span class="sxs-lookup"><span data-stu-id="4cbc6-115">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="4cbc6-116">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="4cbc6-116">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="4cbc6-117">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="4cbc6-117">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="4cbc6-118">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="4cbc6-118">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="4cbc6-119">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="4cbc6-119">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="4cbc6-120">drawControl</span><span class="sxs-lookup"><span data-stu-id="4cbc6-120">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="4cbc6-121">editControl</span><span class="sxs-lookup"><span data-stu-id="4cbc6-121">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="4cbc6-122">filterControl</span><span class="sxs-lookup"><span data-stu-id="4cbc6-122">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="4cbc6-123">queryControl</span><span class="sxs-lookup"><span data-stu-id="4cbc6-123">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
