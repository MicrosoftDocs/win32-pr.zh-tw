---
title: Windows Media Player SDK) 的 Settings 物件 (
description: Settings 物件提供使用下列屬性和方法來修改各種 Windows Media Player 設定的方式。
ms.assetid: f22e8c37-f0c6-4268-a6ed-ce03cff5f3e5
keywords:
- Settings 物件 Windows Media Player
topic_type:
- apiref
api_name:
- Settings Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d01a521dbccb351045f09dc15d71779fd9362cf4
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/12/2019
ms.locfileid: "103841627"
---
# <a name="settings-object"></a><span data-ttu-id="5f62e-104">Settings 物件</span><span class="sxs-lookup"><span data-stu-id="5f62e-104">Settings Object</span></span>

<span data-ttu-id="5f62e-105">**Settings** 物件提供使用下列屬性和方法來修改各種 Windows Media Player 設定的方式。</span><span class="sxs-lookup"><span data-stu-id="5f62e-105">The **Settings** object provides a way to modify various Windows Media Player settings by using the following properties and methods.</span></span>

<span data-ttu-id="5f62e-106">**Settings** 物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="5f62e-106">The **Settings** object supports the following properties.</span></span>



| <span data-ttu-id="5f62e-107">屬性</span><span class="sxs-lookup"><span data-stu-id="5f62e-107">Property</span></span>                                                  | <span data-ttu-id="5f62e-108">描述</span><span class="sxs-lookup"><span data-stu-id="5f62e-108">Description</span></span>                                                                                                                      |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5f62e-109">啟動</span><span class="sxs-lookup"><span data-stu-id="5f62e-109">autoStart</span></span>](settings-autostart.md)                       | <span data-ttu-id="5f62e-110">指定或抓取值，指出目前的媒體專案是否會自動開始播放。</span><span class="sxs-lookup"><span data-stu-id="5f62e-110">Specifies or retrieves a value indicating whether the current media item begins playing automatically.</span></span>                           |
| [<span data-ttu-id="5f62e-111">平衡</span><span class="sxs-lookup"><span data-stu-id="5f62e-111">balance</span></span>](settings-balance.md)                           | <span data-ttu-id="5f62e-112">指定或抓取目前的立體餘額。</span><span class="sxs-lookup"><span data-stu-id="5f62e-112">Specifies or retrieves the current stereo balance.</span></span>                                                                               |
| [<span data-ttu-id="5f62e-113">baseURL</span><span class="sxs-lookup"><span data-stu-id="5f62e-113">baseURL</span></span>](settings-baseurl.md)                           | <span data-ttu-id="5f62e-114">使用內嵌在媒體檔案中的 URL 指令碼命令，指定或抓取用來解析相對路徑的基底 URL。</span><span class="sxs-lookup"><span data-stu-id="5f62e-114">Specifies or retrieves the base URL used for relative path resolution with URL script commands that are embedded in media files.</span></span> |
| [<span data-ttu-id="5f62e-115">defaultAudioLanguage</span><span class="sxs-lookup"><span data-stu-id="5f62e-115">defaultAudioLanguage</span></span>](settings-defaultaudiolanguage.md) | <span data-ttu-id="5f62e-116">抓取 Windows Media Player 中指定之預設音訊語言 (LCID) 的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="5f62e-116">Retrieves the locale identifier (LCID) of the default audio language specified in Windows Media Player.</span></span>                          |
| [<span data-ttu-id="5f62e-117">defaultFrame</span><span class="sxs-lookup"><span data-stu-id="5f62e-117">defaultFrame</span></span>](settings-defaultframe.md)                 | <span data-ttu-id="5f62e-118">指定或抓取用來顯示 **ScriptCommand** 事件中所接收之 URL 的框架名稱。</span><span class="sxs-lookup"><span data-stu-id="5f62e-118">Specifies or retrieves the name of the frame used to display a URL that is received in a **ScriptCommand** event.</span></span>                |
| [<span data-ttu-id="5f62e-119">enableErrorDialogs</span><span class="sxs-lookup"><span data-stu-id="5f62e-119">enableErrorDialogs</span></span>](settings-enableerrordialogs.md)     | <span data-ttu-id="5f62e-120">指定或抓取值，指出是否會自動顯示錯誤對話方塊。</span><span class="sxs-lookup"><span data-stu-id="5f62e-120">Specifies or retrieves a value indicating whether error dialog boxes are shown automatically.</span></span>                                    |
| [<span data-ttu-id="5f62e-121">invokeURLs</span><span class="sxs-lookup"><span data-stu-id="5f62e-121">invokeURLs</span></span>](settings-invokeurls.md)                     | <span data-ttu-id="5f62e-122">指定或抓取值，指出 URL 事件是否應啟動網頁瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="5f62e-122">Specifies or retrieves a value indicating whether URL events should launch a Web browser.</span></span>                                        |
| [<span data-ttu-id="5f62e-123">isAvailable</span><span class="sxs-lookup"><span data-stu-id="5f62e-123">isAvailable</span></span>](settings-isavailable.md)                   | <span data-ttu-id="5f62e-124">抓取指定的資訊類型是否可用，或是否可以執行指定的動作。</span><span class="sxs-lookup"><span data-stu-id="5f62e-124">Retrieves whether a specified type of information is available or a specified action can be performed.</span></span>                           |
| [<span data-ttu-id="5f62e-125">mediaAccessRights</span><span class="sxs-lookup"><span data-stu-id="5f62e-125">mediaAccessRights</span></span>](settings-mediaaccessrights.md)       | <span data-ttu-id="5f62e-126">抓取值，指出目前授與程式庫存取權的許可權。</span><span class="sxs-lookup"><span data-stu-id="5f62e-126">Retrieves a value indicating the rights currently granted for library access.</span></span>                                                    |
| [<span data-ttu-id="5f62e-127">靜音</span><span class="sxs-lookup"><span data-stu-id="5f62e-127">mute</span></span>](settings-mute.md)                                 | <span data-ttu-id="5f62e-128">指定或抓取值，指出音訊是否已靜音。</span><span class="sxs-lookup"><span data-stu-id="5f62e-128">Specifies or retrieves a value indicating whether audio is muted.</span></span>                                                                |
| [<span data-ttu-id="5f62e-129">playCount</span><span class="sxs-lookup"><span data-stu-id="5f62e-129">playCount</span></span>](settings-playcount.md)                       | <span data-ttu-id="5f62e-130">指定或抓取媒體專案將播放的次數。</span><span class="sxs-lookup"><span data-stu-id="5f62e-130">Specifies or retrieves the number of times a media item will play.</span></span>                                                               |
| [<span data-ttu-id="5f62e-131">率</span><span class="sxs-lookup"><span data-stu-id="5f62e-131">rate</span></span>](settings-rate.md)                                 | <span data-ttu-id="5f62e-132">指定或抓取目前的播放速率。</span><span class="sxs-lookup"><span data-stu-id="5f62e-132">Specifies or retrieves the current playback rate.</span></span>                                                                                |
| [<span data-ttu-id="5f62e-133">體積</span><span class="sxs-lookup"><span data-stu-id="5f62e-133">volume</span></span>](settings-volume.md)                             | <span data-ttu-id="5f62e-134">指定或抓取目前的磁片區。</span><span class="sxs-lookup"><span data-stu-id="5f62e-134">Specifies or retrieves the current volume.</span></span>                                                                                       |



 

<span data-ttu-id="5f62e-135">**Settings** 物件支援下列方法。</span><span class="sxs-lookup"><span data-stu-id="5f62e-135">The **Settings** object supports the following methods.</span></span>



| <span data-ttu-id="5f62e-136">方法</span><span class="sxs-lookup"><span data-stu-id="5f62e-136">Method</span></span>                                                            | <span data-ttu-id="5f62e-137">描述</span><span class="sxs-lookup"><span data-stu-id="5f62e-137">Description</span></span>                                                 |
|-------------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="5f62e-138">getMode</span><span class="sxs-lookup"><span data-stu-id="5f62e-138">getMode</span></span>](settings-getmode.md)                                   | <span data-ttu-id="5f62e-139">判斷迴圈模式或隨機播放模式是否為使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="5f62e-139">Determines whether the loop mode or shuffle mode is active.</span></span> |
| [<span data-ttu-id="5f62e-140">requestMediaAccessRights</span><span class="sxs-lookup"><span data-stu-id="5f62e-140">requestMediaAccessRights</span></span>](settings-requestmediaaccessrights.md) | <span data-ttu-id="5f62e-141">要求指定的媒體櫃存取層級。</span><span class="sxs-lookup"><span data-stu-id="5f62e-141">Requests a specified level of access to the library.</span></span>        |
| [<span data-ttu-id="5f62e-142">setMode</span><span class="sxs-lookup"><span data-stu-id="5f62e-142">setMode</span></span>](settings-setmode.md)                                   | <span data-ttu-id="5f62e-143">將迴圈模式或隨機模式設定為 [使用中] 或 [非使用中]。</span><span class="sxs-lookup"><span data-stu-id="5f62e-143">Sets the loop mode or shuffle mode to active or inactive.</span></span>   |



 

<span data-ttu-id="5f62e-144">您可以透過下列屬性來存取 **設定** 物件。</span><span class="sxs-lookup"><span data-stu-id="5f62e-144">The **Settings** object is accessed through the following property.</span></span>



| <span data-ttu-id="5f62e-145">Object</span><span class="sxs-lookup"><span data-stu-id="5f62e-145">Object</span></span>                      | <span data-ttu-id="5f62e-146">屬性</span><span class="sxs-lookup"><span data-stu-id="5f62e-146">Property</span></span>                        |
|-----------------------------|---------------------------------|
| [<span data-ttu-id="5f62e-147">球員</span><span class="sxs-lookup"><span data-stu-id="5f62e-147">Player</span></span>](player-object.md) | [<span data-ttu-id="5f62e-148">設定</span><span class="sxs-lookup"><span data-stu-id="5f62e-148">settings</span></span>](player-settings.md) |



 

## <a name="see-also"></a><span data-ttu-id="5f62e-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f62e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f62e-150">**腳本的物件模型參考**</span><span class="sxs-lookup"><span data-stu-id="5f62e-150">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




