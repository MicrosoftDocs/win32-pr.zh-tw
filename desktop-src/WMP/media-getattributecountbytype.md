---
title: GetAttributeCountByType 方法
description: GetAttributeCountByType 方法會抓取與指定的屬性名稱和語言相關聯的屬性數目。
ms.assetid: 5644e823-a9b1-4b02-9dd6-015e524fde64
keywords:
- getAttributeCountByType 方法 Windows Media Player
- getAttributeCountByType 方法 Windows Media Player，媒體類別
- 媒體類別 Windows Media Player，getAttributeCountByType 方法
topic_type:
- apiref
api_name:
- Media.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 613dca43c32322cd5e7de2b2b04605789009cbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993640"
---
# <a name="mediagetattributecountbytype-method"></a><span data-ttu-id="b44ea-106">GetAttributeCountByType 方法</span><span class="sxs-lookup"><span data-stu-id="b44ea-106">Media.getAttributeCountByType method</span></span>

<span data-ttu-id="b44ea-107">**GetAttributeCountByType** 方法會抓取與指定的屬性名稱和語言相關聯的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="b44ea-107">The **getAttributeCountByType** method retrieves the number of attributes associated with the specified attribute name and language.</span></span>

## <a name="syntax"></a><span data-ttu-id="b44ea-108">語法</span><span class="sxs-lookup"><span data-stu-id="b44ea-108">Syntax</span></span>


```JScript
retVal = Media.getAttributeCountByType(
  name,
  language
)
```



## <a name="parameters"></a><span data-ttu-id="b44ea-109">參數</span><span class="sxs-lookup"><span data-stu-id="b44ea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b44ea-110">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b44ea-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b44ea-111">包含屬性名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="b44ea-111">**String** containing the name of the attribute.</span></span> <span data-ttu-id="b44ea-112">如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player [屬性參考](attribute-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="b44ea-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="b44ea-113">*語言* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b44ea-113">*language* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b44ea-114">表示語言的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="b44ea-114">**String** representing the language.</span></span> <span data-ttu-id="b44ea-115">如果值設定為 null 或 "" (空白字串) ，則會使用目前的地區設定字串。</span><span class="sxs-lookup"><span data-stu-id="b44ea-115">If the value is set to null or "" (empty string), the current locale string is used.</span></span> <span data-ttu-id="b44ea-116">否則，此值必須是有效的 RFC 1766 語言字串，例如 "en-us"。</span><span class="sxs-lookup"><span data-stu-id="b44ea-116">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b44ea-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="b44ea-117">Return value</span></span>

<span data-ttu-id="b44ea-118">這個方法會傳回 **數位** (**long**) 包含屬性計數。</span><span class="sxs-lookup"><span data-stu-id="b44ea-118">This method returns a **Number** (**long**) containing the attribute count.</span></span>

## <a name="remarks"></a><span data-ttu-id="b44ea-119">備註</span><span class="sxs-lookup"><span data-stu-id="b44ea-119">Remarks</span></span>

<span data-ttu-id="b44ea-120">這個方法是用來判斷對應至指定 **媒體** 物件之特定屬性名稱的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="b44ea-120">This method is used to determine the number of attributes corresponding to a particular attribute name for a given **Media** object.</span></span> <span data-ttu-id="b44ea-121">然後，您可以將索引編號傳遞給 **getItemInfoByType** 方法。</span><span class="sxs-lookup"><span data-stu-id="b44ea-121">Index numbers can then be passed to the **getItemInfoByType** method.</span></span> <span data-ttu-id="b44ea-122">例如，當媒體專案已分類為多個內容時，這非常有用。</span><span class="sxs-lookup"><span data-stu-id="b44ea-122">This is useful, for example, when a media item has been categorized under multiple genres.</span></span>

<span data-ttu-id="b44ea-123">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="b44ea-123">To use this method, read access to the library is required.</span></span> <span data-ttu-id="b44ea-124">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="b44ea-124">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="b44ea-125">**Windows Media Player 10** 行動裝置版：此屬性一律會傳回0。</span><span class="sxs-lookup"><span data-stu-id="b44ea-125">**Windows Media Player 10 Mobile:** This property always returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="b44ea-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="b44ea-126">Requirements</span></span>



| <span data-ttu-id="b44ea-127">需求</span><span class="sxs-lookup"><span data-stu-id="b44ea-127">Requirement</span></span> | <span data-ttu-id="b44ea-128">值</span><span class="sxs-lookup"><span data-stu-id="b44ea-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b44ea-129">版本</span><span class="sxs-lookup"><span data-stu-id="b44ea-129">Version</span></span><br/> | <span data-ttu-id="b44ea-130">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="b44ea-130">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="b44ea-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b44ea-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="b44ea-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b44ea-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b44ea-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b44ea-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b44ea-134">**MediaObject**</span><span class="sxs-lookup"><span data-stu-id="b44ea-134">**MediaObject**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="b44ea-135">**GetItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="b44ea-135">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="b44ea-136">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b44ea-136">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="b44ea-137">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b44ea-137">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





