---
description: 從交換影像檔案讀取之相片的曝光時間（以秒為單位） (EXIF) 資訊。
ms.assetid: 44f7e6d5-c4d9-4b41-b6c6-15145abb7983
title: ExposureTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5811a3d375f41883d1db8f392e714b7bbe0dfa8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192500"
---
# <a name="systemphotoexposuretime"></a><span data-ttu-id="1212b-103">ExposureTime</span><span class="sxs-lookup"><span data-stu-id="1212b-103">System.Photo.ExposureTime</span></span>

<span data-ttu-id="1212b-104">從交換影像檔案讀取之相片的曝光時間（以秒為單位） (EXIF) 資訊。</span><span class="sxs-lookup"><span data-stu-id="1212b-104">The exposure time for the photo, in seconds, as read from the Exchangeable Image File (EXIF) information.</span></span> <span data-ttu-id="1212b-105">這個屬性是從 [ExposureTimeNumerator](./props-system-photo-exposuretimenumerator.md) 和 [ExposureTimeDenominator](./props-system-photo-exposuretimedenominator.md)計算而來。</span><span class="sxs-lookup"><span data-stu-id="1212b-105">This property is calculated from [System.Photo.ExposureTimeNumerator](./props-system-photo-exposuretimenumerator.md) and [System.Photo.ExposureTimeDenominator](./props-system-photo-exposuretimedenominator.md).</span></span>

<span data-ttu-id="1212b-106">以下是從 EXIF 2.2 規格中取得的可能值清單。</span><span class="sxs-lookup"><span data-stu-id="1212b-106">The following is a list of possible values taken from the EXIF 2.2 specification.</span></span>

-   <span data-ttu-id="1212b-107">30</span><span class="sxs-lookup"><span data-stu-id="1212b-107">30</span></span>
-   <span data-ttu-id="1212b-108">15</span><span class="sxs-lookup"><span data-stu-id="1212b-108">15</span></span>
-   <span data-ttu-id="1212b-109">8</span><span class="sxs-lookup"><span data-stu-id="1212b-109">8</span></span>
-   <span data-ttu-id="1212b-110">4</span><span class="sxs-lookup"><span data-stu-id="1212b-110">4</span></span>
-   <span data-ttu-id="1212b-111">2</span><span class="sxs-lookup"><span data-stu-id="1212b-111">2</span></span>
-   <span data-ttu-id="1212b-112">1</span><span class="sxs-lookup"><span data-stu-id="1212b-112">1</span></span>
-   <span data-ttu-id="1212b-113">1/2</span><span class="sxs-lookup"><span data-stu-id="1212b-113">1/2</span></span>
-   <span data-ttu-id="1212b-114">1/4</span><span class="sxs-lookup"><span data-stu-id="1212b-114">1/4</span></span>
-   <span data-ttu-id="1212b-115">1/8</span><span class="sxs-lookup"><span data-stu-id="1212b-115">1/8</span></span>
-   <span data-ttu-id="1212b-116">1/15</span><span class="sxs-lookup"><span data-stu-id="1212b-116">1/15</span></span>
-   <span data-ttu-id="1212b-117">1/30</span><span class="sxs-lookup"><span data-stu-id="1212b-117">1/30</span></span>
-   <span data-ttu-id="1212b-118">1/60</span><span class="sxs-lookup"><span data-stu-id="1212b-118">1/60</span></span>
-   <span data-ttu-id="1212b-119">1/125</span><span class="sxs-lookup"><span data-stu-id="1212b-119">1/125</span></span>
-   <span data-ttu-id="1212b-120">1/250</span><span class="sxs-lookup"><span data-stu-id="1212b-120">1/250</span></span>
-   <span data-ttu-id="1212b-121">1/500</span><span class="sxs-lookup"><span data-stu-id="1212b-121">1/500</span></span>
-   <span data-ttu-id="1212b-122">1/1000</span><span class="sxs-lookup"><span data-stu-id="1212b-122">1/1000</span></span>
-   <span data-ttu-id="1212b-123">1/2000</span><span class="sxs-lookup"><span data-stu-id="1212b-123">1/2000</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="1212b-124">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本</span><span class="sxs-lookup"><span data-stu-id="1212b-124">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.ExposureTime
   shellPKey = PKEY_Photo_ExposureTime
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 33434
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="1212b-125">備註</span><span class="sxs-lookup"><span data-stu-id="1212b-125">Remarks</span></span>

<span data-ttu-id="1212b-126">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="1212b-126">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1212b-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="1212b-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1212b-128">數位相機的交換影像檔案格式： Exif 2.2 版</span><span class="sxs-lookup"><span data-stu-id="1212b-128">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="1212b-129">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="1212b-129">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="1212b-130">searchInfo</span><span class="sxs-lookup"><span data-stu-id="1212b-130">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="1212b-131">labelInfo</span><span class="sxs-lookup"><span data-stu-id="1212b-131">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="1212b-132">typeInfo</span><span class="sxs-lookup"><span data-stu-id="1212b-132">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="1212b-133">displayInfo</span><span class="sxs-lookup"><span data-stu-id="1212b-133">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="1212b-134">stringFormat</span><span class="sxs-lookup"><span data-stu-id="1212b-134">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="1212b-135">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="1212b-135">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="1212b-136">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="1212b-136">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="1212b-137">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="1212b-137">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="1212b-138">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="1212b-138">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="1212b-139">drawControl</span><span class="sxs-lookup"><span data-stu-id="1212b-139">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="1212b-140">editControl</span><span class="sxs-lookup"><span data-stu-id="1212b-140">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="1212b-141">filterControl</span><span class="sxs-lookup"><span data-stu-id="1212b-141">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="1212b-142">queryControl</span><span class="sxs-lookup"><span data-stu-id="1212b-142">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
