---
title: IWMPMedia attributeCount 屬性
description: AttributeCount 屬性會取得可針對媒體專案查詢及/或設定的屬性數目。
ms.assetid: 527298ff-365d-41b0-90dd-e236d6adf6fa
keywords:
- attributeCount 屬性 Windows Media Player
- attributeCount 屬性 Windows Media Player，IWMPMedia 介面
- IWMPMedia 介面 Windows Media Player，attributeCount 屬性
topic_type:
- apiref
api_name:
- IWMPMedia.attributeCount
- IWMPMedia.get_attributeCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5a56d06a54590afd315f04a90aa582f3a364db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991203"
---
# <a name="iwmpmediaattributecount-property"></a><span data-ttu-id="a28cc-106">IWMPMedia：： attributeCount 屬性</span><span class="sxs-lookup"><span data-stu-id="a28cc-106">IWMPMedia::attributeCount property</span></span>

<span data-ttu-id="a28cc-107">**AttributeCount** 屬性會取得可針對媒體專案查詢及/或設定的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="a28cc-107">The **attributeCount** property gets the number of attributes that can be queried and/or set for the media item.</span></span>

<span data-ttu-id="a28cc-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="a28cc-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a28cc-109">語法</span><span class="sxs-lookup"><span data-stu-id="a28cc-109">Syntax</span></span>


```CSharp
public System.Int32 attributeCount {get;}
```


```VB

Public ReadOnly Property attributeCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="a28cc-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="a28cc-110">Property value</span></span>

<span data-ttu-id="a28cc-111">作為計數的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="a28cc-111">A **System.Int32** that is the count.</span></span>

## <a name="remarks"></a><span data-ttu-id="a28cc-112">備註</span><span class="sxs-lookup"><span data-stu-id="a28cc-112">Remarks</span></span>

<span data-ttu-id="a28cc-113">使用這個屬性之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="a28cc-113">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="a28cc-114">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="a28cc-114">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="a28cc-115">如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 [屬性參考](attribute-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="a28cc-115">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a28cc-116">範例</span><span class="sxs-lookup"><span data-stu-id="a28cc-116">Examples</span></span>

<span data-ttu-id="a28cc-117">下列範例會使用 **attributeCount** 來判斷目前媒體專案中可用的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="a28cc-117">The following example uses **attributeCount** to determine the number of attributes available in the current media item.</span></span> <span data-ttu-id="a28cc-118">程式碼會使用該值來顯示文字方塊中的屬性名稱和值清單。</span><span class="sxs-lookup"><span data-stu-id="a28cc-118">The code uses that value to display a list of attribute names and values in a text box.</span></span> <span data-ttu-id="a28cc-119">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="a28cc-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store an IWMPMedia3 interface to the current media item. 
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Store the number of attributes in the current media item using attributeCount.
int numAttributes = cm.attributeCount;

// Create strings to hold each attribute name and value.
string atName;
string atValue;

// Create an array to hold the attribute list.
string [] atList = new string[numAttributes];

// Loop through the attribute list.   
for (int i = 0; i < numAttributes; i++)
{
    // Fill the strings with the attribute information.
    atName = cm.getAttributeName(i);
    atValue = cm.getItemInfo(atName);

    // Store the attribute information in an array.
    atList[i] = (atName + ": " + atValue);
}

// Display the attribute information in the text box.
attributeList.Lines = atList;
```


```VB

' Store an IWMPMedia3 interface to the current media item. 
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Store the number of attributes in the current media item using attributeCount.
Dim numAttributes As Integer = cm.attributeCount

&#39; Create strings to hold each attribute name and value.
Dim atName As String
Dim atValue As String

&#39; Create an array to hold the attribute list.
Dim atList(numAttributes) As String

&#39; Loop through the attribute list.   
For i As Integer = 0 To (numAttributes - 1)

    &#39; Fill the strings with the attribute information.
    atName = cm.getAttributeName(i)
    atValue = cm.getItemInfo(atName)

    &#39; Store the attribute information in an array.
    atList(i) = (atName + &quot;: &quot; + atValue)

Next i

&#39; Display the attribute information in the text box.
attributeList.Lines = atList
```





## <a name="requirements"></a><span data-ttu-id="a28cc-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="a28cc-120">Requirements</span></span>



| <span data-ttu-id="a28cc-121">需求</span><span class="sxs-lookup"><span data-stu-id="a28cc-121">Requirement</span></span> | <span data-ttu-id="a28cc-122">值</span><span class="sxs-lookup"><span data-stu-id="a28cc-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a28cc-123">版本</span><span class="sxs-lookup"><span data-stu-id="a28cc-123">Version</span></span><br/>   | <span data-ttu-id="a28cc-124">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="a28cc-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a28cc-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="a28cc-125">Namespace</span></span><br/> | <span data-ttu-id="a28cc-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a28cc-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a28cc-127">組件</span><span class="sxs-lookup"><span data-stu-id="a28cc-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a28cc-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="a28cc-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a28cc-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a28cc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a28cc-130">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="a28cc-130">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





