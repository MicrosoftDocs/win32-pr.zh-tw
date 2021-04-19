---
title: IWMPMedia name 屬性
description: Name 屬性會取得或設定媒體專案的名稱。
ms.assetid: d1057871-bccf-4f84-9b1d-74c41a8f7f7c
keywords:
- name 屬性 Windows Media Player
- name 屬性 Windows Media Player，IWMPMedia 介面
- IWMPMedia 介面 Windows Media Player，name 屬性
topic_type:
- apiref
api_name:
- IWMPMedia.name
- IWMPMedia.get_name
- IWMPMedia.put_name
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c526fc9847b06d0f7b6f4ebadf71761fd29a9d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994860"
---
# <a name="iwmpmedianame-property"></a><span data-ttu-id="56e0b-106">IWMPMedia：： name 屬性</span><span class="sxs-lookup"><span data-stu-id="56e0b-106">IWMPMedia::name property</span></span>

<span data-ttu-id="56e0b-107">**Name** 屬性會取得或設定媒體專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="56e0b-107">The **name** property gets or sets the name of the media item.</span></span>

<span data-ttu-id="56e0b-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="56e0b-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="56e0b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="56e0b-109">Syntax</span></span>


```CSharp
public System.String name {get; set;}
```


```VB

Public Property name As System.String
```





## <a name="property-value"></a><span data-ttu-id="56e0b-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="56e0b-110">Property value</span></span>

<span data-ttu-id="56e0b-111">表示媒體專案名稱的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="56e0b-111">A **System.String** that is the name of the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="56e0b-112">備註</span><span class="sxs-lookup"><span data-stu-id="56e0b-112">Remarks</span></span>

<span data-ttu-id="56e0b-113">使用這個屬性之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="56e0b-113">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="56e0b-114">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="56e0b-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="56e0b-115">範例</span><span class="sxs-lookup"><span data-stu-id="56e0b-115">Examples</span></span>

<span data-ttu-id="56e0b-116">下列範例會使用 **名稱** 來變更目前媒體專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="56e0b-116">The following example uses **name** to change the name of the current media item.</span></span> <span data-ttu-id="56e0b-117">文字方塊可讓使用者輸入新的名稱，而且名稱會變更，以回應按鈕的 Click 事件。</span><span class="sxs-lookup"><span data-stu-id="56e0b-117">A text box allows the user to enter a new name, and the name is changed in response to the Click event of a button.</span></span> <span data-ttu-id="56e0b-118">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="56e0b-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setNewName_Click(object sender, System.EventArgs e)
{
    // ...Add code to ensure that the TextBox contains a valid value.

    // Store a WMPLib.IWMPMedia3 interface to the current media item. 
    WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

    // Change the name. 
    cm.name = nameText.Text;
}
```


```VB

Public Sub setNewName_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setNewName.Click

    &#39; ...Add code to ensure that the TextBox contains a valid value.

    &#39; Store a WMPLib.IWMPMedia3 interface to the current media item. 
    Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

    &#39; Change the name. 
    cm.name = nameText.Text

End Sub
```





## <a name="requirements"></a><span data-ttu-id="56e0b-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="56e0b-119">Requirements</span></span>



| <span data-ttu-id="56e0b-120">需求</span><span class="sxs-lookup"><span data-stu-id="56e0b-120">Requirement</span></span> | <span data-ttu-id="56e0b-121">值</span><span class="sxs-lookup"><span data-stu-id="56e0b-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56e0b-122">版本</span><span class="sxs-lookup"><span data-stu-id="56e0b-122">Version</span></span><br/>   | <span data-ttu-id="56e0b-123">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="56e0b-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="56e0b-124">命名空間</span><span class="sxs-lookup"><span data-stu-id="56e0b-124">Namespace</span></span><br/> | <span data-ttu-id="56e0b-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="56e0b-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="56e0b-126">組件</span><span class="sxs-lookup"><span data-stu-id="56e0b-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="56e0b-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="56e0b-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56e0b-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="56e0b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56e0b-129">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="56e0b-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





