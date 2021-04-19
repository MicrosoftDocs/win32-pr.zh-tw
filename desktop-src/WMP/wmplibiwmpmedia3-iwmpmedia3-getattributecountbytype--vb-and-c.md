---
title: IWMPMedia3 getAttributeCountByType 方法
description: GetAttributeCountByType 方法會傳回與指定之屬性類型相關聯的屬性數目。
ms.assetid: d692635f-f9f1-4d8e-a9c5-9d7fa84f41bd
keywords:
- getAttributeCountByType 方法 Windows Media Player
- getAttributeCountByType 方法 Windows Media Player，IWMPMedia3 介面
- IWMPMedia3 介面 Windows Media Player，getAttributeCountByType 方法
topic_type:
- apiref
api_name:
- IWMPMedia3.getAttributeCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49505f9e9df8778cc2c17ba062da6700b9b8aec4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982496"
---
# <a name="iwmpmedia3getattributecountbytype-method"></a><span data-ttu-id="62751-106">IWMPMedia3：： getAttributeCountByType 方法</span><span class="sxs-lookup"><span data-stu-id="62751-106">IWMPMedia3::getAttributeCountByType method</span></span>

<span data-ttu-id="62751-107">**GetAttributeCountByType** 方法會傳回與指定之屬性類型相關聯的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="62751-107">The **getAttributeCountByType** method returns the number of attributes associated with the specified attribute type.</span></span>

## <a name="syntax"></a><span data-ttu-id="62751-108">語法</span><span class="sxs-lookup"><span data-stu-id="62751-108">Syntax</span></span>


```CSharp
public System.Int32 getAttributeCountByType(
  System.String bstrType,
  System.String bstrLanguage
);
```


```VB

Public Function getAttributeCountByType( _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String _
) As System.Int32
Implements IWMPMedia3.getAttributeCountByType
```





## <a name="parameters"></a><span data-ttu-id="62751-109">參數</span><span class="sxs-lookup"><span data-stu-id="62751-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62751-110">*bstrType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="62751-110">*bstrType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62751-111">屬於屬性型別的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="62751-111">A **System.String** that is the attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="62751-112">*bstrLanguage* \[在\]</span><span class="sxs-lookup"><span data-stu-id="62751-112">*bstrLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62751-113">表示語言的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="62751-113">A **System.String** that is the language.</span></span> <span data-ttu-id="62751-114">如果值設定為 null 或長度為零的字串 ( "" ) ，則會使用目前的地區設定字串。</span><span class="sxs-lookup"><span data-stu-id="62751-114">If the value is set to null or a zero-length string (""), the current locale string is used.</span></span> <span data-ttu-id="62751-115">否則，此值必須是有效的 RFC 1766 語言字串，例如 "en-us"。</span><span class="sxs-lookup"><span data-stu-id="62751-115">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62751-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="62751-116">Return value</span></span>

<span data-ttu-id="62751-117">此為與類型相關聯的屬性計數的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="62751-117">A **System.Int32** that is the count of attributes that are associated with the type.</span></span>

## <a name="remarks"></a><span data-ttu-id="62751-118">備註</span><span class="sxs-lookup"><span data-stu-id="62751-118">Remarks</span></span>

<span data-ttu-id="62751-119">這個方法是用來探索特定媒體專案的特定屬性名稱對應的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="62751-119">This method is used to discover the number of attributes corresponding to a particular attribute name for a given media item.</span></span> <span data-ttu-id="62751-120">然後，您可以將索引編號傳遞給 **getItemInfoByType** 方法。</span><span class="sxs-lookup"><span data-stu-id="62751-120">Index numbers can then be passed to the **getItemInfoByType** method.</span></span> <span data-ttu-id="62751-121">例如，當媒體專案已分類為多個內容時，這非常有用。</span><span class="sxs-lookup"><span data-stu-id="62751-121">This is useful, for example, when a media item has been categorized under multiple genres.</span></span>

<span data-ttu-id="62751-122">在呼叫這個方法之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="62751-122">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="62751-123">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="62751-123">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="62751-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="62751-124">Requirements</span></span>



| <span data-ttu-id="62751-125">需求</span><span class="sxs-lookup"><span data-stu-id="62751-125">Requirement</span></span> | <span data-ttu-id="62751-126">值</span><span class="sxs-lookup"><span data-stu-id="62751-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62751-127">版本</span><span class="sxs-lookup"><span data-stu-id="62751-127">Version</span></span><br/>   | <span data-ttu-id="62751-128">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="62751-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="62751-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="62751-129">Namespace</span></span><br/> | <span data-ttu-id="62751-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="62751-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="62751-131">組件</span><span class="sxs-lookup"><span data-stu-id="62751-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="62751-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="62751-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62751-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62751-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62751-134">**IWMPMedia3 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="62751-134">**IWMPMedia3 Interface (VB and C#)**</span></span>](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="62751-135">**IWMPMedia3. getItemInfoByType (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="62751-135">**IWMPMedia3.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





