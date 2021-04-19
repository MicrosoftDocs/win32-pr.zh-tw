---
title: AxWindowsMediaPlayer 物件的錯誤事件
description: 當 Windows Media Player 控制項有錯誤情況時，就會發生錯誤事件。
ms.assetid: d28c18a9-c650-4169-989b-8727b7a5a831
keywords:
- AxWindowsMediaPlayer 物件的錯誤事件 Windows Media Player
topic_type:
- apiref
api_name:
- Error Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cfd3571538aa2cdd263a9f5d57e479e73818806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989253"
---
# <a name="error-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="d914e-104">AxWindowsMediaPlayer 物件的錯誤事件</span><span class="sxs-lookup"><span data-stu-id="d914e-104">Error Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="d914e-105">當 Windows Media Player 控制項有錯誤情況時，就會發生錯誤事件。</span><span class="sxs-lookup"><span data-stu-id="d914e-105">The Error event occurs when the Windows Media Player control has an error condition.</span></span>

``` syntax
[C#]
private void player_ErrorEvent(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_ErrorEvent(  
  sender As Object,  
  e As System.EventArgs
) Handles player.ErrorEvent
```

## <a name="event-data"></a><span data-ttu-id="d914e-106">事件資料</span><span class="sxs-lookup"><span data-stu-id="d914e-106">Event Data</span></span>

<span data-ttu-id="d914e-107">此事件不包含資料。</span><span class="sxs-lookup"><span data-stu-id="d914e-107">This event does not contain data.</span></span>

## <a name="examples"></a><span data-ttu-id="d914e-108">範例</span><span class="sxs-lookup"><span data-stu-id="d914e-108">Examples</span></span>

<span data-ttu-id="d914e-109">下列範例會建立錯誤事件的事件處理常式，以顯示錯誤佇列中第一個錯誤的描述文字。</span><span class="sxs-lookup"><span data-stu-id="d914e-109">The following example creates an event handler for the Error event to display the description text for the first error in the error queue.</span></span> <span data-ttu-id="d914e-110">AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="d914e-110">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the Error event.
player.ErrorEvent += new EventHandler(player_ErrorEvent);

private void player_ErrorEvent(object sender, System.EventArgs e)
{
    // Get the description of the first error. 
    string errDesc = player.Error.get_Item(0).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc);
}
```


```VB

Public Sub player_ErrorEvent(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the description of the first error. 
    Dim errDesc As String = player.Error.Item(0).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="d914e-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="d914e-111">Requirements</span></span>



| <span data-ttu-id="d914e-112">需求</span><span class="sxs-lookup"><span data-stu-id="d914e-112">Requirement</span></span> | <span data-ttu-id="d914e-113">值</span><span class="sxs-lookup"><span data-stu-id="d914e-113">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d914e-114">版本</span><span class="sxs-lookup"><span data-stu-id="d914e-114">Version</span></span><br/>   | <span data-ttu-id="d914e-115">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="d914e-115">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="d914e-116">命名空間</span><span class="sxs-lookup"><span data-stu-id="d914e-116">Namespace</span></span><br/> | <span data-ttu-id="d914e-117">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="d914e-117">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="d914e-118">組件</span><span class="sxs-lookup"><span data-stu-id="d914e-118">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d914e-119"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="d914e-119"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d914e-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d914e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d914e-121">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d914e-121">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d914e-122">**IWMPError (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d914e-122">**IWMPError.Item (VB and C#)**</span></span>](iwmperror-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d914e-123">**IWMPErrorItem. errorDescription (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d914e-123">**IWMPErrorItem.errorDescription (VB and C#)**</span></span>](wmplibiwmperroritem-iwmperroritem-errordescription--vb-and-c.md)
</dt> </dl>

 

 





