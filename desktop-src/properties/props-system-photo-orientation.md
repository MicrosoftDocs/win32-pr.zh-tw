---
description: 拍攝相片時的方向（如同交換影像檔案中所指定） (EXIF) 資訊，以及資料列和資料行的詞彙。
ms.assetid: d6186248-8944-4bd6-8f04-bab5ea15b169
title: '[列印]'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cac8cec8e199bd8eff52a92c7518a998d805d18d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987495"
---
# <a name="systemphotoorientation"></a><span data-ttu-id="67a41-103">[列印]</span><span class="sxs-lookup"><span data-stu-id="67a41-103">System.Photo.Orientation</span></span>

<span data-ttu-id="67a41-104">拍攝相片時的方向（如同交換影像檔案中所指定） (EXIF) 資訊，以及資料列和資料行的詞彙。</span><span class="sxs-lookup"><span data-stu-id="67a41-104">The orientation of the photo when it was taken, as specified in the Exchangeable Image File (EXIF) information and in terms of rows and columns.</span></span> <span data-ttu-id="67a41-105">這可讓應用程式和 Shell 正確地設定影像的方向，而不是調整圖元的方向，並以要求的顯示方向來保存影像，這可能會導致精確度遺失。</span><span class="sxs-lookup"><span data-stu-id="67a41-105">This allows applications and the Shell to properly orient the image, instead of orienting the pixels and persisting the image in the requested display orientation, which can result in a loss of fidelity.</span></span> <span data-ttu-id="67a41-106">這個屬性不應該顯示在 UI 中。</span><span class="sxs-lookup"><span data-stu-id="67a41-106">This property is not meant to be displayed in the UI.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="67a41-107">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="67a41-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.Orientation
   shellPKey = PKEY_Photo_Orientation
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 274
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Normal
            value = 1
            text = Normal
            defineToken = PHOTO_ORIENTATION_NORMAL
         enum
            name = FlipHorizontal
            value = 2
            text = Flip horizontal
            defineToken = PHOTO_ORIENTATION_FLIPHORIZONTAL
         enum
            name = Rotate180
            value = 3
            text = Rotate 180 degrees
            defineToken = PHOTO_ORIENTATION_ROTATE180
         enum
            name = FlipVertical
            value = 4
            text = Flip vertical
            defineToken = PHOTO_ORIENTATION_FLIPVERTICAL
         enum
            name = Transpose
            value = 5
            text = Transpose
            defineToken = PHOTO_ORIENTATION_TRANSPOSE
         enum
            name = Rotate270
            value = 6
            text = Rotate 270 degrees
            defineToken = PHOTO_ORIENTATION_ROTATE270
         enum
            name = Transverse
            value = 7
            text = Transverse
            defineToken = PHOTO_ORIENTATION_TRANSVERSE
         enum
            name = Rotate90
            value = 8
            text = Rotate 90 degrees
            defineToken = PHOTO_ORIENTATION_ROTATE90
```

## <a name="windows-vista"></a><span data-ttu-id="67a41-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67a41-108">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.Orientation
   shellPKey = PKEY_Photo_Orientation
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 274
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 1
            text = Normal
            defineName = PHOTO_ORIENTATION_NORMAL
         enum
            value = 2
            text = Flip horizontal
            defineName = PHOTO_ORIENTATION_FLIPHORIZONTAL
         enum
            value = 3
            text = Rotate 180 degrees
            defineName = PHOTO_ORIENTATION_ROTATE180
         enum
            value = 4
            text = Flip vertical
            defineName = PHOTO_ORIENTATION_FLIPVERTICAL
         enum
            value = 5
            text = Transpose
            defineName = PHOTO_ORIENTATION_TRANSPOSE
         enum
            value = 6
            text = Rotate 270 degrees
            defineName = PHOTO_ORIENTATION_ROTATE270
         enum
            value = 7
            text = Transverse
            defineName = PHOTO_ORIENTATION_TRANSVERSE
         enum
            value = 8
            text = Rotate 90 degrees
            defineName = PHOTO_ORIENTATION_ROTATE90
```

## <a name="remarks"></a><span data-ttu-id="67a41-109">備註</span><span class="sxs-lookup"><span data-stu-id="67a41-109">Remarks</span></span>

<span data-ttu-id="67a41-110">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="67a41-110">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67a41-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="67a41-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67a41-112">數位相機的交換影像檔案格式： Exif 2.2 版</span><span class="sxs-lookup"><span data-stu-id="67a41-112">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="67a41-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="67a41-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="67a41-114">searchInfo</span><span class="sxs-lookup"><span data-stu-id="67a41-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="67a41-115">labelInfo</span><span class="sxs-lookup"><span data-stu-id="67a41-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="67a41-116">typeInfo</span><span class="sxs-lookup"><span data-stu-id="67a41-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="67a41-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="67a41-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="67a41-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="67a41-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="67a41-119">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="67a41-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="67a41-120">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="67a41-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="67a41-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="67a41-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="67a41-122">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="67a41-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="67a41-123">drawControl</span><span class="sxs-lookup"><span data-stu-id="67a41-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="67a41-124">editControl</span><span class="sxs-lookup"><span data-stu-id="67a41-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="67a41-125">filterControl</span><span class="sxs-lookup"><span data-stu-id="67a41-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="67a41-126">queryControl</span><span class="sxs-lookup"><span data-stu-id="67a41-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
