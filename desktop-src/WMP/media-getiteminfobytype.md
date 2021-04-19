---
title: GetItemInfoByType 方法
description: GetItemInfoByType 方法會抓取對應到指定屬性名稱、語言和索引的屬性值。
ms.assetid: 9d3377c2-7ae8-48ce-a42e-9c965f6b79f9
keywords:
- getItemInfoByType 方法 Windows Media Player
- getItemInfoByType 方法 Windows Media Player，媒體類別
- 媒體類別 Windows Media Player，getItemInfoByType 方法
topic_type:
- apiref
api_name:
- Media.getItemInfoByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2aff2bee7641075bbac1dd04526ee751ea077a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984846"
---
# <a name="mediagetiteminfobytype-method"></a><span data-ttu-id="96eb9-106">GetItemInfoByType 方法</span><span class="sxs-lookup"><span data-stu-id="96eb9-106">Media.getItemInfoByType method</span></span>

<span data-ttu-id="96eb9-107">**GetItemInfoByType** 方法會抓取對應到指定屬性名稱、語言和索引的屬性值。</span><span class="sxs-lookup"><span data-stu-id="96eb9-107">The **getItemInfoByType** method retrieves the value of the attribute corresponding to the specified attribute name, language, and index.</span></span>

## <a name="syntax"></a><span data-ttu-id="96eb9-108">語法</span><span class="sxs-lookup"><span data-stu-id="96eb9-108">Syntax</span></span>


```JScript
retVal = Media.getItemInfoByType(
  name,
  language,
  index
)
```



## <a name="parameters"></a><span data-ttu-id="96eb9-109">參數</span><span class="sxs-lookup"><span data-stu-id="96eb9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96eb9-110">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="96eb9-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96eb9-111">包含屬性名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="96eb9-111">**String** containing the name of the attribute.</span></span> <span data-ttu-id="96eb9-112">如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player [屬性參考](attribute-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="96eb9-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="96eb9-113">*語言* \[在\]</span><span class="sxs-lookup"><span data-stu-id="96eb9-113">*language* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96eb9-114">表示語言的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="96eb9-114">**String** representing the language.</span></span> <span data-ttu-id="96eb9-115">如果值設定為 null 或 "" (空字串) 會使用目前的地區設定字串。</span><span class="sxs-lookup"><span data-stu-id="96eb9-115">If the value is set to null or "" (empty string) the current locale string is used.</span></span> <span data-ttu-id="96eb9-116">否則，此值必須是有效的 RFC 1766 語言字串，例如 "en-us"。</span><span class="sxs-lookup"><span data-stu-id="96eb9-116">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> <dt>

<span data-ttu-id="96eb9-117">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="96eb9-117">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96eb9-118">**Number** (**Long**) ，其中包含要從屬性中取出之值的以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="96eb9-118">**Number** (**long**) containing the zero-based index of the value to retrieve from the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96eb9-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="96eb9-119">Return value</span></span>

<span data-ttu-id="96eb9-120">這個方法會傳回 **數位**、 **字串**、 **MetadataPicture** 物件或 **MetadataText** 物件，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="96eb9-120">This method returns a **Number**, **String**, **MetadataPicture** object, or **MetadataText** object as indicated in the following table.</span></span>



| <span data-ttu-id="96eb9-121">屬性</span><span class="sxs-lookup"><span data-stu-id="96eb9-121">Attribute</span></span>                   | <span data-ttu-id="96eb9-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="96eb9-122">Return value</span></span>                   |
|-----------------------------|--------------------------------|
| <span data-ttu-id="96eb9-123">**SyncState**</span><span class="sxs-lookup"><span data-stu-id="96eb9-123">**SyncState**</span></span>               | <span data-ttu-id="96eb9-124">**數位** (不 **帶正負** 號的 long) </span><span class="sxs-lookup"><span data-stu-id="96eb9-124">**Number** (**unsigned long**)</span></span> |
| <span data-ttu-id="96eb9-125">**WM/歌詞 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="96eb9-125">**WM/Lyrics\_Synchronised**</span></span> | <span data-ttu-id="96eb9-126">**MetadataText** 物件</span><span class="sxs-lookup"><span data-stu-id="96eb9-126">**MetadataText** object</span></span>        |
| <span data-ttu-id="96eb9-127">**WM/圖片**</span><span class="sxs-lookup"><span data-stu-id="96eb9-127">**WM/Picture**</span></span>              | <span data-ttu-id="96eb9-128">**MetadataPicture** 物件</span><span class="sxs-lookup"><span data-stu-id="96eb9-128">**MetadataPicture** object</span></span>     |
| <span data-ttu-id="96eb9-129">**WM/UserWebURL**</span><span class="sxs-lookup"><span data-stu-id="96eb9-129">**WM/UserWebURL**</span></span>           | <span data-ttu-id="96eb9-130">**MetadataText** 物件</span><span class="sxs-lookup"><span data-stu-id="96eb9-130">**MetadataText** object</span></span>        |
| <span data-ttu-id="96eb9-131">所有其他屬性</span><span class="sxs-lookup"><span data-stu-id="96eb9-131">All other attributes</span></span>        | <span data-ttu-id="96eb9-132">**String**</span><span class="sxs-lookup"><span data-stu-id="96eb9-132">**String**</span></span>                     |



 

<span data-ttu-id="96eb9-133">若為其基礎值為 **布林** 值的屬性，這個方法會傳回字串 "true" 或 "false"。</span><span class="sxs-lookup"><span data-stu-id="96eb9-133">For attributes whose underlying value is **Boolean**, this method returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="96eb9-134">備註</span><span class="sxs-lookup"><span data-stu-id="96eb9-134">Remarks</span></span>

<span data-ttu-id="96eb9-135">這個方法會抓取個別數位媒體專案的中繼資料，或屬於播放清單一部分的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="96eb9-135">This method retrieves the metadata for an individual digital media item or a media item that is part of a playlist.</span></span>

<span data-ttu-id="96eb9-136">這個方法支援具有多個值的屬性和具有複雜值的屬性。</span><span class="sxs-lookup"><span data-stu-id="96eb9-136">This method supports attributes with multiple values and attributes with complex values.</span></span> <span data-ttu-id="96eb9-137">**GetItemInfo** 方法不支援具有多個值的屬性和具有複雜值的屬性。</span><span class="sxs-lookup"><span data-stu-id="96eb9-137">The **getItemInfo** method does not support attributes with multiple values and attributes with complex values.</span></span>

<span data-ttu-id="96eb9-138">**AttributeCount** 屬性包含指定 **媒體** 物件可用的屬性名稱數目。</span><span class="sxs-lookup"><span data-stu-id="96eb9-138">The **attributeCount** property contains the number of attribute names available for a given **Media** object.</span></span> <span data-ttu-id="96eb9-139">然後，您可以搭配 **getAttributeName** 方法使用索引編號來判斷每個可用屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="96eb9-139">Index numbers can then be used with the **getAttributeName** method to determine the name of each available attribute.</span></span> <span data-ttu-id="96eb9-140">您可以將個別的屬性名稱傳遞給 **getItemInfoByType** 的 *name* 參數。</span><span class="sxs-lookup"><span data-stu-id="96eb9-140">Individual attribute names can be passed to the *name* parameter of **getItemInfoByType**.</span></span>

<span data-ttu-id="96eb9-141">**GetAttributeCountByType** 方法會傳回對應至指定 **媒體** 物件之特定屬性名稱的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="96eb9-141">The **getAttributeCountByType** method returns the number of attributes that correspond to a particular attribute name for a given **Media** object.</span></span> <span data-ttu-id="96eb9-142">然後，您可以將索引編號傳遞給 **getItemInfoByType** 的 *index* 參數。</span><span class="sxs-lookup"><span data-stu-id="96eb9-142">Index numbers can then be passed to the *index* parameter of **getItemInfoByType**.</span></span> <span data-ttu-id="96eb9-143">例如，當數位媒體專案分類為多個內容（例如）時，這非常有用。</span><span class="sxs-lookup"><span data-stu-id="96eb9-143">This is useful when a digital media item has been categorized under multiple genres, for example.</span></span>

<span data-ttu-id="96eb9-144">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="96eb9-144">To use this method, read access to the library is required.</span></span> <span data-ttu-id="96eb9-145">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="96eb9-145">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="96eb9-146">這個方法可能會造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="96eb9-146">This method can cause errors.</span></span> <span data-ttu-id="96eb9-147">當您呼叫這個方法時，應該包含錯誤處理常式代碼。</span><span class="sxs-lookup"><span data-stu-id="96eb9-147">You should include error-handling code when you call this method.</span></span> <span data-ttu-id="96eb9-148">例如，在 JScript 中，您可以使用 [try ...] 來執行錯誤處理。 **抓住。。。finally** 結構。</span><span class="sxs-lookup"><span data-stu-id="96eb9-148">For example, in JScript you can implement error handling by using the **try...catch...finally** structure.</span></span>

<span data-ttu-id="96eb9-149">**Windows Media Player 10** 行動裝置版：不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="96eb9-149">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="96eb9-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="96eb9-150">Requirements</span></span>



| <span data-ttu-id="96eb9-151">需求</span><span class="sxs-lookup"><span data-stu-id="96eb9-151">Requirement</span></span> | <span data-ttu-id="96eb9-152">值</span><span class="sxs-lookup"><span data-stu-id="96eb9-152">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="96eb9-153">版本</span><span class="sxs-lookup"><span data-stu-id="96eb9-153">Version</span></span><br/> | <span data-ttu-id="96eb9-154">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="96eb9-154">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="96eb9-155">DLL</span><span class="sxs-lookup"><span data-stu-id="96eb9-155">DLL</span></span><br/>     | <dl> <span data-ttu-id="96eb9-156"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96eb9-156"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96eb9-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96eb9-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96eb9-158">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="96eb9-158">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="96eb9-159">**AttributeCount**</span><span class="sxs-lookup"><span data-stu-id="96eb9-159">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="96eb9-160">**GetAttributeCountByType**</span><span class="sxs-lookup"><span data-stu-id="96eb9-160">**Media.getAttributeCountByType**</span></span>](media-getattributecountbytype.md)
</dt> <dt>

[<span data-ttu-id="96eb9-161">**GetAttributeName**</span><span class="sxs-lookup"><span data-stu-id="96eb9-161">**Media.getAttributeName**</span></span>](media-getattributename.md)
</dt> <dt>

[<span data-ttu-id="96eb9-162">**GetItemInfo**</span><span class="sxs-lookup"><span data-stu-id="96eb9-162">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="96eb9-163">**SetItemInfo**</span><span class="sxs-lookup"><span data-stu-id="96eb9-163">**Media.setItemInfo**</span></span>](media-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="96eb9-164">**MetadataPicture 物件**</span><span class="sxs-lookup"><span data-stu-id="96eb9-164">**MetadataPicture Object**</span></span>](metadatapicture-object.md)
</dt> <dt>

[<span data-ttu-id="96eb9-165">**MetadataText 物件**</span><span class="sxs-lookup"><span data-stu-id="96eb9-165">**MetadataText Object**</span></span>](metadatatext-object.md)
</dt> <dt>

[<span data-ttu-id="96eb9-166">**讀取屬性值**</span><span class="sxs-lookup"><span data-stu-id="96eb9-166">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="96eb9-167">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="96eb9-167">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="96eb9-168">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="96eb9-168">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





