---
title: GetItemInfo 方法
description: GetItemInfo 方法會抓取目前媒體專案的指定屬性值。
ms.assetid: a1ee0d40-b979-424b-bd4e-d1acf6354d8d
keywords:
- getItemInfo 方法 Windows Media Player
- getItemInfo 方法 Windows Media Player，媒體類別
- 媒體類別 Windows Media Player，getItemInfo 方法
topic_type:
- apiref
api_name:
- Media.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7e7348e73e3550ed668f6694ccfe9ed615215b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001858"
---
# <a name="mediagetiteminfo-method"></a><span data-ttu-id="37fac-106">GetItemInfo 方法</span><span class="sxs-lookup"><span data-stu-id="37fac-106">Media.getItemInfo method</span></span>

<span data-ttu-id="37fac-107">**GetItemInfo** 方法會抓取目前媒體專案的指定屬性值。</span><span class="sxs-lookup"><span data-stu-id="37fac-107">The **getItemInfo** method retrieves the value of the specified attribute for the current media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="37fac-108">語法</span><span class="sxs-lookup"><span data-stu-id="37fac-108">Syntax</span></span>


```JScript
strRetVal = Media.getItemInfo(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="37fac-109">參數</span><span class="sxs-lookup"><span data-stu-id="37fac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37fac-110">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37fac-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37fac-111">包含屬性名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="37fac-111">**String** containing the name of the attribute.</span></span> <span data-ttu-id="37fac-112">如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player [屬性參考](attribute-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="37fac-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37fac-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="37fac-113">Return value</span></span>

<span data-ttu-id="37fac-114">這個方法會傳回 **字串** ，表示指定之屬性的值。</span><span class="sxs-lookup"><span data-stu-id="37fac-114">This method returns a **String** representing the value of the specified attribute.</span></span> <span data-ttu-id="37fac-115">針對其基礎值為 **布林** 值的屬性，它會傳回字串 "true" 或 "false"。</span><span class="sxs-lookup"><span data-stu-id="37fac-115">For attributes whose underlying value is **Boolean**, it returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="37fac-116">備註</span><span class="sxs-lookup"><span data-stu-id="37fac-116">Remarks</span></span>

<span data-ttu-id="37fac-117">這個方法會抓取個別數位媒體專案的中繼資料，或屬於播放清單一部分的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="37fac-117">This method retrieves the metadata for an individual digital media item or a media item that is part of a playlist.</span></span>

<span data-ttu-id="37fac-118">**AttributeCount** 屬性包含指定 **媒體** 物件可用的屬性名稱數目。</span><span class="sxs-lookup"><span data-stu-id="37fac-118">The **attributeCount** property contains the number of attribute names available for a given **Media** object.</span></span> <span data-ttu-id="37fac-119">然後，您可以搭配 **getAttributeName** 方法使用索引編號來判斷每個可用屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="37fac-119">Index numbers can then be used with the **getAttributeName** method to determine the name of each available attribute.</span></span> <span data-ttu-id="37fac-120">可以將個別的屬性名稱傳遞給 **getItemInfo**。</span><span class="sxs-lookup"><span data-stu-id="37fac-120">Individual attribute names can be passed to **getItemInfo**.</span></span>

<span data-ttu-id="37fac-121">若要使用具有複雜值的多個值和屬性來取得屬性，請使用 **getItemInfoByType** 方法。</span><span class="sxs-lookup"><span data-stu-id="37fac-121">To retrieve attributes with multiple values and attributes with complex values, use the **getItemInfoByType** method.</span></span>

<span data-ttu-id="37fac-122">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="37fac-122">To use this method, read access to the library is required.</span></span> <span data-ttu-id="37fac-123">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="37fac-123">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="37fac-124">若要透過 UPnP 共用 Windows media library，Windows Media Player 建立內容目錄服務 (透過 UPnP 公開的 CD) 。</span><span class="sxs-lookup"><span data-stu-id="37fac-124">To share the Windows media libraries over UPnP, Windows Media Player creates a content directory service (CDS) that is exposed over UPnP.</span></span> <span data-ttu-id="37fac-125">其他裝置則可以流覽和流覽程式庫。</span><span class="sxs-lookup"><span data-stu-id="37fac-125">Other devices can then navigate and browse the libraries.</span></span>

<span data-ttu-id="37fac-126">在 Windows 7 中，應用程式可以使用 Windows Media Player [**TrackingID**](trackingid-attribute.md) 和 [**媒體**](mediatype-attribute.md) 型屬性來為 cd 中的每個專案建立物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="37fac-126">In Windows 7, an application can use the Windows Media Player [**TrackingID**](trackingid-attribute.md) and [**MediaType**](mediatype-attribute.md) attributes to construct the object ID of each item in the CDS.</span></span> <span data-ttu-id="37fac-127">請注意，在未來的 Windows 版本中，此結構可能會變更。</span><span class="sxs-lookup"><span data-stu-id="37fac-127">Note that this construction might change in future versions of Windows.</span></span> <span data-ttu-id="37fac-128">應用程式會在 **getItemInfo** 的呼叫中，傳遞 *name* 參數中的每個屬性字串。</span><span class="sxs-lookup"><span data-stu-id="37fac-128">The application passes each of these attribute strings in the *name* parameter in a call to **getItemInfo**.</span></span> <span data-ttu-id="37fac-129">**getItemInfo** 會傳回傳回值中每個屬性的值。</span><span class="sxs-lookup"><span data-stu-id="37fac-129">**getItemInfo** returns the value for each attribute in the return value.</span></span> <span data-ttu-id="37fac-130">然後，應用程式會使用下列語法來建立每個物件識別碼：</span><span class="sxs-lookup"><span data-stu-id="37fac-130">The application then uses the following syntax to construct each object ID:</span></span>

<span data-ttu-id="37fac-131">*TrackingID*。0。*MediaTypeID*</span><span class="sxs-lookup"><span data-stu-id="37fac-131">*TrackingID*.0.*MediaTypeID*</span></span>

<span data-ttu-id="37fac-132">此語法具有下列意義：</span><span class="sxs-lookup"><span data-stu-id="37fac-132">This syntax has the following meaning:</span></span>

-   <span data-ttu-id="37fac-133">*TrackingID* 是儲存在媒體專案的 Windows Media Player [**TrackingID**](trackingid-attribute.md) 屬性中的字串。</span><span class="sxs-lookup"><span data-stu-id="37fac-133">*TrackingID* is the string that is stored in the Windows Media Player [**TrackingID**](trackingid-attribute.md) attribute of the media item.</span></span>
-   <span data-ttu-id="37fac-134">*MediaTypeID* 取決於 [ [**媒體**](mediatype-attribute.md) ] 屬性的值，如下表所示：</span><span class="sxs-lookup"><span data-stu-id="37fac-134">*MediaTypeID* depends on the value of the [**MediaType**](mediatype-attribute.md) attribute, as shown in the following table:</span></span>

    | <span data-ttu-id="37fac-135">媒體屬性</span><span class="sxs-lookup"><span data-stu-id="37fac-135">MediaType attribute</span></span>                      | <span data-ttu-id="37fac-136">MediaTypeID</span><span class="sxs-lookup"><span data-stu-id="37fac-136">MediaTypeID</span></span> |
    |------------------------------------------|-------------|
    | [<span data-ttu-id="37fac-137">音訊專案</span><span class="sxs-lookup"><span data-stu-id="37fac-137">Audio Items</span></span>](audio-item-attributes.md) | <span data-ttu-id="37fac-138">4</span><span class="sxs-lookup"><span data-stu-id="37fac-138">4</span></span>           |
    | [<span data-ttu-id="37fac-139">相片專案</span><span class="sxs-lookup"><span data-stu-id="37fac-139">Photo Items</span></span>](photo-item-attributes.md) | <span data-ttu-id="37fac-140">B</span><span class="sxs-lookup"><span data-stu-id="37fac-140">B</span></span>           |
    | [<span data-ttu-id="37fac-141">影片專案</span><span class="sxs-lookup"><span data-stu-id="37fac-141">Video Items</span></span>](video-item-attributes.md) | <span data-ttu-id="37fac-142">8</span><span class="sxs-lookup"><span data-stu-id="37fac-142">8</span></span>           |

    

     

<span data-ttu-id="37fac-143">**Windows Media Player 10** 行動裝置版：媒體專案的屬性只有在播放時才能使用，除非是透過媒體集合從專案中取出。</span><span class="sxs-lookup"><span data-stu-id="37fac-143">**Windows Media Player 10 Mobile:** Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="37fac-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="37fac-144">Requirements</span></span>



| <span data-ttu-id="37fac-145">需求</span><span class="sxs-lookup"><span data-stu-id="37fac-145">Requirement</span></span> | <span data-ttu-id="37fac-146">值</span><span class="sxs-lookup"><span data-stu-id="37fac-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="37fac-147">版本</span><span class="sxs-lookup"><span data-stu-id="37fac-147">Version</span></span><br/> | <span data-ttu-id="37fac-148">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="37fac-148">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="37fac-149">DLL</span><span class="sxs-lookup"><span data-stu-id="37fac-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="37fac-150"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37fac-150"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37fac-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37fac-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37fac-152">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="37fac-152">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="37fac-153">**AttributeCount**</span><span class="sxs-lookup"><span data-stu-id="37fac-153">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="37fac-154">**GetAttributeName**</span><span class="sxs-lookup"><span data-stu-id="37fac-154">**Media.getAttributeName**</span></span>](media-getattributename.md)
</dt> <dt>

[<span data-ttu-id="37fac-155">**GetItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="37fac-155">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="37fac-156">**SetItemInfo**</span><span class="sxs-lookup"><span data-stu-id="37fac-156">**Media.setItemInfo**</span></span>](media-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="37fac-157">**讀取屬性值**</span><span class="sxs-lookup"><span data-stu-id="37fac-157">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="37fac-158">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="37fac-158">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="37fac-159">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="37fac-159">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





