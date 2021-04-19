---
title: IWMPNetwork bufferingCount 屬性
description: BufferingCount 屬性會取得在播放期間發生緩衝處理的次數。
ms.assetid: 2e3a2914-fc38-4477-8c4c-15b4a2e424dc
keywords:
- bufferingCount 屬性 Windows Media Player
- bufferingCount 屬性 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，bufferingCount 屬性
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4958892dd9784ee72b51adfedbbcdee81817b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994205"
---
# <a name="iwmpnetworkbufferingcount-property"></a><span data-ttu-id="41e81-106">IWMPNetwork：： bufferingCount 屬性</span><span class="sxs-lookup"><span data-stu-id="41e81-106">IWMPNetwork::bufferingCount property</span></span>

<span data-ttu-id="41e81-107">**BufferingCount** 屬性會取得在播放期間發生緩衝處理的次數。</span><span class="sxs-lookup"><span data-stu-id="41e81-107">The **bufferingCount** property gets the number of times buffering occurred during playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="41e81-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="41e81-108">Syntax</span></span>


```CSharp
public System.Int32 bufferingCount {get; set;}
```


```VB

Public ReadOnly Property bufferingCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="41e81-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="41e81-109">Property value</span></span>

<span data-ttu-id="41e81-110">為緩衝計數的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="41e81-110">A **System.Int32** that is the buffering count.</span></span>

## <a name="remarks"></a><span data-ttu-id="41e81-111">備註</span><span class="sxs-lookup"><span data-stu-id="41e81-111">Remarks</span></span>

<span data-ttu-id="41e81-112">每次播放都會停止並重新啟動，這個屬性會重設為零。</span><span class="sxs-lookup"><span data-stu-id="41e81-112">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="41e81-113">如果播放暫停，則不會重設。</span><span class="sxs-lookup"><span data-stu-id="41e81-113">It is not reset if playback is paused.</span></span>

<span data-ttu-id="41e81-114">緩衝處理只適用于串流內容。</span><span class="sxs-lookup"><span data-stu-id="41e81-114">Buffering applies only to streaming content.</span></span> <span data-ttu-id="41e81-115">這個屬性只會在執行時間使用 **AxWindowsMediaPlayer** url 屬性來設定播放的 URL 時，才會取得有效的資訊。</span><span class="sxs-lookup"><span data-stu-id="41e81-115">This property gets valid information only during run time when the URL for playback is set by using the **AxWindowsMediaPlayer.URL** property.</span></span>

## <a name="examples"></a><span data-ttu-id="41e81-116">範例</span><span class="sxs-lookup"><span data-stu-id="41e81-116">Examples</span></span>

<span data-ttu-id="41e81-117">下列範例會使用 *bufferingCount* 來顯示播放期間緩衝處理的次數。</span><span class="sxs-lookup"><span data-stu-id="41e81-117">The following example uses *bufferingCount* to display the number of times buffering occurs during playback.</span></span> <span data-ttu-id="41e81-118">這項資訊會顯示在標籤中，以回應緩衝事件。</span><span class="sxs-lookup"><span data-stu-id="41e81-118">The information is displayed in a label in response to the Buffering Event.</span></span> <span data-ttu-id="41e81-119">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="41e81-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the Buffering event.
player.Buffering += new AxWMPLib._WMPOCXEvents_BufferingEventHandler(player_Buffering);

// Create an event handler for the Buffering event.
private void player_Buffering(object sender, AxWMPLib._WMPOCXEvents_BufferingEvent e)
{
    // Display the bufferingCount when buffering has started.
    if (e.start == true)
    {
        bufferingCountLabel.Text = ("Buffering count: " + player.network.bufferingCount);
    }  
}
```


```VB

' Create an event handler for the Buffering event.
Public Sub player_Buffering(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_BufferingEvent) Handles player.Buffering

    &#39; Display the bufferingCount when buffering has started.
    If (e.start = True) Then

        bufferingCountLabel.Text = (&quot;Buffering count: &quot; + player.network.bufferingCount)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="41e81-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="41e81-120">Requirements</span></span>



| <span data-ttu-id="41e81-121">需求</span><span class="sxs-lookup"><span data-stu-id="41e81-121">Requirement</span></span> | <span data-ttu-id="41e81-122">值</span><span class="sxs-lookup"><span data-stu-id="41e81-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41e81-123">版本</span><span class="sxs-lookup"><span data-stu-id="41e81-123">Version</span></span><br/>   | <span data-ttu-id="41e81-124">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="41e81-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="41e81-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="41e81-125">Namespace</span></span><br/> | <span data-ttu-id="41e81-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="41e81-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="41e81-127">組件</span><span class="sxs-lookup"><span data-stu-id="41e81-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="41e81-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="41e81-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41e81-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41e81-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41e81-130">**AxWindowsMediaPlayer (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="41e81-130">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="41e81-131">**IWMPNetwork 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="41e81-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





