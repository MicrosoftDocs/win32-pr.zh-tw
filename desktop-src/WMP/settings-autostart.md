---
title: 設定。 autoStart
description: AutoStart 屬性會指定或抓取值，指出目前的媒體專案是否會自動開始播放。
ms.assetid: 553f8534-9e3e-4fdc-bfc1-551939969289
keywords:
- 設定： autoStart Windows Media Player
topic_type:
- apiref
api_name:
- Settings.autoStart
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d08b8f84f4a0b51225ed5692a25fa41cab809ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985988"
---
# <a name="settingsautostart"></a><span data-ttu-id="b3ddc-104">設定。 autoStart</span><span class="sxs-lookup"><span data-stu-id="b3ddc-104">Settings.autoStart</span></span>

<span data-ttu-id="b3ddc-105">**AutoStart** 屬性會指定或抓取值，指出目前的媒體專案是否會自動開始播放。</span><span class="sxs-lookup"><span data-stu-id="b3ddc-105">The **autoStart** property specifies or retrieves a value indicating whether the current media item begins playing automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3ddc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3ddc-106">Syntax</span></span>

<span data-ttu-id="b3ddc-107">設定： autoStart</span><span class="sxs-lookup"><span data-stu-id="b3ddc-107">player.settings.autoStart</span></span>

## <a name="possible-values"></a><span data-ttu-id="b3ddc-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="b3ddc-108">Possible Values</span></span>

<span data-ttu-id="b3ddc-109">這個屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="b3ddc-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="b3ddc-110">值</span><span class="sxs-lookup"><span data-stu-id="b3ddc-110">Value</span></span> | <span data-ttu-id="b3ddc-111">描述</span><span class="sxs-lookup"><span data-stu-id="b3ddc-111">Description</span></span>                                                         |
|-------|---------------------------------------------------------------------|
| <span data-ttu-id="b3ddc-112">true</span><span class="sxs-lookup"><span data-stu-id="b3ddc-112">true</span></span>  | <span data-ttu-id="b3ddc-113">預設值。</span><span class="sxs-lookup"><span data-stu-id="b3ddc-113">Default.</span></span> <span data-ttu-id="b3ddc-114">媒體專案會自動開始播放 (請參閱備註) 。</span><span class="sxs-lookup"><span data-stu-id="b3ddc-114">The media item begins playing automatically (see Remarks).</span></span> |
| <span data-ttu-id="b3ddc-115">false</span><span class="sxs-lookup"><span data-stu-id="b3ddc-115">false</span></span> | <span data-ttu-id="b3ddc-116">媒體專案不會自動開始播放。</span><span class="sxs-lookup"><span data-stu-id="b3ddc-116">The media item does not begin playing automatically.</span></span>                |



 

## <a name="remarks"></a><span data-ttu-id="b3ddc-117">備註</span><span class="sxs-lookup"><span data-stu-id="b3ddc-117">Remarks</span></span>

<span data-ttu-id="b3ddc-118">如果 **自動啟動** 設定為 true，則會在 *播放* 程式時開始播放媒體專案。**URL**、 *播放機*。**currentPlaylist** 或 *播放機*。已設定 **currentMedia** 。</span><span class="sxs-lookup"><span data-stu-id="b3ddc-118">If **autoStart** is set to true, the media item will begin playing when *Player*.**URL**, *Player*.**currentPlaylist**, or *Player*.**currentMedia** is set.</span></span> <span data-ttu-id="b3ddc-119">否則，它將不會開始播放，直到 *控制項* 為止。會呼叫 **play** 方法。</span><span class="sxs-lookup"><span data-stu-id="b3ddc-119">Otherwise, it will not start playing until the *Controls*.**play** method is called.</span></span>

<span data-ttu-id="b3ddc-120">由於 Windows Media Player 完整模式的 **autoStart** 屬性可以由外來事件全域設定 (例如載入 CD) ，因此沒有適用于外觀和遠端播放機控制項的可靠預設值。</span><span class="sxs-lookup"><span data-stu-id="b3ddc-120">Because the **autoStart** property for the full mode of Windows Media Player can be set globally by external events (such as loading a CD), there is no reliable default value for skins and remoted Player controls.</span></span> <span data-ttu-id="b3ddc-121">這是因為在這兩種情況下都會使用完整模式播放機的播放引擎。</span><span class="sxs-lookup"><span data-stu-id="b3ddc-121">This is because the playback engine of the full mode Player is used in both cases.</span></span>

<span data-ttu-id="b3ddc-122">您應該在設定 *Player* 之前，立即將 **autoStart** 設定為 false。**URL**、*播放機*。**currentPlaylist** 或 *播放機*。如果您想要確保媒體專案不會立即開始播放，請在 [外觀] 和 [遠端 Windows Media Player] 控制項中 **currentMedia** 。</span><span class="sxs-lookup"><span data-stu-id="b3ddc-122">You should set **autoStart** to false immediately before you set *Player*.**URL**, *Player*.**currentPlaylist**, or *Player*.**currentMedia** in skins and remoted Windows Media Player controls if you want to ensure that the media item does not start playing immediately.</span></span> <span data-ttu-id="b3ddc-123">此外，除非您在指定媒體專案之前立即將 **autostart** 設定為 true，否則您不應該依賴此設定來替代使用 *控制項*。**play** 方法。</span><span class="sxs-lookup"><span data-stu-id="b3ddc-123">Also, unless you set **autostart** to true immediately before specifying a media item, you should not rely on this setting as a substitute for using the *Controls*.**play** method.</span></span>

## <a name="examples"></a><span data-ttu-id="b3ddc-124">範例</span><span class="sxs-lookup"><span data-stu-id="b3ddc-124">Examples</span></span>

<span data-ttu-id="b3ddc-125">下列範例會建立 HTML CHECKBOX 元素，讓使用者可以指定播放程式控制項是否自動播放目前的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="b3ddc-125">The following example creates an HTML CHECKBOX element that allows the user to specify whether the Player control plays the current media item automatically.</span></span> <span data-ttu-id="b3ddc-126">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="b3ddc-126">The **Player** object was created with ID = "Player".</span></span>


```
<!-- Create an HTML CHECKBOX control. -->
<INPUT  TYPE = "CHECKBOX" ID = AS
              onClick = "
    /* Use the CHECKBOX state to specify the value 
       of the autoStart property. */
    Player.settings.autoStart = AS.checked;
"> 

```



## <a name="requirements"></a><span data-ttu-id="b3ddc-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3ddc-127">Requirements</span></span>



| <span data-ttu-id="b3ddc-128">需求</span><span class="sxs-lookup"><span data-stu-id="b3ddc-128">Requirement</span></span> | <span data-ttu-id="b3ddc-129">值</span><span class="sxs-lookup"><span data-stu-id="b3ddc-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b3ddc-130">版本</span><span class="sxs-lookup"><span data-stu-id="b3ddc-130">Version</span></span><br/> | <span data-ttu-id="b3ddc-131">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="b3ddc-131">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b3ddc-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b3ddc-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="b3ddc-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3ddc-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3ddc-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3ddc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3ddc-135">**CurrentMedia**</span><span class="sxs-lookup"><span data-stu-id="b3ddc-135">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="b3ddc-136">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="b3ddc-136">**Player.URL**</span></span>](player-url.md)
</dt> <dt>

[<span data-ttu-id="b3ddc-137">**Settings 物件**</span><span class="sxs-lookup"><span data-stu-id="b3ddc-137">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





