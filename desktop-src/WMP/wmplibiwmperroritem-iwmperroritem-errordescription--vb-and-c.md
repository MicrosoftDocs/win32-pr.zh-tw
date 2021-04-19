---
title: IWMPErrorItem errorDescription 屬性
description: ErrorDescription 屬性會取得錯誤的描述。
ms.assetid: a9914c24-1d10-422a-bcba-80be9fb85108
keywords:
- errorDescription 屬性 Windows Media Player
- errorDescription 屬性 Windows Media Player，IWMPErrorItem 介面
- IWMPErrorItem 介面 Windows Media Player，errorDescription 屬性
topic_type:
- apiref
api_name:
- IWMPErrorItem.errorDescription
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8725099d1ce49eae8f378b2571dc4030f60611e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991207"
---
# <a name="iwmperroritemerrordescription-property"></a><span data-ttu-id="f765c-106">IWMPErrorItem：： errorDescription 屬性</span><span class="sxs-lookup"><span data-stu-id="f765c-106">IWMPErrorItem::errorDescription property</span></span>

<span data-ttu-id="f765c-107">**ErrorDescription** 屬性會取得錯誤的描述。</span><span class="sxs-lookup"><span data-stu-id="f765c-107">The **errorDescription** property gets a description of the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="f765c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f765c-108">Syntax</span></span>


```CSharp
public System.String errorDescription {get; set;}
```


```VB

Public ReadOnly Property errorDescription As System.String
```





## <a name="property-value"></a><span data-ttu-id="f765c-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="f765c-109">Property value</span></span>

<span data-ttu-id="f765c-110">表示錯誤描述的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="f765c-110">A **System.String** that is the error description.</span></span>

## <a name="remarks"></a><span data-ttu-id="f765c-111">備註</span><span class="sxs-lookup"><span data-stu-id="f765c-111">Remarks</span></span>

<span data-ttu-id="f765c-112">如果您選擇顯示自訂錯誤訊息，則應將 **IWMPSettings enableErrorDialogs** 設定為 **false** 。</span><span class="sxs-lookup"><span data-stu-id="f765c-112">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="f765c-113">範例</span><span class="sxs-lookup"><span data-stu-id="f765c-113">Examples</span></span>

<span data-ttu-id="f765c-114">下列範例會在錯誤事件處理常式中使用 **errorDescription** ，向使用者顯示錯誤描述。</span><span class="sxs-lookup"><span data-stu-id="f765c-114">The following example uses **errorDescription** in an Error event handler to display the error description to the user.</span></span> <span data-ttu-id="f765c-115">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="f765c-115">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_errorDescription(object sender, System.EventArgs e)
{
    // Get the error description for the first error item.
    string errDesc = player.Error.get_Item(0).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show("Error: " + errDesc);
}
```


```VB

Public Sub player_ErrorEvent_errorDescription(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the error description for the first error item.
    Dim errDesc As String = player.Error.Item(0).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(&quot;Error: &quot; + errDesc)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="f765c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="f765c-116">Requirements</span></span>



| <span data-ttu-id="f765c-117">需求</span><span class="sxs-lookup"><span data-stu-id="f765c-117">Requirement</span></span> | <span data-ttu-id="f765c-118">值</span><span class="sxs-lookup"><span data-stu-id="f765c-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f765c-119">版本</span><span class="sxs-lookup"><span data-stu-id="f765c-119">Version</span></span><br/>   | <span data-ttu-id="f765c-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="f765c-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f765c-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="f765c-121">Namespace</span></span><br/> | <span data-ttu-id="f765c-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f765c-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f765c-123">組件</span><span class="sxs-lookup"><span data-stu-id="f765c-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f765c-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="f765c-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f765c-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f765c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f765c-126">**IWMPErrorItem 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="f765c-126">**IWMPErrorItem Interface (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f765c-127">**IWMPSettings. enableErrorDialogs (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="f765c-127">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





