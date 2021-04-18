---
title: IWMPMedia durationString 屬性
description: DurationString 屬性會取得字串，表示目前媒體專案的持續時間（以 HH MM SS 格式表示）。
ms.assetid: de33c737-d73e-41f0-9c1b-944279194738
keywords:
- durationString 屬性 Windows Media Player
- durationString 屬性 Windows Media Player，IWMPMedia 介面
- IWMPMedia 介面 Windows Media Player，durationString 屬性
topic_type:
- apiref
api_name:
- IWMPMedia.durationString
- IWMPMedia.get_durationString
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e6bc732388036aa9e79aeedd988de94fa263bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976229"
---
# <a name="iwmpmediadurationstring-property"></a><span data-ttu-id="3d08d-106">IWMPMedia：:d urationString 屬性</span><span class="sxs-lookup"><span data-stu-id="3d08d-106">IWMPMedia::durationString property</span></span>

<span data-ttu-id="3d08d-107">**DurationString** 屬性會取得字串，指出目前媒體專案的持續時間（以 HH： MM： SS 格式表示）。</span><span class="sxs-lookup"><span data-stu-id="3d08d-107">The **durationString** property gets a string indicating the duration of the current media item in HH:MM:SS format.</span></span>

<span data-ttu-id="3d08d-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="3d08d-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d08d-109">語法</span><span class="sxs-lookup"><span data-stu-id="3d08d-109">Syntax</span></span>


```CSharp
public System.String durationString {get;}
```


```VB

Public ReadOnly Property durationString As System.String
```





## <a name="property-value"></a><span data-ttu-id="3d08d-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="3d08d-110">Property value</span></span>

<span data-ttu-id="3d08d-111">持續期間的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="3d08d-111">A **System.String** that is the duration.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d08d-112">備註</span><span class="sxs-lookup"><span data-stu-id="3d08d-112">Remarks</span></span>

<span data-ttu-id="3d08d-113">如果這個屬性與 AxWindowsMediaPlayer. currentMedia 中所指定的媒體專案不同，它可能不包含有效的值。</span><span class="sxs-lookup"><span data-stu-id="3d08d-113">If this property is used with a media item other than the one specified in AxWindowsMediaPlayer.currentMedia, it may not contain a valid value.</span></span> <span data-ttu-id="3d08d-114">如果媒體專案的長度不到一小時，則會省略傳回值的時數部分。</span><span class="sxs-lookup"><span data-stu-id="3d08d-114">If the media item is less than an hour long, the hours portion of the return value is omitted.</span></span>

<span data-ttu-id="3d08d-115">使用這個屬性之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="3d08d-115">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="3d08d-116">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="3d08d-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3d08d-117">範例</span><span class="sxs-lookup"><span data-stu-id="3d08d-117">Examples</span></span>

<span data-ttu-id="3d08d-118">下列範例會使用 **durationString** ，以標籤中的格式化文字顯示目前媒體專案的持續時間。</span><span class="sxs-lookup"><span data-stu-id="3d08d-118">The following example uses **durationString** to display the duration of the current media item as formatted text in a label.</span></span> <span data-ttu-id="3d08d-119">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="3d08d-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Create an event handler for the OpenStateChange event.
private void player_OpenStateChange(object sender, AxWMPLib._WMPOCXEvents_OpenStateChangeEvent e)
{
    // Test whether the current media item is open.
    if (e.newState == (int)WMPLib.WMPOpenState.wmposMediaOpen)
    {
         // Display the formatted duration string in the label.
         mediaDuration.Text = player.currentMedia.durationString;
    }
}
```


```VB

' Create an event handler for the OpenStateChange event.
Public Sub player_OpenStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_OpenStateChangeEvent) Handles player.OpenStateChange

    &#39; Test whether the current media item is open.
    If (e.newState = 13) Then

        &#39; Display the formatted duration string in the label.
        mediaDuration.Text = player.currentMedia.durationString

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="3d08d-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d08d-120">Requirements</span></span>



| <span data-ttu-id="3d08d-121">需求</span><span class="sxs-lookup"><span data-stu-id="3d08d-121">Requirement</span></span> | <span data-ttu-id="3d08d-122">值</span><span class="sxs-lookup"><span data-stu-id="3d08d-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d08d-123">版本</span><span class="sxs-lookup"><span data-stu-id="3d08d-123">Version</span></span><br/>   | <span data-ttu-id="3d08d-124">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="3d08d-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3d08d-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="3d08d-125">Namespace</span></span><br/> | <span data-ttu-id="3d08d-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="3d08d-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3d08d-127">組件</span><span class="sxs-lookup"><span data-stu-id="3d08d-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3d08d-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="3d08d-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d08d-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d08d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d08d-130">**AxWindowsMediaPlayer. currentMedia (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="3d08d-130">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3d08d-131">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="3d08d-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3d08d-132">**IWMPMedia duration (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="3d08d-132">**IWMPMedia.duration (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-duration--vb-and-c.md)
</dt> </dl>

 

 





