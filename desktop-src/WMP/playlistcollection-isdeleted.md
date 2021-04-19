---
title: PlaylistCollection. isDeleted 方法
description: IsDeleted 方法會抓取值，指出指定的播放清單是否在 [刪除的專案] 資料夾中。
ms.assetid: 5023927a-5d1a-4b61-8122-476947d537c4
keywords:
- isDeleted 方法 Windows Media Player
- isDeleted 方法 Windows Media Player，PlaylistCollection 類別
- PlaylistCollection 類別 Windows Media Player，isDeleted 方法
topic_type:
- apiref
api_name:
- PlaylistCollection.isDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fed3e7e8ff41f23d0f9f741ea99f3382d20532e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990266"
---
# <a name="playlistcollectionisdeleted-method"></a><span data-ttu-id="eaa41-106">PlaylistCollection. isDeleted 方法</span><span class="sxs-lookup"><span data-stu-id="eaa41-106">PlaylistCollection.isDeleted method</span></span>

<span data-ttu-id="eaa41-107">**IsDeleted** 方法會抓取值，指出指定的播放清單是否在 [刪除的專案] 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="eaa41-107">The **isDeleted** method retrieves a value indicating whether the specified playlist is in the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaa41-108">語法</span><span class="sxs-lookup"><span data-stu-id="eaa41-108">Syntax</span></span>


```JScript
bRetVal = PlaylistCollection.isDeleted(
  playlist
)
```



## <a name="parameters"></a><span data-ttu-id="eaa41-109">參數</span><span class="sxs-lookup"><span data-stu-id="eaa41-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaa41-110">*播放清單* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eaa41-110">*playlist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eaa41-111">要搜尋的 **播放清單** 物件。</span><span class="sxs-lookup"><span data-stu-id="eaa41-111">The **Playlist** object to be searched for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaa41-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="eaa41-112">Return value</span></span>

<span data-ttu-id="eaa41-113">這個方法會傳回 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="eaa41-113">This method returns a **Boolean**.</span></span>

<span data-ttu-id="eaa41-114">**Windows Media Player 10** 行動裝置版：此方法一律會傳回 **false**。</span><span class="sxs-lookup"><span data-stu-id="eaa41-114">**Windows Media Player 10 Mobile**: This method always returns **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaa41-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="eaa41-115">Requirements</span></span>



| <span data-ttu-id="eaa41-116">需求</span><span class="sxs-lookup"><span data-stu-id="eaa41-116">Requirement</span></span> | <span data-ttu-id="eaa41-117">值</span><span class="sxs-lookup"><span data-stu-id="eaa41-117">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaa41-118">版本</span><span class="sxs-lookup"><span data-stu-id="eaa41-118">Version</span></span><br/> | <span data-ttu-id="eaa41-119">適用于 Windows XP 的 Windows Media Player 7.0 版、Windows Media Player 7.1 版或 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="eaa41-119">Windows Media Player version 7.0, Windows Media Player version 7.1, or Windows Media Player for Windows XP.</span></span> <span data-ttu-id="eaa41-120">Windows Media Player 9 系列或更新版本不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="eaa41-120">This method is not supported for Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="eaa41-121">DLL</span><span class="sxs-lookup"><span data-stu-id="eaa41-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="eaa41-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eaa41-122"><dt>Wmp.dll</dt></span></span> </dl>                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="eaa41-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eaa41-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaa41-124">**PlaylistCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="eaa41-124">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> </dl>

 

 





