---
title: Media. duration
description: Duration 屬性會取出目前媒體專案的持續時間（以秒為單位）。
ms.assetid: d7d36858-812d-471b-84ce-fe2ab96b86b3
keywords:
- Media. duration Windows Media Player
topic_type:
- apiref
api_name:
- Media.duration
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71586f6aa37401d56a9e9537bfbea6c5af23f318
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994823"
---
# <a name="mediaduration"></a><span data-ttu-id="f23f7-104">Media. duration</span><span class="sxs-lookup"><span data-stu-id="f23f7-104">Media.duration</span></span>

<span data-ttu-id="f23f7-105">**Duration** 屬性會取出目前媒體專案的持續時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f23f7-105">The **duration** property retrieves the duration of the current media item in seconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="f23f7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f23f7-106">Syntax</span></span>

<span data-ttu-id="f23f7-107">*玩家*。*currentMedia*。**持續時間**</span><span class="sxs-lookup"><span data-stu-id="f23f7-107">*player*.*currentMedia*.**duration**</span></span>

## <a name="possible-values"></a><span data-ttu-id="f23f7-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="f23f7-108">Possible Values</span></span>

<span data-ttu-id="f23f7-109">這個屬性是唯讀的 (**雙**) 的 **數位**。</span><span class="sxs-lookup"><span data-stu-id="f23f7-109">This property is a read-only **Number** ( **double**).</span></span>

## <a name="remarks"></a><span data-ttu-id="f23f7-110">備註</span><span class="sxs-lookup"><span data-stu-id="f23f7-110">Remarks</span></span>

<span data-ttu-id="f23f7-111">如果這個屬性與 media 專案一起使用，而不是 *播放* 程式中指定的媒體專案。**currentMedia**，它可能不包含有效的值。</span><span class="sxs-lookup"><span data-stu-id="f23f7-111">If this property is used with a media item other than the one specified in *Player*.**currentMedia**, it may not contain a valid value.</span></span>

<span data-ttu-id="f23f7-112">若要取得不在使用者程式庫中的檔案持續時間，您必須等候 Windows Media Player 開啟檔案;亦即，目前的 OpenState 必須等於 MediaOpen。</span><span class="sxs-lookup"><span data-stu-id="f23f7-112">To retrieve the duration for files that are not in the user's library, you must wait for Windows Media Player to open the file; that is, the current OpenState must equal MediaOpen.</span></span> <span data-ttu-id="f23f7-113">您可以藉由處理 *播放* 程式來確認這一點。**OpenStateChange** 事件，或定期檢查 *Player* 的值。**openState**。</span><span class="sxs-lookup"><span data-stu-id="f23f7-113">You can verify this by handling the *Player*.**OpenStateChange** event or by periodically checking the value of *Player*.**openState**.</span></span>

<span data-ttu-id="f23f7-114">若為播放清單，當個別媒體專案開啟時，可以抓取每個媒體專案的持續時間，而不是開啟播放清單時的。</span><span class="sxs-lookup"><span data-stu-id="f23f7-114">For playlists, the duration of each media item can be retrieved when the individual media item is opened, rather than the when the playlist is opened.</span></span>

<span data-ttu-id="f23f7-115">若要取得這個屬性的值，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="f23f7-115">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="f23f7-116">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="f23f7-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="f23f7-117">下列 JScript 範例會使用 *媒體*。顯示目前媒體專案剩餘時間的 **持續** 時間。</span><span class="sxs-lookup"><span data-stu-id="f23f7-117">The following JScript example uses *Media*.**duration** to display the time remaining in the current media item.</span></span> <span data-ttu-id="f23f7-118">名為 RemTime 的 HTML DIV 元素會顯示資訊。</span><span class="sxs-lookup"><span data-stu-id="f23f7-118">An HTML DIV element named RemTime displays the information.</span></span> <span data-ttu-id="f23f7-119">HTML 計時器會每秒更新 DIV 元素中的文字。</span><span class="sxs-lookup"><span data-stu-id="f23f7-119">An HTML timer updates the text in the DIV element every second.</span></span>

<span data-ttu-id="f23f7-120">下列 JScript 程式碼會啟動計時器：</span><span class="sxs-lookup"><span data-stu-id="f23f7-120">The following JScript code starts the timer:</span></span>


```JScript
// Execute the update() function at one-second intervals.
idTmr = window.setInterval("update()",1000);
```



<span data-ttu-id="f23f7-121">下列 JScript 程式碼會停止計時器：</span><span class="sxs-lookup"><span data-stu-id="f23f7-121">The following JScript code stops the timer:</span></span>


```JScript
window.clearInterval(idTmr);
```



<span data-ttu-id="f23f7-122">使用 *播放*。具有 **switch** 語句的 **PlayStateChange** 事件，以判斷何時要啟動和停止計時器。</span><span class="sxs-lookup"><span data-stu-id="f23f7-122">Use the *Player*.**PlayStateChange** event with a **switch** statement to determine when to start and stop the timer.</span></span>

<span data-ttu-id="f23f7-123">每次計時器呼叫 update 函數時，都會執行下列 JScript 程式碼：</span><span class="sxs-lookup"><span data-stu-id="f23f7-123">The following JScript code executes each time the timer calls the update function:</span></span>


```JScript
// Store the current position of the current media item.
var TimeNow = Player.controls.currentPosition;

// Display the time remaining information.
RemTime.innerHTML = "Seconds remaining: ";

// Subtract the current position from the duration of the current media.
// Use the Math.floor method to round the result down to the nearest integer.
RemTime.innerHTML += Math.floor(Player.currentMedia.duration - TimeNow);
```



## <a name="requirements"></a><span data-ttu-id="f23f7-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f23f7-124">Requirements</span></span>



| <span data-ttu-id="f23f7-125">需求</span><span class="sxs-lookup"><span data-stu-id="f23f7-125">Requirement</span></span> | <span data-ttu-id="f23f7-126">值</span><span class="sxs-lookup"><span data-stu-id="f23f7-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f23f7-127">版本</span><span class="sxs-lookup"><span data-stu-id="f23f7-127">Version</span></span><br/> | <span data-ttu-id="f23f7-128">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="f23f7-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f23f7-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f23f7-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="f23f7-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f23f7-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f23f7-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f23f7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f23f7-132">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="f23f7-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="f23f7-133">**CurrentMedia**</span><span class="sxs-lookup"><span data-stu-id="f23f7-133">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="f23f7-134">**PlayStateChange 事件**</span><span class="sxs-lookup"><span data-stu-id="f23f7-134">**Player.PlayStateChange Event**</span></span>](player-player-playstatechange.md)
</dt> <dt>

[<span data-ttu-id="f23f7-135">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="f23f7-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="f23f7-136">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="f23f7-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





