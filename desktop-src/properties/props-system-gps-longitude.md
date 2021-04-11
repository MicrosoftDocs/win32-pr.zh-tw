---
description: 表示經度。
ms.assetid: ef28141f-1b63-4694-b6df-fcc11ce7e50b
title: System.servicemodel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e65431412b0d46ad7b68100febd4d6e8efd31a17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115933"
---
# <a name="systemgpslongitude"></a><span data-ttu-id="e3a80-103">System.servicemodel</span><span class="sxs-lookup"><span data-stu-id="e3a80-103">System.GPS.Longitude</span></span>

<span data-ttu-id="e3a80-104">表示經度。</span><span class="sxs-lookup"><span data-stu-id="e3a80-104">Indicates the longitude.</span></span> <span data-ttu-id="e3a80-105">這是三個值的陣列，如下所示：索引0是度數，索引1是分鐘，索引2是秒。</span><span class="sxs-lookup"><span data-stu-id="e3a80-105">This is an array of three values, as follows: Index 0 is the degrees, index 1 is the minutes, index 2 is the seconds.</span></span> <span data-ttu-id="e3a80-106">每個都是從 PKEY \_ gps \_ LONGITUDENUMERATOR 和 PKEY \_ gps LongitudeDenominator 中的值計算而來 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e3a80-106">Each is calculated from the values in PKEY\_GPS\_LongitudeNumerator and PKEY\_GPS\_LongitudeDenominator.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="e3a80-107">Windows 10，1703版、Windows 10、1607版、Windows 10、1511版、Windows 10、version 1507、Windows 8.1、Windows 8</span><span class="sxs-lookup"><span data-stu-id="e3a80-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.GPS.Longitude
   shellPKey = PKEY_GPS_Longitude
   formatID = C4C4DBB2-B593-466B-BBDA-D03D27D5E43A
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Multivalue Double
      IsInnate = true
```

## <a name="windows-7-windows-vista"></a><span data-ttu-id="e3a80-108">Windows 7、Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3a80-108">Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.GPS.Longitude
   shellPKey = PKEY_GPS_Longitude
   formatID = C4C4DBB2-B593-466B-BBDA-D03D27D5E43A
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="e3a80-109">備註</span><span class="sxs-lookup"><span data-stu-id="e3a80-109">Remarks</span></span>

<span data-ttu-id="e3a80-110">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="e3a80-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="e3a80-111">`label`針對 Windows Vista Service Pack 1 (SP1) ，已新增 **labelInfo** 屬性之特定間接字串參考的需求。</span><span class="sxs-lookup"><span data-stu-id="e3a80-111">The requirement of a specific indirect string reference for the `label` attribute of **labelInfo** was added for Windows Vista with Service Pack 1 (SP1).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3a80-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="e3a80-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3a80-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="e3a80-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="e3a80-114">searchInfo</span><span class="sxs-lookup"><span data-stu-id="e3a80-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="e3a80-115">labelInfo</span><span class="sxs-lookup"><span data-stu-id="e3a80-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="e3a80-116">typeInfo</span><span class="sxs-lookup"><span data-stu-id="e3a80-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="e3a80-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="e3a80-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="e3a80-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="e3a80-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="e3a80-119">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="e3a80-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="e3a80-120">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="e3a80-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="e3a80-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="e3a80-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="e3a80-122">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="e3a80-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="e3a80-123">drawControl</span><span class="sxs-lookup"><span data-stu-id="e3a80-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="e3a80-124">editControl</span><span class="sxs-lookup"><span data-stu-id="e3a80-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="e3a80-125">filterControl</span><span class="sxs-lookup"><span data-stu-id="e3a80-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="e3a80-126">queryControl</span><span class="sxs-lookup"><span data-stu-id="e3a80-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
