---
title: 播放清單。 dropDownList
description: DropDownList 屬性會指定或抓取值，指出哪些元素會顯示在播放清單元素之指定實例的下拉式清單方塊中。
ms.assetid: 583041b0-25dc-4015-a3b2-37f3cfdcd496
keywords:
- 播放清單. dropDownList Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.dropDownList
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4acf98dec7d50e2a3cd0b53acc07b0b8695f8461
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000716"
---
# <a name="playlistdropdownlist"></a><span data-ttu-id="5d04c-104">播放清單。 dropDownList</span><span class="sxs-lookup"><span data-stu-id="5d04c-104">PLAYLIST.dropDownList</span></span>

<span data-ttu-id="5d04c-105">**DropDownList** 屬性會指定或抓取值，指出哪些元素會顯示在 **播放** 清單元素之指定實例的下拉式清單方塊中。</span><span class="sxs-lookup"><span data-stu-id="5d04c-105">The **dropDownList** attribute specifies or retrieves a value indicating which elements show up in the drop-down list box for a given instance of the **PLAYLIST** element.</span></span>

``` syntax
        elementID.dropDownList
```

## <a name="possible-values"></a><span data-ttu-id="5d04c-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="5d04c-106">Possible Values</span></span>

<span data-ttu-id="5d04c-107">這個屬性是包含下列其中一個值的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="5d04c-107">This attribute is a read/write **String** containing one of the following values.</span></span>



| <span data-ttu-id="5d04c-108">值</span><span class="sxs-lookup"><span data-stu-id="5d04c-108">Value</span></span>       | <span data-ttu-id="5d04c-109">描述</span><span class="sxs-lookup"><span data-stu-id="5d04c-109">Description</span></span>                                                                                      |
|-------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d04c-110">showAlbums</span><span class="sxs-lookup"><span data-stu-id="5d04c-110">showAlbums</span></span>  | <span data-ttu-id="5d04c-111">顯示專輯。</span><span class="sxs-lookup"><span data-stu-id="5d04c-111">Shows albums.</span></span>                                                                                    |
| <span data-ttu-id="5d04c-112">showAll</span><span class="sxs-lookup"><span data-stu-id="5d04c-112">showAll</span></span>     | <span data-ttu-id="5d04c-113">預設值。</span><span class="sxs-lookup"><span data-stu-id="5d04c-113">Default.</span></span> <span data-ttu-id="5d04c-114">顯示所有可用的元素，包括 CD 播放清單、使用者播放清單和選項按鈕。</span><span class="sxs-lookup"><span data-stu-id="5d04c-114">Shows all available elements including CD playlists, user playlists, and radio presets.</span></span> |
| <span data-ttu-id="5d04c-115">showCD</span><span class="sxs-lookup"><span data-stu-id="5d04c-115">showCD</span></span>      | <span data-ttu-id="5d04c-116">顯示 CD 播放清單。</span><span class="sxs-lookup"><span data-stu-id="5d04c-116">Shows the CD playlist.</span></span>                                                                           |
| <span data-ttu-id="5d04c-117">showClips</span><span class="sxs-lookup"><span data-stu-id="5d04c-117">showClips</span></span>   | <span data-ttu-id="5d04c-118">顯示所有剪輯。</span><span class="sxs-lookup"><span data-stu-id="5d04c-118">Shows all clips.</span></span>                                                                                 |
| <span data-ttu-id="5d04c-119">showCurrent</span><span class="sxs-lookup"><span data-stu-id="5d04c-119">showCurrent</span></span> | <span data-ttu-id="5d04c-120">顯示目前、未儲存的播放清單。</span><span class="sxs-lookup"><span data-stu-id="5d04c-120">Shows the current, unsaved playlist.</span></span>                                                             |
| <span data-ttu-id="5d04c-121">showLibrary</span><span class="sxs-lookup"><span data-stu-id="5d04c-121">showLibrary</span></span> | <span data-ttu-id="5d04c-122">只顯示文件庫播放清單。</span><span class="sxs-lookup"><span data-stu-id="5d04c-122">Shows only library playlists.</span></span>                                                                    |
| <span data-ttu-id="5d04c-123">showRadio</span><span class="sxs-lookup"><span data-stu-id="5d04c-123">showRadio</span></span>   | <span data-ttu-id="5d04c-124">顯示選項按鈕。</span><span class="sxs-lookup"><span data-stu-id="5d04c-124">Shows radio presets.</span></span>                                                                             |
| <span data-ttu-id="5d04c-125">showQueries</span><span class="sxs-lookup"><span data-stu-id="5d04c-125">showQueries</span></span> | <span data-ttu-id="5d04c-126">顯示查詢。</span><span class="sxs-lookup"><span data-stu-id="5d04c-126">Shows queries.</span></span>                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="5d04c-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d04c-127">Requirements</span></span>



| <span data-ttu-id="5d04c-128">需求</span><span class="sxs-lookup"><span data-stu-id="5d04c-128">Requirement</span></span> | <span data-ttu-id="5d04c-129">值</span><span class="sxs-lookup"><span data-stu-id="5d04c-129">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="5d04c-130">版本</span><span class="sxs-lookup"><span data-stu-id="5d04c-130">Version</span></span><br/> | <span data-ttu-id="5d04c-131">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="5d04c-131">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5d04c-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d04c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d04c-133">**播放清單元素**</span><span class="sxs-lookup"><span data-stu-id="5d04c-133">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





