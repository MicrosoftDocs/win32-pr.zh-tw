---
title: IWMPControls currentPosition 屬性
description: CurrentPosition 屬性會從開頭取得或設定媒體專案中的目前位置（以秒為單位）。
ms.assetid: 48f5241e-7528-485e-bf47-d655ba842af2
keywords:
- currentPosition 屬性 Windows Media Player
- currentPosition 屬性 Windows Media Player，IWMPControls 介面
- IWMPControls 介面 Windows Media Player，currentPosition 屬性
topic_type:
- apiref
api_name:
- IWMPControls.currentPosition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fee8c2c8244d6034069f21033978ce2883ff852d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987941"
---
# <a name="iwmpcontrolscurrentposition-property"></a><span data-ttu-id="810a5-106">IWMPControls：： currentPosition 屬性</span><span class="sxs-lookup"><span data-stu-id="810a5-106">IWMPControls::currentPosition property</span></span>

<span data-ttu-id="810a5-107">**CurrentPosition** 屬性會從開頭取得或設定媒體專案中的目前位置（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="810a5-107">The **currentPosition** property gets or sets the current position in the media item in seconds from the beginning.</span></span>

## <a name="syntax"></a><span data-ttu-id="810a5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="810a5-108">Syntax</span></span>


```CSharp
public System.Double currentPosition {get; set;}
```


```VB

Public Property currentPosition As System.Double
```





## <a name="property-value"></a><span data-ttu-id="810a5-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="810a5-109">Property value</span></span>

<span data-ttu-id="810a5-110">目前位置的 **雙精度浮點數** 。</span><span class="sxs-lookup"><span data-stu-id="810a5-110">A **System.Double** that is the current position.</span></span>

## <a name="examples"></a><span data-ttu-id="810a5-111">範例</span><span class="sxs-lookup"><span data-stu-id="810a5-111">Examples</span></span>

<span data-ttu-id="810a5-112">下列範例會使用 **currentPosition** 來搜尋使用者提供的位置。</span><span class="sxs-lookup"><span data-stu-id="810a5-112">The following example uses **currentPosition** to seek to a position provided by the user.</span></span> <span data-ttu-id="810a5-113">為了回應按鈕的點擊， **currentPosition** 會設為在名為 newPosition 的文字方塊中輸入的值。</span><span class="sxs-lookup"><span data-stu-id="810a5-113">In response to a button click, **currentPosition** is set to the value entered in a text box called newPosition.</span></span> <span data-ttu-id="810a5-114">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="810a5-114">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setPosition_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Set the current position of the media item to the position entered by the user.
    player.Ctlcontrols.currentPosition = Convert.ToDouble(newPosition.Text);
}
```


```VB

Public Sub setPosition_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setPosition.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Set the current position of the media item to the position entered by the user.
    player.Ctlcontrols.currentPosition = Convert.ToDouble(newPosition.Text)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="810a5-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="810a5-115">Requirements</span></span>



| <span data-ttu-id="810a5-116">需求</span><span class="sxs-lookup"><span data-stu-id="810a5-116">Requirement</span></span> | <span data-ttu-id="810a5-117">值</span><span class="sxs-lookup"><span data-stu-id="810a5-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="810a5-118">版本</span><span class="sxs-lookup"><span data-stu-id="810a5-118">Version</span></span><br/>   | <span data-ttu-id="810a5-119">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="810a5-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="810a5-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="810a5-120">Namespace</span></span><br/> | <span data-ttu-id="810a5-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="810a5-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="810a5-122">組件</span><span class="sxs-lookup"><span data-stu-id="810a5-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="810a5-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="810a5-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="810a5-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="810a5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="810a5-125">**IWMPControls 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="810a5-125">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="810a5-126">**IWMPControls. currentPositionString (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="810a5-126">**IWMPControls.currentPositionString (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)
</dt> </dl>

 

 





