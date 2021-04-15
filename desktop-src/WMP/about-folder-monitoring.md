---
title: 關於資料夾監控
description: 關於資料夾監控
ms.assetid: d3d83e60-ecc7-4501-a6dd-15f7680a6ec9
keywords:
- Windows Media Player，資料夾監控
- Windows Media Player 物件模型，資料夾監控
- 物件模型，資料夾監控
- Windows Media Player 的 ActiveX 控制項、資料夾監控
- ActiveX 控制項，資料夾監控
- Windows Media Player Mobile ActiveX 控制項、資料夾監控
- Windows Media Player 行動裝置、資料夾監控
- 資料夾監控
- 監視資料夾
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3d6af341df706cd85c4158197b27babad09c86
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374367"
---
# <a name="about-folder-monitoring"></a><span data-ttu-id="c447c-112">關於資料夾監控</span><span class="sxs-lookup"><span data-stu-id="c447c-112">About Folder Monitoring</span></span>

<span data-ttu-id="c447c-113">Windows Media Player 可以監視包含數位媒體檔案的資料夾，並在新增或移除檔案時更新文件庫。</span><span class="sxs-lookup"><span data-stu-id="c447c-113">Windows Media Player can monitor folders that contain digital media files and update the library when files are added or removed.</span></span> <span data-ttu-id="c447c-114">此資料夾監控功能是由 [IWMPFolderMonitorServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices) 介面提供。</span><span class="sxs-lookup"><span data-stu-id="c447c-114">This folder monitoring functionality is provided by the [IWMPFolderMonitorServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices) interface.</span></span>

<span data-ttu-id="c447c-115">若要使用資料夾監控服務，您必須以遠端狀態建立 Player 物件。</span><span class="sxs-lookup"><span data-stu-id="c447c-115">To use the folder monitoring services, you must create the Player object in a remote state.</span></span> <span data-ttu-id="c447c-116">如需遠端處理的詳細資訊，請參閱 [遠端處理 Windows Media Player 控制項](remoting-the-windows-media-player-control.md)。</span><span class="sxs-lookup"><span data-stu-id="c447c-116">For more information about remoting, see [Remoting the Windows Media Player Control](remoting-the-windows-media-player-control.md).</span></span> <span data-ttu-id="c447c-117">當您建立了播放程式的遠端實例之後，請呼叫 [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer)介面上的 **QueryInterface** 來取得 **IWMPFolderMonitorServices** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c447c-117">After you have created a remoted instance of the player, obtain a pointer to the **IWMPFolderMonitorServices** interface by calling **QueryInterface** on the [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer) interface.</span></span>

<span data-ttu-id="c447c-118">Windows Media Player 會保留受監視的資料夾清單。</span><span class="sxs-lookup"><span data-stu-id="c447c-118">Windows Media Player keeps a list of folders that are being monitored.</span></span> <span data-ttu-id="c447c-119">若要取得受監視的資料夾清單，請使用 [IWMPFolderMonitorServices：： get \_ Count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_count) 和 [IWMPFolderMonitorServices：： item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-item) 方法。</span><span class="sxs-lookup"><span data-stu-id="c447c-119">To get a list of monitored folders, use the [IWMPFolderMonitorServices::get\_count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_count) and [IWMPFolderMonitorServices::item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-item) methods.</span></span> <span data-ttu-id="c447c-120">若要將資料夾加入清單或從清單中移除它們，請分別使用 [IWMPFolderMonitorServices：： add](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-add) 和 [remove](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-remove) 方法。</span><span class="sxs-lookup"><span data-stu-id="c447c-120">To add folders to the list or remove them from the list, use the [IWMPFolderMonitorServices::add](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-add) and [remove](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-remove) methods, respectively.</span></span>

<span data-ttu-id="c447c-121">**開始掃描**</span><span class="sxs-lookup"><span data-stu-id="c447c-121">**Starting a Scan**</span></span>

<span data-ttu-id="c447c-122">資料夾的監視通常是不需要明確呼叫的背景進程。</span><span class="sxs-lookup"><span data-stu-id="c447c-122">Monitoring of folders is normally a background process that does not need to be called explicitly.</span></span> <span data-ttu-id="c447c-123">如果您想要主動掃描資料夾，請呼叫 [IWMPFolderMonitorServices：： startScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan)。</span><span class="sxs-lookup"><span data-stu-id="c447c-123">If you want to actively scan a folder, call [IWMPFolderMonitorServices::startScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan).</span></span> <span data-ttu-id="c447c-124">您可以使用 [IWMPFolderMonitorServices：： stopScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-stopscan) 方法停止進行中的掃描。</span><span class="sxs-lookup"><span data-stu-id="c447c-124">You can stop a scan in progress with the [IWMPFolderMonitorServices::stopScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-stopscan) method.</span></span>

<span data-ttu-id="c447c-125">**正在抓取資料夾監控狀態**</span><span class="sxs-lookup"><span data-stu-id="c447c-125">**Retrieving the Folder Monitoring Status**</span></span>

<span data-ttu-id="c447c-126">**IWMPFolderMonitorServices** 提供的功能可讓您取得資料夾監控程式的狀態。</span><span class="sxs-lookup"><span data-stu-id="c447c-126">**IWMPFolderMonitorServices** provides functionality for retrieving the status of the folder monitoring process.</span></span>

<span data-ttu-id="c447c-127">資料夾掃描是在兩個階段中完成。</span><span class="sxs-lookup"><span data-stu-id="c447c-127">Folder scanning is done in two passes.</span></span> <span data-ttu-id="c447c-128">在第一次通過時，播放程式會一併掃描 [受監視的資料夾] 清單中所命名的資料夾，並建立要新增至程式庫的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="c447c-128">In the first pass, the Player scans the folders named in the monitored folders list one by one and builds a list of files to be added to the library.</span></span> <span data-ttu-id="c447c-129">在第二個階段中，它會流覽檔案清單並將檔案新增至程式庫，也會從程式庫移除已從檔案系統中刪除對應實體檔案的任何媒體專案。</span><span class="sxs-lookup"><span data-stu-id="c447c-129">In the second pass, it goes through the list of files and adds the files to the library, and also removes any media items from the library whose corresponding physical files have been deleted from the file system.</span></span>

<span data-ttu-id="c447c-130">[FolderScanStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange)事件可用來在玩家切換至新狀態時通知您的程式。</span><span class="sxs-lookup"><span data-stu-id="c447c-130">The [FolderScanStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange) event is used to notify your program whenever the Player switches to a new state.</span></span> <span data-ttu-id="c447c-131">您也可以藉由呼叫 [get \_ scanState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate)來取得目前的狀態。</span><span class="sxs-lookup"><span data-stu-id="c447c-131">You can also retrieve the current state by calling [get\_scanState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate).</span></span> <span data-ttu-id="c447c-132">當第一次行程開始時，會 wmpfssScanning 目前的狀態值。</span><span class="sxs-lookup"><span data-stu-id="c447c-132">When the first pass starts, the current state value is wmpfssScanning.</span></span> <span data-ttu-id="c447c-133">在第二個階段中，狀態會切換至 wmpfssUpdating。</span><span class="sxs-lookup"><span data-stu-id="c447c-133">During the second pass, the state switches to wmpfssUpdating.</span></span> <span data-ttu-id="c447c-134">程式完成後，狀態會變更為 wmpfssStopped。</span><span class="sxs-lookup"><span data-stu-id="c447c-134">After the process is finished, the state changes to wmpfssStopped.</span></span>

<span data-ttu-id="c447c-135">當播放程式在第一次行程掃描受監視的資料夾時，請呼叫 [get \_ scannedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scannedfilescount) 來檢查已掃描的檔案數目。</span><span class="sxs-lookup"><span data-stu-id="c447c-135">While the Player is scanning the monitored folders on the first pass, call [get\_scannedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scannedfilescount) to check how many files have been scanned.</span></span> <span data-ttu-id="c447c-136">[Get \_ currentFolder](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_currentfolder)方法會告訴您目前正在掃描哪個資料夾。</span><span class="sxs-lookup"><span data-stu-id="c447c-136">The [get\_currentFolder](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_currentfolder) method will tell you which folder is currently being scanned.</span></span>

<span data-ttu-id="c447c-137">第二次傳遞之後，請呼叫 [get \_ addedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_addedfilescount) 來檢查已新增至媒體櫃的檔案數目。</span><span class="sxs-lookup"><span data-stu-id="c447c-137">After the second pass starts, call [get\_addedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_addedfilescount) to check how many files have been added to the library.</span></span> <span data-ttu-id="c447c-138">[Get \_ updateProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_updateprogress)方法會告訴您第二次行程的進度，以從0到100的百分比表示。</span><span class="sxs-lookup"><span data-stu-id="c447c-138">The [get\_updateProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_updateprogress) method will tell you the progress of the second pass, as a percentage from 0 to 100.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c447c-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="c447c-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c447c-140">**關於 Player 物件模型**</span><span class="sxs-lookup"><span data-stu-id="c447c-140">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="c447c-141">**IWMPFolderMonitorServices 介面**</span><span class="sxs-lookup"><span data-stu-id="c447c-141">**IWMPFolderMonitorServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
</dt> </dl>

 

 




