---
title: IWMPErrorItem errorCode 屬性
description: ErrorCode 屬性會取得目前的錯誤碼。
ms.assetid: 00719067-685d-4ef2-9eec-72c7892fcdb9
keywords:
- errorCode 屬性 Windows Media Player
- errorCode 屬性 Windows Media Player，IWMPErrorItem 介面
- IWMPErrorItem 介面 Windows Media Player，errorCode 屬性
topic_type:
- apiref
api_name:
- IWMPErrorItem.errorCode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f284d5655fc1f4007695a1f681c744a9c5c6fc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991348"
---
# <a name="iwmperroritemerrorcode-property"></a><span data-ttu-id="0ef24-106">IWMPErrorItem：： errorCode 屬性</span><span class="sxs-lookup"><span data-stu-id="0ef24-106">IWMPErrorItem::errorCode property</span></span>

<span data-ttu-id="0ef24-107">**ErrorCode** 屬性會取得目前的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0ef24-107">The **errorCode** property gets the current error code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ef24-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ef24-108">Syntax</span></span>


```CSharp
public System.Int32 errorCode {get; set;}
```


```VB

Public ReadOnly Property errorCode As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="0ef24-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="0ef24-109">Property value</span></span>

<span data-ttu-id="0ef24-110">錯誤碼的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="0ef24-110">A **System.Int32** that is the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ef24-111">備註</span><span class="sxs-lookup"><span data-stu-id="0ef24-111">Remarks</span></span>

<span data-ttu-id="0ef24-112">如果您選擇顯示自訂錯誤訊息，則應將 **IWMPSettings enableErrorDialogs** 設定為 **false** 。</span><span class="sxs-lookup"><span data-stu-id="0ef24-112">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="0ef24-113">範例</span><span class="sxs-lookup"><span data-stu-id="0ef24-113">Examples</span></span>

<span data-ttu-id="0ef24-114">下列範例會在錯誤事件處理常式中使用 **errorCode** ，向使用者顯示錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0ef24-114">The following example uses **errorCode** in an Error event handler to display the error code to the user.</span></span> <span data-ttu-id="0ef24-115">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="0ef24-115">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_errorCode(object sender, System.EventArgs e)
{
    // Get the error code for the first error item.
    int errCode = player.Error.get_Item(0).errorCode;

    // Display the error code.
    System.Windows.Forms.MessageBox.Show("Error number: " + errCode.ToString());
}
```


```VB

Public Sub player_ErrorEvent_errorCode(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the error code for the first error item.
    Dim errCode As Integer = player.Error.Item(0).errorCode

    &#39; Display the error code.
    System.Windows.Forms.MessageBox.Show(&quot;Error number: &quot; + errCode.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="0ef24-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ef24-116">Requirements</span></span>



| <span data-ttu-id="0ef24-117">需求</span><span class="sxs-lookup"><span data-stu-id="0ef24-117">Requirement</span></span> | <span data-ttu-id="0ef24-118">值</span><span class="sxs-lookup"><span data-stu-id="0ef24-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ef24-119">版本</span><span class="sxs-lookup"><span data-stu-id="0ef24-119">Version</span></span><br/>   | <span data-ttu-id="0ef24-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="0ef24-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="0ef24-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="0ef24-121">Namespace</span></span><br/> | <span data-ttu-id="0ef24-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="0ef24-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0ef24-123">組件</span><span class="sxs-lookup"><span data-stu-id="0ef24-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0ef24-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="0ef24-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ef24-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ef24-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ef24-126">**IWMPErrorItem 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="0ef24-126">**IWMPErrorItem Interface (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0ef24-127">**IWMPSettings. enableErrorDialogs (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="0ef24-127">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





