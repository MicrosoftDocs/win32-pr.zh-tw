---
title: PlaylistArray 專案方法
description: Item 方法會在指定的索引處抓取播放清單。
ms.assetid: cc851695-f9a2-4594-8bd3-3555c18bfa10
keywords:
- item 方法 Windows Media Player
- item 方法 Windows Media Player，PlaylistArray 類別
- PlaylistArray 類別 Windows Media Player，item 方法
topic_type:
- apiref
api_name:
- PlaylistArray.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6144f6e1cfda93be32060e8206a96b0da7568d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978805"
---
# <a name="playlistarrayitem-method"></a><span data-ttu-id="d0367-106">PlaylistArray 專案方法</span><span class="sxs-lookup"><span data-stu-id="d0367-106">PlaylistArray.item method</span></span>

<span data-ttu-id="d0367-107">**Item** 方法會在指定的索引處抓取播放清單。</span><span class="sxs-lookup"><span data-stu-id="d0367-107">The **item** method retrieves the playlist at the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0367-108">語法</span><span class="sxs-lookup"><span data-stu-id="d0367-108">Syntax</span></span>


```JScript
retVal = PlaylistArray.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="d0367-109">參數</span><span class="sxs-lookup"><span data-stu-id="d0367-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0367-110">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d0367-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0367-111">包含要抓取之播放清單索引的 (**長**) **數目**。</span><span class="sxs-lookup"><span data-stu-id="d0367-111">**Number** (**long**) containing the index of the playlist to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0367-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d0367-112">Return value</span></span>

<span data-ttu-id="d0367-113">這個方法會傳回 **播放清單** 物件。</span><span class="sxs-lookup"><span data-stu-id="d0367-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0367-114">備註</span><span class="sxs-lookup"><span data-stu-id="d0367-114">Remarks</span></span>

<span data-ttu-id="d0367-115">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="d0367-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="d0367-116">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="d0367-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0367-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0367-117">Requirements</span></span>



| <span data-ttu-id="d0367-118">需求</span><span class="sxs-lookup"><span data-stu-id="d0367-118">Requirement</span></span> | <span data-ttu-id="d0367-119">值</span><span class="sxs-lookup"><span data-stu-id="d0367-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d0367-120">版本</span><span class="sxs-lookup"><span data-stu-id="d0367-120">Version</span></span><br/> | <span data-ttu-id="d0367-121">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="d0367-121">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d0367-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d0367-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="d0367-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0367-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0367-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0367-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0367-125">**PlaylistArray 物件**</span><span class="sxs-lookup"><span data-stu-id="d0367-125">**PlaylistArray Object**</span></span>](playlistarray-object.md)
</dt> <dt>

[<span data-ttu-id="d0367-126">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="d0367-126">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="d0367-127">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="d0367-127">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





