---
title: IWMPControls 上一個方法
description: 先前的方法會將播放清單中的上一個專案設定為目前的專案。
ms.assetid: 380524f5-e8b6-45c4-9f6c-3dbb49b1ac9f
keywords:
- 上一個方法 Windows Media Player
- 先前的方法 Windows Media Player，IWMPControls 介面
- IWMPControls 介面 Windows Media Player，previous 方法
topic_type:
- apiref
api_name:
- IWMPControls.previous
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 823038205a026afb7141491f562698eb60515a5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994863"
---
# <a name="iwmpcontrolsprevious-method"></a><span data-ttu-id="a8727-106">IWMPControls：:p revious 方法</span><span class="sxs-lookup"><span data-stu-id="a8727-106">IWMPControls::previous method</span></span>

<span data-ttu-id="a8727-107">**先前** 的方法會將播放清單中的上一個專案設定為目前的專案。</span><span class="sxs-lookup"><span data-stu-id="a8727-107">The **previous** method sets the previous item in the playlist as the current item.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8727-108">語法</span><span class="sxs-lookup"><span data-stu-id="a8727-108">Syntax</span></span>


```CSharp
public void previous();
```


```VB

Public Sub previous()
Implements IWMPControls.previous
```





## <a name="parameters"></a><span data-ttu-id="a8727-109">參數</span><span class="sxs-lookup"><span data-stu-id="a8727-109">Parameters</span></span>

<span data-ttu-id="a8727-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a8727-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a8727-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a8727-111">Return value</span></span>

<span data-ttu-id="a8727-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a8727-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8727-113">備註</span><span class="sxs-lookup"><span data-stu-id="a8727-113">Remarks</span></span>

<span data-ttu-id="a8727-114">如果播放清單是在叫用 **先前** 的第一個專案時，播放清單中的最後一個專案會成為目前的專案。</span><span class="sxs-lookup"><span data-stu-id="a8727-114">If the playlist is on the first entry when **previous** is invoked, the last entry in the playlist will become the current one.</span></span>

## <a name="examples"></a><span data-ttu-id="a8727-115">範例</span><span class="sxs-lookup"><span data-stu-id="a8727-115">Examples</span></span>

<span data-ttu-id="a8727-116">下列範例會使用 [ **上一步** ] 移至目前播放清單中的上一個專案，以回應按鈕的 Click 事件。</span><span class="sxs-lookup"><span data-stu-id="a8727-116">The following example uses **previous** to move to the previous item in the current playlist in response to the Click event of a button.</span></span> <span data-ttu-id="a8727-117">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="a8727-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void previousButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("previous"))
    {
        controls.previous();
    }
}
```


```VB

Public Sub previousButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles previousButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;previous&quot;)) Then

        controls.previous()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="a8727-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8727-118">Requirements</span></span>



| <span data-ttu-id="a8727-119">需求</span><span class="sxs-lookup"><span data-stu-id="a8727-119">Requirement</span></span> | <span data-ttu-id="a8727-120">值</span><span class="sxs-lookup"><span data-stu-id="a8727-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8727-121">版本</span><span class="sxs-lookup"><span data-stu-id="a8727-121">Version</span></span><br/>   | <span data-ttu-id="a8727-122">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="a8727-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a8727-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="a8727-123">Namespace</span></span><br/> | <span data-ttu-id="a8727-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a8727-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a8727-125">組件</span><span class="sxs-lookup"><span data-stu-id="a8727-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a8727-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="a8727-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8727-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8727-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8727-128">**IWMPControls 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="a8727-128">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a8727-129">**IWMPControls：接下來 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="a8727-129">**IWMPControls.next (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a8727-130">**IWMPControls。停止 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="a8727-130">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> </dl>

 

 





