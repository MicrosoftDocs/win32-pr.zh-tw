---
description: 影像拍攝時的數位縮放比例。
ms.assetid: 1164e2c9-0864-4520-a3be-0c29a5b70ba4
title: DigitalZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b681b898b8faadcf4366e9d7668975e598d95c24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944074"
---
# <a name="systemphotodigitalzoom"></a><span data-ttu-id="12391-103">DigitalZoom</span><span class="sxs-lookup"><span data-stu-id="12391-103">System.Photo.DigitalZoom</span></span>

<span data-ttu-id="12391-104">影像拍攝時的數位縮放比例。</span><span class="sxs-lookup"><span data-stu-id="12391-104">The digital zoom ratio when the image was shot.</span></span> <span data-ttu-id="12391-105">在檔案的交換影像檔案中讀取相機 (EXIF) 資訊。</span><span class="sxs-lookup"><span data-stu-id="12391-105">Read from the camera in the file's Exchangeable Image File (EXIF) information.</span></span> <span data-ttu-id="12391-106">這個屬性是從 [DigitalZoomNumerator](./props-system-photo-digitalzoomnumerator.md) 和 [DigitalZoomDenominator](./props-system-photo-digitalzoomdenominator.md)計算而來。</span><span class="sxs-lookup"><span data-stu-id="12391-106">This property is calculated from [System.Photo.DigitalZoomNumerator](./props-system-photo-digitalzoomnumerator.md) and [System.Photo.DigitalZoomDenominator](./props-system-photo-digitalzoomdenominator.md).</span></span> <span data-ttu-id="12391-107">如果記錄值的分子為0，則不會使用數位縮放。</span><span class="sxs-lookup"><span data-stu-id="12391-107">If the numerator of the recorded value is 0, a digital zoom was not used.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="12391-108">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本</span><span class="sxs-lookup"><span data-stu-id="12391-108">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.DigitalZoom
   shellPKey = PKEY_Photo_DigitalZoom
   formatID = F85BF840-A925-4BC2-B0C4-8E36B598679E
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="12391-109">備註</span><span class="sxs-lookup"><span data-stu-id="12391-109">Remarks</span></span>

<span data-ttu-id="12391-110">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="12391-110">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12391-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="12391-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12391-112">數位相機的交換影像檔案格式： Exif 2.2 版</span><span class="sxs-lookup"><span data-stu-id="12391-112">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="12391-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="12391-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="12391-114">searchInfo</span><span class="sxs-lookup"><span data-stu-id="12391-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="12391-115">labelInfo</span><span class="sxs-lookup"><span data-stu-id="12391-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="12391-116">typeInfo</span><span class="sxs-lookup"><span data-stu-id="12391-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="12391-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="12391-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="12391-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="12391-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="12391-119">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="12391-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="12391-120">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="12391-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="12391-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="12391-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="12391-122">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="12391-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="12391-123">drawControl</span><span class="sxs-lookup"><span data-stu-id="12391-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="12391-124">editControl</span><span class="sxs-lookup"><span data-stu-id="12391-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="12391-125">filterControl</span><span class="sxs-lookup"><span data-stu-id="12391-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="12391-126">queryControl</span><span class="sxs-lookup"><span data-stu-id="12391-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
