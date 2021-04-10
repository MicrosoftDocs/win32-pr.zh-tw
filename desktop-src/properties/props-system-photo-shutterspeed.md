---
description: 拍攝相片時相機的快門速度。 這是以頂點單位提供。
ms.assetid: 7f51b3b9-d701-4e7a-80bd-87c1a60e56f7
title: ShutterSpeed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172ce97bf87e79dd86f83e68c91940748bbc283f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026663"
---
# <a name="systemphotoshutterspeed"></a><span data-ttu-id="df925-104">ShutterSpeed</span><span class="sxs-lookup"><span data-stu-id="df925-104">System.Photo.ShutterSpeed</span></span>

<span data-ttu-id="df925-105">拍攝相片時相機的快門速度。</span><span class="sxs-lookup"><span data-stu-id="df925-105">The shutter speed of the camera when the photo was taken.</span></span> <span data-ttu-id="df925-106">這是以頂點單位提供。</span><span class="sxs-lookup"><span data-stu-id="df925-106">This is given in APEX units.</span></span> <span data-ttu-id="df925-107">這個屬性是從 [ShutterSpeedNumerator](./props-system-photo-shutterspeednumerator.md) 和 [ShutterSpeedDenominator](./props-system-photo-shutterspeeddenominator.md)計算而來。</span><span class="sxs-lookup"><span data-stu-id="df925-107">This property is calculated from [System.Photo.ShutterSpeedNumerator](./props-system-photo-shutterspeednumerator.md) and [System.Photo.ShutterSpeedDenominator](./props-system-photo-shutterspeeddenominator.md).</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="df925-108">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="df925-108">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.ShutterSpeed
   shellPKey = PKEY_Photo_ShutterSpeed
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37377
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="windows-vista"></a><span data-ttu-id="df925-109">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df925-109">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.ShutterSpeed
   shellPKey = PKEY_Photo_ShutterSpeed
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37377
   SearchInfo
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="df925-110">備註</span><span class="sxs-lookup"><span data-stu-id="df925-110">Remarks</span></span>

<span data-ttu-id="df925-111">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="df925-111">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="df925-112">如需將此值轉換為曝光時間，請參閱交換影像檔案 (EXIF) 2.2 規格（附錄 C）。</span><span class="sxs-lookup"><span data-stu-id="df925-112">See the Exchangeable Image File (EXIF) 2.2 specification, Annex C, for the conversion of this value to exposure time.</span></span> <span data-ttu-id="df925-113">在任何 Shell 視圖中使用 [ExposureTime](./props-system-photo-exposuretime.md) ，而不是 [ShutterSpeed]()。</span><span class="sxs-lookup"><span data-stu-id="df925-113">Use [System.Photo.ExposureTime](./props-system-photo-exposuretime.md) in any Shell views instead of [System.Photo.ShutterSpeed]().</span></span>

## <a name="related-topics"></a><span data-ttu-id="df925-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="df925-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df925-115">數位相機的交換影像檔案格式： Exif 2.2 版</span><span class="sxs-lookup"><span data-stu-id="df925-115">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="df925-116">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="df925-116">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="df925-117">searchInfo</span><span class="sxs-lookup"><span data-stu-id="df925-117">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="df925-118">labelInfo</span><span class="sxs-lookup"><span data-stu-id="df925-118">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="df925-119">typeInfo</span><span class="sxs-lookup"><span data-stu-id="df925-119">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="df925-120">displayInfo</span><span class="sxs-lookup"><span data-stu-id="df925-120">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="df925-121">stringFormat</span><span class="sxs-lookup"><span data-stu-id="df925-121">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="df925-122">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="df925-122">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="df925-123">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="df925-123">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="df925-124">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="df925-124">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="df925-125">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="df925-125">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="df925-126">drawControl</span><span class="sxs-lookup"><span data-stu-id="df925-126">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="df925-127">editControl</span><span class="sxs-lookup"><span data-stu-id="df925-127">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="df925-128">filterControl</span><span class="sxs-lookup"><span data-stu-id="df925-128">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="df925-129">queryControl</span><span class="sxs-lookup"><span data-stu-id="df925-129">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
