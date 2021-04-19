---
title: IWMPMedia getAttributeName 方法
description: GetAttributeName 方法會傳回對應至指定之索引的屬性名稱。
ms.assetid: d2496484-34cc-4222-9bc3-1d3ebb9a4173
keywords:
- getAttributeName 方法 Windows Media Player
- getAttributeName 方法 Windows Media Player，IWMPMedia 介面
- IWMPMedia 介面 Windows Media Player，getAttributeName 方法
topic_type:
- apiref
api_name:
- IWMPMedia.getAttributeName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb40ef8c0c984258dc11dd00c80807db2f4eb64a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997738"
---
# <a name="iwmpmediagetattributename-method"></a><span data-ttu-id="d43c2-106">IWMPMedia：： getAttributeName 方法</span><span class="sxs-lookup"><span data-stu-id="d43c2-106">IWMPMedia::getAttributeName method</span></span>

<span data-ttu-id="d43c2-107">**GetAttributeName** 方法會傳回對應至指定之索引的屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="d43c2-107">The **getAttributeName** method returns the name of the attribute corresponding to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="d43c2-108">語法</span><span class="sxs-lookup"><span data-stu-id="d43c2-108">Syntax</span></span>


```CSharp
public System.String getAttributeName(
  System.Int32 lIndex
);
```


```VB

Public Function getAttributeName( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPMedia.getAttributeName
```





## <a name="parameters"></a><span data-ttu-id="d43c2-109">參數</span><span class="sxs-lookup"><span data-stu-id="d43c2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d43c2-110">*lIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d43c2-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d43c2-111">作為索引的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="d43c2-111">A **System.Int32** that is the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d43c2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d43c2-112">Return value</span></span>

<span data-ttu-id="d43c2-113">表示屬性名稱的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="d43c2-113">A **System.String** that is the attribute name.</span></span>

## <a name="remarks"></a><span data-ttu-id="d43c2-114">備註</span><span class="sxs-lookup"><span data-stu-id="d43c2-114">Remarks</span></span>

<span data-ttu-id="d43c2-115">傳回的屬性名稱可以與 **getItemInfo** 搭配使用，以抓取特定命名屬性的值。</span><span class="sxs-lookup"><span data-stu-id="d43c2-115">The attribute name returned can be used in conjunction with **getItemInfo** to retrieve the value for a specific named attribute.</span></span>

<span data-ttu-id="d43c2-116">在呼叫這個方法之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="d43c2-116">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="d43c2-117">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="d43c2-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="d43c2-118">如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 [屬性參考](attribute-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="d43c2-118">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d43c2-119">範例</span><span class="sxs-lookup"><span data-stu-id="d43c2-119">Examples</span></span>

<span data-ttu-id="d43c2-120">下列範例會使用 **getAttributeName** ，在多行文字方塊中填入目前媒體專案的每個屬性的索引和名稱。</span><span class="sxs-lookup"><span data-stu-id="d43c2-120">The following example uses **getAttributeName** to fill a multi-line text box with the index and name of each attribute for the current media item.</span></span> <span data-ttu-id="d43c2-121">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="d43c2-121">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store an IWMPMedia3 interface for the current media item. 
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Get the number of attributes for the current media item. 
int attCount = cm.attributeCount;

// Create an array of strings to hold the index and name for each attribute.
string[] attInfo = new string[attCount];

// Loop through the attribute list.
for (int i = 0; i < attCount; i++)
{
    // Store the attribute index and name in the array.
    attInfo[i] = ("Attribute " + i + ": " + cm.getAttributeName(i));
}

// Display the attribute information in the text box.
attributeNames.Lines = attInfo;
```


```VB

' Store an IWMPMedia3 interface for the current media item. 
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Get the number of attributes for the current media. 
Dim attCount As Integer = cm.attributeCount

&#39; Create an array of strings to hold the index and name for each attribute.
Dim attInfo(attCount) As String

&#39; Loop through the attribute list.
For i As Integer = 0 To (attCount - 1)

    &#39; Store the attribute index and name in the array.
    attInfo(i) = (&quot;Attribute &quot; + i.ToString() + &quot;: &quot; + cm.getAttributeName(i))

Next i

&#39; Display the attribute information in the text box.
attributeNames.Lines = attInfo
```





## <a name="requirements"></a><span data-ttu-id="d43c2-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="d43c2-122">Requirements</span></span>



| <span data-ttu-id="d43c2-123">需求</span><span class="sxs-lookup"><span data-stu-id="d43c2-123">Requirement</span></span> | <span data-ttu-id="d43c2-124">值</span><span class="sxs-lookup"><span data-stu-id="d43c2-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d43c2-125">版本</span><span class="sxs-lookup"><span data-stu-id="d43c2-125">Version</span></span><br/>   | <span data-ttu-id="d43c2-126">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="d43c2-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d43c2-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="d43c2-127">Namespace</span></span><br/> | <span data-ttu-id="d43c2-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d43c2-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d43c2-129">組件</span><span class="sxs-lookup"><span data-stu-id="d43c2-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d43c2-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="d43c2-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d43c2-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d43c2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d43c2-132">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d43c2-132">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d43c2-133">**IWMPMedia. getItemInfo (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d43c2-133">**IWMPMedia.getItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 





