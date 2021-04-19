---
title: SetItemInfo 方法
description: SetItemInfo 方法會指定播放清單屬性的值。
ms.assetid: ffecb43f-343d-4a4f-9356-0e3cfa85ce77
keywords:
- setItemInfo 方法 Windows Media Player
- setItemInfo 方法 Windows Media Player，播放清單類別
- 播放清單類別 Windows Media Player，setItemInfo 方法
topic_type:
- apiref
api_name:
- Playlist.setItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ff42e56e549100044db0881bb38ade5f2f1711a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980244"
---
# <a name="playlistsetiteminfo-method"></a><span data-ttu-id="65a9b-106">SetItemInfo 方法</span><span class="sxs-lookup"><span data-stu-id="65a9b-106">Playlist.setItemInfo method</span></span>

<span data-ttu-id="65a9b-107">**SetItemInfo** 方法會指定播放清單屬性的值。</span><span class="sxs-lookup"><span data-stu-id="65a9b-107">The **setItemInfo** method specifies the value of a playlist attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="65a9b-108">語法</span><span class="sxs-lookup"><span data-stu-id="65a9b-108">Syntax</span></span>


```JScript
Playlist.setItemInfo(
  name,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="65a9b-109">參數</span><span class="sxs-lookup"><span data-stu-id="65a9b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65a9b-110">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="65a9b-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65a9b-111">包含要設定之屬性名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="65a9b-111">**String** containing the name of the attribute to be set.</span></span> <span data-ttu-id="65a9b-112">如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player [屬性參考](attribute-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="65a9b-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="65a9b-113">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="65a9b-113">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65a9b-114">包含屬性之新值的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="65a9b-114">**String** containing the new value for the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65a9b-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="65a9b-115">Return value</span></span>

<span data-ttu-id="65a9b-116">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="65a9b-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="65a9b-117">備註</span><span class="sxs-lookup"><span data-stu-id="65a9b-117">Remarks</span></span>

<span data-ttu-id="65a9b-118">**SetItemInfo** 方法的特殊用途是使用 SortAttribute 屬性來排序播放清單中的專案。</span><span class="sxs-lookup"><span data-stu-id="65a9b-118">A special use of the **setItemInfo** method is to sort the items in the playlist by using the SortAttribute attribute.</span></span> <span data-ttu-id="65a9b-119">下列 JScript 範例會依 UserLastPlayedTime 屬性的值來排序播放清單。</span><span class="sxs-lookup"><span data-stu-id="65a9b-119">The following JScript example sorts a playlist by the values of the UserLastPlayedTime attribute.</span></span> <span data-ttu-id="65a9b-120">變數播放清單是 **播放清單** 物件的參考。</span><span class="sxs-lookup"><span data-stu-id="65a9b-120">The variable playlist is a reference to a **Playlist** object.</span></span>


```JScript
playlist.setItemInfo("SortAttribute", "UserLastPlayedTime")
```



<span data-ttu-id="65a9b-121">若要使用此方法，需要有程式庫的完整存取權。</span><span class="sxs-lookup"><span data-stu-id="65a9b-121">To use this method, full access to the library is required.</span></span> <span data-ttu-id="65a9b-122">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="65a9b-122">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="65a9b-123">**Windows Media Player 10** 行動裝置版：不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="65a9b-123">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="65a9b-124">範例</span><span class="sxs-lookup"><span data-stu-id="65a9b-124">Examples</span></span>

<span data-ttu-id="65a9b-125">如需使用這個屬性的範例程式碼，請參閱 [attributeCount](playlist-attributecount.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="65a9b-125">See the [attributeCount](playlist-attributecount.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="65a9b-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="65a9b-126">Requirements</span></span>



| <span data-ttu-id="65a9b-127">需求</span><span class="sxs-lookup"><span data-stu-id="65a9b-127">Requirement</span></span> | <span data-ttu-id="65a9b-128">值</span><span class="sxs-lookup"><span data-stu-id="65a9b-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="65a9b-129">版本</span><span class="sxs-lookup"><span data-stu-id="65a9b-129">Version</span></span><br/> | <span data-ttu-id="65a9b-130">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="65a9b-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="65a9b-131">DLL</span><span class="sxs-lookup"><span data-stu-id="65a9b-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="65a9b-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65a9b-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65a9b-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65a9b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65a9b-134">**播放清單物件**</span><span class="sxs-lookup"><span data-stu-id="65a9b-134">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="65a9b-135">**播放清單。 getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="65a9b-135">**Playlist.getItemInfo**</span></span>](playlist-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="65a9b-136">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="65a9b-136">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="65a9b-137">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="65a9b-137">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





