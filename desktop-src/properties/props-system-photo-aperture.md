---
description: 影像的光圈值（以頂點單位）。
ms.assetid: ec8c0271-1e1e-4d37-a09a-f430d0682213
title: System.servicemodel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2273425c1974617b7d76657f818c4f1c39cd3aea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192506"
---
# <a name="systemphotoaperture"></a><span data-ttu-id="89a44-103">System.servicemodel</span><span class="sxs-lookup"><span data-stu-id="89a44-103">System.Photo.Aperture</span></span>

<span data-ttu-id="89a44-104">影像的光圈值（以頂點單位）。</span><span class="sxs-lookup"><span data-stu-id="89a44-104">The aperture value of the image, in APEX units.</span></span> <span data-ttu-id="89a44-105">如需比較[FNumber](./props-system-photo-fnumber.md) [的值]()，請參閱交換影像檔案 (EXIF) 2.2 規格（附錄 C）。</span><span class="sxs-lookup"><span data-stu-id="89a44-105">See the Exchangeable Image File (EXIF) 2.2 specification, Annex C, for a comparison of [System.Photo.Aperture]() numbers and [System.Photo.FNumber](./props-system-photo-fnumber.md) values.</span></span> <span data-ttu-id="89a44-106">這個屬性是從 [ApertureNumerator](./props-system-photo-aperturenumerator.md) 和 [ApertureDenominator](./props-system-photo-aperturedenominator.md)計算而來。</span><span class="sxs-lookup"><span data-stu-id="89a44-106">This property is calculated from [System.Photo.ApertureNumerator](./props-system-photo-aperturenumerator.md) and [System.Photo.ApertureDenominator](./props-system-photo-aperturedenominator.md).</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="89a44-107">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="89a44-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.Aperture
   shellPKey = PKEY_Photo_Aperture
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37378
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="windows-vista"></a><span data-ttu-id="89a44-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89a44-108">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.Aperture
   shellPKey = PKEY_Photo_Aperture
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37378
   SearchInfo
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="89a44-109">備註</span><span class="sxs-lookup"><span data-stu-id="89a44-109">Remarks</span></span>

<span data-ttu-id="89a44-110">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="89a44-110">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89a44-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="89a44-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89a44-112">數位相機的交換影像檔案格式： Exif 2.2 版</span><span class="sxs-lookup"><span data-stu-id="89a44-112">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="89a44-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="89a44-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="89a44-114">searchInfo</span><span class="sxs-lookup"><span data-stu-id="89a44-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="89a44-115">labelInfo</span><span class="sxs-lookup"><span data-stu-id="89a44-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="89a44-116">typeInfo</span><span class="sxs-lookup"><span data-stu-id="89a44-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="89a44-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="89a44-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="89a44-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="89a44-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="89a44-119">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="89a44-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="89a44-120">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="89a44-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="89a44-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="89a44-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="89a44-122">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="89a44-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="89a44-123">drawControl</span><span class="sxs-lookup"><span data-stu-id="89a44-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="89a44-124">editControl</span><span class="sxs-lookup"><span data-stu-id="89a44-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="89a44-125">filterControl</span><span class="sxs-lookup"><span data-stu-id="89a44-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="89a44-126">queryControl</span><span class="sxs-lookup"><span data-stu-id="89a44-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
