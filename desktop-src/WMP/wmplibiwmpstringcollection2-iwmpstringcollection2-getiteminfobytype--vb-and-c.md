---
title: IWMPStringCollection2 getItemInfobyType 方法
description: GetItemInfoByType 方法會傳回對應至指定之字串集合專案索引、名稱、語言和屬性索引的值。
ms.assetid: 51035fed-51ce-4cd2-a936-4c99802128f2
keywords:
- getItemInfobyType 方法 Windows Media Player
- getItemInfobyType 方法 Windows Media Player，IWMPStringCollection2 介面
- IWMPStringCollection2 介面 Windows Media Player，getItemInfobyType 方法
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getItemInfobyType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e227d6471ecf41c8f48420ded61c6f4e7eaac8cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996245"
---
# <a name="iwmpstringcollection2getiteminfobytype-method"></a><span data-ttu-id="b30e1-106">IWMPStringCollection2：： getItemInfobyType 方法</span><span class="sxs-lookup"><span data-stu-id="b30e1-106">IWMPStringCollection2::getItemInfobyType method</span></span>

<span data-ttu-id="b30e1-107">**GetItemInfoByType** 方法會傳回對應至指定之字串集合專案索引、名稱、語言和屬性索引的值。</span><span class="sxs-lookup"><span data-stu-id="b30e1-107">The **getItemInfoByType** method returns the value corresponding to the specified string collection item index, name, language, and attribute index.</span></span>

## <a name="syntax"></a><span data-ttu-id="b30e1-108">語法</span><span class="sxs-lookup"><span data-stu-id="b30e1-108">Syntax</span></span>


```CSharp
public System.Object getItemInfobyType(
  System.Int32 lCollectionIndex,
  System.String bstrType,
  System.String bstrLanguage,
  System.Int32 lAttributeIndex
);
```


```VB

Public Function getItemInfobyType( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String, _
  ByVal lAttributeIndex As System.Int32 _
) As System.Object
Implements IWMPStringCollection2.getItemInfobyType
```





## <a name="parameters"></a><span data-ttu-id="b30e1-109">參數</span><span class="sxs-lookup"><span data-stu-id="b30e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b30e1-110">*lCollectionIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b30e1-110">*lCollectionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b30e1-111">要從中取得屬性之字串收集項的以零為基底之索引的 **system.object。**</span><span class="sxs-lookup"><span data-stu-id="b30e1-111">The **System.Int32** that is the zero-based index of the string collection item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="b30e1-112">*bstrType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b30e1-112">*bstrType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b30e1-113">做為屬性名稱的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="b30e1-113">The **System.String** that is the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="b30e1-114">*bstrLanguage* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b30e1-114">*bstrLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b30e1-115">表示語言的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="b30e1-115">The **System.String** that indicates the language.</span></span> <span data-ttu-id="b30e1-116">如果值設定為 null 或零長度的字串 ( "" ) ，則會使用目前的地區設定字串。</span><span class="sxs-lookup"><span data-stu-id="b30e1-116">If the value is set to null or to a zero-length string (""), the current locale string is used.</span></span> <span data-ttu-id="b30e1-117">否則，此值必須是有效的 RFC 1766 語言字串，例如 "en-us"。</span><span class="sxs-lookup"><span data-stu-id="b30e1-117">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> <dt>

<span data-ttu-id="b30e1-118">*lAttributeIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b30e1-118">*lAttributeIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b30e1-119">以零為基底的屬性索引的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="b30e1-119">A **System.Int32** that is the zero-based index of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b30e1-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="b30e1-120">Return value</span></span>

<span data-ttu-id="b30e1-121">表示字串收集項目的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="b30e1-121">A **System.Object** that is the string collection item.</span></span>

## <a name="remarks"></a><span data-ttu-id="b30e1-122">備註</span><span class="sxs-lookup"><span data-stu-id="b30e1-122">Remarks</span></span>

<span data-ttu-id="b30e1-123">這個方法支援具有多個值的屬性和具有複雜值的屬性。</span><span class="sxs-lookup"><span data-stu-id="b30e1-123">This method supports attributes with multiple values and attributes with complex values.</span></span> <span data-ttu-id="b30e1-124">**GetItemInfo** 方法不支援具有多個值的屬性或具有複雜值的屬性。</span><span class="sxs-lookup"><span data-stu-id="b30e1-124">The **getItemInfo** method does not support attributes with multiple values or attributes with complex values.</span></span>

<span data-ttu-id="b30e1-125">藉由在 *bstrType* 參數中傳遞 "ChildList" 值，您就可以取出新的字串集合，其中包含父字串集合中其中一個專案的子系。</span><span class="sxs-lookup"><span data-stu-id="b30e1-125">By passing the value "ChildList" in the *bstrType* parameter, you can retrieve a new string collection that contains the children of one of the items in the parent string collection.</span></span> <span data-ttu-id="b30e1-126">比方說，如果父集合包含 AlbumIDs 的清單，您可以使用這個方法來取得子字串集合，其中包含其中一個專輯的所有追蹤。</span><span class="sxs-lookup"><span data-stu-id="b30e1-126">For instance, if the parent collection contains a list of AlbumIDs, you can use this method to obtain a child string collection that contains all the tracks for one of the albums.</span></span> <span data-ttu-id="b30e1-127">這種方法比呼叫 **IWMPMediaCollection2. getStringCollectionByQuery** 方法兩次更快且更有效率;一次是取得 AlbumIDs 的集合，而第二次是取得特定 AlbumID 的追蹤集合。</span><span class="sxs-lookup"><span data-stu-id="b30e1-127">This approach is faster and more efficient than calling the **IWMPMediaCollection2.getStringCollectionByQuery** method twice; once to get a collection of AlbumIDs, and a second time to get a collection of tracks for a particular AlbumID.</span></span> <span data-ttu-id="b30e1-128">若要在剛剛描述的方式中使用 ChildList，必須透過 **IWMPLibraryServices** 從媒體集合取得父字串集合，而不是使用 **AxWindowsMediaPlayer. mediaCollection** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b30e1-128">To use ChildList in the way just described, the parent string collection must be obtained from a media collection through **IWMPLibraryServices**, and not by using the **AxWindowsMediaPlayer.mediaCollection** property.</span></span>

<span data-ttu-id="b30e1-129">使用 ChildList 時，請在 *bstrType* 參數中傳遞值 "ChildList"，並在 *lAttributeIndex* 參數中傳遞值0。</span><span class="sxs-lookup"><span data-stu-id="b30e1-129">When using ChildList, pass the value "ChildList" in the *bstrType* parameter, and the value 0 in the *lAttributeIndex* parameter.</span></span> <span data-ttu-id="b30e1-130">然後，您可以將傳回的物件轉換成 **IWMPStringCollection2** 介面，以存取子清單。</span><span class="sxs-lookup"><span data-stu-id="b30e1-130">You can then cast the object that is returned to an **IWMPStringCollection2** interface to access the child list.</span></span>

<span data-ttu-id="b30e1-131">若要使用這個方法，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="b30e1-131">To use this method, you must have read access to the library.</span></span> <span data-ttu-id="b30e1-132">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="b30e1-132">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b30e1-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="b30e1-133">Requirements</span></span>



| <span data-ttu-id="b30e1-134">需求</span><span class="sxs-lookup"><span data-stu-id="b30e1-134">Requirement</span></span> | <span data-ttu-id="b30e1-135">值</span><span class="sxs-lookup"><span data-stu-id="b30e1-135">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b30e1-136">版本</span><span class="sxs-lookup"><span data-stu-id="b30e1-136">Version</span></span><br/>   | <span data-ttu-id="b30e1-137">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="b30e1-137">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="b30e1-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="b30e1-138">Namespace</span></span><br/> | <span data-ttu-id="b30e1-139">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b30e1-139">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b30e1-140">組件</span><span class="sxs-lookup"><span data-stu-id="b30e1-140">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b30e1-141"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="b30e1-141"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b30e1-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b30e1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b30e1-143">**AlbumID 屬性**</span><span class="sxs-lookup"><span data-stu-id="b30e1-143">**AlbumID Attribute**</span></span>](albumid-attribute.md)
</dt> <dt>

[<span data-ttu-id="b30e1-144">**IWMPLibraryServices 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b30e1-144">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b30e1-145">**IWMPMediaCollection2. getStringCollectionByQuery (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b30e1-145">**IWMPMediaCollection2.getStringCollectionByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b30e1-146">**IWMPStringCollection2 介面**</span><span class="sxs-lookup"><span data-stu-id="b30e1-146">**IWMPStringCollection2 Interface**</span></span>](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b30e1-147">**IWMPStringCollection2. getItemInfo (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b30e1-147">**IWMPStringCollection2.getItemInfo (VB and C#)**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 





