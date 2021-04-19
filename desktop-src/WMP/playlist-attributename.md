---
title: 播放清單。 attributeName
description: AttributeName 屬性會在指定的索引處，抓取屬性的名稱。
ms.assetid: 3ff68e78-5fa1-4ca6-aa59-4752dbaee52a
keywords:
- 播放清單. attributeName Windows Media Player
topic_type:
- apiref
api_name:
- Playlist.attributeName
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4560a7ca2766ee0bbadc582af878bca87e0834e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995743"
---
# <a name="playlistattributename"></a><span data-ttu-id="8d396-104">播放清單。 attributeName</span><span class="sxs-lookup"><span data-stu-id="8d396-104">Playlist.attributeName</span></span>

<span data-ttu-id="8d396-105">**AttributeName** 屬性會在指定的索引處，抓取屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d396-105">The **attributeName** property retrieves the name of an attribute at a specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d396-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d396-106">Syntax</span></span>

<span data-ttu-id="8d396-107">*玩家*。*currentPlaylist*。**attributeName** ( *索引* ) </span><span class="sxs-lookup"><span data-stu-id="8d396-107">*player*.*currentPlaylist*.**attributeName**( *index* )</span></span>

## <a name="parameters"></a><span data-ttu-id="8d396-108">參數</span><span class="sxs-lookup"><span data-stu-id="8d396-108">Parameters</span></span>

<span data-ttu-id="8d396-109">*index*</span><span class="sxs-lookup"><span data-stu-id="8d396-109">*index*</span></span>

<span data-ttu-id="8d396-110">包含索引的 (**長**) **數目**。</span><span class="sxs-lookup"><span data-stu-id="8d396-110">**Number** (**long**) containing the index.</span></span>

## <a name="possible-values"></a><span data-ttu-id="8d396-111">可能的值</span><span class="sxs-lookup"><span data-stu-id="8d396-111">Possible Values</span></span>

<span data-ttu-id="8d396-112">這個屬性是唯讀 **字串**。</span><span class="sxs-lookup"><span data-stu-id="8d396-112">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d396-113">備註</span><span class="sxs-lookup"><span data-stu-id="8d396-113">Remarks</span></span>

<span data-ttu-id="8d396-114">**AttributeCount** 屬性會抓取屬性數目。</span><span class="sxs-lookup"><span data-stu-id="8d396-114">The number of attributes is retrieved by the **attributeCount** property.</span></span> <span data-ttu-id="8d396-115">有了索引， **attributeName** 會傳回可搭配 **setItemInfo** 或 **getItemInfo** 使用的 **字串**，以指定或抓取屬性的值。</span><span class="sxs-lookup"><span data-stu-id="8d396-115">Given an index, **attributeName** returns a **String** that can be used in conjunction with **setItemInfo** or **getItemInfo** to specify or retrieve a value for the attribute.</span></span>

<span data-ttu-id="8d396-116">若要取得這個屬性的值，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="8d396-116">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="8d396-117">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="8d396-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="8d396-118">如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player [屬性參考](attribute-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="8d396-118">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

<span data-ttu-id="8d396-119">如需使用這個屬性的範例程式碼，請參閱 [attributeCount](playlist-attributecount.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="8d396-119">See the [attributeCount](playlist-attributecount.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d396-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d396-120">Requirements</span></span>



| <span data-ttu-id="8d396-121">需求</span><span class="sxs-lookup"><span data-stu-id="8d396-121">Requirement</span></span> | <span data-ttu-id="8d396-122">值</span><span class="sxs-lookup"><span data-stu-id="8d396-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8d396-123">版本</span><span class="sxs-lookup"><span data-stu-id="8d396-123">Version</span></span><br/> | <span data-ttu-id="8d396-124">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="8d396-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="8d396-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8d396-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="8d396-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d396-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d396-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d396-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d396-128">**播放清單物件**</span><span class="sxs-lookup"><span data-stu-id="8d396-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="8d396-129">**播放清單。 attributeCount**</span><span class="sxs-lookup"><span data-stu-id="8d396-129">**Playlist.attributeCount**</span></span>](playlist-attributecount.md)
</dt> <dt>

[<span data-ttu-id="8d396-130">**播放清單。 getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="8d396-130">**Playlist.getItemInfo**</span></span>](playlist-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="8d396-131">**播放清單。 setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="8d396-131">**Playlist.setItemInfo**</span></span>](playlist-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="8d396-132">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="8d396-132">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="8d396-133">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="8d396-133">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





