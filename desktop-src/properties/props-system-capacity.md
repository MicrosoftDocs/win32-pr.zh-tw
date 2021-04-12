---
description: 總儲存空間量（以位元組為單位）。
ms.assetid: 14cd6b5d-0534-4527-8439-e7ba8cdef8da
title: 系統容量
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d62e117b11f0f689a5fbbbd301714aef87e217bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192131"
---
# <a name="systemcapacity"></a><span data-ttu-id="99593-103">系統容量</span><span class="sxs-lookup"><span data-stu-id="99593-103">System.Capacity</span></span>

<span data-ttu-id="99593-104">總儲存空間量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="99593-104">The amount of total storage space, expressed in bytes.</span></span> <span data-ttu-id="99593-105">這個屬性主要是用來指出儲存媒體（例如硬碟）的容量。</span><span class="sxs-lookup"><span data-stu-id="99593-105">This property is mainly used to indicate the capacity of storage media such as hard drives.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="99593-106">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="99593-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Capacity
   shellPKey = PKEY_Capacity
   formatID = 9B174B35-40FF-11D2-A27E-00C04FC30871
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt64
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = Empty
            minValue = 0
            setValue = 0
            text = 0 GB
            defineToken = CAPACITY_EMPTY
            mnemonics = empty
         enumRange
            name = Tiny
            minValue = 1
            setValue = 1
            text = 0 - 16 GB
            defineToken = CAPACITY_TINY
            mnemonics = tiny
         enumRange
            name = Small
            minValue = 17179869185
            setValue = 17179869185
            text = 16 - 80 GB
            defineToken = CAPACITY_SMALL
            mnemonics = small
         enumRange
            name = Medium
            minValue = 85899345921
            setValue = 85899345921
            text = 80 - 250 GB
            defineToken = CAPACITY_MEDIUM
            mnemonics = medium
         enumRange
            name = Large
            minValue = 274877906945
            setValue = 274877906945
            text = 250 - 500 GB
            defineToken = CAPACITY_LARGE
            mnemonics = large
         enumRange
            name = Huge
            minValue = 549755813889
            setValue = 549755813889
            text = 500 - 1 TB
            defineToken = CAPACITY_HUGE
            mnemonics = huge
         enumRange
            name = Gigantic
            minValue = 1099511627777
            setValue = 1099511627777
            text = >1 TB
            defineToken = CAPACITY_GIGANTIC
            mnemonics = gigantic
```

## <a name="windows-vista"></a><span data-ttu-id="99593-107">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="99593-107">Windows Vista</span></span>

```
propertyDescription
   name = System.Capacity
   shellPKey = PKEY_Capacity
   formatID = 9B174B35-40FF-11D2-A27E-00C04FC30871
   propID = 3
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
            text = 0 GB
            mnemonics = empty
         enumRange
            minValue = 1
            setValue = 1
            text = 0 - 2 GB
            mnemonics = tiny
         enumRange
            minValue = 2147483649
            setValue = 2147483649
            text = 2 - 10 GB
            mnemonics = small
         enumRange
            minValue = 10737418241
            setValue = 10737418241
            text = 10 - 40 GB
            mnemonics = medium
         enumRange
            minValue = 42949672961
            setValue = 42949672961
            text = 40 - 80 GB
            mnemonics = large
         enumRange
            minValue = 85899345921
            setValue = 85899345921
            text = 80 - 120 GB
            mnemonics = huge
         enumRange
            minValue = 137438953473
            setValue = 137438953473
            text = >120 GB
            mnemonics = gigantic
```

## <a name="remarks"></a><span data-ttu-id="99593-108">備註</span><span class="sxs-lookup"><span data-stu-id="99593-108">Remarks</span></span>

<span data-ttu-id="99593-109">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="99593-109">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="99593-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="99593-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99593-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="99593-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="99593-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="99593-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="99593-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="99593-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="99593-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="99593-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="99593-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="99593-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="99593-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="99593-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="99593-117">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="99593-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="99593-118">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="99593-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="99593-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="99593-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="99593-120">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="99593-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="99593-121">drawControl</span><span class="sxs-lookup"><span data-stu-id="99593-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="99593-122">editControl</span><span class="sxs-lookup"><span data-stu-id="99593-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="99593-123">filterControl</span><span class="sxs-lookup"><span data-stu-id="99593-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="99593-124">queryControl</span><span class="sxs-lookup"><span data-stu-id="99593-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
