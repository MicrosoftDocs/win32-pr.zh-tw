---
title: IWMPStringCollection2 getAttributeCountByType 方法
description: GetAttributeCountByType 方法會傳回與指定的字串集合索引、屬性名稱和語言相關聯的屬性數目。
ms.assetid: 30312039-3676-4322-b6f6-fb86098bf578
keywords:
- getAttributeCountByType 方法 Windows Media Player
- getAttributeCountByType 方法 Windows Media Player，IWMPStringCollection2 介面
- IWMPStringCollection2 介面 Windows Media Player，getAttributeCountByType 方法
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getAttributeCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9bb60fdd843fb3f45b6e4e3aff444a8a915fa0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983168"
---
# <a name="iwmpstringcollection2getattributecountbytype-method"></a><span data-ttu-id="19543-106">IWMPStringCollection2：： getAttributeCountByType 方法</span><span class="sxs-lookup"><span data-stu-id="19543-106">IWMPStringCollection2::getAttributeCountByType method</span></span>

<span data-ttu-id="19543-107">**GetAttributeCountByType** 方法會傳回與指定的字串集合索引、屬性名稱和語言相關聯的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="19543-107">The **getAttributeCountByType** method returns the number of attributes associated with the specified string collection index, attribute name, and language.</span></span>

## <a name="syntax"></a><span data-ttu-id="19543-108">語法</span><span class="sxs-lookup"><span data-stu-id="19543-108">Syntax</span></span>


```CSharp
public System.Int32 getAttributeCountByType(
  System.Int32 lCollectionIndex,
  System.String bstrType,
  System.String bstrLanguage
);
```


```VB

Public Function getAttributeCountByType( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String _
) As System.Int32
Implements IWMPStringCollection2.getAttributeCountByType
```





## <a name="parameters"></a><span data-ttu-id="19543-109">參數</span><span class="sxs-lookup"><span data-stu-id="19543-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19543-110">*lCollectionIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19543-110">*lCollectionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19543-111">指定要從中取得屬性之字串收集項的以零為基底之索引的 **system.object。**</span><span class="sxs-lookup"><span data-stu-id="19543-111">The **System.Int32** specifying the zero-based index of the string collection item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="19543-112">*bstrType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19543-112">*bstrType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19543-113">表示屬性名稱的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="19543-113">The **System.String** that is the name of the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="19543-114">*bstrLanguage* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19543-114">*bstrLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19543-115">表示語言名稱的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="19543-115">The **System.String** that is the name of the language.</span></span> <span data-ttu-id="19543-116">如果值設定為 null 或零長度的字串 ( "" ) ，則會使用目前的地區設定字串。</span><span class="sxs-lookup"><span data-stu-id="19543-116">If the value is set to null or to a zero-length string (""), the current locale string is used.</span></span> <span data-ttu-id="19543-117">否則，此值必須是有效的 RFC 1766 語言字串，例如 "en-us"。</span><span class="sxs-lookup"><span data-stu-id="19543-117">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19543-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="19543-118">Return value</span></span>

<span data-ttu-id="19543-119">作為計數的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="19543-119">The **System.Int32** that is the count.</span></span>

## <a name="remarks"></a><span data-ttu-id="19543-120">備註</span><span class="sxs-lookup"><span data-stu-id="19543-120">Remarks</span></span>

<span data-ttu-id="19543-121">這個方法是用來針對指定的 **StringCollection** 專案，探索對應至特定屬性名稱的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="19543-121">This method is used to discover the number of attributes corresponding to a particular attribute name for a given **StringCollection** item.</span></span> <span data-ttu-id="19543-122">然後，您可以將索引編號傳遞給 **getItemInfoByType** 方法的第四個參數。</span><span class="sxs-lookup"><span data-stu-id="19543-122">Index numbers can then be passed to the fourth parameter of the **getItemInfoByType** method.</span></span>

<span data-ttu-id="19543-123">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="19543-123">To use this method, read access to the library is required.</span></span> <span data-ttu-id="19543-124">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="19543-124">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="19543-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="19543-125">Requirements</span></span>



| <span data-ttu-id="19543-126">需求</span><span class="sxs-lookup"><span data-stu-id="19543-126">Requirement</span></span> | <span data-ttu-id="19543-127">值</span><span class="sxs-lookup"><span data-stu-id="19543-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19543-128">版本</span><span class="sxs-lookup"><span data-stu-id="19543-128">Version</span></span><br/>   | <span data-ttu-id="19543-129">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="19543-129">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="19543-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="19543-130">Namespace</span></span><br/> | <span data-ttu-id="19543-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="19543-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="19543-132">組件</span><span class="sxs-lookup"><span data-stu-id="19543-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="19543-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="19543-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19543-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19543-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19543-135">**IWMPStringCollection2 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="19543-135">**IWMPStringCollection2 Interface (VB and C#)**</span></span>](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="19543-136">**IWMPStringCollection2. getItemInfoByType (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="19543-136">**IWMPStringCollection2.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





