---
title: IWMPMedia setItemInfo 方法
description: SetItemInfo 方法會設定媒體專案的指定屬性值。
ms.assetid: 247bbba5-7d9b-489d-8e41-ae8ec6e266fd
keywords:
- setItemInfo 方法 Windows Media Player
- setItemInfo 方法 Windows Media Player，IWMPMedia 介面
- IWMPMedia 介面 Windows Media Player，setItemInfo 方法
topic_type:
- apiref
api_name:
- IWMPMedia.setItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6702c80c13090a370e2922ccecade49bc06645de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994310"
---
# <a name="iwmpmediasetiteminfo-method"></a><span data-ttu-id="4bf9f-106">IWMPMedia：： setItemInfo 方法</span><span class="sxs-lookup"><span data-stu-id="4bf9f-106">IWMPMedia::setItemInfo method</span></span>

<span data-ttu-id="4bf9f-107">**SetItemInfo** 方法會設定媒體專案的指定屬性值。</span><span class="sxs-lookup"><span data-stu-id="4bf9f-107">The **setItemInfo** method sets the value of the specified attribute for the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bf9f-108">語法</span><span class="sxs-lookup"><span data-stu-id="4bf9f-108">Syntax</span></span>


```CSharp
public void setItemInfo(
  System.String bstrItemName,
  System.String bstrVal
);
```


```VB

Public Sub setItemInfo( _
  ByVal bstrItemName As System.String, _
  ByVal bstrVal As System.String _
)
Implements IWMPMedia.setItemInfo
```





## <a name="parameters"></a><span data-ttu-id="4bf9f-109">參數</span><span class="sxs-lookup"><span data-stu-id="4bf9f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bf9f-110">*bstrItemName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4bf9f-110">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bf9f-111">表示屬性名稱的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="4bf9f-111">A **System.String** that is the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="4bf9f-112">*bstrVal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4bf9f-112">*bstrVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bf9f-113">表示新值的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="4bf9f-113">A **System.String** that is the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bf9f-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="4bf9f-114">Return value</span></span>

<span data-ttu-id="4bf9f-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4bf9f-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bf9f-116">備註</span><span class="sxs-lookup"><span data-stu-id="4bf9f-116">Remarks</span></span>

<span data-ttu-id="4bf9f-117">**AttributeCount** 屬性會取得指定媒體專案可用的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="4bf9f-117">The **attributeCount** property gets the number of attributes available for a given media item.</span></span> <span data-ttu-id="4bf9f-118">然後，您可以搭配 **getAttributeName** 方法使用索引編號來判斷可搭配此方法使用的內建屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="4bf9f-118">Index numbers can then be used with the **getAttributeName** method to determine the names of the built-in attributes that can be used with this method.</span></span>

<span data-ttu-id="4bf9f-119">使用這個方法之前，請使用 **isReadOnlyItem** 方法來探索是否可以設定特定屬性。</span><span class="sxs-lookup"><span data-stu-id="4bf9f-119">Before using this method, use the **isReadOnlyItem** method to discover whether a particular attribute can be set.</span></span>

<span data-ttu-id="4bf9f-120">在呼叫這個方法之前，您必須擁有程式庫的完整存取權。</span><span class="sxs-lookup"><span data-stu-id="4bf9f-120">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="4bf9f-121">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="4bf9f-121">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="4bf9f-122">注意</span><span class="sxs-lookup"><span data-stu-id="4bf9f-122">Note</span></span>

<span data-ttu-id="4bf9f-123">如果您在應用程式中內嵌 Windows Media Player 控制項，您所變更的檔案屬性將不會寫入數位媒體檔案，直到使用者執行 Windows Media Player 為止。</span><span class="sxs-lookup"><span data-stu-id="4bf9f-123">If you embed the Windows Media Player control in your application, file attributes that you change will not be written to the digital media file until the user runs Windows Media Player.</span></span>

## <a name="examples"></a><span data-ttu-id="4bf9f-124">範例</span><span class="sxs-lookup"><span data-stu-id="4bf9f-124">Examples</span></span>

<span data-ttu-id="4bf9f-125">下列範例會使用 **setItemInfo** 來變更目前媒體專案的 [內容類型] 屬性值。</span><span class="sxs-lookup"><span data-stu-id="4bf9f-125">The following example uses **setItemInfo** to change the value of the Genre attribute for the current media item.</span></span> <span data-ttu-id="4bf9f-126">文字方塊可讓使用者輸入字串，然後用它來變更屬性資訊，以回應按鈕的 Click 事件。</span><span class="sxs-lookup"><span data-stu-id="4bf9f-126">A text box allows the user to enter a string, which is then used to change the attribute information in response to the Click event of a button.</span></span> <span data-ttu-id="4bf9f-127">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="4bf9f-127">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setNewGenre_Click(object sender, System.EventArgs e)
{
    // Store a WMPLib.IWMPMedia3 interface to the current media item. 
    WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

    // Get the user input from the TextBox. 
    string atValue = genText.Text;

    // Test for read-only status of the attribute. 
    if( cm.isReadOnlyItem("Genre") == false )
    {
        // Change the attribute value. 
        cm.setItemInfo("Genre", atValue);
    } 
}
```


```VB

Public Sub setNewGenre_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setNewGenre.Click

    &#39; Store a WMPLib.IWMPMedia3 interface to the current media item. 
    Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

    &#39; Get the user input from the TextBox. 
    Dim atValue = genText.Text

    &#39; Test for read-only status of the attribute. 
    If (cm.isReadOnlyItem(&quot;Genre&quot;) = False) Then

        &#39; Change the attribute value. 
        cm.setItemInfo(&quot;Genre&quot;, atValue)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="4bf9f-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="4bf9f-128">Requirements</span></span>



| <span data-ttu-id="4bf9f-129">需求</span><span class="sxs-lookup"><span data-stu-id="4bf9f-129">Requirement</span></span> | <span data-ttu-id="4bf9f-130">值</span><span class="sxs-lookup"><span data-stu-id="4bf9f-130">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bf9f-131">版本</span><span class="sxs-lookup"><span data-stu-id="4bf9f-131">Version</span></span><br/>   | <span data-ttu-id="4bf9f-132">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="4bf9f-132">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="4bf9f-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="4bf9f-133">Namespace</span></span><br/> | <span data-ttu-id="4bf9f-134">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="4bf9f-134">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4bf9f-135">組件</span><span class="sxs-lookup"><span data-stu-id="4bf9f-135">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4bf9f-136"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="4bf9f-136"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bf9f-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4bf9f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bf9f-138">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="4bf9f-138">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4bf9f-139">**IWMPMedia. attributeCount (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="4bf9f-139">**IWMPMedia.attributeCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4bf9f-140">**IWMPMedia. getAttributeName (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="4bf9f-140">**IWMPMedia.getAttributeName (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4bf9f-141">**IWMPMedia. isReadOnlyItem (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="4bf9f-141">**IWMPMedia.isReadOnlyItem (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)
</dt> </dl>

 

 





