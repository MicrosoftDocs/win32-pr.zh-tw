---
title: IWMPNetwork bufferingTime 屬性
description: BufferingTime 屬性會取得或設定在開始播放之前，為了緩衝處理傳入資料所配置的時間量（以毫秒為單位）。
ms.assetid: b5936b21-a17b-4801-a5fc-c6d6521e05aa
keywords:
- bufferingTime 屬性 Windows Media Player
- bufferingTime 屬性 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，bufferingTime 屬性
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingTime
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8594d53797b028dd74a8ef11cb8f2fa64b3654cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975743"
---
# <a name="iwmpnetworkbufferingtime-property"></a><span data-ttu-id="69f31-106">IWMPNetwork：： bufferingTime 屬性</span><span class="sxs-lookup"><span data-stu-id="69f31-106">IWMPNetwork::bufferingTime property</span></span>

<span data-ttu-id="69f31-107">**BufferingTime** 屬性會取得或設定在開始播放之前，為了緩衝處理傳入資料所配置的時間量（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="69f31-107">The **bufferingTime** property gets or sets the amount of time in milliseconds allocated for buffering incoming data before playback begins.</span></span>

## <a name="syntax"></a><span data-ttu-id="69f31-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="69f31-108">Syntax</span></span>


```CSharp
public System.Int32 bufferingTime {get; set;}
```


```VB

Public Property bufferingTime As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="69f31-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="69f31-109">Property value</span></span>

<span data-ttu-id="69f31-110">以 **毫秒** 為單位的緩衝時間（以毫秒為單位），其範圍從零到60000，預設值是5000。</span><span class="sxs-lookup"><span data-stu-id="69f31-110">A **System.Int32** that is the buffering time in milliseconds, which ranges from zero to 60,000 with a default value of 5,000.</span></span>

## <a name="examples"></a><span data-ttu-id="69f31-111">範例</span><span class="sxs-lookup"><span data-stu-id="69f31-111">Examples</span></span>

<span data-ttu-id="69f31-112">下列程式碼範例會使用 **bufferingTime** 來指定配置給緩衝處理傳入資料的秒數。</span><span class="sxs-lookup"><span data-stu-id="69f31-112">The following code example uses **bufferingTime** to specify the number of seconds allocated for buffering incoming data.</span></span> <span data-ttu-id="69f31-113">文字方塊可讓使用者輸入新的 **bufferingTime** 值，而屬性則會更新以回應按鈕的 Click 事件。</span><span class="sxs-lookup"><span data-stu-id="69f31-113">A text box allows the user to enter a new value for **bufferingTime**, and the property is updated in response to the Click event of a button.</span></span> <span data-ttu-id="69f31-114">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="69f31-114">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setBufTime_Click(object sender, System.EventArgs e)
{
    // Retrieve input from the user and convert it to an integer.
    int newTime = System.Convert.ToInt32(bufText.Text);

    // Test whether the integer is within the valid range. 
    if (newTime >= 0 & newTime <= 60) 
    {
        // Set the new bufferingTime in miliseconds.
        player.network.bufferingTime = (newTime * 1000);
    }
    else
    {
        System.Windows.Forms.MessageBox.Show("Buffering time must be between 0 and 60.");
    }
}
```


```VB

Public Sub setBufTime_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setBufTime.Click

    &#39; Retrieve input from the user and convert it to an integer.
    Dim newTime As Integer = System.Convert.ToInt32(bufText.Text)

    &#39; Test whether the integer is within the valid range. 
    If (newTime >= 0 And newTime <= 60) Then

        &#39; Set the new bufferingTime in miliseconds.
        player.network.bufferingTime = (newTime * 1000)

    Else

        System.Windows.Forms.MessageBox.Show(&quot;Buffering time must be between 0 and 60.&quot;)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="69f31-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="69f31-115">Requirements</span></span>



| <span data-ttu-id="69f31-116">需求</span><span class="sxs-lookup"><span data-stu-id="69f31-116">Requirement</span></span> | <span data-ttu-id="69f31-117">值</span><span class="sxs-lookup"><span data-stu-id="69f31-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69f31-118">版本</span><span class="sxs-lookup"><span data-stu-id="69f31-118">Version</span></span><br/>   | <span data-ttu-id="69f31-119">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="69f31-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="69f31-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="69f31-120">Namespace</span></span><br/> | <span data-ttu-id="69f31-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="69f31-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="69f31-122">組件</span><span class="sxs-lookup"><span data-stu-id="69f31-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="69f31-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="69f31-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69f31-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69f31-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69f31-125">**IWMPNetwork 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="69f31-125">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





