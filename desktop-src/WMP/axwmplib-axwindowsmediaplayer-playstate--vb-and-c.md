---
title: AxWindowsMediaPlayer. playState 屬性
description: PlayState 屬性會取得列舉值，指出 Windows Media Player 作業的狀態。
ms.assetid: ab9f1547-5c28-4289-beaf-9262f7f59b07
keywords:
- playState 屬性 Windows Media Player
- playState 屬性 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，playState 屬性
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.playState
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d397c65c1cfd7f4adb040cc94e208a66c6c42d1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001175"
---
# <a name="axwindowsmediaplayerplaystate-property"></a><span data-ttu-id="4b412-106">AxWindowsMediaPlayer. playState 屬性</span><span class="sxs-lookup"><span data-stu-id="4b412-106">AxWindowsMediaPlayer.playState property</span></span>

<span data-ttu-id="4b412-107">PlayState 屬性會取得列舉值，指出 Windows Media Player 作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="4b412-107">The playState property gets an enumeration value indicating the state of the Windows Media Player operation.</span></span>

<span data-ttu-id="4b412-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="4b412-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b412-109">語法</span><span class="sxs-lookup"><span data-stu-id="4b412-109">Syntax</span></span>


```CSharp
public WMPPlayState playState {get;}
```


```VB

Public ReadOnly Property playState As WMPPlayState
```





## <a name="property-value"></a><span data-ttu-id="4b412-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="4b412-110">Property value</span></span>

<span data-ttu-id="4b412-111">WMPLib. WMPPlayState 列舉值。</span><span class="sxs-lookup"><span data-stu-id="4b412-111">The WMPLib.WMPPlayState enumeration value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b412-112">備註</span><span class="sxs-lookup"><span data-stu-id="4b412-112">Remarks</span></span>

<span data-ttu-id="4b412-113">Windows Media Player 狀態不保證會以任何特定順序發生。</span><span class="sxs-lookup"><span data-stu-id="4b412-113">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="4b412-114">此外，並非每個狀態都一定會在一連串的事件期間發生。</span><span class="sxs-lookup"><span data-stu-id="4b412-114">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="4b412-115">您不應該撰寫依賴狀態順序的程式碼。</span><span class="sxs-lookup"><span data-stu-id="4b412-115">You should not write code that relies upon state order.</span></span>

## <a name="examples"></a><span data-ttu-id="4b412-116">範例</span><span class="sxs-lookup"><span data-stu-id="4b412-116">Examples</span></span>

<span data-ttu-id="4b412-117">下列範例會使用 playState 屬性，在標籤中顯示播放程式目前的播放狀態。</span><span class="sxs-lookup"><span data-stu-id="4b412-117">The following example uses the playState property to display the current playing status of the player in a label.</span></span> <span data-ttu-id="4b412-118">AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="4b412-118">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Test whether Windows Media Player is in the playing state. 
if (player.playState == WMPLib.WMPPlayState.wmppsPlaying)
{
    playStateLabel.Text = "Windows Media Player is playing!";
}
else
{
    playStateLabel.Text = "Windows Media Player is NOT playing!";
}
```


```VB

' Test whether Windows Media Player is in the playing state. 
If (player.playState = WMPLib.WMPPlayState.wmppsPlaying) Then

    playStateLabel.Text = &quot;Windows Media Player is playing!&quot;

Else

    playStateLabel.Text = &quot;Windows Media Player is NOT playing!&quot;

End If
```





## <a name="requirements"></a><span data-ttu-id="4b412-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b412-119">Requirements</span></span>



| <span data-ttu-id="4b412-120">需求</span><span class="sxs-lookup"><span data-stu-id="4b412-120">Requirement</span></span> | <span data-ttu-id="4b412-121">值</span><span class="sxs-lookup"><span data-stu-id="4b412-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b412-122">版本</span><span class="sxs-lookup"><span data-stu-id="4b412-122">Version</span></span><br/>   | <span data-ttu-id="4b412-123">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="4b412-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="4b412-124">命名空間</span><span class="sxs-lookup"><span data-stu-id="4b412-124">Namespace</span></span><br/> | <span data-ttu-id="4b412-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="4b412-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="4b412-126">組件</span><span class="sxs-lookup"><span data-stu-id="4b412-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4b412-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="4b412-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b412-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4b412-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b412-129">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="4b412-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4b412-130">**AxWindowsMediaPlayer PlayStateChange 事件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="4b412-130">**AxWindowsMediaPlayer.PlayStateChange Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playstatechange.md)
</dt> <dt>

[<span data-ttu-id="4b412-131">**WMPPlayState**</span><span class="sxs-lookup"><span data-stu-id="4b412-131">**WMPPlayState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaystate)
</dt> </dl>

 

 





