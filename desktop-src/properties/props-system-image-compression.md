---
description: 用來壓縮影像的演算法。
ms.assetid: b355351d-b0b4-4f5d-a440-fc408a29e700
title: 系統映射壓縮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b33b75d2d291edbc16a8cfd6c0c96c2a3db610e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981545"
---
# <a name="systemimagecompression"></a><span data-ttu-id="044da-103">系統映射壓縮</span><span class="sxs-lookup"><span data-stu-id="044da-103">System.Image.Compression</span></span>

<span data-ttu-id="044da-104">用來壓縮影像的演算法。</span><span class="sxs-lookup"><span data-stu-id="044da-104">The algorithm used to compress the image.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="044da-105">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="044da-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Image.Compression
   shellPKey = PKEY_Image_Compression
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 259
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Uncompressed
            value = 1
            text = Uncompressed
            defineToken = IMAGE_COMPRESSION_UNCOMPRESSED
         enum
            name = CCITT.T3
            value = 2
            text = CCITT T.3
            defineToken = IMAGE_COMPRESSION_CCITT_T3
         enum
            name = CCITT.T4
            value = 3
            text = CCITT T.4
            defineToken = IMAGE_COMPRESSION_CCITT_T4
         enum
            name = CCITT.T6
            value = 4
            text = CCITT T.6
            defineToken = IMAGE_COMPRESSION_CCITT_T6
         enum
            name = LZW
            value = 5
            text = LZW
            defineToken = IMAGE_COMPRESSION_LZW
         enum
            name = JPEG
            value = 6
            text = JPEG
            defineToken = IMAGE_COMPRESSION_JPEG
         enum
            name = PackBits
            value = 32773
            text = PackBits
            defineToken = IMAGE_COMPRESSION_PACKBITS
```

## <a name="windows-vista"></a><span data-ttu-id="044da-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="044da-106">Windows Vista</span></span>

```
propertyDescription
   name = System.Image.Compression
   shellPKey = PKEY_Image_Compression
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 259
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
            text = Uncompressed
            defineName = IMAGE_COMPRESSION_UNCOMPRESSED
         enum
            value = 2
            text = CCITT T.3
            defineName = IMAGE_COMPRESSION_CCITT_T3
         enum
            value = 3
            text = CCITT T.4
            defineName = IMAGE_COMPRESSION_CCITT_T4
         enum
            value = 4
            text = CCITT T.6
            defineName = IMAGE_COMPRESSION_CCITT_T6
         enum
            value = 5
            text = LZW
            defineName = IMAGE_COMPRESSION_LZW
         enum
            value = 6
            text = JPEG
            defineName = IMAGE_COMPRESSION_JPEG
         enum
            value = 32773
            text = PackBits
            defineName = IMAGE_COMPRESSION_PACKBITS
```

## <a name="remarks"></a><span data-ttu-id="044da-107">備註</span><span class="sxs-lookup"><span data-stu-id="044da-107">Remarks</span></span>

<span data-ttu-id="044da-108">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="044da-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="044da-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="044da-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="044da-110">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="044da-110">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="044da-111">searchInfo</span><span class="sxs-lookup"><span data-stu-id="044da-111">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="044da-112">labelInfo</span><span class="sxs-lookup"><span data-stu-id="044da-112">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="044da-113">typeInfo</span><span class="sxs-lookup"><span data-stu-id="044da-113">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="044da-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="044da-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="044da-115">stringFormat</span><span class="sxs-lookup"><span data-stu-id="044da-115">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="044da-116">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="044da-116">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="044da-117">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="044da-117">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="044da-118">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="044da-118">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="044da-119">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="044da-119">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="044da-120">drawControl</span><span class="sxs-lookup"><span data-stu-id="044da-120">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="044da-121">editControl</span><span class="sxs-lookup"><span data-stu-id="044da-121">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="044da-122">filterControl</span><span class="sxs-lookup"><span data-stu-id="044da-122">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="044da-123">queryControl</span><span class="sxs-lookup"><span data-stu-id="044da-123">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
