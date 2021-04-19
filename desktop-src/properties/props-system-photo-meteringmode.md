---
description: 相機使用的計量模式，取自交換影像檔案 (EXIF) 資訊。
ms.assetid: 9dd031a8-f1fa-4753-a86b-18051c624a00
title: MeteringMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e90fff67abe04486504ecda67684f85cb5ac1a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974421"
---
# <a name="systemphotometeringmode"></a><span data-ttu-id="c22df-103">MeteringMode</span><span class="sxs-lookup"><span data-stu-id="c22df-103">System.Photo.MeteringMode</span></span>

<span data-ttu-id="c22df-104">相機使用的計量模式，取自交換影像檔案 (EXIF) 資訊。</span><span class="sxs-lookup"><span data-stu-id="c22df-104">The metering mode used by the camera, taken from the Exchangeable Image File (EXIF) information.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="c22df-105">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="c22df-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.MeteringMode
   shellPKey = PKEY_Photo_MeteringMode
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37383
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Unknown
            value = 0
            text = Unknown
            defineToken = PHOTO_METERINGMODE_UNKNOWN
         enum
            name = Average
            value = 1
            text = Average
            defineToken = PHOTO_METERINGMODE_AVERAGE
         enum
            name = Center
            value = 2
            text = Center Weighted Average
            defineToken = PHOTO_METERINGMODE_CENTER
         enum
            name = Spot
            value = 3
            text = Spot
            defineToken = PHOTO_METERINGMODE_SPOT
         enum
            name = MultiSpot
            value = 4
            text = Multi Spot
            defineToken = PHOTO_METERINGMODE_MULTISPOT
         enum
            name = Pattern
            value = 5
            text = Pattern
            defineToken = PHOTO_METERINGMODE_PATTERN
         enum
            name = Partial
            value = 6
            text = Partial
            defineToken = PHOTO_METERINGMODE_PARTIAL
```

## <a name="windows-vista"></a><span data-ttu-id="c22df-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c22df-106">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.MeteringMode
   shellPKey = PKEY_Photo_MeteringMode
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37383
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Unknown
            defineName = PHOTO_METERINGMODE_UNKNOWN
         enum
            value = 1
            text = Average
            defineName = PHOTO_METERINGMODE_AVERAGE
         enum
            value = 2
            text = Center Weighted Average
            defineName = PHOTO_METERINGMODE_CENTER
         enum
            value = 3
            text = Spot
            defineName = PHOTO_METERINGMODE_SPOT
         enum
            value = 4
            text = Multi Spot
            defineName = PHOTO_METERINGMODE_MULTISPOT
         enum
            value = 5
            text = Pattern
            defineName = PHOTO_METERINGMODE_PATTERN
         enum
            value = 6
            text = Partial
            defineName = PHOTO_METERINGMODE_PARTIAL
```

## <a name="remarks"></a><span data-ttu-id="c22df-107">備註</span><span class="sxs-lookup"><span data-stu-id="c22df-107">Remarks</span></span>

<span data-ttu-id="c22df-108">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="c22df-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c22df-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="c22df-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c22df-110">數位相機的交換影像檔案格式： Exif 2.2 版</span><span class="sxs-lookup"><span data-stu-id="c22df-110">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="c22df-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="c22df-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="c22df-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="c22df-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="c22df-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="c22df-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="c22df-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="c22df-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="c22df-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="c22df-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="c22df-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="c22df-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="c22df-117">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="c22df-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="c22df-118">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="c22df-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="c22df-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="c22df-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="c22df-120">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="c22df-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="c22df-121">drawControl</span><span class="sxs-lookup"><span data-stu-id="c22df-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="c22df-122">editControl</span><span class="sxs-lookup"><span data-stu-id="c22df-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="c22df-123">filterControl</span><span class="sxs-lookup"><span data-stu-id="c22df-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="c22df-124">queryControl</span><span class="sxs-lookup"><span data-stu-id="c22df-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
