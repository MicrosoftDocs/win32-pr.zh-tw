---
title: 將檔案寫入至裝置
description: 將檔案寫入至裝置
ms.assetid: 66eaed16-032b-4ac0-a768-aded80f10255
keywords:
- Windows Media 裝置管理員，將檔案寫入裝置
- 裝置管理員，將檔案寫入裝置
- 程式設計指南，將檔案寫入裝置
- 桌面應用程式，將檔案寫入裝置
- 建立 Windows Media 裝置管理員應用程式，將檔案寫入裝置
- 將檔案寫入裝置，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62d8b5234cc275eed1b4aa344c16a2b927b8122d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507057"
---
# <a name="writing-files-to-the-device"></a><span data-ttu-id="f20db-109">將檔案寫入至裝置</span><span class="sxs-lookup"><span data-stu-id="f20db-109">Writing Files to the Device</span></span>

<span data-ttu-id="f20db-110">將檔案傳送至裝置之前，您的應用程式必須找出裝置可以處理的檔和格式類型，讓應用程式可以在傳送或傳送未修改或未傳送的情況下，判斷是否應該轉碼檔案。</span><span class="sxs-lookup"><span data-stu-id="f20db-110">Before sending a file to a device, your application must find out what types of files and formats the device can handle, so that the application can determine whether the file should be transcoded before sending, or sent unmodified, or not sent at all.</span></span>

<span data-ttu-id="f20db-111">下列步驟說明如何將現有的檔案傳送至裝置。</span><span class="sxs-lookup"><span data-stu-id="f20db-111">The following steps show how to send an existing file down to the device.</span></span> <span data-ttu-id="f20db-112">若要在裝置上建立新檔案（例如播放清單），請參閱在 [裝置上建立播放清單](creating-a-playlist-on-the-device.md)。</span><span class="sxs-lookup"><span data-stu-id="f20db-112">To create a new file on the device, such as a playlist, see [Creating a Playlist on the Device](creating-a-playlist-on-the-device.md).</span></span>

1.  <span data-ttu-id="f20db-113">取得您想要傳送至裝置的檔案名格式。</span><span class="sxs-lookup"><span data-stu-id="f20db-113">Get the format of the file you intend to send to the device.</span></span> <span data-ttu-id="f20db-114">如需詳細資訊，請參閱 [探索檔案的格式](discovering-a-files-format.md)。</span><span class="sxs-lookup"><span data-stu-id="f20db-114">For more information, see [Discovering a File's Format](discovering-a-files-format.md).</span></span>
2.  <span data-ttu-id="f20db-115">如果裝置打算播放檔案，</span><span class="sxs-lookup"><span data-stu-id="f20db-115">If the device is intended to play the file,</span></span>
    -   <span data-ttu-id="f20db-116">查詢檔案的格式功能。</span><span class="sxs-lookup"><span data-stu-id="f20db-116">Query the file for its format capabilities.</span></span> <span data-ttu-id="f20db-117">如需詳細資訊，請參閱 [探索裝置格式功能](discovering-device-format-capabilities.md)。</span><span class="sxs-lookup"><span data-stu-id="f20db-117">For more information, see [Discovering Device Format Capabilities](discovering-device-format-capabilities.md).</span></span>
    -   <span data-ttu-id="f20db-118">尋找應用程式可從原始檔案建立的可接受格式。</span><span class="sxs-lookup"><span data-stu-id="f20db-118">Find an acceptable format that the application can create from the original file.</span></span>
    -   <span data-ttu-id="f20db-119">如果需要轉碼檔案，請轉碼該檔案。</span><span class="sxs-lookup"><span data-stu-id="f20db-119">If the file needs to be transcoded, transcode it.</span></span>
3.  <span data-ttu-id="f20db-120">尋找新物件的父儲存體。</span><span class="sxs-lookup"><span data-stu-id="f20db-120">Find a parent storage for the new object.</span></span> <span data-ttu-id="f20db-121">Windows Media 裝置管理員不會提供一種方式來探索任何特定檔案類型的標準儲存位置 (影片或音訊檔案、WMV 或 BMP、「我的最愛」資料夾等) ，所以您必須檢查每個裝置，以嘗試找出最適合儲存新物件的位置。</span><span class="sxs-lookup"><span data-stu-id="f20db-121">Windows Media Device Manager does not provide a way to discover the standard storage location for any particular file types (video or audio files, WMV or BMP, a "Favorites" folder, and so on), so you will have to examine each device to try to figure out where best to store the new object.</span></span> <span data-ttu-id="f20db-122"> (其他應用程式會強制執行特定的資料夾結構，例如，Windows Media Player 會建立專輯、播放清單和音樂資料夾，其中的 [音樂] 資料夾包含演出者和 AlbumName 階層。</span><span class="sxs-lookup"><span data-stu-id="f20db-122">(Other applications enforce a certain folder structure, for example, Windows Media Player creates Albums, Playlists and Music folders where the Music folder contains an Artist and AlbumName heirarchy.</span></span> <span data-ttu-id="f20db-123">基於這個理由，而且因為某些裝置可能尚未使用 Windows Media Player 以外的軟體進行測試，請注意，在 [播放清單] 或 [專輯] 資料夾以外的任何資料夾中，播放清單或專輯物件的位置，有時可能會導致某些裝置上的 nonfunctioning 物件。 ) </span><span class="sxs-lookup"><span data-stu-id="f20db-123">For this reason, and because some devices may not have been tested with software other than Windows Media Player, be aware that the placement of playlist or album objects in any folder other than the Playlists or Albums folders may sometimes lead to nonfunctioning objects on some devices.)</span></span>
4.  <span data-ttu-id="f20db-124">如果目標儲存體支援 [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3)，請呼叫 [**IWMDMStorage3：： CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject)來建立新的中繼資料介面。</span><span class="sxs-lookup"><span data-stu-id="f20db-124">If the target storage supports [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3), create a new metadata interface by calling [**IWMDMStorage3::CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject).</span></span> <span data-ttu-id="f20db-125">在 [**IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata) 介面上設定中繼資料。</span><span class="sxs-lookup"><span data-stu-id="f20db-125">Set metadata on an [**IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata) interface.</span></span> <span data-ttu-id="f20db-126">如需詳細資訊，請參閱 [在檔案上設定中繼資料](setting-metadata-on-a-file.md)。</span><span class="sxs-lookup"><span data-stu-id="f20db-126">For more information, see [Setting Metadata on a File](setting-metadata-on-a-file.md).</span></span> <span data-ttu-id="f20db-127">唯一必要的中繼資料是 g \_ wszWMDMFormatCode ([**WMDM \_ FORMATCODE**](wmdm-formatcode.md) 值，其描述內容) ，但您可以提供的中繼資料越多，服務提供者的傳送效率就愈高。</span><span class="sxs-lookup"><span data-stu-id="f20db-127">The only required metadata is g\_wszWMDMFormatCode (a [**WMDM\_FORMATCODE**](wmdm-formatcode.md) value describing the content), but the more metadata you can provide, the more efficient the transfer will be for the service provider.</span></span>
5.  <span data-ttu-id="f20db-128">使用 [**Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert)、 [**Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)或 [**Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) 方法，將檔案傳送至裝置。</span><span class="sxs-lookup"><span data-stu-id="f20db-128">Send the file to the device by using the [**Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert), [**Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2), or [**Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) method.</span></span> <span data-ttu-id="f20db-129">**Insert3** 可讓您在裝置上包含中繼資料作為方法的一部分。</span><span class="sxs-lookup"><span data-stu-id="f20db-129">**Insert3** allows you to include the metadata on the device as part of the method.</span></span> <span data-ttu-id="f20db-130">如需詳細資訊，請參閱將檔案傳送 [至裝置](sending-the-file-to-the-device.md)。</span><span class="sxs-lookup"><span data-stu-id="f20db-130">For more information, see [Sending the File to the Device](sending-the-file-to-the-device.md).</span></span>

<span data-ttu-id="f20db-131">示範每個步驟的程式碼都是在連結的主題頁面上提供。</span><span class="sxs-lookup"><span data-stu-id="f20db-131">Code demonstrating each of these steps is provided on the linked topic pages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f20db-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="f20db-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f20db-133">**建立 Windows Media 裝置管理員應用程式**</span><span class="sxs-lookup"><span data-stu-id="f20db-133">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




