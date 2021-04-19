---
title: IWMPMedia duration 屬性
description: Duration 屬性會取得目前媒體專案的持續時間（以秒為單位）。
ms.assetid: f8a0bf3e-eeaf-46f5-90c8-d3b11ce4eb39
keywords:
- duration 屬性 Windows Media Player
- duration 屬性 Windows Media Player，IWMPMedia 介面
- IWMPMedia 介面 Windows Media Player，duration 屬性
topic_type:
- apiref
api_name:
- IWMPMedia.duration
- IWMPMedia.get_duration
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f796cab042713082ce2066659f62736855e62787
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996269"
---
# <a name="iwmpmediaduration-property"></a><span data-ttu-id="e093e-106">IWMPMedia：:d uration 屬性</span><span class="sxs-lookup"><span data-stu-id="e093e-106">IWMPMedia::duration property</span></span>

<span data-ttu-id="e093e-107">**Duration** 屬性會取得目前媒體專案的持續時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e093e-107">The **duration** property gets the duration in seconds of the current media item.</span></span>

<span data-ttu-id="e093e-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e093e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e093e-109">語法</span><span class="sxs-lookup"><span data-stu-id="e093e-109">Syntax</span></span>


```CSharp
public System.Double duration {get;}
```


```VB

Public ReadOnly Property duration As System.Double
```





## <a name="property-value"></a><span data-ttu-id="e093e-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="e093e-110">Property value</span></span>

<span data-ttu-id="e093e-111">以秒為間隔的 **Double** 。</span><span class="sxs-lookup"><span data-stu-id="e093e-111">A **System.Double** that is the duration in seconds.</span></span>

## <a name="remarks"></a><span data-ttu-id="e093e-112">備註</span><span class="sxs-lookup"><span data-stu-id="e093e-112">Remarks</span></span>

<span data-ttu-id="e093e-113">如果這個屬性與 AxWindowsMediaPlayer. currentMedia 中所指定的媒體專案不同，它可能不包含有效的值。</span><span class="sxs-lookup"><span data-stu-id="e093e-113">If this property is used with a media item other than the one specified in AxWindowsMediaPlayer.currentMedia, it may not contain a valid value.</span></span>

<span data-ttu-id="e093e-114">若要取得不在使用者程式庫中的檔案持續時間，您必須等候 Windows Media Player 開啟檔案;亦即，目前的 **OpenState** 必須等於 **MediaOpen**。</span><span class="sxs-lookup"><span data-stu-id="e093e-114">To retrieve the duration for files that are not in the user's library, you must wait for Windows Media Player to open the file; that is, the current **OpenState** must equal **MediaOpen**.</span></span> <span data-ttu-id="e093e-115">您可以藉由處理 AxWindowsMediaPlayer 來確認這一點 **。 \_WMPOCXEvents \_ OpenStateChange** 事件，或定期檢查 **AxWindowsMediaPlayer. openState** 的值。</span><span class="sxs-lookup"><span data-stu-id="e093e-115">You can verify this by handling the **AxWindowsMediaPlayer.\_WMPOCXEvents\_OpenStateChange** event or by periodically checking the value of **AxWindowsMediaPlayer.openState**.</span></span>

<span data-ttu-id="e093e-116">若為播放清單，當個別媒體專案開啟時，可以抓取每個媒體專案的持續時間，而不是開啟播放清單時的。</span><span class="sxs-lookup"><span data-stu-id="e093e-116">For playlists, the duration of each media item can be retrieved when the individual media item is opened, rather than the when the playlist is opened.</span></span>

<span data-ttu-id="e093e-117">使用這個屬性之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="e093e-117">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="e093e-118">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="e093e-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e093e-119">範例</span><span class="sxs-lookup"><span data-stu-id="e093e-119">Examples</span></span>

<span data-ttu-id="e093e-120">下列範例會使用 **持續時間** ，在標籤中顯示目前媒體專案的剩餘時間。</span><span class="sxs-lookup"><span data-stu-id="e093e-120">The following example uses **duration** to display the time remaining in the current media item in a label.</span></span> <span data-ttu-id="e093e-121">計時器會每秒更新標籤中的文字。</span><span class="sxs-lookup"><span data-stu-id="e093e-121">A timer updates the text in the label every second.</span></span>


```CSharp
// Set the timer to fire an event every second and start the timer.
timer.Interval = 1000;
timer.Start();

// Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
// determine when to start and stop the timer. 

private void TimerEventProcessor(object sender, System.EventArgs e)
{
    // Subtract the current position from the duration of the current media to get
    // the time remaining. Use the Math.floor method to round the result down to the
    // nearest whole number.
    double t = Math.Floor(player.currentMedia.duration - player.Ctlcontrols.currentPosition);

    // Display the time remaining in the current media.
    timeRemaining.Text = ("Seconds remaining: " + t.ToString());        
}
```


```VB

' Set the timer to fire an event every second and start the timer.
Timer.Interval = 1000
Timer.Start()

&#39; Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a Select Case statement to
&#39; determine when to start and stop the timer. 

Public Sub TimerEventProcessor(ByVal sender As Object, ByVal e As System.EventArgs) Handles Timer.Tick

    &#39; Subtract the current position from the duration of the current media to get
    &#39; the time remaining. Use the Math.Floor method to round the result down to the
    &#39; nearest whole number.
    Dim t As Double = Math.Floor(player.currentMedia.duration - player.Ctlcontrols.currentPosition)

    &#39; Display the time remaining in the current media.
    timeRemaining.Text = (&quot;Seconds remaining: &quot; + t.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="e093e-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="e093e-122">Requirements</span></span>



| <span data-ttu-id="e093e-123">需求</span><span class="sxs-lookup"><span data-stu-id="e093e-123">Requirement</span></span> | <span data-ttu-id="e093e-124">值</span><span class="sxs-lookup"><span data-stu-id="e093e-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e093e-125">版本</span><span class="sxs-lookup"><span data-stu-id="e093e-125">Version</span></span><br/>   | <span data-ttu-id="e093e-126">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="e093e-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e093e-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="e093e-127">Namespace</span></span><br/> | <span data-ttu-id="e093e-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e093e-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e093e-129">組件</span><span class="sxs-lookup"><span data-stu-id="e093e-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e093e-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="e093e-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e093e-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e093e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e093e-132">**AxWindowsMediaPlayer. currentMedia (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="e093e-132">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e093e-133">**AxWindowsMediaPlayer. openState (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="e093e-133">**AxWindowsMediaPlayer.openState (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e093e-134">**AxWindowsMediaPlayer OpenStateChange 事件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="e093e-134">**AxWindowsMediaPlayer.OpenStateChange Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[<span data-ttu-id="e093e-135">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="e093e-135">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e093e-136">**IWMPMedia. durationString (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="e093e-136">**IWMPMedia.durationString (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)
</dt> </dl>

 

 





