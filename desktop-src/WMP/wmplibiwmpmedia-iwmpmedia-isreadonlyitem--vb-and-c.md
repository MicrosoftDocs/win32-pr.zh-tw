---
title: IWMPMedia isReadOnlyItem 方法
description: IsReadOnlyItem 方法會傳回值，指出是否可以編輯指定之媒體專案的屬性。
ms.assetid: c810c5c1-8cb9-4ac7-ac49-1ebdc86f5d7f
keywords:
- isReadOnlyItem 方法 Windows Media Player
- isReadOnlyItem 方法 Windows Media Player，IWMPMedia 介面
- IWMPMedia 介面 Windows Media Player，isReadOnlyItem 方法
topic_type:
- apiref
api_name:
- IWMPMedia.isReadOnlyItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21d3dfefc1222832783e62962298da8bcb02b25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999695"
---
# <a name="iwmpmediaisreadonlyitem-method"></a><span data-ttu-id="a8ce0-106">IWMPMedia：： isReadOnlyItem 方法</span><span class="sxs-lookup"><span data-stu-id="a8ce0-106">IWMPMedia::isReadOnlyItem method</span></span>

<span data-ttu-id="a8ce0-107">**IsReadOnlyItem** 方法會傳回值，指出是否可以編輯指定之媒體專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="a8ce0-107">The **isReadOnlyItem** method returns a value indicating whether the attributes of the specified media item can be edited.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8ce0-108">語法</span><span class="sxs-lookup"><span data-stu-id="a8ce0-108">Syntax</span></span>


```CSharp
public System.Boolean isReadOnlyItem(
  System.String bstrItemName
);
```


```VB

Public Function isReadOnlyItem( _
  ByVal bstrItemName As System.String _
) As System.Boolean
Implements IWMPMedia.isReadOnlyItem
```





## <a name="parameters"></a><span data-ttu-id="a8ce0-109">參數</span><span class="sxs-lookup"><span data-stu-id="a8ce0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8ce0-110">*bstrItemName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a8ce0-110">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8ce0-111">表示媒體專案名稱的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="a8ce0-111">A **System.String** that is the name of the media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8ce0-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="a8ce0-112">Return value</span></span>

<span data-ttu-id="a8ce0-113">指出屬性是否為唯讀的 **布林** 值。</span><span class="sxs-lookup"><span data-stu-id="a8ce0-113">A **System.Boolean** value that indicates whether the attributes are read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8ce0-114">備註</span><span class="sxs-lookup"><span data-stu-id="a8ce0-114">Remarks</span></span>

<span data-ttu-id="a8ce0-115">如果屬性是唯讀的，則無法使用 **setItemInfo** 方法來設定它。</span><span class="sxs-lookup"><span data-stu-id="a8ce0-115">If an attribute is read-only, then it cannot be set with the **setItemInfo** method.</span></span> <span data-ttu-id="a8ce0-116">請注意，使用不同版本的 Windows Media Player 時，這個方法可能會針對特定屬性傳回不同的值。</span><span class="sxs-lookup"><span data-stu-id="a8ce0-116">Note that this method may return different values for a particular attribute when used with different versions of Windows Media Player.</span></span>

<span data-ttu-id="a8ce0-117">在呼叫這個方法之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="a8ce0-117">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="a8ce0-118">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="a8ce0-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a8ce0-119">範例</span><span class="sxs-lookup"><span data-stu-id="a8ce0-119">Examples</span></span>

<span data-ttu-id="a8ce0-120">下列範例會使用 **isReadOnlyItem** ，在多行文字方塊中填入目前媒體專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a8ce0-120">The following example uses **isReadOnlyItem** to fill a multi-line text box with information about the current media item.</span></span> <span data-ttu-id="a8ce0-121">程式碼會顯示目前媒體專案的每個屬性，以及指出屬性為唯讀還是讀取/寫入的文字。</span><span class="sxs-lookup"><span data-stu-id="a8ce0-121">The code displays each attribute of the current media item, along with text indicating whether the attribute is read-only or read/write.</span></span> <span data-ttu-id="a8ce0-122">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="a8ce0-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store a WMPLib.IWMPMedia3 interface to the current media item.
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Get the number of attributes in the current media item.
int attCount = player.currentMedia.attributeCount;

// Create an array to store the list of attribute information.
string[] atInfo = new string[attCount];

// Create a variable to hold each attribute name.
string atName;

// Loop through the attribute list.
for (int i = 0; i < cm.attributeCount; i++)
{
    // Get the attribute name.
    atName = cm.getAttributeName(i);

    // Test whether the attribute is read-only.
    string test = ((cm.isReadOnlyItem(atName)) ? "Read-Only" : "Read/Write");

    // Store the attribute information in the array.
    atInfo[i] = (atName + " is " + test);
}

// Display the attribute information in the text box.
rwText.Lines = atInfo;
```


```VB

' Store a WMPLib.IWMPMedia3 interface to the current media item.
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Get the number of attributes in the current media item.
Dim attCount As Integer = player.currentMedia.attributeCount

&#39; Create an array to store the list of attribute information.
Dim atInfo(attCount) As String

&#39; Create a variable to hold each attribute name.
Dim atName As String

&#39; Loop through the attribute list.
For i As Integer = 0 To (cm.attributeCount - 1)

    &#39; Get the attribute name.
    atName = cm.getAttributeName(i)

    &#39; Test whether the attribute is read-only.
    If (cm.isReadOnlyItem(atName)) Then

        atInfo(i) = (atName + &quot; is Read-Only&quot;)

    Else

        atInfo(i) = (atName + &quot; is Read/Write&quot;)

    End If

Next i

&#39; Display the attribute information in the text box.
rwText.Lines = atInfo
```





## <a name="requirements"></a><span data-ttu-id="a8ce0-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8ce0-123">Requirements</span></span>



| <span data-ttu-id="a8ce0-124">需求</span><span class="sxs-lookup"><span data-stu-id="a8ce0-124">Requirement</span></span> | <span data-ttu-id="a8ce0-125">值</span><span class="sxs-lookup"><span data-stu-id="a8ce0-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8ce0-126">版本</span><span class="sxs-lookup"><span data-stu-id="a8ce0-126">Version</span></span><br/>   | <span data-ttu-id="a8ce0-127">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="a8ce0-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a8ce0-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="a8ce0-128">Namespace</span></span><br/> | <span data-ttu-id="a8ce0-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a8ce0-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a8ce0-130">組件</span><span class="sxs-lookup"><span data-stu-id="a8ce0-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a8ce0-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="a8ce0-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8ce0-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8ce0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8ce0-133">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="a8ce0-133">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a8ce0-134">**IWMPMedia. setItemInfo (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="a8ce0-134">**IWMPMedia.setItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





