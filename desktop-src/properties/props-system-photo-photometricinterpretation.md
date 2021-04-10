---
description: 圖元組合。
ms.assetid: e2bb7f82-10dc-4fa0-875d-fc58c133024d
title: PhotometricInterpretation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79f6b431470780def946dbb8958e9e3eb6698322
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026666"
---
# <a name="systemphotophotometricinterpretation"></a><span data-ttu-id="89e2b-103">PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="89e2b-103">System.Photo.PhotometricInterpretation</span></span>

<span data-ttu-id="89e2b-104">圖元組合。</span><span class="sxs-lookup"><span data-stu-id="89e2b-104">The pixel composition.</span></span> <span data-ttu-id="89e2b-105">在 JPEG 壓縮的資料中，會使用 JPEG 標記，而不是此屬性。</span><span class="sxs-lookup"><span data-stu-id="89e2b-105">In JPEG compressed data, a JPEG marker is used instead of this property.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="89e2b-106">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="89e2b-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.PhotometricInterpretation
   shellPKey = PKEY_Photo_PhotometricInterpretation
   formatID = 341796F1-1DF9-4B1C-A564-91BDEFA43877
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt16
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = RGB
            value = 2
            text = RGB
            defineToken = PHOTO_PHOTOMETRIC_RGB
         enum
            name = YCbCr
            value = 6
            text = YCbCr
            defineToken = PHOTO_PHOTOMETRIC_YCBCR
```

## <a name="windows-vista"></a><span data-ttu-id="89e2b-107">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89e2b-107">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.PhotometricInterpretation
   shellPKey = PKEY_Photo_PhotometricInterpretation
   formatID = 341796F1-1DF9-4B1C-A564-91BDEFA43877
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt16
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 2
            text = RGB
            defineName = PHOTO_PHOTOMETRIC_RGB
         enum
            value = 6
            text = YCbCr
            defineName = PHOTO_PHOTOMETRIC_YCBCR
```

## <a name="remarks"></a><span data-ttu-id="89e2b-108">備註</span><span class="sxs-lookup"><span data-stu-id="89e2b-108">Remarks</span></span>

<span data-ttu-id="89e2b-109">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="89e2b-109">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="89e2b-110">在 `isInnate` Windows Vista Service Pack 1 (SP1) 的情況下， **typeInfo** 元素的屬性預設值已從 **false** 變更為 **true** 。</span><span class="sxs-lookup"><span data-stu-id="89e2b-110">The default value of the `isInnate` attribute of the **typeInfo** element was changed from **false** to **true** as of Windows Vista with Service Pack 1 (SP1).</span></span>

## <a name="related-topics"></a><span data-ttu-id="89e2b-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="89e2b-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89e2b-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="89e2b-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="89e2b-113">searchInfo</span><span class="sxs-lookup"><span data-stu-id="89e2b-113">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="89e2b-114">labelInfo</span><span class="sxs-lookup"><span data-stu-id="89e2b-114">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="89e2b-115">typeInfo</span><span class="sxs-lookup"><span data-stu-id="89e2b-115">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="89e2b-116">displayInfo</span><span class="sxs-lookup"><span data-stu-id="89e2b-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="89e2b-117">stringFormat</span><span class="sxs-lookup"><span data-stu-id="89e2b-117">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="89e2b-118">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="89e2b-118">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="89e2b-119">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="89e2b-119">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="89e2b-120">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="89e2b-120">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="89e2b-121">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="89e2b-121">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="89e2b-122">drawControl</span><span class="sxs-lookup"><span data-stu-id="89e2b-122">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="89e2b-123">editControl</span><span class="sxs-lookup"><span data-stu-id="89e2b-123">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="89e2b-124">filterControl</span><span class="sxs-lookup"><span data-stu-id="89e2b-124">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="89e2b-125">queryControl</span><span class="sxs-lookup"><span data-stu-id="89e2b-125">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
