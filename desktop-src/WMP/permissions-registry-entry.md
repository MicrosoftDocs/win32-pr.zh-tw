---
title: 許可權登錄專案
description: 許可權登錄專案
ms.assetid: 01d55d2d-fe29-4006-a34b-9fbc730f9cbc
keywords:
- Windows Media Player、副檔名
- Windows Media Player，許可權
- Windows Media Player，登錄
- 登錄、副檔名
- 登錄，許可權
- 登錄，Windows Media Player 的設定
- 副檔名登錄設定
- 權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aec86b4facec4babed4afed04ca342903670dbb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023018"
---
# <a name="permissions-registry-entry"></a><span data-ttu-id="7a159-111">許可權登錄專案</span><span class="sxs-lookup"><span data-stu-id="7a159-111">Permissions Registry Entry</span></span>

<span data-ttu-id="7a159-112">當 Windows Media Player 遇到自訂副檔名時，它會尋找符合擴充功能的登錄子機碼。</span><span class="sxs-lookup"><span data-stu-id="7a159-112">When Windows Media Player encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="7a159-113">此子機碼描述于副檔名登錄 [設定](file-name-extension-registry-settings.md)中。</span><span class="sxs-lookup"><span data-stu-id="7a159-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="7a159-114">其中一個可出現在擴充功能子機碼底下的登錄專案是 **許可權** 專案。</span><span class="sxs-lookup"><span data-stu-id="7a159-114">One of the registry entries that can appear under the extension's subkey is the **Permissions** entry.</span></span>

<span data-ttu-id="7a159-115">**許可權** 專案指定允許在具有自訂延伸模組的檔案上執行 Windows Media Player 的動作。</span><span class="sxs-lookup"><span data-stu-id="7a159-115">The **Permissions** entry specifies the actions that Windows Media Player is allowed to perform on files that have the custom extension.</span></span> <span data-ttu-id="7a159-116">**許可權** 專案具有下列格式。</span><span class="sxs-lookup"><span data-stu-id="7a159-116">The **Permissions** entry has the following form.</span></span>



| <span data-ttu-id="7a159-117">名稱</span><span class="sxs-lookup"><span data-stu-id="7a159-117">Name</span></span>        | <span data-ttu-id="7a159-118">類型</span><span class="sxs-lookup"><span data-stu-id="7a159-118">Type</span></span>           | <span data-ttu-id="7a159-119">值</span><span class="sxs-lookup"><span data-stu-id="7a159-119">Value</span></span>                                                                  |
|-------------|----------------|------------------------------------------------------------------------|
| <span data-ttu-id="7a159-120">權限</span><span class="sxs-lookup"><span data-stu-id="7a159-120">Permissions</span></span> | <span data-ttu-id="7a159-121">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="7a159-121">**REG\_DWORD**</span></span> | <span data-ttu-id="7a159-122">一組旗標，每個旗標都授與特定動作的許可權。</span><span class="sxs-lookup"><span data-stu-id="7a159-122">A set of flags, each of which grants permission for a specific action.</span></span> |



 

<span data-ttu-id="7a159-123">**許可權** 專案的值是下列其中一個或多個旗標的位 **or** 。</span><span class="sxs-lookup"><span data-stu-id="7a159-123">The value of the **Permissions** entry is a bitwise **OR** of one or more of the following flags.</span></span>



| <span data-ttu-id="7a159-124"> (decimal 值的旗標) </span><span class="sxs-lookup"><span data-stu-id="7a159-124">Flag (decimal value)</span></span> | <span data-ttu-id="7a159-125">描述</span><span class="sxs-lookup"><span data-stu-id="7a159-125">Description</span></span>                                                                                                                                                                                                                                                                   |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a159-126">1</span><span class="sxs-lookup"><span data-stu-id="7a159-126">1</span></span>                    | <span data-ttu-id="7a159-127">播放的許可權。</span><span class="sxs-lookup"><span data-stu-id="7a159-127">Permission for playback.</span></span> <span data-ttu-id="7a159-128">可以播放具有已註冊之副檔名的檔案。</span><span class="sxs-lookup"><span data-stu-id="7a159-128">Files having the registered file name extension can be played.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="7a159-129">2</span><span class="sxs-lookup"><span data-stu-id="7a159-129">2</span></span>                    | <span data-ttu-id="7a159-130">放置資料夾的許可權。</span><span class="sxs-lookup"><span data-stu-id="7a159-130">Permission for folder drop.</span></span> <span data-ttu-id="7a159-131">當使用者拖曳包含檔案的資料夾，並將它放在播放程式的使用者介面上時，所建立的播放清單中會包含已註冊之副檔名的檔案。</span><span class="sxs-lookup"><span data-stu-id="7a159-131">Files having the registered file name extension will be included in the playlist created when the user drags a folder containing the files and drops it on the user interface of the Player.</span></span>                                                      |
| <span data-ttu-id="7a159-132">4</span><span class="sxs-lookup"><span data-stu-id="7a159-132">4</span></span>                    | <span data-ttu-id="7a159-133">媒體 CD 的許可權。</span><span class="sxs-lookup"><span data-stu-id="7a159-133">Permission for media CD.</span></span> <span data-ttu-id="7a159-134">當包含檔案的 CD 插入 cd-rom 光碟機時，會在建立的播放清單中包含已註冊副檔名的檔案。</span><span class="sxs-lookup"><span data-stu-id="7a159-134">Files having the registered file name extension will be included in the playlist created when a CD containing the files is inserted into the CD-ROM drive.</span></span>                                                                                           |
| <span data-ttu-id="7a159-135">8</span><span class="sxs-lookup"><span data-stu-id="7a159-135">8</span></span>                    | <span data-ttu-id="7a159-136">程式庫的許可權。</span><span class="sxs-lookup"><span data-stu-id="7a159-136">Permission for the library.</span></span> <span data-ttu-id="7a159-137">具有已註冊之副檔名的檔案可以新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="7a159-137">Files having the registered file name extension can be added to the library.</span></span> <span data-ttu-id="7a159-138">轉換外掛程式的必要項。</span><span class="sxs-lookup"><span data-stu-id="7a159-138">Required for conversion plug-ins.</span></span>                                                                                                                                    |
| <span data-ttu-id="7a159-139">16</span><span class="sxs-lookup"><span data-stu-id="7a159-139">16</span></span>                   | <span data-ttu-id="7a159-140">HTML 串流的許可權。</span><span class="sxs-lookup"><span data-stu-id="7a159-140">Permission for HTML streaming.</span></span> <span data-ttu-id="7a159-141">從 Web 串流傳遞時，具有已註冊之副檔名的檔案將會插入 Internet Explorer 快取中。</span><span class="sxs-lookup"><span data-stu-id="7a159-141">Files having the registered file name extension will be inserted into the Internet Explorer cache when delivered from a Web stream.</span></span>                                                                                                            |
| <span data-ttu-id="7a159-142">128</span><span class="sxs-lookup"><span data-stu-id="7a159-142">128</span></span>                  | <span data-ttu-id="7a159-143">轉碼的許可權。</span><span class="sxs-lookup"><span data-stu-id="7a159-143">Permission for transcoding.</span></span> <span data-ttu-id="7a159-144">具有已註冊之副檔名的檔案，在特定情況下可以轉碼為 Windows Media 格式。</span><span class="sxs-lookup"><span data-stu-id="7a159-144">Files having the registered file name extension can be transcoded to Windows Media Format under certain conditions.</span></span> <span data-ttu-id="7a159-145">請參閱 [IWMPTranscodePolicy：： allowTranscode](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmptranscodepolicy-allowtranscode)。</span><span class="sxs-lookup"><span data-stu-id="7a159-145">See [IWMPTranscodePolicy::allowTranscode](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmptranscodepolicy-allowtranscode).</span></span> <span data-ttu-id="7a159-146">需要 Windows Media Player 10 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="7a159-146">Requires Windows Media Player 10 or later.</span></span> |



 

<span data-ttu-id="7a159-147">當使用者嘗試播放具有自訂副檔名的媒體檔案時，Windows Media Player 會尋找符合延伸模組的登錄子機碼。</span><span class="sxs-lookup"><span data-stu-id="7a159-147">When the user attempts to play a media file that has a custom file name extension, Windows Media Player looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="7a159-148">如果找不到相符項，播放程式會向使用者呈現警告對話方塊，提示使用者嘗試播放該檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="7a159-148">If no match is found, the Player presents the user with a warning dialog box that prompts the user for permission to attempt to play the file.</span></span> <span data-ttu-id="7a159-149">如果您使用自訂副檔名來建立數位媒體檔案，您可以註冊副檔名並提供 **許可權** 專案，以防止此警告出現在使用者的電腦上。</span><span class="sxs-lookup"><span data-stu-id="7a159-149">If you create digital media files with custom file name extensions, you can prevent this warning from appearing on the user's computer by registering the file name extension and providing a **Permissions** entry.</span></span>

<span data-ttu-id="7a159-150">Windows Media Player 9 系列和更新版本支援旗標值 128) 以外的 **許可權** 專案 (。</span><span class="sxs-lookup"><span data-stu-id="7a159-150">The **Permissions** entry (except for the flag value 128) is supported by Windows Media Player 9 Series and later.</span></span> <span data-ttu-id="7a159-151">Windows Media Player 10 和更新版本支援旗標值128。</span><span class="sxs-lookup"><span data-stu-id="7a159-151">The flag value 128 is supported by Windows Media Player 10 and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a159-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="7a159-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a159-153">**副檔名登錄設定**</span><span class="sxs-lookup"><span data-stu-id="7a159-153">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




