---
description: 指出整體影像增益調整的程度。 從 PKEY \_ photo \_ GAINCONTROLNUMERATOR 和 PKEY \_ photo GainControlDenominator 計算 \_ 。
ms.assetid: 5076e03b-2c8a-4ef4-93d6-271a4bd697a6
title: GainControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8278120e5e65137eda491f52af7bc36f1c163c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944066"
---
# <a name="systemphotogaincontrol"></a><span data-ttu-id="3a93d-104">GainControl</span><span class="sxs-lookup"><span data-stu-id="3a93d-104">System.Photo.GainControl</span></span>

<span data-ttu-id="3a93d-105">指出整體影像增益調整的程度。</span><span class="sxs-lookup"><span data-stu-id="3a93d-105">Indicates the degree of overall image gain adjustment.</span></span> <span data-ttu-id="3a93d-106">從 PKEY \_ photo \_ GAINCONTROLNUMERATOR 和 PKEY \_ photo GainControlDenominator 計算 \_ 。</span><span class="sxs-lookup"><span data-stu-id="3a93d-106">Calculated from PKEY\_Photo\_GainControlNumerator and PKEY\_Photo\_GainControlDenominator.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="3a93d-107">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="3a93d-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.GainControl
   shellPKey = PKEY_Photo_GainControl
   formatID = FA304789-00C7-4D80-904A-1E4DCC7265AA
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Double
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = None
            value = 0.0
            text = None
            defineToken = PHOTO_GAINCONTROL_NONE
         enum
            name = LowGainUp
            value = 1.0
            text = Low gain up
            defineToken = PHOTO_GAINCONTROL_LOWGAINUP
         enum
            name = HighGainUp
            value = 2.0
            text = High gain up
            defineToken = PHOTO_GAINCONTROL_HIGHGAINUP
         enum
            name = LowGainDown
            value = 3.0
            text = Low gain down
            defineToken = PHOTO_GAINCONTROL_LOWGAINDOWN
         enum
            name = HighGainDown
            value = 4.0
            text = High gain down
            defineToken = PHOTO_GAINCONTROL_HIGHGAINDOWN
```

## <a name="windows-vista"></a><span data-ttu-id="3a93d-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a93d-108">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.GainControl
   shellPKey = PKEY_Photo_GainControl
   formatID = FA304789-00C7-4D80-904A-1E4DCC7265AA
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Double
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0.0
            text = None
            defineName = PHOTO_GAINCONTROL_NONE
         enum
            value = 1.0
            text = Low gain up
            defineName = PHOTO_GAINCONTROL_LOWGAINUP
         enum
            value = 2.0
            text = High gain up
            defineName = PHOTO_GAINCONTROL_HIGHGAINUP
         enum
            value = 3.0
            text = Low gain down
            defineName = PHOTO_GAINCONTROL_LOWGAINDOWN
         enum
            value = 4.0
            text = High gain down
            defineName = PHOTO_GAINCONTROL_HIGHGAINDOWN
```

## <a name="remarks"></a><span data-ttu-id="3a93d-109">備註</span><span class="sxs-lookup"><span data-stu-id="3a93d-109">Remarks</span></span>

<span data-ttu-id="3a93d-110">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="3a93d-110">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a93d-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="3a93d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a93d-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="3a93d-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="3a93d-113">searchInfo</span><span class="sxs-lookup"><span data-stu-id="3a93d-113">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="3a93d-114">labelInfo</span><span class="sxs-lookup"><span data-stu-id="3a93d-114">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="3a93d-115">typeInfo</span><span class="sxs-lookup"><span data-stu-id="3a93d-115">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="3a93d-116">displayInfo</span><span class="sxs-lookup"><span data-stu-id="3a93d-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="3a93d-117">stringFormat</span><span class="sxs-lookup"><span data-stu-id="3a93d-117">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="3a93d-118">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="3a93d-118">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="3a93d-119">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="3a93d-119">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="3a93d-120">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="3a93d-120">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="3a93d-121">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="3a93d-121">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="3a93d-122">drawControl</span><span class="sxs-lookup"><span data-stu-id="3a93d-122">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="3a93d-123">editControl</span><span class="sxs-lookup"><span data-stu-id="3a93d-123">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="3a93d-124">filterControl</span><span class="sxs-lookup"><span data-stu-id="3a93d-124">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="3a93d-125">queryControl</span><span class="sxs-lookup"><span data-stu-id="3a93d-125">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
