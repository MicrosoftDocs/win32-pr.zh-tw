---
title: 自訂配置登錄設定
description: 自訂配置登錄設定
ms.assetid: ded2b492-7755-4ba5-87cf-720a79ec79de
keywords:
- Windows Media Player，自訂配置登錄設定
- Windows Media Player，架構
- Windows Media Player，登錄
- 登錄，自訂配置設定
- 登錄，配置
- 登錄，Windows Media Player 的設定
- 配置
- 自訂配置登錄設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a02649d9536140fff0ff0d3188a5b25feb49688
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021038"
---
# <a name="custom-scheme-registry-settings"></a><span data-ttu-id="446f8-111">自訂配置登錄設定</span><span class="sxs-lookup"><span data-stu-id="446f8-111">Custom Scheme Registry Settings</span></span>

<span data-ttu-id="446f8-112">配置是自訂的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="446f8-112">Schemes are custom protocols.</span></span> <span data-ttu-id="446f8-113">Windows Media Player 會維護使用者電腦上登錄中的配置清單。</span><span class="sxs-lookup"><span data-stu-id="446f8-113">Windows Media Player maintains a list of schemes in the registry on the user's computer.</span></span> <span data-ttu-id="446f8-114">當使用者嘗試播放數位媒體檔案時，Player 會先檢查 Windows Media 格式 SDK 是否支援該配置。</span><span class="sxs-lookup"><span data-stu-id="446f8-114">When the user attempts to play a digital media file, the Player first checks whether the Windows Media Format SDK supports the scheme.</span></span> <span data-ttu-id="446f8-115">如果不是，則播放清單會根據登錄中的清單來檢查配置。</span><span class="sxs-lookup"><span data-stu-id="446f8-115">If it doesn't, the Player checks the scheme against the list in the registry.</span></span> <span data-ttu-id="446f8-116">如果找到相符的值，播放程式就會檢查指出哪些基礎技術或 *運行* 時間 (（例如 Microsoft DirectShow 或 Windows MEDIA Format SDK) ）可以用來播放檔案的值。</span><span class="sxs-lookup"><span data-stu-id="446f8-116">If a match is found, the Player then checks a value that indicates which underlying technology, or *runtime* (such as Microsoft DirectShow or the Windows Media Format SDK), can be used to play the file.</span></span> <span data-ttu-id="446f8-117">如果找不到相符項，播放程式會向使用者呈現警告對話方塊，提示使用者嘗試播放該檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="446f8-117">If no match is found, the Player presents the user with a warning dialog box that prompts the user for permission to attempt to play the file.</span></span> <span data-ttu-id="446f8-118">如果您使用自訂通訊協定配置串流數位媒體檔案，您可以註冊配置並提供執行時間的值，以防止此警告出現在使用者的電腦上。</span><span class="sxs-lookup"><span data-stu-id="446f8-118">If you stream digital media files using a custom protocol scheme, you can prevent this warning from appearing on the user's computer by registering the scheme and providing a value for the runtime.</span></span>

<span data-ttu-id="446f8-119">配置清單會以一組符合已註冊配置的登錄機碼來維護，而不含冒號和兩個斜線 (：//) 。</span><span class="sxs-lookup"><span data-stu-id="446f8-119">The list of schemes is maintained as a set of registry keys that match the registered schemes, without the colon and the two slashes (://).</span></span> <span data-ttu-id="446f8-120">例如，用來串流豐富媒體的 wmhtml://配置金鑰，名為 "wmhtml"。</span><span class="sxs-lookup"><span data-stu-id="446f8-120">For example, the key for the wmhtml:// scheme, which is used to stream rich media, is named "wmhtml".</span></span> <span data-ttu-id="446f8-121">針對本機電腦和每個使用者都可以維護個別的清單。</span><span class="sxs-lookup"><span data-stu-id="446f8-121">A separate list is maintained for the local machine and for each user.</span></span> <span data-ttu-id="446f8-122">針對本機電腦，配置索引鍵是下列登錄機碼的子機碼：</span><span class="sxs-lookup"><span data-stu-id="446f8-122">For the local machine, the scheme keys are subkeys of the following registry key:</span></span>

<span data-ttu-id="446f8-123">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ 多媒體 \\ WMPlayer \\ 架構\\**</span><span class="sxs-lookup"><span data-stu-id="446f8-123">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Schemes\\**</span></span>

<span data-ttu-id="446f8-124">例如，本機電腦的 wmhtml://配置機碼為：</span><span class="sxs-lookup"><span data-stu-id="446f8-124">For example, the key for the wmhtml:// scheme for the local machine is:</span></span>

<span data-ttu-id="446f8-125">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ 多媒體 \\ WMPlayer \\ 配置 \\ wmhtml**</span><span class="sxs-lookup"><span data-stu-id="446f8-125">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Schemes\\wmhtml**</span></span>

<span data-ttu-id="446f8-126">若要變更此機碼中的值或建立新的子機碼，目前的使用者必須是電腦的系統管理員。</span><span class="sxs-lookup"><span data-stu-id="446f8-126">To change values in this key or to create a new subkey, the current user must be an administrator for the computer.</span></span>

<span data-ttu-id="446f8-127">針對個別使用者，配置索引鍵是下列登錄機碼的子機碼：</span><span class="sxs-lookup"><span data-stu-id="446f8-127">For individual users, the scheme keys are subkeys of the following registry key:</span></span>

<span data-ttu-id="446f8-128">**HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ MediaPlayer \\ Player \\ 方案\\**</span><span class="sxs-lookup"><span data-stu-id="446f8-128">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Player\\Schemes\\**</span></span>

<span data-ttu-id="446f8-129">例如，目前使用者的 wmhtml://配置索引鍵為：</span><span class="sxs-lookup"><span data-stu-id="446f8-129">For example, the key for the wmhtml:// scheme for the current user is:</span></span>

<span data-ttu-id="446f8-130">**HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ MediaPlayer \\ Player \\ 方案 \\ wmhtml**</span><span class="sxs-lookup"><span data-stu-id="446f8-130">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Player\\Schemes\\wmhtml**</span></span>

<span data-ttu-id="446f8-131">檢查已註冊的配置時，播放程式會先檢查位於 **HKEY \_ 本機 \_ 電腦** 中的值。</span><span class="sxs-lookup"><span data-stu-id="446f8-131">When checking for registered schemes, the Player first checks the values located in **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="446f8-132">如果找不到目前配置的任何值，則播放程式會接著檢查 **HKEY \_ 目前 \_ 使用者** 中的值。</span><span class="sxs-lookup"><span data-stu-id="446f8-132">If none are found for the current scheme, the Player next checks the values in **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="446f8-133">如果找不到目前配置的任何內容，播放程式會向使用者顯示警告。</span><span class="sxs-lookup"><span data-stu-id="446f8-133">If none are found for the current scheme, the Player displays the warning to the user.</span></span>

<span data-ttu-id="446f8-134">每個配置子機碼可能包含下列 *運行* 時間的其中一個可能值。</span><span class="sxs-lookup"><span data-stu-id="446f8-134">Each scheme subkey may contain one of the following possible values for *Runtime*.</span></span>



| <span data-ttu-id="446f8-135">值</span><span class="sxs-lookup"><span data-stu-id="446f8-135">Value</span></span> | <span data-ttu-id="446f8-136">描述</span><span class="sxs-lookup"><span data-stu-id="446f8-136">Description</span></span>                                |
|-------|--------------------------------------------|
| <span data-ttu-id="446f8-137">6</span><span class="sxs-lookup"><span data-stu-id="446f8-137">6</span></span>     | <span data-ttu-id="446f8-138">使用 Windows Media Format SDK 轉譯。</span><span class="sxs-lookup"><span data-stu-id="446f8-138">Render using the Windows Media Format SDK.</span></span> |
| <span data-ttu-id="446f8-139">7</span><span class="sxs-lookup"><span data-stu-id="446f8-139">7</span></span>     | <span data-ttu-id="446f8-140">使用 Microsoft DirectShow 轉譯。</span><span class="sxs-lookup"><span data-stu-id="446f8-140">Render using Microsoft DirectShow.</span></span>         |



 

<span data-ttu-id="446f8-141">變更 Windows Media 格式 SDK 支援的配置 *運行* 時間值將不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="446f8-141">Changing the *Runtime* value for a scheme that the Windows Media Format SDK supports will have no effect.</span></span> <span data-ttu-id="446f8-142">播放程式一律會使用 Windows Media Format SDK 做為 Windows Media Format SDK 所支援的配置執行時間。</span><span class="sxs-lookup"><span data-stu-id="446f8-142">The Player will always use the Windows Media Format SDK as the runtime for schemes that the Windows Media Format SDK supports.</span></span> <span data-ttu-id="446f8-143">此登錄值是設計來允許自訂配置的執行時間設定。</span><span class="sxs-lookup"><span data-stu-id="446f8-143">This registry value is designed to allow runtime configuration for custom schemes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="446f8-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="446f8-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="446f8-145">**登錄設定**</span><span class="sxs-lookup"><span data-stu-id="446f8-145">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




