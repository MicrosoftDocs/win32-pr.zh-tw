---
description: 指出音訊檔案的頻道計數。 Mono 的可能值是1，而針對身歷聲則為2。
ms.assetid: 8a028167-dc0f-4ed9-a710-568caf1b9a47
title: ChannelCount
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9a370e517f8c3552e27bf034c4873b5e1cb593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848681"
---
# <a name="systemaudiochannelcount"></a><span data-ttu-id="6c16e-104">ChannelCount</span><span class="sxs-lookup"><span data-stu-id="6c16e-104">System.Audio.ChannelCount</span></span>

<span data-ttu-id="6c16e-105">指出音訊檔案的頻道計數。</span><span class="sxs-lookup"><span data-stu-id="6c16e-105">Indicates the channel count for the audio file.</span></span> <span data-ttu-id="6c16e-106">Mono 的可能值是1，而針對身歷聲則為2。</span><span class="sxs-lookup"><span data-stu-id="6c16e-106">Possible values are 1 for mono and 2 for stereo.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="6c16e-107">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="6c16e-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Audio.ChannelCount
   shellPKey = PKEY_Audio_ChannelCount
   formatID = 64440490-4C8B-11D1-8B70-080036B11A03
   propID = 7
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Mono
            value = 1
            text = 1 (mono)
            defineToken = AUDIO_CHANNELCOUNT_MONO
         enum
            name = Stereo
            value = 2
            text = 2 (stereo)
            defineToken = AUDIO_CHANNELCOUNT_STEREO
```

## <a name="windows-vista"></a><span data-ttu-id="6c16e-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c16e-108">Windows Vista</span></span>

```
propertyDescription
   name = System.Audio.ChannelCount
   shellPKey = PKEY_Audio_ChannelCount
   formatID = 64440490-4C8B-11D1-8B70-080036B11A03
   propID = 7
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 1
            text = 1 (mono)
            defineName = AUDIO_CHANNELCOUNT_MONO
         enum
            value = 2
            text = 2 (stereo)
            defineName = AUDIO_CHANNELCOUNT_STEREO
```

## <a name="remarks"></a><span data-ttu-id="6c16e-109">備註</span><span class="sxs-lookup"><span data-stu-id="6c16e-109">Remarks</span></span>

<span data-ttu-id="6c16e-110">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="6c16e-110">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c16e-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="6c16e-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c16e-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="6c16e-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="6c16e-113">searchInfo</span><span class="sxs-lookup"><span data-stu-id="6c16e-113">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="6c16e-114">labelInfo</span><span class="sxs-lookup"><span data-stu-id="6c16e-114">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="6c16e-115">typeInfo</span><span class="sxs-lookup"><span data-stu-id="6c16e-115">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="6c16e-116">displayInfo</span><span class="sxs-lookup"><span data-stu-id="6c16e-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="6c16e-117">stringFormat</span><span class="sxs-lookup"><span data-stu-id="6c16e-117">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="6c16e-118">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="6c16e-118">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="6c16e-119">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="6c16e-119">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="6c16e-120">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="6c16e-120">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="6c16e-121">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="6c16e-121">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="6c16e-122">drawControl</span><span class="sxs-lookup"><span data-stu-id="6c16e-122">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="6c16e-123">editControl</span><span class="sxs-lookup"><span data-stu-id="6c16e-123">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="6c16e-124">filterControl</span><span class="sxs-lookup"><span data-stu-id="6c16e-124">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="6c16e-125">queryControl</span><span class="sxs-lookup"><span data-stu-id="6c16e-125">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
