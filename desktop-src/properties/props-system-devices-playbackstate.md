---
description: 裝置的播放狀態。
ms.assetid: 7F77459B-5900-4967-A2A3-AAEE78DF84E1
title: PlaybackState
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a95b736d80df49587954f20c4c000c82779d5648
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001364"
---
# <a name="systemdevicesplaybackstate"></a><span data-ttu-id="7d3ea-103">PlaybackState</span><span class="sxs-lookup"><span data-stu-id="7d3ea-103">System.Devices.PlaybackState</span></span>

<span data-ttu-id="7d3ea-104">裝置的播放狀態。</span><span class="sxs-lookup"><span data-stu-id="7d3ea-104">The playback state of the device.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="7d3ea-105">Windows 10，1703版、Windows 10、1607版、Windows 10、1511版、Windows 10、version 1507、Windows 8.1、Windows 8</span><span class="sxs-lookup"><span data-stu-id="7d3ea-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.Devices.PlaybackState
   shellPKey = PKEY_Devices_PlaybackState
   formatID = 3633DE59-6825-4381-A49B-9F6BA13A1471
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Byte
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = UnknownState
            value = 0
            text = Unknown State
            defineToken = PLAYBACKSTATE_UNKNOWN
         enum
            name = Stopped
            value = 1
            text = Stopped
            defineToken = PLAYBACKSTATE_STOPPED
         enum
            name = Playing
            value = 2
            text = Playing
            defineToken = PLAYBACKSTATE_PLAYING
         enum
            name = Transitioning
            value = 3
            text = Transitioning
            defineToken = PLAYBACKSTATE_TRANSITIONING
         enum
            name = PlaybackPaused
            value = 4
            text = Paused
            defineToken = PLAYBACKSTATE_PAUSED
         enum
            name = RecordingPaused
            value = 5
            text = Recording Paused
            defineToken = PLAYBACKSTATE_RECORDINGPAUSED
         enum
            name = Recording
            value = 6
            text = Recording
            defineToken = PLAYBACKSTATE_RECORDING
         enum
            name = NoMedia
            value = 7
            text = No Media
            defineToken = PLAYBACKSTATE_NOMEDIA
```

## <a name="remarks"></a><span data-ttu-id="7d3ea-106">備註</span><span class="sxs-lookup"><span data-stu-id="7d3ea-106">Remarks</span></span>

<span data-ttu-id="7d3ea-107">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="7d3ea-107">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d3ea-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="7d3ea-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d3ea-109">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="7d3ea-109">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="7d3ea-110">searchInfo</span><span class="sxs-lookup"><span data-stu-id="7d3ea-110">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="7d3ea-111">labelInfo</span><span class="sxs-lookup"><span data-stu-id="7d3ea-111">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="7d3ea-112">typeInfo</span><span class="sxs-lookup"><span data-stu-id="7d3ea-112">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="7d3ea-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="7d3ea-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="7d3ea-114">stringFormat</span><span class="sxs-lookup"><span data-stu-id="7d3ea-114">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="7d3ea-115">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="7d3ea-115">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="7d3ea-116">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="7d3ea-116">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="7d3ea-117">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="7d3ea-117">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="7d3ea-118">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="7d3ea-118">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="7d3ea-119">drawControl</span><span class="sxs-lookup"><span data-stu-id="7d3ea-119">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="7d3ea-120">editControl</span><span class="sxs-lookup"><span data-stu-id="7d3ea-120">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="7d3ea-121">filterControl</span><span class="sxs-lookup"><span data-stu-id="7d3ea-121">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="7d3ea-122">queryControl</span><span class="sxs-lookup"><span data-stu-id="7d3ea-122">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
