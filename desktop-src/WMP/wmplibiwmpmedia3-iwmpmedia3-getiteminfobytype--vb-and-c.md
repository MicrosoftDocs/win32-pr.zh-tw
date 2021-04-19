---
title: IWMPMedia3 getItemInfoByType 方法
description: GetItemInfoByType 方法會傳回對應至指定之屬性型別和索引的屬性值。
ms.assetid: e4cf14b4-3c59-485f-a573-734a0076647b
keywords:
- getItemInfoByType 方法 Windows Media Player
- getItemInfoByType 方法 Windows Media Player，IWMPMedia3 介面
- IWMPMedia3 介面 Windows Media Player，getItemInfoByType 方法
topic_type:
- apiref
api_name:
- IWMPMedia3.getItemInfoByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f37992201d5d19397724071f8c2a4b8e851aac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977388"
---
# <a name="iwmpmedia3getiteminfobytype-method"></a><span data-ttu-id="440e5-106">IWMPMedia3：： getItemInfoByType 方法</span><span class="sxs-lookup"><span data-stu-id="440e5-106">IWMPMedia3::getItemInfoByType method</span></span>

<span data-ttu-id="440e5-107">**GetItemInfoByType** 方法會傳回對應至指定之屬性型別和索引的屬性值。</span><span class="sxs-lookup"><span data-stu-id="440e5-107">The **getItemInfoByType** method returns the value of the attribute corresponding to the specified attribute type and index.</span></span>

## <a name="syntax"></a><span data-ttu-id="440e5-108">語法</span><span class="sxs-lookup"><span data-stu-id="440e5-108">Syntax</span></span>


```CSharp
public System.Object getItemInfoByType(
  System.String bstrType,
  System.String bstrLanguage,
  System.Int32 lIndex
);
```


```VB

Public Function getItemInfoByType( _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String, _
  ByVal lIndex As System.Int32 _
) As System.Object
Implements IWMPMedia3.getItemInfoByType
```





## <a name="parameters"></a><span data-ttu-id="440e5-109">參數</span><span class="sxs-lookup"><span data-stu-id="440e5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="440e5-110">*bstrType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="440e5-110">*bstrType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="440e5-111">屬於屬性型別的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="440e5-111">A **System.String** that is the attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="440e5-112">*bstrLanguage* \[在\]</span><span class="sxs-lookup"><span data-stu-id="440e5-112">*bstrLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="440e5-113">表示語言的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="440e5-113">A **System.String** that is the language.</span></span> <span data-ttu-id="440e5-114">如果值設定為 null 或長度為零的字串 ( "" ) ，則會使用目前的地區設定字串。</span><span class="sxs-lookup"><span data-stu-id="440e5-114">If the value is set to null or a zero-length string (""), the current locale string is used.</span></span> <span data-ttu-id="440e5-115">否則，此值必須是有效的 RFC 1766 語言字串，例如 "en-us"。</span><span class="sxs-lookup"><span data-stu-id="440e5-115">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> <dt>

<span data-ttu-id="440e5-116">*lIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="440e5-116">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="440e5-117">為屬性索引的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="440e5-117">A **System.Int32** that is the attribute index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="440e5-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="440e5-118">Return value</span></span>

<span data-ttu-id="440e5-119">表示屬性值的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="440e5-119">A **System.Object** that is the value of the attribute.</span></span> <span data-ttu-id="440e5-120">要轉換此物件的類型取決於屬性的類型。</span><span class="sxs-lookup"><span data-stu-id="440e5-120">The type to cast this object to depends on the type of the attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="440e5-121">備註</span><span class="sxs-lookup"><span data-stu-id="440e5-121">Remarks</span></span>

<span data-ttu-id="440e5-122">這個方法會傳回個別數位媒體專案的中繼資料，或屬於播放清單一部分的媒體專案的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="440e5-122">This method returns the metadata for an individual digital media item or a media item that is part of a playlist.</span></span>

<span data-ttu-id="440e5-123">這個方法支援具有多個值的屬性和具有複雜值的屬性。</span><span class="sxs-lookup"><span data-stu-id="440e5-123">This method supports attributes with multiple values and attributes with complex values.</span></span> <span data-ttu-id="440e5-124">**GetItemInfo** 方法不支援具有多個值的屬性和具有複雜值的屬性。</span><span class="sxs-lookup"><span data-stu-id="440e5-124">The **getItemInfo** method does not support attributes with multiple values and attributes with complex values.</span></span>

<span data-ttu-id="440e5-125">**AttributeCount** 屬性會取得指定媒體專案可用的屬性名稱數目。</span><span class="sxs-lookup"><span data-stu-id="440e5-125">The **attributeCount** property gets the number of attribute names available for a given media item.</span></span> <span data-ttu-id="440e5-126">然後，您可以搭配 **getAttributeName** 方法使用索引編號來判斷每個可用屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="440e5-126">Index numbers can then be used with the **getAttributeName** method to determine the name of each available attribute.</span></span> <span data-ttu-id="440e5-127">您可以將個別的屬性名稱傳遞給 **getItemInfoByType** 的 *name* 參數。</span><span class="sxs-lookup"><span data-stu-id="440e5-127">Individual attribute names can be passed to the *name* parameter of **getItemInfoByType**.</span></span>

<span data-ttu-id="440e5-128">**GetAttributeCountByType** 方法會傳回對應至指定媒體專案特定屬性名稱的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="440e5-128">The **getAttributeCountByType** method returns the number of attributes that correspond to a particular attribute name for a given media item.</span></span> <span data-ttu-id="440e5-129">然後，您可以將索引編號傳遞給 **getItemInfoByType** 的 *index* 參數。</span><span class="sxs-lookup"><span data-stu-id="440e5-129">Index numbers can then be passed to the *index* parameter of **getItemInfoByType**.</span></span> <span data-ttu-id="440e5-130">例如，當媒體專案分類為多個內容時，這非常有用。</span><span class="sxs-lookup"><span data-stu-id="440e5-130">This is useful when a media item has been categorized under multiple genres, for example.</span></span>

<span data-ttu-id="440e5-131">如果媒體專案來自呼叫 [IWMPLibrary mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)所抓取的程式庫，可用屬性的集合就會與可透過呼叫 [AxWindowsMediaPlayer](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)所抓取的本機程式庫查詢的不同。</span><span class="sxs-lookup"><span data-stu-id="440e5-131">If the media item came from a library that was retrieved by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), the set of available attributes will differ from those which can be queried from the local library retrieved by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md).</span></span> <span data-ttu-id="440e5-132">例如，使用 **IWMPLibrary** 抓取的本機程式庫中所提供的屬性，將會是使用 **AxWindowsMediaPlayer** 抓取之本機程式庫中可用屬性的子集。</span><span class="sxs-lookup"><span data-stu-id="440e5-132">For example, the attributes available from the local library retrieved by using **IWMPLibrary** will be a subset of the attributes available from the local library retrieved by using **AxWindowsMediaPlayer**.</span></span> <span data-ttu-id="440e5-133">其他來源的可用屬性集 (遠端程式庫、可攜式裝置或 Cd 是由其他來源所定義。</span><span class="sxs-lookup"><span data-stu-id="440e5-133">The set of attributes available from other sources (remote libraries, portable devices, or CDs is defined by the other sources.</span></span>

<span data-ttu-id="440e5-134">在呼叫這個方法之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="440e5-134">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="440e5-135">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="440e5-135">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="440e5-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="440e5-136">Requirements</span></span>



| <span data-ttu-id="440e5-137">需求</span><span class="sxs-lookup"><span data-stu-id="440e5-137">Requirement</span></span> | <span data-ttu-id="440e5-138">值</span><span class="sxs-lookup"><span data-stu-id="440e5-138">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="440e5-139">版本</span><span class="sxs-lookup"><span data-stu-id="440e5-139">Version</span></span><br/>   | <span data-ttu-id="440e5-140">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="440e5-140">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="440e5-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="440e5-141">Namespace</span></span><br/> | <span data-ttu-id="440e5-142">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="440e5-142">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="440e5-143">組件</span><span class="sxs-lookup"><span data-stu-id="440e5-143">Assembly</span></span><br/>  | <dl> <span data-ttu-id="440e5-144"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="440e5-144"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="440e5-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="440e5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="440e5-146">**IWMPMedia3 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="440e5-146">**IWMPMedia3 Interface (VB and C#)**</span></span>](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="440e5-147">**IWMPMedia. attributeCount (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="440e5-147">**IWMPMedia.attributeCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="440e5-148">**IWMPMedia. getAttributeName (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="440e5-148">**IWMPMedia.getAttributeName (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="440e5-149">**IWMPMedia. getItemInfo (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="440e5-149">**IWMPMedia.getItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="440e5-150">**IWMPMedia3. getAttributeCountByType (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="440e5-150">**IWMPMedia3.getAttributeCountByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getattributecountbytype--vb-and-c.md)
</dt> </dl>

 

 





