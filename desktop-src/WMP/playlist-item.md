---
title: 播放清單. item 方法
description: Item 方法會抓取位於指定之索引處的媒體專案。
ms.assetid: a564f6db-ede4-4c85-87ca-0e2539d914c2
keywords:
- item 方法 Windows Media Player
- item 方法 Windows Media Player，播放清單類別
- 播放清單類別 Windows Media Player、item 方法
topic_type:
- apiref
api_name:
- Playlist.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79c69386871aeec33dbc36a066ce3f75e80d7514
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995476"
---
# <a name="playlistitem-method"></a><span data-ttu-id="233b7-106">播放清單. item 方法</span><span class="sxs-lookup"><span data-stu-id="233b7-106">Playlist.item method</span></span>

<span data-ttu-id="233b7-107">**Item** 方法會抓取位於指定之索引處的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="233b7-107">The **item** method retrieves the media item at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="233b7-108">語法</span><span class="sxs-lookup"><span data-stu-id="233b7-108">Syntax</span></span>


```JScript
retVal = Playlist.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="233b7-109">參數</span><span class="sxs-lookup"><span data-stu-id="233b7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="233b7-110">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="233b7-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="233b7-111">**Number** (**Long**) ，其中包含要抓取之專案的索引。</span><span class="sxs-lookup"><span data-stu-id="233b7-111">**Number** (**long**) containing the index of the item to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="233b7-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="233b7-112">Return value</span></span>

<span data-ttu-id="233b7-113">這個方法會傳回 **媒體** 物件。</span><span class="sxs-lookup"><span data-stu-id="233b7-113">This method returns a **Media** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="233b7-114">備註</span><span class="sxs-lookup"><span data-stu-id="233b7-114">Remarks</span></span>

<span data-ttu-id="233b7-115">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="233b7-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="233b7-116">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="233b7-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="233b7-117">範例</span><span class="sxs-lookup"><span data-stu-id="233b7-117">Examples</span></span>

<span data-ttu-id="233b7-118">下列 JScript 範例會使用 *播放清單*。用來根據使用者選取專案從目前播放清單取出媒體專案的 **專案** 。</span><span class="sxs-lookup"><span data-stu-id="233b7-118">The following JScript example uses *Playlist*.**item** to retrieve a media item from the current playlist based on a user selection.</span></span> <span data-ttu-id="233b7-119">使用名稱 "weblist" 建立的 HTML SELECT 元素，並填入目前播放清單中的標題。</span><span class="sxs-lookup"><span data-stu-id="233b7-119">An HTML SELECT element was created with name "weblist", and filled with the titles from the current playlist.</span></span> <span data-ttu-id="233b7-120">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="233b7-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the value of the selected item in the list box
// using the selectedIndex property.
var index = weblist.selectedIndex;

// Store the corresponding digital media object from the current playlist.
var listItem = Player.currentPlaylist.item(index);

// Set the URL using the listItem variable.
Player.URL = listItem.sourceURL;

```



## <a name="requirements"></a><span data-ttu-id="233b7-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="233b7-121">Requirements</span></span>



| <span data-ttu-id="233b7-122">需求</span><span class="sxs-lookup"><span data-stu-id="233b7-122">Requirement</span></span> | <span data-ttu-id="233b7-123">值</span><span class="sxs-lookup"><span data-stu-id="233b7-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="233b7-124">版本</span><span class="sxs-lookup"><span data-stu-id="233b7-124">Version</span></span><br/> | <span data-ttu-id="233b7-125">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="233b7-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="233b7-126">DLL</span><span class="sxs-lookup"><span data-stu-id="233b7-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="233b7-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="233b7-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="233b7-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="233b7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="233b7-129">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="233b7-129">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="233b7-130">**播放清單物件**</span><span class="sxs-lookup"><span data-stu-id="233b7-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="233b7-131">**播放清單。 insertItem**</span><span class="sxs-lookup"><span data-stu-id="233b7-131">**Playlist.insertItem**</span></span>](playlist-insertitem.md)
</dt> <dt>

[<span data-ttu-id="233b7-132">**播放清單。 removeItem**</span><span class="sxs-lookup"><span data-stu-id="233b7-132">**Playlist.removeItem**</span></span>](playlist-removeitem.md)
</dt> <dt>

[<span data-ttu-id="233b7-133">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="233b7-133">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="233b7-134">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="233b7-134">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





