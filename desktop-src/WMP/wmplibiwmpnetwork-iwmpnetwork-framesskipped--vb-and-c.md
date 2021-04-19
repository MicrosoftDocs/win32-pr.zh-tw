---
title: IWMPNetwork framesSkipped 屬性
description: FramesSkipped 屬性會取得播放期間略過的總畫面數。
ms.assetid: eedecfa9-0c82-4800-979e-ca85fb78c480
keywords:
- framesSkipped 屬性 Windows Media Player
- framesSkipped 屬性 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，framesSkipped 屬性
topic_type:
- apiref
api_name:
- IWMPNetwork.framesSkipped
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8409cec50089111184f96e4463f57cc9c4fbae07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993501"
---
# <a name="iwmpnetworkframesskipped-property"></a><span data-ttu-id="beb96-106">IWMPNetwork：： framesSkipped 屬性</span><span class="sxs-lookup"><span data-stu-id="beb96-106">IWMPNetwork::framesSkipped property</span></span>

<span data-ttu-id="beb96-107">**FramesSkipped** 屬性會取得播放期間略過的總畫面數。</span><span class="sxs-lookup"><span data-stu-id="beb96-107">The **framesSkipped** property gets the total number of frames skipped during playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="beb96-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="beb96-108">Syntax</span></span>


```CSharp
public System.Int32 framesSkipped {get; set;}
```


```VB

Public ReadOnly Property framesSkipped As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="beb96-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="beb96-109">Property value</span></span>

<span data-ttu-id="beb96-110">已略過的框架數目的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="beb96-110">A **System.Int32** that is the number of frames skipped.</span></span>

## <a name="examples"></a><span data-ttu-id="beb96-111">範例</span><span class="sxs-lookup"><span data-stu-id="beb96-111">Examples</span></span>

<span data-ttu-id="beb96-112">下列程式碼範例會使用 **framesSkipped** 來顯示播放期間跳過的總畫面格數。</span><span class="sxs-lookup"><span data-stu-id="beb96-112">The following code example uses **framesSkipped** to display the total number of frames skipped during playback.</span></span> <span data-ttu-id="beb96-113">當使用者按一下按鈕時，此資訊就會顯示在標籤中。</span><span class="sxs-lookup"><span data-stu-id="beb96-113">The information is displayed in a label when the user clicks a button.</span></span> <span data-ttu-id="beb96-114">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="beb96-114">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void showFramesSkipped_Click(object sender, System.EventArgs e)
{
    framesSkippedLabel.Text = ("Frames skipped: " + player.network.framesSkipped.ToString());
}
```


```VB

Public Sub showFramesSkipped_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showFramesSkipped.Click

    framesSkippedLabel.Text = (&quot;Frames skipped: &quot; + player.network.framesSkipped.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="beb96-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="beb96-115">Requirements</span></span>



| <span data-ttu-id="beb96-116">需求</span><span class="sxs-lookup"><span data-stu-id="beb96-116">Requirement</span></span> | <span data-ttu-id="beb96-117">值</span><span class="sxs-lookup"><span data-stu-id="beb96-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="beb96-118">版本</span><span class="sxs-lookup"><span data-stu-id="beb96-118">Version</span></span><br/>   | <span data-ttu-id="beb96-119">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="beb96-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="beb96-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="beb96-120">Namespace</span></span><br/> | <span data-ttu-id="beb96-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="beb96-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="beb96-122">組件</span><span class="sxs-lookup"><span data-stu-id="beb96-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="beb96-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="beb96-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="beb96-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="beb96-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beb96-125">**IWMPNetwork 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="beb96-125">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





