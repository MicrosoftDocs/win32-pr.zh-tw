---
description: 指出拍攝相片時，相機所套用的飽和度處理方向。
ms.assetid: 209edf55-fd6c-416b-b175-346f5158fc2a
title: 照相
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50655b1d9344bb3c25576de9ece3ac6ef2bba95c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999885"
---
# <a name="systemphotosaturation"></a><span data-ttu-id="2cae8-103">照相</span><span class="sxs-lookup"><span data-stu-id="2cae8-103">System.Photo.Saturation</span></span>

<span data-ttu-id="2cae8-104">指出拍攝相片時，相機所套用的飽和度處理方向。</span><span class="sxs-lookup"><span data-stu-id="2cae8-104">Indicates the direction of saturation processing applied by the camera when the photo was taken.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="2cae8-105">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="2cae8-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.Saturation
   shellPKey = PKEY_Photo_Saturation
   formatID = 49237325-A95A-4F67-B211-816B2D45D2E0
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Normal
            value = 0
            text = Normal
            defineToken = PHOTO_SATURATION_NORMAL
         enum
            name = Low
            value = 1
            text = Low saturation
            defineToken = PHOTO_SATURATION_LOW
         enum
            name = High
            value = 2
            text = High saturation
            defineToken = PHOTO_SATURATION_HIGH
```

## <a name="windows-vista"></a><span data-ttu-id="2cae8-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2cae8-106">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.Saturation
   shellPKey = PKEY_Photo_Saturation
   formatID = 49237325-A95A-4F67-B211-816B2D45D2E0
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Normal
            defineName = PHOTO_SATURATION_NORMAL
         enum
            value = 1
            text = Low saturation
            defineName = PHOTO_SATURATION_LOW
         enum
            value = 2
            text = High saturation
            defineName = PHOTO_SATURATION_HIGH
```

## <a name="remarks"></a><span data-ttu-id="2cae8-107">備註</span><span class="sxs-lookup"><span data-stu-id="2cae8-107">Remarks</span></span>

<span data-ttu-id="2cae8-108">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="2cae8-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2cae8-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="2cae8-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cae8-110">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="2cae8-110">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="2cae8-111">searchInfo</span><span class="sxs-lookup"><span data-stu-id="2cae8-111">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="2cae8-112">labelInfo</span><span class="sxs-lookup"><span data-stu-id="2cae8-112">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="2cae8-113">typeInfo</span><span class="sxs-lookup"><span data-stu-id="2cae8-113">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="2cae8-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="2cae8-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="2cae8-115">stringFormat</span><span class="sxs-lookup"><span data-stu-id="2cae8-115">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="2cae8-116">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="2cae8-116">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="2cae8-117">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="2cae8-117">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="2cae8-118">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="2cae8-118">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="2cae8-119">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="2cae8-119">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="2cae8-120">drawControl</span><span class="sxs-lookup"><span data-stu-id="2cae8-120">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="2cae8-121">editControl</span><span class="sxs-lookup"><span data-stu-id="2cae8-121">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="2cae8-122">filterControl</span><span class="sxs-lookup"><span data-stu-id="2cae8-122">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="2cae8-123">queryControl</span><span class="sxs-lookup"><span data-stu-id="2cae8-123">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
