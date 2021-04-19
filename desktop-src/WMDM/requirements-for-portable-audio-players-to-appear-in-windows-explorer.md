---
title: 便攜音訊播放程式需要出現在 Windows 檔案總管中的需求
description: 便攜音訊播放程式需要出現在 Windows 檔案總管中的需求
ms.assetid: 94227ed8-56e7-4366-9c38-9b5dbf907e16
keywords:
- Windows Media 裝置管理員、便攜音訊播放機
- 裝置管理員、便攜音訊播放機
- 程式設計指南，便攜音訊播放機
- 服務提供者，便攜音訊播放機
- 建立服務提供者，便攜音訊播放機
- 便攜音訊播放機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a163bf04f4185bc1325aa12ea6acddd43191529
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969460"
---
# <a name="requirements-for-portable-audio-players-to-appear-in-windows-explorer"></a><span data-ttu-id="55b64-109">便攜音訊播放程式需要出現在 Windows 檔案總管中的需求</span><span class="sxs-lookup"><span data-stu-id="55b64-109">Requirements for Portable Audio Players to Appear in Windows Explorer</span></span>

<span data-ttu-id="55b64-110">便攜音訊播放機 shell 命名空間延伸模組可讓 Windows 使用者以一致的方式管理由 Windows Media 裝置管理員管理的音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="55b64-110">The portable audio player shell namespace extension provides Windows users with a consistent way to manage audio devices that are managed by Windows Media Device Manager.</span></span> <span data-ttu-id="55b64-111">如果您根據下列指導方針來撰寫服務提供者和驅動程式元件，則您的裝置會顯示在 shell 命名空間中。</span><span class="sxs-lookup"><span data-stu-id="55b64-111">If you author your service provider and driver components according to the following guidelines, your device will show up in the shell namespace.</span></span> <span data-ttu-id="55b64-112">使用者將能夠在 Windows 檔案總管中以一致的方式與裝置內容互動，以執行複製、刪除和重新命名等基本作業。</span><span class="sxs-lookup"><span data-stu-id="55b64-112">Users will be able to interact with the contents of your device in a consistent manner in Windows Explorer to perform basic operations such as copy, delete, and rename.</span></span>

<span data-ttu-id="55b64-113">下列服務提供者和驅動程式元件的 shell 需求，旨在補充一般 Windows Media 裝置管理員指導方針。</span><span class="sxs-lookup"><span data-stu-id="55b64-113">The following shell requirements for service provider and driver components are intended to supplement the general Windows Media Device Manager guidelines.</span></span>

<span data-ttu-id="55b64-114">裝置功能</span><span class="sxs-lookup"><span data-stu-id="55b64-114">Device Capabilities</span></span>

<span data-ttu-id="55b64-115">Windows Media 裝置管理員服務提供者的支援功能應該是明確的。</span><span class="sxs-lookup"><span data-stu-id="55b64-115">Windows Media Device Manager service providers should be explicit in their supported capabilities.</span></span> <span data-ttu-id="55b64-116">如果不支援呼叫，就必須傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="55b64-116">If a call is not supported, an error code must be returned.</span></span> <span data-ttu-id="55b64-117">您必須設定適當的欄位，以便在從下列函式傳回時存在或缺少功能：</span><span class="sxs-lookup"><span data-stu-id="55b64-117">The appropriate fields must be set for the presence or absence of capabilities on return from the following functions:</span></span>

-   [<span data-ttu-id="55b64-118">**IMDSPStorageGlobals::GetCapabilities**</span><span class="sxs-lookup"><span data-stu-id="55b64-118">**IMDSPStorageGlobals::GetCapabilities**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getcapabilities)
-   [<span data-ttu-id="55b64-119">**IMDSPStorage：： GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="55b64-119">**IMDSPStorage::GetAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
-   [<span data-ttu-id="55b64-120">**IMDSPDevice::GetFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="55b64-120">**IMDSPDevice::GetFormatSupport**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)

<span data-ttu-id="55b64-121">服務提供者必須支援下列功能，才能與 shell 相容：</span><span class="sxs-lookup"><span data-stu-id="55b64-121">Service providers must support the following capabilities to be compatible with the shell:</span></span>

-   <span data-ttu-id="55b64-122">複製到裝置 (支援取消和進度回呼) </span><span class="sxs-lookup"><span data-stu-id="55b64-122">Copy to device (with support for cancel and progress callbacks)</span></span>
-   <span data-ttu-id="55b64-123">刪除裝置 (的檔案，並支援取消和進度回呼) </span><span class="sxs-lookup"><span data-stu-id="55b64-123">Delete file from device (with support for cancel and progress callbacks)</span></span>
-   <span data-ttu-id="55b64-124">重新命名裝置上的檔案</span><span class="sxs-lookup"><span data-stu-id="55b64-124">Rename file on device</span></span>
-   <span data-ttu-id="55b64-125">空間報告 (空間總計、可用空間、無法使用的空間) </span><span class="sxs-lookup"><span data-stu-id="55b64-125">Space reporting (total space, free space, unusable space)</span></span>
-   <span data-ttu-id="55b64-126">隨插即用 (請參閱 [為裝置啟用 PnP](enabling-pnp-for-devices.md)) </span><span class="sxs-lookup"><span data-stu-id="55b64-126">Plug and Play (see [Enabling PnP for Devices](enabling-pnp-for-devices.md))</span></span>
-   <span data-ttu-id="55b64-127">格式化 (最好支援取消和進度回呼) </span><span class="sxs-lookup"><span data-stu-id="55b64-127">Format (preferably with support for cancel and progress callbacks)</span></span>

<span data-ttu-id="55b64-128">如果支援中繼資料，則必須針對個別檔案支援下欄欄位。</span><span class="sxs-lookup"><span data-stu-id="55b64-128">If metadata is supported, the following fields must be supported for individual files.</span></span> <span data-ttu-id="55b64-129">如果沒有可用的資料，應該將欄位初始化為空字串：</span><span class="sxs-lookup"><span data-stu-id="55b64-129">If no data is available, the field should be initialized as an empty string:</span></span>



| <span data-ttu-id="55b64-130">欄位</span><span class="sxs-lookup"><span data-stu-id="55b64-130">Field</span></span>        | <span data-ttu-id="55b64-131">WMDM 中定義的常數 () </span><span class="sxs-lookup"><span data-stu-id="55b64-131">Constant (defined in WMDM.idl)</span></span> | <span data-ttu-id="55b64-132">元資料標記</span><span class="sxs-lookup"><span data-stu-id="55b64-132">Metadata tag</span></span>    |
|--------------|--------------------------------|-----------------|
| <span data-ttu-id="55b64-133">歌曲標題</span><span class="sxs-lookup"><span data-stu-id="55b64-133">Song Title</span></span>   | <span data-ttu-id="55b64-134">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="55b64-134">g\_wszWMDMTitle</span></span>                | <span data-ttu-id="55b64-135">WMDM/標題</span><span class="sxs-lookup"><span data-stu-id="55b64-135">WMDM/Title</span></span>      |
| <span data-ttu-id="55b64-136">追蹤編號</span><span class="sxs-lookup"><span data-stu-id="55b64-136">Track Number</span></span> | <span data-ttu-id="55b64-137">g \_ wszWMDMTrack</span><span class="sxs-lookup"><span data-stu-id="55b64-137">g\_wszWMDMTrack</span></span>                | <span data-ttu-id="55b64-138">WMDM/追蹤</span><span class="sxs-lookup"><span data-stu-id="55b64-138">WMDM/Track</span></span>      |
| <span data-ttu-id="55b64-139">演出者</span><span class="sxs-lookup"><span data-stu-id="55b64-139">Artist</span></span>       | <span data-ttu-id="55b64-140">g \_ wszWMDMAuthor</span><span class="sxs-lookup"><span data-stu-id="55b64-140">g\_wszWMDMAuthor</span></span>               | <span data-ttu-id="55b64-141">WMDM/作者</span><span class="sxs-lookup"><span data-stu-id="55b64-141">WMDM/Author</span></span>     |
| <span data-ttu-id="55b64-142">專輯</span><span class="sxs-lookup"><span data-stu-id="55b64-142">Album</span></span>        | <span data-ttu-id="55b64-143">g \_ wszWMDMAlbumTitle</span><span class="sxs-lookup"><span data-stu-id="55b64-143">g\_wszWMDMAlbumTitle</span></span>           | <span data-ttu-id="55b64-144">WMDM/AlbumTitle</span><span class="sxs-lookup"><span data-stu-id="55b64-144">WMDM/AlbumTitle</span></span> |
| <span data-ttu-id="55b64-145">Year</span><span class="sxs-lookup"><span data-stu-id="55b64-145">Year</span></span>         | <span data-ttu-id="55b64-146">g \_ wszWMDMYear</span><span class="sxs-lookup"><span data-stu-id="55b64-146">g\_wszWMDMYear</span></span>                 | <span data-ttu-id="55b64-147">WMDM/Year</span><span class="sxs-lookup"><span data-stu-id="55b64-147">WMDM/Year</span></span>       |
| <span data-ttu-id="55b64-148">Genre</span><span class="sxs-lookup"><span data-stu-id="55b64-148">Genre</span></span>        | <span data-ttu-id="55b64-149">g \_ wszWMDMGenre</span><span class="sxs-lookup"><span data-stu-id="55b64-149">g\_wszWMDMGenre</span></span>                | <span data-ttu-id="55b64-150">WMDM/內容類型</span><span class="sxs-lookup"><span data-stu-id="55b64-150">WMDM/Genre</span></span>      |



 

<span data-ttu-id="55b64-151">並行</span><span class="sxs-lookup"><span data-stu-id="55b64-151">Concurrency</span></span>

<span data-ttu-id="55b64-152">Windows Media 裝置管理員的核心模式驅動程式必須健全，才能處理平行存取。</span><span class="sxs-lookup"><span data-stu-id="55b64-152">Kernel mode drivers for Windows Media Device Manager need to be robust in handling concurrent access.</span></span> <span data-ttu-id="55b64-153">例如，使用者可以同時透過 shell 和 media player 存取裝置，或直接透過 shell 中的多個視窗存取裝置。</span><span class="sxs-lookup"><span data-stu-id="55b64-153">For example, a user can be concurrently accessing the device through both the shell and media player or simply through multiple windows in the shell.</span></span> <span data-ttu-id="55b64-154">在處理並行處理的過程中，驅動程式應該不會假設是因為已載入服務提供者，而是裝置正在使用中。</span><span class="sxs-lookup"><span data-stu-id="55b64-154">As part of handling concurrency, drivers should not assume, just because the service provider is loaded, that the device is in use.</span></span> <span data-ttu-id="55b64-155">相反地，它們應該會執行鎖定機制，視個別作業的需要將裝置存取序列化。</span><span class="sxs-lookup"><span data-stu-id="55b64-155">Instead, they should implement a locking mechanism to serialize access to the device as needed for individual operations.</span></span>

<span data-ttu-id="55b64-156">UI</span><span class="sxs-lookup"><span data-stu-id="55b64-156">UI</span></span>

<span data-ttu-id="55b64-157">Windows Media 裝置管理員的服務提供者不應顯示任何使用者介面。</span><span class="sxs-lookup"><span data-stu-id="55b64-157">Service providers for Windows Media Device Manager should not show any user interface.</span></span> <span data-ttu-id="55b64-158">任何錯誤都應該盡可能地從方法呼叫傳回，做為特定的 Windows Media 裝置管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="55b64-158">Any errors should be returned from method calls as specific Windows Media Device Manager error codes whenever possible.</span></span>

<span data-ttu-id="55b64-159">在 Shell 中啟用</span><span class="sxs-lookup"><span data-stu-id="55b64-159">Enabling in the Shell</span></span>

<span data-ttu-id="55b64-160">如果您的套件符合所有 shell 需求，您可以在裝置參數下將 *ShowInShell* 值設定為1，讓您的裝置顯示在 shell 中。</span><span class="sxs-lookup"><span data-stu-id="55b64-160">If your package meets all of the shell requirements, you can enable your device to be shown in the shell by setting the *ShowInShell* value to 1 under the device parameters.</span></span> <span data-ttu-id="55b64-161">如需詳細資訊，請參閱 [裝置參數](device-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="55b64-161">For more information, see [Device Parameters](device-parameters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="55b64-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="55b64-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55b64-163">**建立服務提供者**</span><span class="sxs-lookup"><span data-stu-id="55b64-163">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




