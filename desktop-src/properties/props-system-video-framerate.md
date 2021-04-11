---
description: 表示影片串流的畫面播放速率，以每1000秒的畫面格速率表示。
ms.assetid: cd5a2ae0-43ef-44e4-aa70-bca33baf2a56
title: System.string
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcbdee7991186621a9d636e2072cecafc70176d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193578"
---
# <a name="systemvideoframerate"></a><span data-ttu-id="9771d-103">System.string</span><span class="sxs-lookup"><span data-stu-id="9771d-103">System.Video.FrameRate</span></span>

<span data-ttu-id="9771d-104">表示影片串流的畫面播放速率，以每1000秒的畫面格速率表示。</span><span class="sxs-lookup"><span data-stu-id="9771d-104">Indicates the frame rate for the video stream, in frames per 1000 seconds.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="9771d-105">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="9771d-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Video.FrameRate
   shellPKey = PKEY_Video_FrameRate
   formatID = 64440491-4C8B-11D1-8B70-080036B11A03
   propID = 6
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
```

## <a name="windows-vista"></a><span data-ttu-id="9771d-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9771d-106">Windows Vista</span></span>

```
propertyDescription
   name = System.Video.FrameRate
   shellPKey = PKEY_Video_FrameRate
   formatID = 64440491-4C8B-11D1-8B70-080036B11A03
   propID = 6
   SearchInfo
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="9771d-107">備註</span><span class="sxs-lookup"><span data-stu-id="9771d-107">Remarks</span></span>

<span data-ttu-id="9771d-108">為了避免截斷錯誤，此屬性不會使用每秒畫面格的標準畫面播放速率量值 (FPS) 。</span><span class="sxs-lookup"><span data-stu-id="9771d-108">To help reduce truncation error, this property does not use the standard frame rate measure of frames per second (FPS).</span></span> <span data-ttu-id="9771d-109">相反地，此屬性會將畫面播放速率測量為每1000秒的框架 (FPS 乘以 1000) 。</span><span class="sxs-lookup"><span data-stu-id="9771d-109">Instead, this property measures frame rate as frames per 1000 seconds (FPS multiplied by 1000).</span></span> <span data-ttu-id="9771d-110">例如，system.string [會將]() 29.97 FPS 的畫面播放速率表示為整數值29970。</span><span class="sxs-lookup"><span data-stu-id="9771d-110">For example, [System.Video.FrameRate]() would express a frame rate of 29.97 FPS as an integer value of 29970.</span></span>

<span data-ttu-id="9771d-111">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="9771d-111">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9771d-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="9771d-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9771d-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="9771d-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="9771d-114">searchInfo</span><span class="sxs-lookup"><span data-stu-id="9771d-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="9771d-115">labelInfo</span><span class="sxs-lookup"><span data-stu-id="9771d-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="9771d-116">typeInfo</span><span class="sxs-lookup"><span data-stu-id="9771d-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="9771d-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="9771d-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="9771d-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="9771d-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="9771d-119">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="9771d-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="9771d-120">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="9771d-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="9771d-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="9771d-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="9771d-122">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="9771d-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="9771d-123">drawControl</span><span class="sxs-lookup"><span data-stu-id="9771d-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="9771d-124">editControl</span><span class="sxs-lookup"><span data-stu-id="9771d-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="9771d-125">filterControl</span><span class="sxs-lookup"><span data-stu-id="9771d-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="9771d-126">queryControl</span><span class="sxs-lookup"><span data-stu-id="9771d-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
