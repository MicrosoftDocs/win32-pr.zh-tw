---
title: IWMPMedia imageSourceWidth 屬性
description: ImageSourceWidth 屬性會取得目前媒體專案的寬度（以圖元為單位）。
ms.assetid: d3644217-6faf-415e-b0c0-23db85c31a3a
keywords:
- imageSourceWidth 屬性 Windows Media Player
- imageSourceWidth 屬性 Windows Media Player，IWMPMedia 介面
- IWMPMedia 介面 Windows Media Player，imageSourceWidth 屬性
topic_type:
- apiref
api_name:
- IWMPMedia.imageSourceWidth
- IWMPMedia.get_imageSourceWidth
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 441c4fb4a05f610aee5a2c923353fb9688bffcc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000968"
---
# <a name="iwmpmediaimagesourcewidth-property"></a><span data-ttu-id="e4d00-106">IWMPMedia：： imageSourceWidth 屬性</span><span class="sxs-lookup"><span data-stu-id="e4d00-106">IWMPMedia::imageSourceWidth property</span></span>

<span data-ttu-id="e4d00-107">**ImageSourceWidth** 屬性會取得目前媒體專案的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="e4d00-107">The **imageSourceWidth** property gets the width of the current media item in pixels.</span></span>

<span data-ttu-id="e4d00-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e4d00-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4d00-109">語法</span><span class="sxs-lookup"><span data-stu-id="e4d00-109">Syntax</span></span>


```CSharp
public System.Int32 imageSourceWidth {get;}
```


```VB

Public ReadOnly Property imageSourceWidth As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="e4d00-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="e4d00-110">Property value</span></span>

<span data-ttu-id="e4d00-111">表示媒體專案寬度的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="e4d00-111">A **System.Int32** that is the width of the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4d00-112">備註</span><span class="sxs-lookup"><span data-stu-id="e4d00-112">Remarks</span></span>

<span data-ttu-id="e4d00-113">如果媒體專案不是目前的，則這個屬性會傳回零。</span><span class="sxs-lookup"><span data-stu-id="e4d00-113">If the media item is not the current one, this property returns zero.</span></span>

<span data-ttu-id="e4d00-114">使用這個屬性之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="e4d00-114">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="e4d00-115">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="e4d00-115">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e4d00-116">範例</span><span class="sxs-lookup"><span data-stu-id="e4d00-116">Examples</span></span>

<span data-ttu-id="e4d00-117">下列範例會使用 **imageSourceWidth** ，在文字方塊中顯示目前媒體專案的影像大小（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="e4d00-117">The following example uses **imageSourceWidth** to display the image size, in pixels, of the current media item in a text box.</span></span> <span data-ttu-id="e4d00-118">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="e4d00-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Create an event handler for the OpenStateChange event.
private void player_OpenStateChange(object sender, AxWMPLib._WMPOCXEvents_OpenStateChangeEvent e)
{
    // Test whether the new media item is open.
    if (e.newState == (int)WMPLib.WMPOpenState.wmposMediaOpen)
    {
        // Store the height and width of the new media item.
        int height = player.currentMedia.imageSourceHeight;
        int width = player.currentMedia.imageSourceWidth;

        // Clear all the information in the text box.
        videoSize.Clear();

        // Test whether an image is visible.
        if (height != 0 && width != 0)
        {
            // Display the image size information.
            videoSize.Text = (width.ToString() + " x " + height.ToString());
        }
    }
}
```


```VB

' Create an event handler for the OpenStateChange event.
Public Sub player_OpenStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_OpenStateChangeEvent) Handles player.OpenStateChange

    &#39; Test whether the new media item is open.
    If (e.newState = WMPLib.WMPOpenState.wmposMediaOpen) Then

        &#39; Store the height and width of the new media item.
        Dim Height As Integer = player.currentMedia.imageSourceHeight
        Dim Width As Integer = player.currentMedia.imageSourceWidth

        &#39; Clear all the information in the text box.
        videoSize.Clear()

        &#39; Test whether an image is visible.
        If (Height <> 0 And Width <> 0) Then

            &#39; Display the image size information.
            videoSize.Text = (Width.ToString() + &quot; x &quot; + Height.ToString())

        End If

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="e4d00-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4d00-119">Requirements</span></span>



| <span data-ttu-id="e4d00-120">需求</span><span class="sxs-lookup"><span data-stu-id="e4d00-120">Requirement</span></span> | <span data-ttu-id="e4d00-121">值</span><span class="sxs-lookup"><span data-stu-id="e4d00-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4d00-122">版本</span><span class="sxs-lookup"><span data-stu-id="e4d00-122">Version</span></span><br/>   | <span data-ttu-id="e4d00-123">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="e4d00-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e4d00-124">命名空間</span><span class="sxs-lookup"><span data-stu-id="e4d00-124">Namespace</span></span><br/> | <span data-ttu-id="e4d00-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e4d00-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e4d00-126">組件</span><span class="sxs-lookup"><span data-stu-id="e4d00-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e4d00-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="e4d00-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4d00-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4d00-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4d00-129">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="e4d00-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





