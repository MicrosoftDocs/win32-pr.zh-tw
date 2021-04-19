---
title: IWMPError errorCount 屬性
description: ErrorCount 屬性會取得錯誤佇列中的錯誤數目。
ms.assetid: a30750c8-2025-4087-bd2b-f313ccbde38c
keywords:
- errorCount 屬性 Windows Media Player
- errorCount 屬性 Windows Media Player，IWMPError 介面
- IWMPError 介面 Windows Media Player，errorCount 屬性
topic_type:
- apiref
api_name:
- IWMPError.errorCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b62c16f07260847c91f1c9f18885587444a4ceb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999497"
---
# <a name="iwmperrorerrorcount-property"></a><span data-ttu-id="1e52d-106">IWMPError：： errorCount 屬性</span><span class="sxs-lookup"><span data-stu-id="1e52d-106">IWMPError::errorCount property</span></span>

<span data-ttu-id="1e52d-107">**ErrorCount** 屬性會取得錯誤佇列中的錯誤數目。</span><span class="sxs-lookup"><span data-stu-id="1e52d-107">The **errorCount** property gets the number of errors in the error queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e52d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e52d-108">Syntax</span></span>


```CSharp
public System.Int32 errorCount {get; set;}
```


```VB

Public ReadOnly Property errorCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="1e52d-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="1e52d-109">Property value</span></span>

<span data-ttu-id="1e52d-110">錯誤數目的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="1e52d-110">A **System.Int32** that is the number of errors.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e52d-111">備註</span><span class="sxs-lookup"><span data-stu-id="1e52d-111">Remarks</span></span>

<span data-ttu-id="1e52d-112">如果您選擇顯示自訂錯誤訊息，則應將 **IWMPSettings enableErrorDialogs** 設定為 **false** 。</span><span class="sxs-lookup"><span data-stu-id="1e52d-112">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="1e52d-113">範例</span><span class="sxs-lookup"><span data-stu-id="1e52d-113">Examples</span></span>

<span data-ttu-id="1e52d-114">下列範例會在錯誤事件處理常式中使用 **errorCount** ，警示使用者錯誤佇列中的最新錯誤。</span><span class="sxs-lookup"><span data-stu-id="1e52d-114">The following example uses **errorCount** in an Error event handler to alert the user about the most recent error in the error queue.</span></span> <span data-ttu-id="1e52d-115">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="1e52d-115">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_errorCount(object sender, System.EventArgs e)
{
    // Store the number of errors in the queue.
    int max = player.Error.errorCount;

    // Get the description of the last error. Error items start at zero,
    // so the item index will always be one less than the error count.
    string errDesc = player.Error.get_Item(max-1).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc);
}
```


```VB

Public Sub player_ErrorEvent_errorCount(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the number of errors in the queue.
    Dim max As Integer = player.Error.errorCount

    &#39; Get the description of the last error. Error items start at zero,
    &#39; so the item index will always be one less than the error count.
    Dim errDesc As String = player.Error.Item(max - 1).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="1e52d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e52d-116">Requirements</span></span>



| <span data-ttu-id="1e52d-117">需求</span><span class="sxs-lookup"><span data-stu-id="1e52d-117">Requirement</span></span> | <span data-ttu-id="1e52d-118">值</span><span class="sxs-lookup"><span data-stu-id="1e52d-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e52d-119">版本</span><span class="sxs-lookup"><span data-stu-id="1e52d-119">Version</span></span><br/>   | <span data-ttu-id="1e52d-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="1e52d-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="1e52d-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="1e52d-121">Namespace</span></span><br/> | <span data-ttu-id="1e52d-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="1e52d-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1e52d-123">組件</span><span class="sxs-lookup"><span data-stu-id="1e52d-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1e52d-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="1e52d-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e52d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e52d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e52d-126">**IWMPError 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="1e52d-126">**IWMPError Interface (VB and C#)**</span></span>](iwmperror--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1e52d-127">**IWMPSettings. enableErrorDialogs (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="1e52d-127">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





