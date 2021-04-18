---
description: 表示目的地點的緯度。
ms.assetid: 72a3fb10-4554-4a4d-bb73-ee515341b9c1
title: DestLongitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e11cb93fece8b5d2d95c649bdaf87c01390a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983468"
---
# <a name="systemgpsdestlongitude"></a><span data-ttu-id="17379-103">DestLongitude</span><span class="sxs-lookup"><span data-stu-id="17379-103">System.GPS.DestLongitude</span></span>

<span data-ttu-id="17379-104">表示目的地點的緯度。</span><span class="sxs-lookup"><span data-stu-id="17379-104">Indicates the latitude of the destination point.</span></span> <span data-ttu-id="17379-105">這是三個值的陣列，如下所示：索引0是度數，索引1是分鐘，索引2是秒。</span><span class="sxs-lookup"><span data-stu-id="17379-105">This is an array of three values, as follows: index 0 is the degrees, index 1 is the minutes, index 2 is the seconds.</span></span> <span data-ttu-id="17379-106">每個都是從 PKEY \_ gps \_ DESTLONGITUDENUMERATOR 和 PKEY \_ gps DestLongitudeDenominator 中的值計算而來 \_ 。</span><span class="sxs-lookup"><span data-stu-id="17379-106">Each is calculated from the values in PKEY\_GPS\_DestLongitudeNumerator and PKEY\_GPS\_DestLongitudeDenominator.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="17379-107">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本</span><span class="sxs-lookup"><span data-stu-id="17379-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.GPS.DestLongitude
   shellPKey = PKEY_GPS_DestLongitude
   formatID = 47A96261-CB4C-4807-8AD3-40B9D9DBC6BC
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="17379-108">備註</span><span class="sxs-lookup"><span data-stu-id="17379-108">Remarks</span></span>

<span data-ttu-id="17379-109">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="17379-109">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17379-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="17379-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17379-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="17379-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="17379-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="17379-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="17379-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="17379-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="17379-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="17379-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="17379-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="17379-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="17379-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="17379-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="17379-117">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="17379-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="17379-118">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="17379-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="17379-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="17379-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="17379-120">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="17379-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="17379-121">drawControl</span><span class="sxs-lookup"><span data-stu-id="17379-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="17379-122">editControl</span><span class="sxs-lookup"><span data-stu-id="17379-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="17379-123">filterControl</span><span class="sxs-lookup"><span data-stu-id="17379-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="17379-124">queryControl</span><span class="sxs-lookup"><span data-stu-id="17379-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
