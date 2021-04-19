---
title: IWMPNetwork lostPackets 屬性
description: LostPackets 屬性會取得遺失的封包數目。
ms.assetid: 611218d3-c4d3-4d4e-835c-1e7a956b2718
keywords:
- lostPackets 屬性 Windows Media Player
- lostPackets 屬性 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，lostPackets 屬性
topic_type:
- apiref
api_name:
- IWMPNetwork.lostPackets
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd1adac5f4aa8b1f58c023a556af04b8eae4bd8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998887"
---
# <a name="iwmpnetworklostpackets-property"></a><span data-ttu-id="62204-106">IWMPNetwork：： lostPackets 屬性</span><span class="sxs-lookup"><span data-stu-id="62204-106">IWMPNetwork::lostPackets property</span></span>

<span data-ttu-id="62204-107">**LostPackets** 屬性會取得遺失的封包數目。</span><span class="sxs-lookup"><span data-stu-id="62204-107">The **lostPackets** property gets the number of packets lost.</span></span>

## <a name="syntax"></a><span data-ttu-id="62204-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="62204-108">Syntax</span></span>


```CSharp
public System.Int32 lostPackets {get; set;}
```


```VB

Public ReadOnly Property lostPackets As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="62204-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="62204-109">Property value</span></span>

<span data-ttu-id="62204-110">會遺失封包數的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="62204-110">A **System.Int32** that is the number of lost packets.</span></span>

## <a name="remarks"></a><span data-ttu-id="62204-111">備註</span><span class="sxs-lookup"><span data-stu-id="62204-111">Remarks</span></span>

<span data-ttu-id="62204-112">這個屬性只包含串流媒體封包，而且在使用 HTTP 通訊協定時，會傳回零，而這是不失真的。</span><span class="sxs-lookup"><span data-stu-id="62204-112">This property includes streaming media packets only, and will return zero when using the HTTP protocol, which is lossless.</span></span>

<span data-ttu-id="62204-113">封包可能因為許多原因而遺失，例如網路連線的類型和品質。</span><span class="sxs-lookup"><span data-stu-id="62204-113">Packets can be lost for a number of reasons, such as the type and quality of the network connection.</span></span>

<span data-ttu-id="62204-114">每次播放都會停止並重新啟動，這個屬性會重設為零。</span><span class="sxs-lookup"><span data-stu-id="62204-114">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="62204-115">如果播放暫停，則不會重設此值。</span><span class="sxs-lookup"><span data-stu-id="62204-115">The value is not reset if playback is paused.</span></span> <span data-ttu-id="62204-116">這個屬性只會在執行時間使用 **AxWindowsMediaPlayer** url 屬性來設定播放的 URL 時，才會取得有效的資訊。</span><span class="sxs-lookup"><span data-stu-id="62204-116">This property gets valid information only during run time when the URL for playback is set by using the **AxWindowsMediaPlayer.URL** property.</span></span>

## <a name="examples"></a><span data-ttu-id="62204-117">範例</span><span class="sxs-lookup"><span data-stu-id="62204-117">Examples</span></span>

<span data-ttu-id="62204-118">下列程式碼範例使用 **lostPackets** 來顯示播放期間遺失的封包總數。</span><span class="sxs-lookup"><span data-stu-id="62204-118">The following code example uses **lostPackets** to display the total number of packets lost during playback.</span></span> <span data-ttu-id="62204-119">當使用者按一下按鈕時，此資訊就會顯示在標籤中。</span><span class="sxs-lookup"><span data-stu-id="62204-119">The information is displayed in a label when the user clicks a button.</span></span> <span data-ttu-id="62204-120">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="62204-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void showLostPackets_Click(object sender, System.EventArgs e)
{
    lostPacketsLabel.Text = ("Packets lost: " + player.network.lostPackets.ToString());
}
```


```VB

Public Sub showLostPackets_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showLostPackets.Click

    lostPacketsLabel.Text = (&quot;Packets lost: &quot; + player.network.lostPackets.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="62204-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="62204-121">Requirements</span></span>



| <span data-ttu-id="62204-122">需求</span><span class="sxs-lookup"><span data-stu-id="62204-122">Requirement</span></span> | <span data-ttu-id="62204-123">值</span><span class="sxs-lookup"><span data-stu-id="62204-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62204-124">版本</span><span class="sxs-lookup"><span data-stu-id="62204-124">Version</span></span><br/>   | <span data-ttu-id="62204-125">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="62204-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="62204-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="62204-126">Namespace</span></span><br/> | <span data-ttu-id="62204-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="62204-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="62204-128">組件</span><span class="sxs-lookup"><span data-stu-id="62204-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="62204-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="62204-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62204-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62204-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62204-131">**IWMPNetwork 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="62204-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="62204-132">**AxWindowsMediaPlayer (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="62204-132">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> </dl>

 

 





