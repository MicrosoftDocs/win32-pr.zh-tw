---
title: CurrentItem
description: CurrentItem 屬性會指定或抓取目前的媒體專案。
ms.assetid: 77e21585-3cc8-41f5-97b5-da6eb992c7bc
keywords:
- CurrentItem Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentItem
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81658665cb6f31acd327f5050a733a2fc3c70371
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994160"
---
# <a name="controlscurrentitem"></a><span data-ttu-id="7efbf-104">CurrentItem</span><span class="sxs-lookup"><span data-stu-id="7efbf-104">Controls.currentItem</span></span>

<span data-ttu-id="7efbf-105">**CurrentItem** 屬性會指定或抓取目前的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="7efbf-105">The **currentItem** property specifies or retrieves the current media item.</span></span>

``` syntax
player.controls.currentItem
      
```

## <a name="possible-values"></a><span data-ttu-id="7efbf-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="7efbf-106">Possible Values</span></span>

<span data-ttu-id="7efbf-107">此屬性是讀取/寫入 **媒體** 物件。</span><span class="sxs-lookup"><span data-stu-id="7efbf-107">This property is a read/write **Media** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7efbf-108">備註</span><span class="sxs-lookup"><span data-stu-id="7efbf-108">Remarks</span></span>

<span data-ttu-id="7efbf-109">此方法僅適用于 *Player* 中的專案。**currentPlaylist**。</span><span class="sxs-lookup"><span data-stu-id="7efbf-109">This method works only with items in *Player*.**currentPlaylist**.</span></span> <span data-ttu-id="7efbf-110">不支援使用已儲存媒體專案的參考來呼叫 **currentItem** 。</span><span class="sxs-lookup"><span data-stu-id="7efbf-110">Calling **currentItem** with a reference to a saved media item is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="7efbf-111">範例</span><span class="sxs-lookup"><span data-stu-id="7efbf-111">Examples</span></span>

<span data-ttu-id="7efbf-112">下列 JScript 範例會使用 **currentItem** ，將播放程式控制項目前的媒體專案設定為 HTML SELECT 專案中所選取的值。</span><span class="sxs-lookup"><span data-stu-id="7efbf-112">The following JScript example uses **currentItem** to set the player control current media item to the selected value in an HTML SELECT element.</span></span> <span data-ttu-id="7efbf-113">目前的播放清單是使用 *PlaylistCollection* 來指定。**getByName**。</span><span class="sxs-lookup"><span data-stu-id="7efbf-113">The current playlist was first specified by using *PlaylistCollection*.**getByName**.</span></span> <span data-ttu-id="7efbf-114">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="7efbf-114">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SELECT ID = playItem  NAME = "playItem"  LANGUAGE = "JScript"

    /* Specify the current item when the selected list value changes. */
    onChange = "Player.controls.currentItem = Player.currentPlaylist.item(playItem.value);">

    /* Fill the SELECT element list with three items that match
       the songs in the playlist. */
    <OPTION VALUE = 0 >Laure
    <OPTION VALUE = 1 >Jeanne
    <OPTION VALUE = 2 >House
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="7efbf-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="7efbf-115">Requirements</span></span>



| <span data-ttu-id="7efbf-116">需求</span><span class="sxs-lookup"><span data-stu-id="7efbf-116">Requirement</span></span> | <span data-ttu-id="7efbf-117">值</span><span class="sxs-lookup"><span data-stu-id="7efbf-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7efbf-118">版本</span><span class="sxs-lookup"><span data-stu-id="7efbf-118">Version</span></span><br/> | <span data-ttu-id="7efbf-119">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="7efbf-119">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7efbf-120">DLL</span><span class="sxs-lookup"><span data-stu-id="7efbf-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="7efbf-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7efbf-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7efbf-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7efbf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7efbf-123">**Controls 物件**</span><span class="sxs-lookup"><span data-stu-id="7efbf-123">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="7efbf-124">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="7efbf-124">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="7efbf-125">**PlaylistCollection.getByName**</span><span class="sxs-lookup"><span data-stu-id="7efbf-125">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> </dl>

 

 





