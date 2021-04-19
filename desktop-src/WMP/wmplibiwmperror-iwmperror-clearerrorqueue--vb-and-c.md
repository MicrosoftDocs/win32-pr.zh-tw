---
title: IWMPError clearErrorQueue 方法
description: ClearErrorQueue 方法會清除錯誤佇列中的錯誤。 |IWMPError clearErrorQueue 方法
ms.assetid: a8e8e666-56e4-4e75-9ed5-2714d272ce7c
keywords:
- clearErrorQueue 方法 Windows Media Player
- clearErrorQueue 方法 Windows Media Player，IWMPError 介面
- IWMPError 介面 Windows Media Player，clearErrorQueue 方法
topic_type:
- apiref
api_name:
- IWMPError.clearErrorQueue
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98c3f422a9bc32049106d83c970bd8d2c9b2110f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981397"
---
# <a name="iwmperrorclearerrorqueue-method"></a><span data-ttu-id="69b2b-107">IWMPError：： clearErrorQueue 方法</span><span class="sxs-lookup"><span data-stu-id="69b2b-107">IWMPError::clearErrorQueue method</span></span>

<span data-ttu-id="69b2b-108">**ClearErrorQueue** 方法會清除錯誤佇列中的錯誤。</span><span class="sxs-lookup"><span data-stu-id="69b2b-108">The **clearErrorQueue** method clears the errors from the error queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="69b2b-109">語法</span><span class="sxs-lookup"><span data-stu-id="69b2b-109">Syntax</span></span>


```CSharp
public void clearErrorQueue();
```


```VB

Public Sub clearErrorQueue()
Implements IWMPError.clearErrorQueue
```





## <a name="parameters"></a><span data-ttu-id="69b2b-110">參數</span><span class="sxs-lookup"><span data-stu-id="69b2b-110">Parameters</span></span>

<span data-ttu-id="69b2b-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="69b2b-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="69b2b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="69b2b-112">Return value</span></span>

<span data-ttu-id="69b2b-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="69b2b-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="69b2b-114">備註</span><span class="sxs-lookup"><span data-stu-id="69b2b-114">Remarks</span></span>

<span data-ttu-id="69b2b-115">使用這個方法可在處理一系列錯誤之後清除錯誤佇列。</span><span class="sxs-lookup"><span data-stu-id="69b2b-115">Use this method to clear the error queue after a series of errors has been processed.</span></span>

<span data-ttu-id="69b2b-116">如果您選擇顯示自訂錯誤訊息，則應將 **IWMPSettings enableErrorDialogs** 設定為 **false** 。</span><span class="sxs-lookup"><span data-stu-id="69b2b-116">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="69b2b-117">範例</span><span class="sxs-lookup"><span data-stu-id="69b2b-117">Examples</span></span>

<span data-ttu-id="69b2b-118">下列範例會在顯示所有錯誤描述之後，于錯誤事件處理常式中使用 **clearErrorQueue** 來清空錯誤佇列。</span><span class="sxs-lookup"><span data-stu-id="69b2b-118">The following example uses **clearErrorQueue** in an Error event handler to empty the error queue after all error descriptions have been displayed.</span></span> <span data-ttu-id="69b2b-119">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="69b2b-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_clearErrorQueue(object sender, System.EventArgs e)
{
    // Store the number of errors in the queue.
    int max = player.Error.errorCount;

    // Loop through the list of errors.
    for (int i = 0; i < max; i++)
    {
        // Get the description for this error.
        string errDesc = player.Error.get_Item(i).errorDescription;

        // Display the error message.
        System.Windows.Forms.MessageBox.Show(errDesc);
    }

    // Clear the error queue to prepare for the next group of errors.
    player.Error.clearErrorQueue();
}
```


```VB

Public Sub player_ErrorEvent_clearErrorQueue(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the number of errors in the queue.
    Dim max As Integer = player.Error.errorCount

    &#39; Loop through the list of errors.
    For i As Integer = 0 To (max - 1)

        &#39; Get the description for this error.
        Dim errDesc As String = player.Error.Item(i).errorDescription

        &#39; Display the error message.
        System.Windows.Forms.MessageBox.Show(errDesc)

    Next i

    &#39; Clear the error queue to prepare for the next group of errors.
    player.Error.clearErrorQueue()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="69b2b-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="69b2b-120">Requirements</span></span>



| <span data-ttu-id="69b2b-121">需求</span><span class="sxs-lookup"><span data-stu-id="69b2b-121">Requirement</span></span> | <span data-ttu-id="69b2b-122">值</span><span class="sxs-lookup"><span data-stu-id="69b2b-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69b2b-123">版本</span><span class="sxs-lookup"><span data-stu-id="69b2b-123">Version</span></span><br/>   | <span data-ttu-id="69b2b-124">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="69b2b-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="69b2b-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="69b2b-125">Namespace</span></span><br/> | <span data-ttu-id="69b2b-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="69b2b-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="69b2b-127">組件</span><span class="sxs-lookup"><span data-stu-id="69b2b-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="69b2b-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="69b2b-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69b2b-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69b2b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69b2b-130">**IWMPError 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="69b2b-130">**IWMPError Interface (VB and C#)**</span></span>](iwmperror--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="69b2b-131">**IWMPSettings. enableErrorDialogs (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="69b2b-131">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





