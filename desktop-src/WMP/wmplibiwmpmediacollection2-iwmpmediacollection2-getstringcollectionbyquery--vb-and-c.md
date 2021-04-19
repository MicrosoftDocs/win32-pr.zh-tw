---
title: IWMPMediaCollection2 getStringCollectionByQuery 方法
description: GetStringCollectionByQuery 方法會傳回 IWMPStringCollection 介面，此介面可讓您存取符合查詢準則之指定屬性的所有字串值集。
ms.assetid: 2d3b29af-0b6c-4405-8334-9a47a30ff6de
keywords:
- getStringCollectionByQuery 方法 Windows Media Player
- getStringCollectionByQuery 方法 Windows Media Player，IWMPMediaCollection2 介面
- IWMPMediaCollection2 介面 Windows Media Player，getStringCollectionByQuery 方法
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getStringCollectionByQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 322781bc9ddec3e6f8d74d7229f16ce38e519f05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994743"
---
# <a name="iwmpmediacollection2getstringcollectionbyquery-method"></a><span data-ttu-id="49633-106">IWMPMediaCollection2：： getStringCollectionByQuery 方法</span><span class="sxs-lookup"><span data-stu-id="49633-106">IWMPMediaCollection2::getStringCollectionByQuery method</span></span>

<span data-ttu-id="49633-107">`getStringCollectionByQuery`方法會傳回 **IWMPStringCollection** 介面，此介面可讓您存取符合查詢準則之指定屬性的所有字串值集。</span><span class="sxs-lookup"><span data-stu-id="49633-107">The `getStringCollectionByQuery` method returns an **IWMPStringCollection** interface that provides access to the set of all string values for a specified attribute that match the query conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="49633-108">語法</span><span class="sxs-lookup"><span data-stu-id="49633-108">Syntax</span></span>


```CSharp
public IWMPStringCollection getStringCollectionByQuery(
  System.String bstrAttribute,
  IWMPQuery pQuery,
  System.String bstrMediaType,
  System.String bstrSortAttribute,
  System.Boolean fSortAscending
);
```


```VB

Public Function getStringCollectionByQuery( _
  ByVal bstrAttribute As System.String, _
  ByVal pQuery As IWMPQuery, _
  ByVal bstrMediaType As System.String, _
  ByVal bstrSortAttribute As System.String, _
  ByVal fSortAscending As System.Boolean _
) As IWMPStringCollection
Implements IWMPMediaCollection2.getStringCollectionByQuery
```





## <a name="parameters"></a><span data-ttu-id="49633-109">參數</span><span class="sxs-lookup"><span data-stu-id="49633-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49633-110">*bstrAttribute* \[在\]</span><span class="sxs-lookup"><span data-stu-id="49633-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49633-111">做為屬性名稱的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="49633-111">The **System.String** that is the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="49633-112">*pQuery* \[在\]</span><span class="sxs-lookup"><span data-stu-id="49633-112">*pQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49633-113">**WMPLib. IWMPQuery** 介面，這個介面會定義用來取出字串集合的條件。</span><span class="sxs-lookup"><span data-stu-id="49633-113">The **WMPLib.IWMPQuery** interface that is the query that defines the conditions used to retrieve the string collection.</span></span>

</dd> <dt>

<span data-ttu-id="49633-114">*bstrMediaType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="49633-114">*bstrMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49633-115">表示媒體類型的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="49633-115">The **System.String** that is the media type.</span></span> <span data-ttu-id="49633-116">必須包含下列其中一個值：「音訊」、「影片」、「相片」、「播放清單」或「其他」。</span><span class="sxs-lookup"><span data-stu-id="49633-116">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> <dt>

<span data-ttu-id="49633-117">*bstrSortAttribute* \[在\]</span><span class="sxs-lookup"><span data-stu-id="49633-117">*bstrSortAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49633-118">用來排序的屬性名稱的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="49633-118">The **System.String** that is the attribute name used for sorting.</span></span> <span data-ttu-id="49633-119">長度為零的字串 ( "" ) 表示不套用排序。</span><span class="sxs-lookup"><span data-stu-id="49633-119">A zero-length string ("") means no sorting is applied.</span></span>

</dd> <dt>

<span data-ttu-id="49633-120">*fSortAscending* \[在\]</span><span class="sxs-lookup"><span data-stu-id="49633-120">*fSortAscending* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49633-121">此為 **布林** 值，指出字串值集是否必須以遞增順序排序。</span><span class="sxs-lookup"><span data-stu-id="49633-121">The **System.Boolean** value that indicates whether the set of string values must be sorted in ascending order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49633-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="49633-122">Return value</span></span>

<span data-ttu-id="49633-123">已抓取之字串值集的 **WMPLib IWMPStringCollection** 介面。</span><span class="sxs-lookup"><span data-stu-id="49633-123">A **WMPLib.IWMPStringCollection** interface for the retrieved set of string values.</span></span>

## <a name="remarks"></a><span data-ttu-id="49633-124">備註</span><span class="sxs-lookup"><span data-stu-id="49633-124">Remarks</span></span>

<span data-ttu-id="49633-125">使用 **IWMPQuery** 的複合查詢不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="49633-125">Compound queries using **IWMPQuery** are not case sensitive.</span></span>

<span data-ttu-id="49633-126">當 *pQuery* 參數所指定的複合查詢包含在「 **媒體** 類型」屬性上建立的條件時，就會忽略該條件。</span><span class="sxs-lookup"><span data-stu-id="49633-126">When the compound query specified by the *pQuery* parameter contains a condition built on the **MediaType** attribute, that condition is ignored.</span></span> <span data-ttu-id="49633-127">一律會使用 *bstrMediaType* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="49633-127">The value for the *bstrMediaType* parameter is always used.</span></span> <span data-ttu-id="49633-128">例如，如果複合查詢包含條件「媒體的等於音訊」，而 *bstrMediaType* 參數的值為「影片」，則產生的播放清單只會包含影片專案。</span><span class="sxs-lookup"><span data-stu-id="49633-128">For example, if the compound query contains the condition "MediaType Equals audio" and the value for the *bstrMediaType* parameter is "video", the resulting playlist will contain only video items.</span></span>

## <a name="requirements"></a><span data-ttu-id="49633-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="49633-129">Requirements</span></span>



| <span data-ttu-id="49633-130">需求</span><span class="sxs-lookup"><span data-stu-id="49633-130">Requirement</span></span> | <span data-ttu-id="49633-131">值</span><span class="sxs-lookup"><span data-stu-id="49633-131">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49633-132">版本</span><span class="sxs-lookup"><span data-stu-id="49633-132">Version</span></span><br/>   | <span data-ttu-id="49633-133">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="49633-133">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="49633-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="49633-134">Namespace</span></span><br/> | <span data-ttu-id="49633-135">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="49633-135">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="49633-136">組件</span><span class="sxs-lookup"><span data-stu-id="49633-136">Assembly</span></span><br/>  | <dl> <span data-ttu-id="49633-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="49633-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49633-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49633-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49633-139">**IWMPMediaCollection2 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="49633-139">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="49633-140">**IWMPQuery 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="49633-140">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="49633-141">**IWMPStringCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="49633-141">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="49633-142">**媒體屬性**</span><span class="sxs-lookup"><span data-stu-id="49633-142">**MediaType Attribute**</span></span>](mediatype-attribute.md)
</dt> </dl>

 

 





