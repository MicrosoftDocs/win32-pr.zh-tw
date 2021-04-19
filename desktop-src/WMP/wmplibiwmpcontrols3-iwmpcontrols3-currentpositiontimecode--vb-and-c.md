---
title: IWMPControls3 currentPositionTimecode 屬性
description: CurrentPositionTimecode 屬性會使用時間碼格式，取得或設定目前媒體專案中的目前位置。 這個屬性目前支援 SMPTE 時間代碼。
ms.assetid: 035b812c-e976-4b4e-b4e5-820653257732
keywords:
- currentPositionTimecode 屬性 Windows Media Player
- currentPositionTimecode 屬性 Windows Media Player，IWMPControls3 介面
- IWMPControls3 介面 Windows Media Player，currentPositionTimecode 屬性
topic_type:
- apiref
api_name:
- IWMPControls3.currentPositionTimecode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7660e6dc2690c310cf06f64e38190dc1cb3f24ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000970"
---
# <a name="iwmpcontrols3currentpositiontimecode-property"></a><span data-ttu-id="b085c-107">IWMPControls3：： currentPositionTimecode 屬性</span><span class="sxs-lookup"><span data-stu-id="b085c-107">IWMPControls3::currentPositionTimecode property</span></span>

<span data-ttu-id="b085c-108">**CurrentPositionTimecode** 屬性會使用時間碼格式，取得或設定目前媒體專案中的目前位置。</span><span class="sxs-lookup"><span data-stu-id="b085c-108">The **currentPositionTimecode** property gets or sets the current position in the current media item using a time code format.</span></span> <span data-ttu-id="b085c-109">這個屬性目前支援 SMPTE 時間代碼。</span><span class="sxs-lookup"><span data-stu-id="b085c-109">This property currently supports SMPTE time code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b085c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b085c-110">Syntax</span></span>


```CSharp
public System.String currentPositionTimecode {get; set;}
```


```VB

Public Property currentPositionTimecode As System.String
```





## <a name="property-value"></a><span data-ttu-id="b085c-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="b085c-111">Property value</span></span>

<span data-ttu-id="b085c-112">作為 SMPTE 時間代碼的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="b085c-112">A **System.String** that is the SMPTE time code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b085c-113">備註</span><span class="sxs-lookup"><span data-stu-id="b085c-113">Remarks</span></span>

<span data-ttu-id="b085c-114">SMPTE 時間程式碼提供一種標準方式來識別個別的影片畫面，這對同步播放很有用。</span><span class="sxs-lookup"><span data-stu-id="b085c-114">SMPTE time code provides a standard way of identifying an individual video frame, which is useful for synchronizing playback.</span></span> <span data-ttu-id="b085c-115">如果數位媒體檔案支援 SMPTE 時間代碼，Windows Media Player 可以取出目前時間代碼位置資訊，或搜尋特定時間代碼所識別的影片畫面。</span><span class="sxs-lookup"><span data-stu-id="b085c-115">If a digital media file supports SMPTE time code, Windows Media Player can retrieve the current time code position information or seek to a video frame identified by a particular time code.</span></span>

<span data-ttu-id="b085c-116">SMPTE 時間代碼會依時數、分鐘數、秒數和框架數來識別特定的畫面格，以將其與特定的參考框架（指定為時間0）隔開。</span><span class="sxs-lookup"><span data-stu-id="b085c-116">SMPTE time code identifies a particular frame by the number of hours, minutes, seconds, and frames that separate it from a particular reference frame the frame designated as time zero.</span></span> <span data-ttu-id="b085c-117">通常，時間為零的框架是檔案的開頭，而特定的 SMPTE 時間代碼值代表自檔案開始以來經過的時間。</span><span class="sxs-lookup"><span data-stu-id="b085c-117">Usually the time zero frame is the start of the file and a particular SMPTE time code value represents the elapsed time since the start of the file.</span></span>

<span data-ttu-id="b085c-118">時間碼的格式 \[ *範圍* 為 \] *hh*：*mm*：*ss*。*ff* 的 \[ *範圍* \] 代表範圍，hh 代表小時， *mm* 代表分鐘， *ss* 代表秒，而 *ff* 代表畫面格。</span><span class="sxs-lookup"><span data-stu-id="b085c-118">The time code is in the format \[*range*\]*hh*:*mm*:*ss*.*ff* where \[*range*\] represents the range, hh represents hours, *mm* represents minutes, *ss* represents seconds, and *ff* represents frames.</span></span> <span data-ttu-id="b085c-119">設定 **currentPositionTimecode** 的值時，您必須包含全部八位數，並使用零做為預留位置。</span><span class="sxs-lookup"><span data-stu-id="b085c-119">When setting a value for **currentPositionTimecode**, you must include all eight digits, using zeros as placeholders.</span></span>

<span data-ttu-id="b085c-120">\[*範圍* \]對應至 Windows Media Format **WMT 時間 \_ 碼 \_ 延伸模組 \_ 資料** 結構的 **wRange** 成員。</span><span class="sxs-lookup"><span data-stu-id="b085c-120">\[*range*\] corresponds to the **wRange** member of the Windows Media Format **WMT\_TIMECODE\_EXTENSION\_DATA** structure.</span></span> <span data-ttu-id="b085c-121">如需時間碼範圍的詳細資訊，請參閱 Windows Media Format SDK。</span><span class="sxs-lookup"><span data-stu-id="b085c-121">For more information about time code ranges, see the Windows Media Format SDK.</span></span>

<span data-ttu-id="b085c-122">只有包含 SMPTE 時間程式碼資訊的檔案才支援設定和取得 **currentPositionTimecode** 。</span><span class="sxs-lookup"><span data-stu-id="b085c-122">Setting and getting **currentPositionTimecode** is supported only for files that contain SMPTE time code information.</span></span>

## <a name="examples"></a><span data-ttu-id="b085c-123">範例</span><span class="sxs-lookup"><span data-stu-id="b085c-123">Examples</span></span>

<span data-ttu-id="b085c-124">下列程式碼範例會將 **currentPositionTimecode** 指定為1小時、零分鐘、30秒和5個框架。</span><span class="sxs-lookup"><span data-stu-id="b085c-124">The following code example specifies **currentPositionTimecode** as 1 hour, zero minutes, 30 seconds, and 5 frames.</span></span> <span data-ttu-id="b085c-125">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="b085c-125">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Cast the interface returned by player.Ctlcontrols to an IWMPControls3 interface
// so that you can use the currentPositionTimecode property.
WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

// Seek to a frame using SMPTE time code.
controls.currentPositionTimecode = "[00000]01:00:30.05";
```


```VB

' Cast the interface returned by player.Ctlcontrols to an IWMPControls3 interface
&#39; so that you can use the currentPositionTimecode property.
Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

&#39; Seek to a frame using SMPTE time code.
Controls.currentPositionTimecode = &quot;[00000]01:00:30.05&quot;
```





## <a name="requirements"></a><span data-ttu-id="b085c-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="b085c-126">Requirements</span></span>



| <span data-ttu-id="b085c-127">需求</span><span class="sxs-lookup"><span data-stu-id="b085c-127">Requirement</span></span> | <span data-ttu-id="b085c-128">值</span><span class="sxs-lookup"><span data-stu-id="b085c-128">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b085c-129">版本</span><span class="sxs-lookup"><span data-stu-id="b085c-129">Version</span></span><br/>   | <span data-ttu-id="b085c-130">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="b085c-130">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b085c-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="b085c-131">Namespace</span></span><br/> | <span data-ttu-id="b085c-132">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b085c-132">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b085c-133">組件</span><span class="sxs-lookup"><span data-stu-id="b085c-133">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b085c-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="b085c-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b085c-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b085c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b085c-136">**IWMPControls3 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b085c-136">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





