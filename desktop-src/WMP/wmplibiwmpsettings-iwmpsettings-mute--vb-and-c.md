---
title: IWMPSettings 靜音屬性
description: '[靜音] 屬性會取得或設定值，指出音訊是否為靜音。'
ms.assetid: d99e47db-70cc-41e0-aca9-b765b075e7b4
keywords:
- 靜音屬性 Windows Media Player
- 靜音屬性 Windows Media Player、IWMPSettings 介面
- IWMPSettings 介面 Windows Media Player，靜音屬性
topic_type:
- apiref
api_name:
- IWMPSettings.mute
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67518bb9a6eccee13e4cc262f37341d30689439e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001232"
---
# <a name="iwmpsettingsmute-property"></a><span data-ttu-id="403c1-106">IWMPSettings：：靜音屬性</span><span class="sxs-lookup"><span data-stu-id="403c1-106">IWMPSettings::mute property</span></span>

<span data-ttu-id="403c1-107">[ **靜音** ] 屬性會取得或設定值，指出音訊是否為靜音。</span><span class="sxs-lookup"><span data-stu-id="403c1-107">The **mute** property gets or sets a value indicating whether audio is muted.</span></span>

## <a name="syntax"></a><span data-ttu-id="403c1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="403c1-108">Syntax</span></span>


```CSharp
public System.Boolean mute {get; set;}
```


```VB

Public Property mute As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="403c1-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="403c1-109">Property value</span></span>

<span data-ttu-id="403c1-110">指出音訊是否已靜音的 **system.object** 值。</span><span class="sxs-lookup"><span data-stu-id="403c1-110">A **System.Boolean** value indicating whether audio is muted.</span></span> <span data-ttu-id="403c1-111">預設值為 **false**。</span><span class="sxs-lookup"><span data-stu-id="403c1-111">The default is **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="403c1-112">範例</span><span class="sxs-lookup"><span data-stu-id="403c1-112">Examples</span></span>

<span data-ttu-id="403c1-113">下列範例會建立核取方塊，並在方塊的核取狀態變更時，切換 [ **靜音** ] 屬性以將音訊靜音並取消靜音。</span><span class="sxs-lookup"><span data-stu-id="403c1-113">The following example creates a check box, and toggles the **mute** property to mute and un-mute audio when the checked state of the box is changed.</span></span> <span data-ttu-id="403c1-114">**AxWMPLib. AxWindowsMediaPlayer** 物件是由名為 player 的變數表示。</span><span class="sxs-lookup"><span data-stu-id="403c1-114">**AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void Mute_CheckStateChanged(object sender, System.EventArgs e)
{
    System.Windows.Forms.CheckBox Mute = (System.Windows.Forms.CheckBox)sender;

    // Change the check box text depending on the checked state.
    Mute.Text = Mute.Checked ? "Un-mute Audio" : Mute.Text = "Mute Audio";

    // Use the checked state to set the mute property. 
    player.settings.mute = Mute.Checked;
}
```


```VB

Public Sub Mute_CheckStateChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles Mute.CheckStateChanged

    Dim cb As System.Windows.Forms.CheckBox = sender

    &#39;  Change the check box text depending on the checked state.
    If (cb.Checked) Then

        cb.Text = &quot;Un-mute Audio&quot;

    Else

        cb.Text = &quot;Mute Audio&quot;

    End If

    &#39;  Use the checked state to set the mute property. 
    player.settings.mute = cb.Checked

End Sub
```





## <a name="requirements"></a><span data-ttu-id="403c1-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="403c1-115">Requirements</span></span>



| <span data-ttu-id="403c1-116">需求</span><span class="sxs-lookup"><span data-stu-id="403c1-116">Requirement</span></span> | <span data-ttu-id="403c1-117">值</span><span class="sxs-lookup"><span data-stu-id="403c1-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="403c1-118">版本</span><span class="sxs-lookup"><span data-stu-id="403c1-118">Version</span></span><br/>   | <span data-ttu-id="403c1-119">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="403c1-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="403c1-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="403c1-120">Namespace</span></span><br/> | <span data-ttu-id="403c1-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="403c1-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="403c1-122">組件</span><span class="sxs-lookup"><span data-stu-id="403c1-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="403c1-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="403c1-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="403c1-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="403c1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="403c1-125">**IWMPSettings 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="403c1-125">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="403c1-126">**IWMPSettings (VB 和 c # 的速率 )**</span><span class="sxs-lookup"><span data-stu-id="403c1-126">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





