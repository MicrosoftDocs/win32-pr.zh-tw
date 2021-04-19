---
title: CurrentPlaylistChange 事件
description: 當目前播放清單中的某個專案發生變更時，就會發生 CurrentPlaylistChange 事件。 |CurrentPlaylistChange 事件
ms.assetid: 5270373e-e401-40c6-bf8c-ef0557610372
keywords:
- CurrentPlaylistChange 事件 Windows Media Player
- CurrentPlaylistChange 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，CurrentPlaylistChange 事件
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4722db224285587198e3ddb021022ec5d8f2cea6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977168"
---
# <a name="playercurrentplaylistchange-event"></a><span data-ttu-id="c5bcc-107">CurrentPlaylistChange 事件</span><span class="sxs-lookup"><span data-stu-id="c5bcc-107">Player.CurrentPlaylistChange event</span></span>

<span data-ttu-id="c5bcc-108">當目前播放清單中的某個專案發生變更時，就會發生 **CurrentPlaylistChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-108">The **CurrentPlaylistChange** event occurs when something changes within the current playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5bcc-109">語法</span><span class="sxs-lookup"><span data-stu-id="c5bcc-109">Syntax</span></span>


```JScript
Player.CurrentPlaylistChange(
  change
)
```



## <a name="parameters"></a><span data-ttu-id="c5bcc-110">參數</span><span class="sxs-lookup"><span data-stu-id="c5bcc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5bcc-111">*change*</span><span class="sxs-lookup"><span data-stu-id="c5bcc-111">*change*</span></span> 
</dt> <dd>

<span data-ttu-id="c5bcc-112">**Number** (**long**) 指出播放清單所發生的變更類型。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-112">**Number** (**long**) indicating what type of change occurred to the playlist.</span></span> <span data-ttu-id="c5bcc-113">查看 *播放機*。可能值資料表的 **PlaylistChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-113">See the *Player*.**PlaylistChange** event for a table of possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5bcc-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5bcc-114">Return value</span></span>

<span data-ttu-id="c5bcc-115">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5bcc-116">備註</span><span class="sxs-lookup"><span data-stu-id="c5bcc-116">Remarks</span></span>

<span data-ttu-id="c5bcc-117">當不同的播放清單變成目前的播放清單時，就不會發生此事件。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-117">This event does not occur when a different playlist becomes the current playlist.</span></span> <span data-ttu-id="c5bcc-118">只有在目前的播放清單中發生變更時才會發生，例如將媒體專案附加至播放清單。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-118">It only occurs when a change happens within the current playlist, such as a media item being appended to the playlist.</span></span>

<span data-ttu-id="c5bcc-119">事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-119">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="c5bcc-120">此參數名稱的類型必須完全如所示，包括大小寫。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-120">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="examples"></a><span data-ttu-id="c5bcc-121">範例</span><span class="sxs-lookup"><span data-stu-id="c5bcc-121">Examples</span></span>

<span data-ttu-id="c5bcc-122">下列 JScript 範例會更新名為 PlItems 之 HTML DIV 元素中的文字，以顯示目前播放清單中的媒體專案名稱。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-122">The following JScript example updates the text in an HTML DIV element, named PlItems, to display the names of the media items in the current playlist.</span></span> <span data-ttu-id="c5bcc-123">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for current playlist change. -->
<SCRIPT FOR = "Player" EVENT = "currentPlaylistChange(change)">
   switch (change){
      // Only update for move, delete, insert, and append events.
      case 3, 4, 5, 6:

         // Clear the contents of the DIV.
         PlItems.innerHTML = "";

         // Loop through the playlist and display each item name.
         for (var i = 0; i < Player.currentPlaylist.count; i++){
            PlItems.innerHTML += Player.currentPlaylist.item(i).name;
            PlItems.innerHTML += "<br>";
         }
         break;
      
      default:
   } 
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="c5bcc-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5bcc-124">Requirements</span></span>



| <span data-ttu-id="c5bcc-125">需求</span><span class="sxs-lookup"><span data-stu-id="c5bcc-125">Requirement</span></span> | <span data-ttu-id="c5bcc-126">值</span><span class="sxs-lookup"><span data-stu-id="c5bcc-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c5bcc-127">版本</span><span class="sxs-lookup"><span data-stu-id="c5bcc-127">Version</span></span><br/> | <span data-ttu-id="c5bcc-128">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c5bcc-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c5bcc-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="c5bcc-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5bcc-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5bcc-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5bcc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5bcc-132">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="c5bcc-132">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="c5bcc-133">**CurrentPlaylist**</span><span class="sxs-lookup"><span data-stu-id="c5bcc-133">**Player.currentPlaylist**</span></span>](player-currentplaylist.md)
</dt> <dt>

[<span data-ttu-id="c5bcc-134">**PlaylistChange**</span><span class="sxs-lookup"><span data-stu-id="c5bcc-134">**Player.PlaylistChange**</span></span>](player-player-playlistchange.md)
</dt> </dl>

 

 





