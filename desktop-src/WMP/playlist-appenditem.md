---
title: AppendItem 方法
description: AppendItem 方法會將媒體專案新增至播放清單的結尾。
ms.assetid: cc956491-7936-49e7-90ca-1f71e03448cd
keywords:
- appendItem 方法 Windows Media Player
- appendItem 方法 Windows Media Player，播放清單類別
- 播放清單類別 Windows Media Player，appendItem 方法
topic_type:
- apiref
api_name:
- Playlist.appendItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 828799d5b6e71e7ff0e7be4c1e55714f6343be51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982579"
---
# <a name="playlistappenditem-method"></a><span data-ttu-id="2a376-106">AppendItem 方法</span><span class="sxs-lookup"><span data-stu-id="2a376-106">Playlist.appendItem method</span></span>

<span data-ttu-id="2a376-107">**AppendItem** 方法會將媒體專案新增至播放清單的結尾。</span><span class="sxs-lookup"><span data-stu-id="2a376-107">The **appendItem** method adds a media item to the end of the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a376-108">語法</span><span class="sxs-lookup"><span data-stu-id="2a376-108">Syntax</span></span>


```JScript
Playlist.appendItem(
  item
)
```



## <a name="parameters"></a><span data-ttu-id="2a376-109">參數</span><span class="sxs-lookup"><span data-stu-id="2a376-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a376-110">*專案* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2a376-110">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a376-111">要加入的 **媒體** 物件。</span><span class="sxs-lookup"><span data-stu-id="2a376-111">**Media** object to be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a376-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="2a376-112">Return value</span></span>

<span data-ttu-id="2a376-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2a376-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a376-114">備註</span><span class="sxs-lookup"><span data-stu-id="2a376-114">Remarks</span></span>

<span data-ttu-id="2a376-115">若要使用此方法，需要有程式庫的完整存取權。</span><span class="sxs-lookup"><span data-stu-id="2a376-115">To use this method, full access to the library is required.</span></span> <span data-ttu-id="2a376-116">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="2a376-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2a376-117">範例</span><span class="sxs-lookup"><span data-stu-id="2a376-117">Examples</span></span>

<span data-ttu-id="2a376-118">下列 JScript 範例會使用 *播放清單*。**appendItem** 將目前的媒體專案新增至名為 "ThreeList" 的播放清單。</span><span class="sxs-lookup"><span data-stu-id="2a376-118">The following JScript example uses *Playlist*.**appendItem** to add the current media item to the playlist named "ThreeList".</span></span> <span data-ttu-id="2a376-119">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="2a376-119">The **Player** object was created with ID="Player".</span></span>


```JScript
// Get the current media item.
var currMedia = Player.currentMedia;

// Get the playlist object by name.
var plThreeList = Player.playlistCollection.getByName("ThreeList").item(0);

// Append the media item to the playlist.
plThreeList.appendItem(currMedia);

```



## <a name="requirements"></a><span data-ttu-id="2a376-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a376-120">Requirements</span></span>



| <span data-ttu-id="2a376-121">需求</span><span class="sxs-lookup"><span data-stu-id="2a376-121">Requirement</span></span> | <span data-ttu-id="2a376-122">值</span><span class="sxs-lookup"><span data-stu-id="2a376-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2a376-123">版本</span><span class="sxs-lookup"><span data-stu-id="2a376-123">Version</span></span><br/> | <span data-ttu-id="2a376-124">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="2a376-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="2a376-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2a376-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="2a376-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a376-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a376-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a376-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a376-128">**播放清單物件**</span><span class="sxs-lookup"><span data-stu-id="2a376-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="2a376-129">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="2a376-129">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="2a376-130">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="2a376-130">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





