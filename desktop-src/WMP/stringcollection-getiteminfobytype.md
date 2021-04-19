---
title: StringCollection. getItemInfoByType 方法
description: GetItemInfoByType 方法會抓取對應于指定 StringCollection 索引、名稱、語言和屬性索引的值。
ms.assetid: 32a25c69-9399-4857-84c1-143c529be58f
keywords:
- getItemInfoByType 方法 Windows Media Player
- getItemInfoByType 方法 Windows Media Player，StringCollection 類別
- StringCollection 類別 Windows Media Player，getItemInfoByType 方法
topic_type:
- apiref
api_name:
- StringCollection.getItemInfoByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4b3aa8c5bc367095765f24f19f107dd7cb986ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998602"
---
# <a name="stringcollectiongetiteminfobytype-method"></a><span data-ttu-id="403e7-106">StringCollection. getItemInfoByType 方法</span><span class="sxs-lookup"><span data-stu-id="403e7-106">StringCollection.getItemInfoByType method</span></span>

<span data-ttu-id="403e7-107">**GetItemInfoByType** 方法會抓取對應于指定 **StringCollection** 索引、名稱、語言和屬性索引的值。</span><span class="sxs-lookup"><span data-stu-id="403e7-107">The **getItemInfoByType** method retrieves the value corresponding to the specified **StringCollection** index, name, language, and attribute index.</span></span>

## <a name="syntax"></a><span data-ttu-id="403e7-108">語法</span><span class="sxs-lookup"><span data-stu-id="403e7-108">Syntax</span></span>


```JScript
retVal = StringCollection.getItemInfoByType(
  index,
  name,
  language,
  attributeIndex
)
```



## <a name="parameters"></a><span data-ttu-id="403e7-109">參數</span><span class="sxs-lookup"><span data-stu-id="403e7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="403e7-110">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="403e7-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="403e7-111">**Number** (**long**) 指定要從中取得屬性之 **StringCollection** 專案的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="403e7-111">**Number** (**long**) specifying the zero-based index of the **StringCollection** item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="403e7-112">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="403e7-112">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="403e7-113">包含屬性名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="403e7-113">**String** containing the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="403e7-114">*語言* \[在\]</span><span class="sxs-lookup"><span data-stu-id="403e7-114">*language* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="403e7-115">包含語言的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="403e7-115">**String** containing the language.</span></span> <span data-ttu-id="403e7-116">如果值設定為 null 或空字串 ( "" ) 就會使用目前的地區設定字串。</span><span class="sxs-lookup"><span data-stu-id="403e7-116">If the value is set to null or the empty string ("") the current locale string is used.</span></span> <span data-ttu-id="403e7-117">否則，此值必須是有效的 RFC 1766 語言字串，例如 "en-us"。</span><span class="sxs-lookup"><span data-stu-id="403e7-117">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> <dt>

<span data-ttu-id="403e7-118">*attributeIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="403e7-118">*attributeIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="403e7-119">**Number** (**Long**) ，其中包含要從屬性中取出之值的以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="403e7-119">**Number** (**long**) containing the zero-based index of the value to retrieve from the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="403e7-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="403e7-120">Return value</span></span>

<span data-ttu-id="403e7-121">這個方法會傳回 **數位**、 **字串**、 **MetadataPicture** 物件或 **MetadataText** 物件，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="403e7-121">This method returns a **Number**, **String**, **MetadataPicture** object, or **MetadataText** object as indicated in the following table.</span></span>



| <span data-ttu-id="403e7-122">屬性</span><span class="sxs-lookup"><span data-stu-id="403e7-122">Attribute</span></span>                   | <span data-ttu-id="403e7-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="403e7-123">Return value</span></span>                   |
|-----------------------------|--------------------------------|
| <span data-ttu-id="403e7-124">**SyncState**</span><span class="sxs-lookup"><span data-stu-id="403e7-124">**SyncState**</span></span>               | <span data-ttu-id="403e7-125">**數位** (不 **帶正負** 號的 long) </span><span class="sxs-lookup"><span data-stu-id="403e7-125">**Number** (**unsigned long**)</span></span> |
| <span data-ttu-id="403e7-126">**WM/歌詞 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="403e7-126">**WM/Lyrics\_Synchronised**</span></span> | <span data-ttu-id="403e7-127">**MetadataText** 物件</span><span class="sxs-lookup"><span data-stu-id="403e7-127">**MetadataText** object</span></span>        |
| <span data-ttu-id="403e7-128">**WM/圖片**</span><span class="sxs-lookup"><span data-stu-id="403e7-128">**WM/Picture**</span></span>              | <span data-ttu-id="403e7-129">**MetadataPicture** 物件</span><span class="sxs-lookup"><span data-stu-id="403e7-129">**MetadataPicture** object</span></span>     |
| <span data-ttu-id="403e7-130">**WM/UserWebURL**</span><span class="sxs-lookup"><span data-stu-id="403e7-130">**WM/UserWebURL**</span></span>           | <span data-ttu-id="403e7-131">**MetadataText** 物件</span><span class="sxs-lookup"><span data-stu-id="403e7-131">**MetadataText** object</span></span>        |
| <span data-ttu-id="403e7-132">所有其他屬性</span><span class="sxs-lookup"><span data-stu-id="403e7-132">All other attributes</span></span>        | <span data-ttu-id="403e7-133">String</span><span class="sxs-lookup"><span data-stu-id="403e7-133">String</span></span>                         |



 

<span data-ttu-id="403e7-134">若為其基礎值為 **布林** 值的屬性，這個方法會傳回字串 "true" 或 "false"。</span><span class="sxs-lookup"><span data-stu-id="403e7-134">For attributes whose underlying value is **Boolean**, this method returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="403e7-135">備註</span><span class="sxs-lookup"><span data-stu-id="403e7-135">Remarks</span></span>

<span data-ttu-id="403e7-136">這個方法支援具有多個值的屬性，以及具有複雜值的屬性。</span><span class="sxs-lookup"><span data-stu-id="403e7-136">This method supports attributes with multiple values, and attributes with complex values.</span></span> <span data-ttu-id="403e7-137">**GetItemInfo** 方法不支援具有多個或複雜值的屬性。</span><span class="sxs-lookup"><span data-stu-id="403e7-137">The **getItemInfo** method does not support attributes with multiple or complex values.</span></span>

<span data-ttu-id="403e7-138">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="403e7-138">To use this method, read access to the library is required.</span></span> <span data-ttu-id="403e7-139">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="403e7-139">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="403e7-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="403e7-140">Requirements</span></span>



| <span data-ttu-id="403e7-141">需求</span><span class="sxs-lookup"><span data-stu-id="403e7-141">Requirement</span></span> | <span data-ttu-id="403e7-142">值</span><span class="sxs-lookup"><span data-stu-id="403e7-142">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="403e7-143">版本</span><span class="sxs-lookup"><span data-stu-id="403e7-143">Version</span></span><br/> | <span data-ttu-id="403e7-144">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="403e7-144">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="403e7-145">DLL</span><span class="sxs-lookup"><span data-stu-id="403e7-145">DLL</span></span><br/>     | <dl> <span data-ttu-id="403e7-146"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="403e7-146"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="403e7-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="403e7-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="403e7-148">**MetadataPicture 物件**</span><span class="sxs-lookup"><span data-stu-id="403e7-148">**MetadataPicture Object**</span></span>](metadatapicture-object.md)
</dt> <dt>

[<span data-ttu-id="403e7-149">**MetadataText 物件**</span><span class="sxs-lookup"><span data-stu-id="403e7-149">**MetadataText Object**</span></span>](metadatatext-object.md)
</dt> <dt>

[<span data-ttu-id="403e7-150">**StringCollection. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="403e7-150">**StringCollection.getItemInfo**</span></span>](stringcollection-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="403e7-151">**StringCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="403e7-151">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





