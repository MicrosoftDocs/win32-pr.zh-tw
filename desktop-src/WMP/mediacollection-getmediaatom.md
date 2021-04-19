---
title: MediaCollection. getMediaAtom 方法
description: GetMediaAtom 方法會抓取可用屬性集合中指定的屬性所在的索引。
ms.assetid: 17501a95-1196-43ff-9a4e-a78cf28e7a2d
keywords:
- getMediaAtom 方法 Windows Media Player
- getMediaAtom 方法 Windows Media Player，MediaCollection 類別
- MediaCollection 類別 Windows Media Player，getMediaAtom 方法
topic_type:
- apiref
api_name:
- MediaCollection.getMediaAtom
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16728b20c26b90c10f144f278f7dec24195b536a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987102"
---
# <a name="mediacollectiongetmediaatom-method"></a><span data-ttu-id="a23e9-106">MediaCollection. getMediaAtom 方法</span><span class="sxs-lookup"><span data-stu-id="a23e9-106">MediaCollection.getMediaAtom method</span></span>

<span data-ttu-id="a23e9-107">**GetMediaAtom** 方法會抓取可用屬性集合中指定的屬性所在的索引。</span><span class="sxs-lookup"><span data-stu-id="a23e9-107">The **getMediaAtom** method retrieves the index at which a specified attribute resides within the set of available attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a23e9-108">語法</span><span class="sxs-lookup"><span data-stu-id="a23e9-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getMediaAtom(
  attribute
)
```



## <a name="parameters"></a><span data-ttu-id="a23e9-109">參數</span><span class="sxs-lookup"><span data-stu-id="a23e9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a23e9-110">*屬性* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a23e9-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a23e9-111">包含屬性名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="a23e9-111">**String** containing the attribute name.</span></span> <span data-ttu-id="a23e9-112">如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player [屬性參考](attribute-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="a23e9-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a23e9-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a23e9-113">Return value</span></span>

<span data-ttu-id="a23e9-114">這個方法會傳回 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="a23e9-114">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="a23e9-115">備註</span><span class="sxs-lookup"><span data-stu-id="a23e9-115">Remarks</span></span>

<span data-ttu-id="a23e9-116">使用這個方法取出的索引編號可以傳遞至 *媒體*。用來存取屬性值的 **getItemInfoByAtom** 方法。</span><span class="sxs-lookup"><span data-stu-id="a23e9-116">The index number retrieved with this method can be passed to the *Media*.**getItemInfoByAtom** method to access attribute values.</span></span> <span data-ttu-id="a23e9-117">使用大型播放清單時，這項技術通常更有效率，而不是透過 *媒體* 依名稱存取屬性值。**getItemInfo** 或 *媒體*。**getItemInfoByType**。</span><span class="sxs-lookup"><span data-stu-id="a23e9-117">This technique is generally more efficient when working with large playlists than accessing an attribute value by name through *Media*.**getItemInfo** or *Media*.**getItemInfoByType**.</span></span>

<span data-ttu-id="a23e9-118">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="a23e9-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="a23e9-119">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="a23e9-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a23e9-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="a23e9-120">Requirements</span></span>



| <span data-ttu-id="a23e9-121">需求</span><span class="sxs-lookup"><span data-stu-id="a23e9-121">Requirement</span></span> | <span data-ttu-id="a23e9-122">值</span><span class="sxs-lookup"><span data-stu-id="a23e9-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a23e9-123">版本</span><span class="sxs-lookup"><span data-stu-id="a23e9-123">Version</span></span><br/> | <span data-ttu-id="a23e9-124">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="a23e9-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a23e9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a23e9-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="a23e9-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a23e9-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a23e9-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a23e9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a23e9-128">**GetItemInfo**</span><span class="sxs-lookup"><span data-stu-id="a23e9-128">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="a23e9-129">**GetItemInfoByAtom**</span><span class="sxs-lookup"><span data-stu-id="a23e9-129">**Media.getItemInfoByAtom**</span></span>](media-getiteminfobyatom.md)
</dt> <dt>

[<span data-ttu-id="a23e9-130">**GetItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="a23e9-130">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="a23e9-131">**MediaCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="a23e9-131">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="a23e9-132">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="a23e9-132">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="a23e9-133">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="a23e9-133">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





