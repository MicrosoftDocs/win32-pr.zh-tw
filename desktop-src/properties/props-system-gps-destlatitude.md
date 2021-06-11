---
description: 瞭解 DestLatitude 屬性如何表示目的地點的緯度。
ms.assetid: 63d8a3a3-76ec-4121-b48b-eb5034117d04
title: DestLatitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbed51e89926b8bb505457bd9fd7bf7bd3b69ff2
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988963"
---
# <a name="systemgpsdestlatitude"></a><span data-ttu-id="b73d8-103">DestLatitude</span><span class="sxs-lookup"><span data-stu-id="b73d8-103">System.GPS.DestLatitude</span></span>

<span data-ttu-id="b73d8-104">表示目的地點的緯度。</span><span class="sxs-lookup"><span data-stu-id="b73d8-104">Indicates the latitude of the destination point.</span></span> <span data-ttu-id="b73d8-105">這是三個值的陣列，如下所示：索引0是度數，索引1是分鐘，索引2是秒。</span><span class="sxs-lookup"><span data-stu-id="b73d8-105">This is an array of three values, as follows: index 0 is the degrees, index 1 is the minutes, index 2 is the seconds.</span></span> <span data-ttu-id="b73d8-106">每個都是從 PKEY \_ gps \_ DESTLATITUDENUMERATOR 和 PKEY \_ gps DestLatitudeDenominator 中的值計算而來 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b73d8-106">Each is calculated from the values in PKEY\_GPS\_DestLatitudeNumerator and PKEY\_GPS\_DestLatitudeDenominator.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="b73d8-107">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本</span><span class="sxs-lookup"><span data-stu-id="b73d8-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.GPS.DestLatitude
   shellPKey = PKEY_GPS_DestLatitude
   formatID = 9D1D7CC5-5C39-451C-86B3-928E2D18CC47
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="b73d8-108">備註</span><span class="sxs-lookup"><span data-stu-id="b73d8-108">Remarks</span></span>

<span data-ttu-id="b73d8-109">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="b73d8-109">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b73d8-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="b73d8-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b73d8-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="b73d8-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="b73d8-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="b73d8-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="b73d8-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="b73d8-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="b73d8-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="b73d8-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="b73d8-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="b73d8-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="b73d8-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="b73d8-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="b73d8-117">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="b73d8-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="b73d8-118">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="b73d8-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="b73d8-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="b73d8-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="b73d8-120">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="b73d8-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="b73d8-121">drawControl</span><span class="sxs-lookup"><span data-stu-id="b73d8-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="b73d8-122">editControl</span><span class="sxs-lookup"><span data-stu-id="b73d8-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="b73d8-123">filterControl</span><span class="sxs-lookup"><span data-stu-id="b73d8-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="b73d8-124">queryControl</span><span class="sxs-lookup"><span data-stu-id="b73d8-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
