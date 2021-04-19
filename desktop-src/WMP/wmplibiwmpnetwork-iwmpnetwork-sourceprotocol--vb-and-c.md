---
title: IWMPNetwork sourceProtocol 屬性
description: SourceProtocol 屬性會取得用來接收資料的來源通訊協定。
ms.assetid: db1d7651-3f25-4ac9-a3e1-dc3a8ddf8c40
keywords:
- sourceProtocol 屬性 Windows Media Player
- sourceProtocol 屬性 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，sourceProtocol 屬性
topic_type:
- apiref
api_name:
- IWMPNetwork.sourceProtocol
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5017e1a053c124a1f7f50668c6f392eb541d57f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998681"
---
# <a name="iwmpnetworksourceprotocol-property"></a><span data-ttu-id="6f792-106">IWMPNetwork：： sourceProtocol 屬性</span><span class="sxs-lookup"><span data-stu-id="6f792-106">IWMPNetwork::sourceProtocol property</span></span>

<span data-ttu-id="6f792-107">**SourceProtocol** 屬性會取得用來接收資料的來源通訊協定。</span><span class="sxs-lookup"><span data-stu-id="6f792-107">The **sourceProtocol** property gets the source protocol used to receive data.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f792-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f792-108">Syntax</span></span>


```CSharp
public System.String sourceProtocol {get; set;}
```


```VB

Public ReadOnly Property sourceProtocol As System.String
```





## <a name="property-value"></a><span data-ttu-id="6f792-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="6f792-109">Property value</span></span>

<span data-ttu-id="6f792-110">**System.string** ，此為來源通訊協定的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f792-110">A **System.String** that is the name of the source protocol.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f792-111">備註</span><span class="sxs-lookup"><span data-stu-id="6f792-111">Remarks</span></span>

<span data-ttu-id="6f792-112">播放 CD 或 DVD 時，這個屬性會取得零長度的字串 ( "" ) 。</span><span class="sxs-lookup"><span data-stu-id="6f792-112">This property gets a zero-length string ("") when playing a CD or DVD.</span></span>

## <a name="examples"></a><span data-ttu-id="6f792-113">範例</span><span class="sxs-lookup"><span data-stu-id="6f792-113">Examples</span></span>

<span data-ttu-id="6f792-114">下列程式碼範例會使用 **sourceProtocol** 來顯示用來接收資料的來源通訊協定。</span><span class="sxs-lookup"><span data-stu-id="6f792-114">The following code example uses **sourceProtocol** to display the source protocol used to receive data.</span></span> <span data-ttu-id="6f792-115">這項資訊會顯示在標籤中，以回應 **PlayStateChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="6f792-115">The information is displayed in a label, in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="6f792-116">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="6f792-116">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the network source protocol when the player is playing by testing for a 
    // play state enum value of WMPLib.WMPPlayState.wmppsPlaying which equals 3. 
    if (e.newState == 3) 
    {
        sourceProtocolLabel.Text = ("Source protocol: " + player.network.sourceProtocol);
    } 
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    &#39; Display the network source protocol when the player is playing by testing for a 
    &#39; play state enum value of WMPLib.WMPPlayState.wmppsPlaying which equals 3.
    If (e.newState = 3) Then

        sourceProtocolLabel.Text = (&quot;Source protocol: &quot; + player.network.sourceProtocol)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="6f792-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f792-117">Requirements</span></span>



| <span data-ttu-id="6f792-118">需求</span><span class="sxs-lookup"><span data-stu-id="6f792-118">Requirement</span></span> | <span data-ttu-id="6f792-119">值</span><span class="sxs-lookup"><span data-stu-id="6f792-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f792-120">版本</span><span class="sxs-lookup"><span data-stu-id="6f792-120">Version</span></span><br/>   | <span data-ttu-id="6f792-121">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="6f792-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="6f792-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="6f792-122">Namespace</span></span><br/> | <span data-ttu-id="6f792-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="6f792-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6f792-124">組件</span><span class="sxs-lookup"><span data-stu-id="6f792-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6f792-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="6f792-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f792-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f792-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f792-127">**IWMPNetwork 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="6f792-127">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





