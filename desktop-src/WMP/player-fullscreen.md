---
title: Media Player. 全螢幕
description: 全螢幕屬性會指定或抓取值，指出是否以全螢幕模式播放影片內容。
ms.assetid: 43eeeddd-13a6-44d8-9cff-a60e976fc189
keywords:
- Media Player. 全螢幕 Windows Media Player
topic_type:
- apiref
api_name:
- Player.fullScreen
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3f71b4100c359effd95f79c574a52b5a5bae28c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995191"
---
# <a name="playerfullscreen"></a><span data-ttu-id="a6b90-104">Media Player. 全螢幕</span><span class="sxs-lookup"><span data-stu-id="a6b90-104">Player.fullScreen</span></span>

<span data-ttu-id="a6b90-105">**全** 螢幕屬性會指定或抓取值，指出是否以全螢幕模式播放影片內容。</span><span class="sxs-lookup"><span data-stu-id="a6b90-105">The **fullScreen** property specifies or retrieves a value indicating whether video content is played back in full-screen mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6b90-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6b90-106">Syntax</span></span>

<span data-ttu-id="a6b90-107">*玩家* 。**全螢幕**</span><span class="sxs-lookup"><span data-stu-id="a6b90-107">*player* .**fullScreen**</span></span>

## <a name="possible-values"></a><span data-ttu-id="a6b90-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="a6b90-108">Possible Values</span></span>

<span data-ttu-id="a6b90-109">這個屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="a6b90-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="a6b90-110">值</span><span class="sxs-lookup"><span data-stu-id="a6b90-110">Value</span></span> | <span data-ttu-id="a6b90-111">描述</span><span class="sxs-lookup"><span data-stu-id="a6b90-111">Description</span></span>                                                    |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="a6b90-112">true</span><span class="sxs-lookup"><span data-stu-id="a6b90-112">true</span></span>  | <span data-ttu-id="a6b90-113">影片內容會以全螢幕模式播放。</span><span class="sxs-lookup"><span data-stu-id="a6b90-113">Video content is played back in full-screen mode.</span></span>              |
| <span data-ttu-id="a6b90-114">false</span><span class="sxs-lookup"><span data-stu-id="a6b90-114">false</span></span> | <span data-ttu-id="a6b90-115">預設值。</span><span class="sxs-lookup"><span data-stu-id="a6b90-115">Default.</span></span> <span data-ttu-id="a6b90-116">影片內容不會以全螢幕模式播放。</span><span class="sxs-lookup"><span data-stu-id="a6b90-116">Video content is not played back in full-screen mode.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a6b90-117">備註</span><span class="sxs-lookup"><span data-stu-id="a6b90-117">Remarks</span></span>

<span data-ttu-id="a6b90-118">若要在內嵌 Windows Media Player 控制項時讓全螢幕模式正常運作，影片顯示區域必須具有至少一個圖元的高度和寬度。</span><span class="sxs-lookup"><span data-stu-id="a6b90-118">For full-screen mode to work properly when embedding the Windows Media Player control, the video display area must have a height and width of at least one pixel.</span></span> <span data-ttu-id="a6b90-119">如果 **uiMode** 設定為「迷你」或「完整」，則控制項本身的高度必須是65或更大，才能容納除了使用者介面之外的影片顯示區域。</span><span class="sxs-lookup"><span data-stu-id="a6b90-119">If **uiMode** is set to "mini" or "full", the height of the control itself must be 65 or greater to accommodate the video display area in addition to the user interface.</span></span>

<span data-ttu-id="a6b90-120">如果 **uiMode** 設為「隱藏」，則將這個屬性設定為 true 會引發錯誤，而且不會影響控制項的行為。</span><span class="sxs-lookup"><span data-stu-id="a6b90-120">If **uiMode** is set to "invisible", then setting this property to true raises an error and does not affect the behavior of the control.</span></span>

<span data-ttu-id="a6b90-121">在全螢幕播放期間，Windows Media Player 會在 **enableCoNtextMenu** 等於 False 且 **uiMode** 等於 "none" 時隱藏滑鼠游標。</span><span class="sxs-lookup"><span data-stu-id="a6b90-121">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

<span data-ttu-id="a6b90-122">如果 **uiMode** 設為「完整」或「迷你」，Windows Media Player 在滑鼠游標移動時，以全螢幕模式顯示傳輸控制項。</span><span class="sxs-lookup"><span data-stu-id="a6b90-122">If **uiMode** is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode when the mouse cursor moves.</span></span> <span data-ttu-id="a6b90-123">在不移動滑鼠的短暫間隔之後，就會隱藏傳輸控制項。</span><span class="sxs-lookup"><span data-stu-id="a6b90-123">After a brief interval of no mouse movement, the transport controls are hidden.</span></span> <span data-ttu-id="a6b90-124">如果 **uiMode** 設為 "none"，就不會在全螢幕模式中顯示任何控制項。</span><span class="sxs-lookup"><span data-stu-id="a6b90-124">If **uiMode** is set to "none", no controls are displayed in full-screen mode.</span></span>

<span data-ttu-id="a6b90-125">**注意**</span><span class="sxs-lookup"><span data-stu-id="a6b90-125">**Note**</span></span>

<span data-ttu-id="a6b90-126">以全螢幕模式顯示傳輸控制項需要 Windows XP 作業系統。</span><span class="sxs-lookup"><span data-stu-id="a6b90-126">Displaying transport controls in full-screen mode requires the Windows XP operating system.</span></span>

<span data-ttu-id="a6b90-127">如果傳輸控制項未以全螢幕模式顯示，則 Windows Media Player 會在播放停止時自動離開全螢幕模式。</span><span class="sxs-lookup"><span data-stu-id="a6b90-127">If transport controls are not displayed in full-screen mode, then Windows Media Player automatically exits full-screen mode when playback stops.</span></span>

<span data-ttu-id="a6b90-128">**注意**</span><span class="sxs-lookup"><span data-stu-id="a6b90-128">**Note**</span></span>

<span data-ttu-id="a6b90-129">務必通知使用者如何從全螢幕模式中返回。</span><span class="sxs-lookup"><span data-stu-id="a6b90-129">Always be sure to inform the user how to return from full-screen mode.</span></span>

## <a name="examples"></a><span data-ttu-id="a6b90-130">範例</span><span class="sxs-lookup"><span data-stu-id="a6b90-130">Examples</span></span>

<span data-ttu-id="a6b90-131">下列範例會建立使用 *Player* 的 HTML 輸入按鈕。將內嵌播放機物件切換至全螢幕模式的 **全** 螢幕。</span><span class="sxs-lookup"><span data-stu-id="a6b90-131">The following example creates an HTML input button that uses *Player*.**fullScreen** to switch an embedded player object to full-screen mode.</span></span> <span data-ttu-id="a6b90-132">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="a6b90-132">The **Player** object was created with ID = "Player".</span></span>


```
<INPUT type = button 
       value = "Full Screen" 
       name = FSBUTTON
       onclick = "
               /* Check to be sure the player is playing. */
               if (Player.playState == 3) 
                  Player.fullScreen = 'true';
               ">
```



## <a name="requirements"></a><span data-ttu-id="a6b90-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="a6b90-133">Requirements</span></span>



| <span data-ttu-id="a6b90-134">需求</span><span class="sxs-lookup"><span data-stu-id="a6b90-134">Requirement</span></span> | <span data-ttu-id="a6b90-135">值</span><span class="sxs-lookup"><span data-stu-id="a6b90-135">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a6b90-136">版本</span><span class="sxs-lookup"><span data-stu-id="a6b90-136">Version</span></span><br/> | <span data-ttu-id="a6b90-137">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="a6b90-137">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a6b90-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a6b90-138">DLL</span></span><br/>     | <dl> <span data-ttu-id="a6b90-139"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6b90-139"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6b90-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a6b90-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6b90-141">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="a6b90-141">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





