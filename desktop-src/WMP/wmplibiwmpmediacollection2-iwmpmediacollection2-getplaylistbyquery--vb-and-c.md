---
title: IWMPMediaCollection2 getPlaylistByQuery 方法
description: GetPlaylistByQuery 方法會傳回 IWMPPlaylist 介面，以提供符合查詢準則之媒體專案的存取權。
ms.assetid: ebbb631f-1faa-4c89-8c1d-cc2b128126b8
keywords:
- getPlaylistByQuery 方法 Windows Media Player
- getPlaylistByQuery 方法 Windows Media Player，IWMPMediaCollection2 介面
- IWMPMediaCollection2 介面 Windows Media Player，getPlaylistByQuery 方法
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getPlaylistByQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109f6e49e77d1cfa8c6d3b45bef1d011faf21a8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000454"
---
# <a name="iwmpmediacollection2getplaylistbyquery-method"></a><span data-ttu-id="cb240-106">IWMPMediaCollection2：： getPlaylistByQuery 方法</span><span class="sxs-lookup"><span data-stu-id="cb240-106">IWMPMediaCollection2::getPlaylistByQuery method</span></span>

<span data-ttu-id="cb240-107">`getPlaylistByQuery`方法會傳回 **IWMPPlaylist** 介面，以提供符合查詢準則之媒體專案的存取權。</span><span class="sxs-lookup"><span data-stu-id="cb240-107">The `getPlaylistByQuery` method returns an **IWMPPlaylist** interface that provides access to media items that match the query conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb240-108">語法</span><span class="sxs-lookup"><span data-stu-id="cb240-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getPlaylistByQuery(
  IWMPQuery pQuery,
  System.String bstrMediaType,
  System.String bstrSortAttribute,
  System.Boolean fSortAscending
);
```


```VB

Public Function getPlaylistByQuery( _
  ByVal pQuery As IWMPQuery, _
  ByVal bstrMediaType As System.String, _
  ByVal bstrSortAttribute As System.String, _
  ByVal fSortAscending As System.Boolean _
) As IWMPPlaylist
Implements IWMPMediaCollection2.getPlaylistByQuery
```





## <a name="parameters"></a><span data-ttu-id="cb240-109">參數</span><span class="sxs-lookup"><span data-stu-id="cb240-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb240-110">*pQuery* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cb240-110">*pQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb240-111">代表查詢的 **WMPLib. IWMPQuery** 介面。</span><span class="sxs-lookup"><span data-stu-id="cb240-111">The **WMPLib.IWMPQuery** interface that represents the query.</span></span>

</dd> <dt>

<span data-ttu-id="cb240-112">*bstrMediaType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cb240-112">*bstrMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb240-113">表示媒體類型的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="cb240-113">The **System.String** that is the media type.</span></span> <span data-ttu-id="cb240-114">必須包含下列其中一個值：「音訊」、「影片」、「相片」、「播放清單」或「其他」。</span><span class="sxs-lookup"><span data-stu-id="cb240-114">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> <dt>

<span data-ttu-id="cb240-115">*bstrSortAttribute* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cb240-115">*bstrSortAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb240-116">用來排序的屬性名稱的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="cb240-116">The **System.String** that is the attribute name used for sorting.</span></span> <span data-ttu-id="cb240-117">長度為零的字串 ( "" ) 表示不套用排序。</span><span class="sxs-lookup"><span data-stu-id="cb240-117">A zero-length string ("") means no sorting is applied.</span></span>

</dd> <dt>

<span data-ttu-id="cb240-118">*fSortAscending* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cb240-118">*fSortAscending* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb240-119">此為 **布林** 值，指出播放清單是否必須以遞增順序排序。</span><span class="sxs-lookup"><span data-stu-id="cb240-119">The **System.Boolean** value that indicates whether the playlist must be sorted in ascending order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb240-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="cb240-120">Return value</span></span>

<span data-ttu-id="cb240-121">已抓取播放清單的 **WMPLib IWMPPlaylist** 介面。</span><span class="sxs-lookup"><span data-stu-id="cb240-121">A **WMPLib.IWMPPlaylist** interface for the retrieved playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb240-122">備註</span><span class="sxs-lookup"><span data-stu-id="cb240-122">Remarks</span></span>

<span data-ttu-id="cb240-123">使用 **IWMPQuery** 的複合查詢不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="cb240-123">Compound queries using **IWMPQuery** are not case sensitive.</span></span>

<span data-ttu-id="cb240-124">當 *pQuery* 參數所指定的複合查詢包含在「 **媒體** 類型」屬性上建立的條件時，就會忽略該條件。</span><span class="sxs-lookup"><span data-stu-id="cb240-124">When the compound query specified by the *pQuery* parameter contains a condition built on the **MediaType** attribute, that condition is ignored.</span></span> <span data-ttu-id="cb240-125">一律會使用 *bstrMediaType* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="cb240-125">The value for the *bstrMediaType* parameter is always used.</span></span> <span data-ttu-id="cb240-126">例如，如果複合查詢包含條件「媒體的等於音訊」，而 *bstrMediaType* 參數的值為「影片」，則產生的播放清單只會包含影片專案。</span><span class="sxs-lookup"><span data-stu-id="cb240-126">For example, if the compound query contains the condition "MediaType Equals audio" and the value for the *bstrMediaType* parameter is "video", the resulting playlist will contain only video items.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb240-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb240-127">Requirements</span></span>



| <span data-ttu-id="cb240-128">需求</span><span class="sxs-lookup"><span data-stu-id="cb240-128">Requirement</span></span> | <span data-ttu-id="cb240-129">值</span><span class="sxs-lookup"><span data-stu-id="cb240-129">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb240-130">版本</span><span class="sxs-lookup"><span data-stu-id="cb240-130">Version</span></span><br/>   | <span data-ttu-id="cb240-131">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="cb240-131">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="cb240-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="cb240-132">Namespace</span></span><br/> | <span data-ttu-id="cb240-133">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="cb240-133">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="cb240-134">組件</span><span class="sxs-lookup"><span data-stu-id="cb240-134">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cb240-135"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="cb240-135"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb240-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb240-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb240-137">**IWMPMediaCollection2 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="cb240-137">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cb240-138">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="cb240-138">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cb240-139">**IWMPQuery 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="cb240-139">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cb240-140">**媒體屬性**</span><span class="sxs-lookup"><span data-stu-id="cb240-140">**MediaType Attribute**</span></span>](mediatype-attribute.md)
</dt> </dl>

 

 





