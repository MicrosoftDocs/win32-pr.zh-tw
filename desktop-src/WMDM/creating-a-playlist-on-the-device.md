---
title: 在裝置上建立播放清單
description: 在裝置上建立播放清單
ms.assetid: 9f803e1a-ff33-443a-9448-e8c875d77e51
keywords:
- Windows Media 裝置管理員、播放清單
- 裝置管理員，播放清單
- 程式設計指南，播放清單
- 桌面應用程式，播放清單
- 建立 Windows Media 裝置管理員應用程式、播放清單
- 摘要播放清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c287cc406b795db07fde3f10103822dea32185a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300611"
---
# <a name="creating-a-playlist-on-the-device"></a><span data-ttu-id="6d204-109">在裝置上建立播放清單</span><span class="sxs-lookup"><span data-stu-id="6d204-109">Creating a Playlist on the Device</span></span>

<span data-ttu-id="6d204-110">Windows Media 裝置管理員 SDK 提供 MTP 應用程式在裝置上建立播放清單的方法。</span><span class="sxs-lookup"><span data-stu-id="6d204-110">The Windows Media Device Manager SDK provides the means for an MTP application to create a playlist on a device.</span></span> <span data-ttu-id="6d204-111">這種類型的播放清單稱為「摘要播放清單」（ *abstract* 播放清單），因為在裝置上建立的檔案不包含媒體資料，而只有中繼資料（保存播放清單中媒體檔案的連結）。</span><span class="sxs-lookup"><span data-stu-id="6d204-111">This type of playlist is called an *abstract* playlist, because the file created on the device contains no media data, but only metadata, which holds the links to media files in the playlist.</span></span>

<span data-ttu-id="6d204-112">您可以在裝置上建立的其他抽象專案包括專輯 (基本上是具有額外屬性的播放清單，例如封面) 、連絡人和訊息。</span><span class="sxs-lookup"><span data-stu-id="6d204-112">Other abstract items that can be created on the device include albums (essentially playlists with extra properties such as cover art), contacts, and messages.</span></span>

<span data-ttu-id="6d204-113">**建立播放清單**</span><span class="sxs-lookup"><span data-stu-id="6d204-113">**To create a playlist**</span></span>

1.  <span data-ttu-id="6d204-114">取得目標裝置的 [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3) 介面。</span><span class="sxs-lookup"><span data-stu-id="6d204-114">Acquire an [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3) interface to the target device.</span></span>
2.  <span data-ttu-id="6d204-115">呼叫 [**IWMDMDevice3：： GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) 以取得 g \_ wszWMDMFormatsSupported 屬性。</span><span class="sxs-lookup"><span data-stu-id="6d204-115">Call [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) to obtain the g\_wszWMDMFormatsSupported property.</span></span>
3.  <span data-ttu-id="6d204-116">如果不支援播放清單的格式，則不允許將播放清單傳送至裝置，並略過下列步驟。</span><span class="sxs-lookup"><span data-stu-id="6d204-116">If no playlist formats are supported, disallow sending playlists to the device, and skip the following steps.</span></span> <span data-ttu-id="6d204-117">否則，請選擇與最接近預期物件類型相符的裝置支援格式代碼。</span><span class="sxs-lookup"><span data-stu-id="6d204-117">Otherwise, choose the device-supported format code that matches most closely the intended object type.</span></span> <span data-ttu-id="6d204-118">一般 WMDM \_ FORMATCODE \_ ABSTRACTAUDIOVIDEOPLAYLIST 和 WMDM \_ FORMATCODE \_ ABSTRACTAUDIOLAYLIST 格式代碼是最常支援的。</span><span class="sxs-lookup"><span data-stu-id="6d204-118">The generic WMDM\_FORMATCODE\_ABSTRACTAUDIOVIDEOPLAYLIST and WMDM\_FORMATCODE\_ABSTRACTAUDIOLAYLIST format codes are the most commonly supported.</span></span>
4.  <span data-ttu-id="6d204-119">取得儲存體 (您要在其中建立物件) 根目錄或資料夾的 [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) 介面。</span><span class="sxs-lookup"><span data-stu-id="6d204-119">Obtain an [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) interface for the storage (the root or a folder) where you want to create the object.</span></span> <span data-ttu-id="6d204-120">如果播放清單物件放在名為「播放清單」的最上層資料夾中，某些裝置的效果最佳。</span><span class="sxs-lookup"><span data-stu-id="6d204-120">Some devices work best if the playlist object is placed in a top level folder named "Playlists".</span></span>
5.  <span data-ttu-id="6d204-121">使用 [**IWMDMStorage3：： CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject)建立空白的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="6d204-121">Create an empty metadata object by using [**IWMDMStorage3::CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject).</span></span>
6.  <span data-ttu-id="6d204-122">使用上一個步驟中取得的 **IWMDMMetaData** 介面，呼叫 [**IWMDMMetaData：： AddItem**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-additem) 將您選擇的格式程式碼 (從步驟 3) 新增至儲存體中繼資料屬性。</span><span class="sxs-lookup"><span data-stu-id="6d204-122">Using the **IWMDMMetaData** interface obtained in the previous step, call [**IWMDMMetaData::AddItem**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-additem) to add your chosen format code (from step 3) to the storage metadata properties.</span></span>
7.  <span data-ttu-id="6d204-123">從 **IWMDMStorage3** 介面取得 [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3)介面。</span><span class="sxs-lookup"><span data-stu-id="6d204-123">Obtain the [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) interface from the **IWMDMStorage3** interface.</span></span>
8.  <span data-ttu-id="6d204-124">呼叫 [**IWMDMStorageControl3：： Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) ，以在選取的儲存體中插入新的播放清單檔案。</span><span class="sxs-lookup"><span data-stu-id="6d204-124">Call [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) to insert a new playlist file in the selected storage.</span></span> <span data-ttu-id="6d204-125">此檔案包含您在步驟5中建立並傳遞至 **Insert3** 之 **IWMDMMetaData** 介面所代表的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="6d204-125">This file contains the metadata represented by the **IWMDMMetaData** interface you created in step 5 and passed to **Insert3**.</span></span> <span data-ttu-id="6d204-126">方法會傳回播放清單檔案的 **IWMDMStorage** 介面;您可以查詢 [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4) 介面。</span><span class="sxs-lookup"><span data-stu-id="6d204-126">The method returns an **IWMDMStorage** interface for the playlist file; you can query for the [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4) interface.</span></span>
9.  <span data-ttu-id="6d204-127">呼叫 [**IWMDMStorage4：： SetReferences**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences) ，以建立播放清單中媒體檔案的 **IWMDMStorage** 介面參考。</span><span class="sxs-lookup"><span data-stu-id="6d204-127">Call [**IWMDMStorage4::SetReferences**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences) to create references to the **IWMDMStorage** interfaces of the media files in the playlist.</span></span>

<span data-ttu-id="6d204-128">如需範例程式碼，請參閱 \_ [範例桌面應用程式](sample-desktop-application.md)中的 OnCreatePlaylist 函式。</span><span class="sxs-lookup"><span data-stu-id="6d204-128">For example code, see the \_OnCreatePlaylist function in the [Sample Desktop Application](sample-desktop-application.md).</span></span>

> [!Note]  
> <span data-ttu-id="6d204-129">Microsoft 提供的 MTP 服務提供者可讓應用程式在中繼資料中設定參考。</span><span class="sxs-lookup"><span data-stu-id="6d204-129">The Microsoft-provided MTP service provider enables an application to set references in metadata.</span></span> <span data-ttu-id="6d204-130">若要執行播放清單，您的應用程式必須與 MTP 裝置進行通訊，或使用可處理抽象物件的自訂服務提供者。</span><span class="sxs-lookup"><span data-stu-id="6d204-130">To implement playlists, your application must be communicating with an MTP device or using a custom service provider that can handle abstract objects.</span></span> <span data-ttu-id="6d204-131">CE 服務提供者會處理播放清單和專輯物件。</span><span class="sxs-lookup"><span data-stu-id="6d204-131">The CE service provider handles playlist and album objects.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6d204-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="6d204-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d204-133">**將檔案寫入至裝置**</span><span class="sxs-lookup"><span data-stu-id="6d204-133">**Writing Files to the Device**</span></span>](writing-files-to-the-device.md)
</dt> </dl>

 

 




