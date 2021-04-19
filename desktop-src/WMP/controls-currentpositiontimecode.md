---
title: CurrentPositionTimecode
description: CurrentPositionTimecode 屬性會使用時間碼格式來指定或抓取目前媒體專案中的目前位置。 這個屬性目前支援 SMPTE 時間代碼。
ms.assetid: 98d79756-c6cf-4dbc-936a-58229452451c
keywords:
- CurrentPositionTimecode Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentPositionTimecode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e2a4ddeb0849a829ff7a16fd80ff4891cfe56c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985976"
---
# <a name="controlscurrentpositiontimecode"></a><span data-ttu-id="b3a76-105">CurrentPositionTimecode</span><span class="sxs-lookup"><span data-stu-id="b3a76-105">Controls.currentPositionTimecode</span></span>

<span data-ttu-id="b3a76-106">**CurrentPositionTimecode** 屬性會使用時間碼格式來指定或抓取目前媒體專案中的目前位置。</span><span class="sxs-lookup"><span data-stu-id="b3a76-106">The **currentPositionTimecode** property specifies or retrieves the current position in the current media item using a time code format.</span></span> <span data-ttu-id="b3a76-107">這個屬性目前支援 SMPTE 時間代碼。</span><span class="sxs-lookup"><span data-stu-id="b3a76-107">This property currently supports SMPTE time code.</span></span>

``` syntax
player.controls.currentPositionTimecode
      
```

## <a name="possible-values"></a><span data-ttu-id="b3a76-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="b3a76-108">Possible Values</span></span>

<span data-ttu-id="b3a76-109">這個屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="b3a76-109">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3a76-110">備註</span><span class="sxs-lookup"><span data-stu-id="b3a76-110">Remarks</span></span>

<span data-ttu-id="b3a76-111">SMPTE 時間程式碼提供一種標準方式來識別個別的影片畫面，這對同步播放很有用。</span><span class="sxs-lookup"><span data-stu-id="b3a76-111">SMPTE time code provides a standard way of identifying an individual video frame, which is useful for synchronizing playback.</span></span> <span data-ttu-id="b3a76-112">如果數位媒體檔案支援 SMPTE 時間代碼，Windows Media Player 可以取出目前時間代碼位置資訊，或搜尋特定時間碼 **字串** 所識別的影片畫面。</span><span class="sxs-lookup"><span data-stu-id="b3a76-112">If a digital media file supports SMPTE time code, Windows Media Player can retrieve the current time code position information or seek to a video frame identified by a particular time code **String**.</span></span>

<span data-ttu-id="b3a76-113">SMPTE 時間代碼會依時數、分鐘數、秒數和框架數來識別特定的畫面格，以將其與特定的參考框架（指定為時間0）隔開。</span><span class="sxs-lookup"><span data-stu-id="b3a76-113">SMPTE time code identifies a particular frame by the number of hours, minutes, seconds, and frames that separate it from a particular reference frame the frame designated as time zero.</span></span> <span data-ttu-id="b3a76-114">通常，時間為零的框架是檔案的開頭，而特定的 SMPTE 時間代碼值代表自檔案開始以來經過的時間。</span><span class="sxs-lookup"><span data-stu-id="b3a76-114">Usually the time zero frame is the start of the file and a particular SMPTE time code value represents the elapsed time since the start of the file.</span></span>

<span data-ttu-id="b3a76-115">時間代碼 **字串** 的格式 \[ *範圍* 為 \] *hh*：*mm*：*ss*。*ff* 的 \[ *範圍* \] 代表範圍， *hh* 代表小時， *mm* 代表分鐘， *ss* 代表秒，而 *ff* 代表畫面格。</span><span class="sxs-lookup"><span data-stu-id="b3a76-115">The time code **String** is in the format \[*range*\]*hh*:*mm*:*ss*.*ff* where \[*range*\] represents the range, *hh* represents hours, *mm* represents minutes, *ss* represents seconds, and *ff* represents frames.</span></span> <span data-ttu-id="b3a76-116">使用 **currentPositionTimecode** 指定值時，您必須使用零做為預留位置來包含全部八位數。</span><span class="sxs-lookup"><span data-stu-id="b3a76-116">When specifying a value using **currentPositionTimecode**, you must include all eight digits using zeros as placeholders.</span></span>

<span data-ttu-id="b3a76-117">\[*範圍* \] 規範會對應至 Windows Media Format **WMT 時間 \_ 碼 \_ 延伸模組 \_ 資料** 結構的 **wRange** 成員。</span><span class="sxs-lookup"><span data-stu-id="b3a76-117">The \[*range*\] specifier corresponds to the **wRange** member of the Windows Media Format **WMT\_TIMECODE\_EXTENSION\_DATA** structure.</span></span> <span data-ttu-id="b3a76-118">如需時間碼範圍的詳細資訊，請參閱 Windows Media Format SDK。</span><span class="sxs-lookup"><span data-stu-id="b3a76-118">For more information about time code ranges, see the Windows Media Format SDK.</span></span>

<span data-ttu-id="b3a76-119">只有包含 SMPTE 時間程式碼資訊的檔案才支援指定和取出 **currentPositionTimecode** 。</span><span class="sxs-lookup"><span data-stu-id="b3a76-119">Specifying and retrieving **currentPositionTimecode** is only supported for files that contain SMPTE time code information.</span></span>

## <a name="examples"></a><span data-ttu-id="b3a76-120">範例</span><span class="sxs-lookup"><span data-stu-id="b3a76-120">Examples</span></span>

<span data-ttu-id="b3a76-121">下列程式碼範例會將 **currentPositionTimecode** 指定為1小時、零分鐘、30秒和5個框架。</span><span class="sxs-lookup"><span data-stu-id="b3a76-121">The following code example specifies **currentPositionTimecode** as 1 hour, zero minutes, 30 seconds, and 5 frames.</span></span> <span data-ttu-id="b3a76-122">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="b3a76-122">The **Player** object was created with ID = "Player".</span></span>


```
// Seek to a frame using SMPTE time code.
Player.controls.currentPositionTimecode = "[00000]01:00:30.05";

```



## <a name="requirements"></a><span data-ttu-id="b3a76-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3a76-123">Requirements</span></span>



| <span data-ttu-id="b3a76-124">需求</span><span class="sxs-lookup"><span data-stu-id="b3a76-124">Requirement</span></span> | <span data-ttu-id="b3a76-125">值</span><span class="sxs-lookup"><span data-stu-id="b3a76-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b3a76-126">版本</span><span class="sxs-lookup"><span data-stu-id="b3a76-126">Version</span></span><br/> | <span data-ttu-id="b3a76-127">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="b3a76-127">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="b3a76-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b3a76-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="b3a76-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3a76-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3a76-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3a76-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3a76-131">**Controls 物件**</span><span class="sxs-lookup"><span data-stu-id="b3a76-131">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





