---
title: IWMPMediaCollection getAttributeStringCollection 方法
description: GetAttributeStringCollection 方法會傳回 IWMPStringCollection 介面，此介面表示媒體類型內指定之屬性的所有值集合。
ms.assetid: 5ac19c04-75db-4618-9c4e-b20e2f709024
keywords:
- getAttributeStringCollection 方法 Windows Media Player
- getAttributeStringCollection 方法 Windows Media Player，IWMPMediaCollection 介面
- IWMPMediaCollection 介面 Windows Media Player，getAttributeStringCollection 方法
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getAttributeStringCollection
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bef25cd811890e82273fd5d634633e25e7ec460c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999739"
---
# <a name="iwmpmediacollectiongetattributestringcollection-method"></a><span data-ttu-id="b44a9-106">IWMPMediaCollection：： getAttributeStringCollection 方法</span><span class="sxs-lookup"><span data-stu-id="b44a9-106">IWMPMediaCollection::getAttributeStringCollection method</span></span>

<span data-ttu-id="b44a9-107">**GetAttributeStringCollection** 方法會傳回 **IWMPStringCollection** 介面，此介面表示媒體類型內指定之屬性的所有值集合。</span><span class="sxs-lookup"><span data-stu-id="b44a9-107">The **getAttributeStringCollection** method returns an **IWMPStringCollection** interface that represents the set of all values for a specified attribute within a media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="b44a9-108">語法</span><span class="sxs-lookup"><span data-stu-id="b44a9-108">Syntax</span></span>


```CSharp
public IWMPStringCollection getAttributeStringCollection(
  System.String bstrAttribute,
  System.String bstrMediaType
);
```


```VB

Public Function getAttributeStringCollection( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrMediaType As System.String _
) As IWMPStringCollection
Implements IWMPMediaCollection.getAttributeStringCollection
```





## <a name="parameters"></a><span data-ttu-id="b44a9-109">參數</span><span class="sxs-lookup"><span data-stu-id="b44a9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b44a9-110">*bstrAttribute* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b44a9-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b44a9-111">**System.string** ，這是要抓取值的屬性。</span><span class="sxs-lookup"><span data-stu-id="b44a9-111">A **System.String** that is the attribute for which the values are retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="b44a9-112">*bstrMediaType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b44a9-112">*bstrMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b44a9-113">**System.string** ，這是要抓取值的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="b44a9-113">A **System.String** that is the media type for which the values are retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b44a9-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="b44a9-114">Return value</span></span>

<span data-ttu-id="b44a9-115">所抓取值的 **WMPLib IWMPStringCollection** 介面。</span><span class="sxs-lookup"><span data-stu-id="b44a9-115">A **WMPLib.IWMPStringCollection** interface for the retrieved values.</span></span>

## <a name="remarks"></a><span data-ttu-id="b44a9-116">備註</span><span class="sxs-lookup"><span data-stu-id="b44a9-116">Remarks</span></span>

<span data-ttu-id="b44a9-117">在呼叫這個方法之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="b44a9-117">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="b44a9-118">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="b44a9-118">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="b44a9-119">如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 [屬性參考](attribute-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="b44a9-119">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b44a9-120">範例</span><span class="sxs-lookup"><span data-stu-id="b44a9-120">Examples</span></span>

<span data-ttu-id="b44a9-121">下列範例會使用 **getAttributeStringCollection** 來顯示值的清單，這些值會對應至媒體集合中音訊專案的特定屬性。</span><span class="sxs-lookup"><span data-stu-id="b44a9-121">The following example uses **getAttributeStringCollection** to display a list of values that correspond to a particular attribute for audio items in the media collection.</span></span> <span data-ttu-id="b44a9-122">清單方塊可讓使用者選取屬性，例如 [演出者]、[內容類型] 或 [專輯]，而多行文字方塊則會顯示結果。</span><span class="sxs-lookup"><span data-stu-id="b44a9-122">A list box allows the user to select an attribute, such as Artist, Genre, or Album and a multi-line text box displays the result.</span></span> <span data-ttu-id="b44a9-123">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="b44a9-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void audioAttributes_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Retrieve the attribute type from the ListBox
    string attributeType = (string)((System.Windows.Forms.ListBox)sender).SelectedItem;

    // Get an interface to the mediaCollection.  
    WMPLib.IWMPMediaCollection2 library = (WMPLib.IWMPMediaCollection2)player.mediaCollection;

    // Get an interface to the string collection for the attribute type the user selects.
    WMPLib.IWMPStringCollection2 all = (WMPLib.IWMPStringCollection2)library.getAttributeStringCollection(attributeType, "Audio");

    // Clear the text box of previous results.
    attributeValues.Clear();

    // Create an array to hold the attribute values.
    string[] attributeArray = new string[all.count];
    
    // Loop through the string collection.
    for (int i = 0; i < all.count; i++)
    {
        // Store the items in the array.
        attributeArray[i] = all.Item(i);
    }

    // Display the items in the text box.
    attributeValues.Lines = attributeArray;
}
```


```VB

Public Sub audioAttributes_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles audioAttributes.SelectedIndexChanged

    &#39; Retrieve the attribute type from the ListBox
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim attributeType As String = lb.SelectedItem

    &#39; Get an interface to the mediaCollection.  
    Dim library As WMPLib.IWMPMediaCollection2 = player.mediaCollection

    &#39; Get an interface to the string collection for the attribute type the user selects.
    Dim all As WMPLib.IWMPStringCollection2 = library.getAttributeStringCollection(attributeType, &quot;Audio&quot;)

    &#39; Clear the text box of previous results.
    attributeValues.Clear()

    &#39; Create an array to hold the attribute values.
    Dim attributeArray(all.count) As String

    &#39; Loop through the string collection.
    For i As Integer = 0 To (all.count - 1)

        &#39; Store the items in the array.
        attributeArray(i) = all.Item(i)

    Next i

    &#39; Display the items in the text box.
    attributeValues.Lines = attributeArray

End Sub
```





## <a name="requirements"></a><span data-ttu-id="b44a9-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="b44a9-124">Requirements</span></span>



| <span data-ttu-id="b44a9-125">需求</span><span class="sxs-lookup"><span data-stu-id="b44a9-125">Requirement</span></span> | <span data-ttu-id="b44a9-126">值</span><span class="sxs-lookup"><span data-stu-id="b44a9-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b44a9-127">版本</span><span class="sxs-lookup"><span data-stu-id="b44a9-127">Version</span></span><br/>   | <span data-ttu-id="b44a9-128">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="b44a9-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b44a9-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="b44a9-129">Namespace</span></span><br/> | <span data-ttu-id="b44a9-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b44a9-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b44a9-131">組件</span><span class="sxs-lookup"><span data-stu-id="b44a9-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b44a9-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="b44a9-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b44a9-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b44a9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b44a9-134">**IWMPMediaCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b44a9-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b44a9-135">**IWMPStringCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b44a9-135">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





