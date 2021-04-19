---
description: 拍攝相片時的燈光來源（從交換影像檔案讀取） (EXIF) 資訊。
ms.assetid: 323bff11-2107-42df-87da-435e440c94bc
title: LightSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0f8c469c0f2c5e1588778b9f23219e3f9a3e1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979114"
---
# <a name="systemphotolightsource"></a><span data-ttu-id="d3565-103">LightSource</span><span class="sxs-lookup"><span data-stu-id="d3565-103">System.Photo.LightSource</span></span>

<span data-ttu-id="d3565-104">拍攝相片時的燈光來源（從交換影像檔案讀取） (EXIF) 資訊。</span><span class="sxs-lookup"><span data-stu-id="d3565-104">The light source when the photo was taken, as read from the Exchangeable Image File (EXIF) information.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="d3565-105">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="d3565-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.LightSource
   shellPKey = PKEY_Photo_LightSource
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37384
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Unknown
            value = 0
            text = Unknown
            defineToken = PHOTO_LIGHTSOURCE_UNKNOWN
         enum
            name = Daylight
            value = 1
            text = Daylight
            defineToken = PHOTO_LIGHTSOURCE_DAYLIGHT
         enum
            name = Fluorescent
            value = 2
            text = Fluorescent
            defineToken = PHOTO_LIGHTSOURCE_FLUORESCENT
         enum
            name = Tungsten
            value = 3
            text = Tungsten
            defineToken = PHOTO_LIGHTSOURCE_TUNGSTEN
         enum
            name = StandardA
            value = 17
            text = Standard Illuminant A
            defineToken = PHOTO_LIGHTSOURCE_STANDARD_A
         enum
            name = StandardB
            value = 18
            text = Standard Illuminant B
            defineToken = PHOTO_LIGHTSOURCE_STANDARD_B
         enum
            name = StandardC
            value = 19
            text = Standard Illuminant C
            defineToken = PHOTO_LIGHTSOURCE_STANDARD_C
         enum
            name = D55
            value = 20
            text = D55
            defineToken = PHOTO_LIGHTSOURCE_D55
         enum
            name = D65
            value = 21
            text = D65
            defineToken = PHOTO_LIGHTSOURCE_D65
         enum
            name = D75
            value = 22
            text = D75
            defineToken = PHOTO_LIGHTSOURCE_D75
```

## <a name="windows-vista"></a><span data-ttu-id="d3565-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3565-106">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.LightSource
   shellPKey = PKEY_Photo_LightSource
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37384
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Unknown
            defineName = PHOTO_LIGHTSOURCE_UNKNOWN
         enum
            value = 1
            text = Daylight
            defineName = PHOTO_LIGHTSOURCE_DAYLIGHT
         enum
            value = 2
            text = Fluorescent
            defineName = PHOTO_LIGHTSOURCE_FLUORESCENT
         enum
            value = 3
            text = Tungsten
            defineName = PHOTO_LIGHTSOURCE_TUNGSTEN
         enum
            value = 17
            text = Standard Illuminant A
            defineName = PHOTO_LIGHTSOURCE_STANDARD_A
         enum
            value = 18
            text = Standard Illuminant B
            defineName = PHOTO_LIGHTSOURCE_STANDARD_B
         enum
            value = 19
            text = Standard Illuminant C
            defineName = PHOTO_LIGHTSOURCE_STANDARD_C
         enum
            value = 20
            text = D55
            defineName = PHOTO_LIGHTSOURCE_D55
         enum
            value = 21
            text = D65
            defineName = PHOTO_LIGHTSOURCE_D65
         enum
            value = 22
            text = D75
            defineName = PHOTO_LIGHTSOURCE_D75
```

## <a name="remarks"></a><span data-ttu-id="d3565-107">備註</span><span class="sxs-lookup"><span data-stu-id="d3565-107">Remarks</span></span>

<span data-ttu-id="d3565-108">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="d3565-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3565-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="d3565-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3565-110">數位相機的交換影像檔案格式： Exif 2.2 版</span><span class="sxs-lookup"><span data-stu-id="d3565-110">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="d3565-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="d3565-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="d3565-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="d3565-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="d3565-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="d3565-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="d3565-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="d3565-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="d3565-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="d3565-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="d3565-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="d3565-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="d3565-117">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="d3565-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="d3565-118">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="d3565-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="d3565-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="d3565-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="d3565-120">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="d3565-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="d3565-121">drawControl</span><span class="sxs-lookup"><span data-stu-id="d3565-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="d3565-122">editControl</span><span class="sxs-lookup"><span data-stu-id="d3565-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="d3565-123">filterControl</span><span class="sxs-lookup"><span data-stu-id="d3565-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="d3565-124">queryControl</span><span class="sxs-lookup"><span data-stu-id="d3565-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
