---
title: 下載管理員總覽
description: 下載管理員總覽
ms.assetid: a13435ac-3784-4d4c-ba49-a51e373a2874
keywords:
- Windows Media Player 線上商店，下載管理員
- 線上商店、下載管理員
- 輸入2個線上商店、下載管理員
- Windows Media Player 線上商店，即時下載
- 線上商店，即時下載
- 輸入2個線上商店，即時下載
- Windows Media Player 線上商店，背景下載
- 線上商店，背景下載
- 輸入2個線上商店，背景下載
- Windows Media Player，下載管理員
- Windows Media Player 下載管理員
- 下載管理員
- 即時下載
- 背景下載
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b709df13e239b0fbd7f5c5403998b8c996c228d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021993"
---
# <a name="download-manager-overview"></a><span data-ttu-id="87801-117">下載管理員總覽</span><span class="sxs-lookup"><span data-stu-id="87801-117">Download Manager Overview</span></span>

<span data-ttu-id="87801-118">Microsoft Windows Media Player 提供包含託管瀏覽器視窗的線上商店工作窗格。</span><span class="sxs-lookup"><span data-stu-id="87801-118">Microsoft Windows Media Player provides online store task panes that contain a hosted browser window.</span></span> <span data-ttu-id="87801-119">透過線上商店，使用者可以在網際網路上與線上商店網頁互動。</span><span class="sxs-lookup"><span data-stu-id="87801-119">Through the online stores, users can interact with online store webpages across the Internet.</span></span>

<span data-ttu-id="87801-120">Windows Media Player 下載管理員提供的物件模型，可讓您用來處理與從 Microsoft Internet Information Services (IIS) 使用超文字傳輸通訊協定 (HTTP) ，將內容下載到使用者電腦相關聯的工作。</span><span class="sxs-lookup"><span data-stu-id="87801-120">The Windows Media Player Download Manager provides an object model that you can use to handle the tasks associated with downloading content to the user's computer from Microsoft Internet Information Services (IIS) using Hypertext Transfer Protocol (HTTP).</span></span> <span data-ttu-id="87801-121">使用下載管理員，您可以：</span><span class="sxs-lookup"><span data-stu-id="87801-121">With the Download Manager, you can:</span></span>

-   <span data-ttu-id="87801-122">以集合的形式同時管理多個下載。</span><span class="sxs-lookup"><span data-stu-id="87801-122">Manage multiple downloads simultaneously as a collection.</span></span>
-   <span data-ttu-id="87801-123">指定檔案的 URL，並使用 HTTP 來開始下載。</span><span class="sxs-lookup"><span data-stu-id="87801-123">Specify a URL for a file and start it downloading using HTTP.</span></span>
-   <span data-ttu-id="87801-124">查詢下載狀態和進度。</span><span class="sxs-lookup"><span data-stu-id="87801-124">Query for the download state and progress.</span></span>
-   <span data-ttu-id="87801-125">暫停、繼續或取消下載。</span><span class="sxs-lookup"><span data-stu-id="87801-125">Pause, resume, or cancel a download.</span></span>
-   <span data-ttu-id="87801-126">指定下載是否會在背景或即時進行。</span><span class="sxs-lookup"><span data-stu-id="87801-126">Specify whether a download occurs in the background or in real time.</span></span> <span data-ttu-id="87801-127"> (背景下載僅適用于 Microsoft Windows XP 作業系統。 ) 查看 [有關背景和即時下載的資訊](#about-background-and-real-time-downloading)。</span><span class="sxs-lookup"><span data-stu-id="87801-127">(Background downloading is only available on the Microsoft Windows XP operating system.) See [About Background and Real-time Downloading](#about-background-and-real-time-downloading).</span></span>
-   <span data-ttu-id="87801-128">指定內容在文件庫中的顯示方式。</span><span class="sxs-lookup"><span data-stu-id="87801-128">Specify how content is displayed in the library.</span></span> <span data-ttu-id="87801-129">請參閱 [關於程式庫整合](#about-library-integration)。</span><span class="sxs-lookup"><span data-stu-id="87801-129">See [About Library Integration](#about-library-integration).</span></span>

<span data-ttu-id="87801-130">下載管理員是從裝載的網頁中的腳本下載內容的解決方案。</span><span class="sxs-lookup"><span data-stu-id="87801-130">The Download Manager is the solution for downloading content from script code in hosted webpages.</span></span> <span data-ttu-id="87801-131">若要使用 c + + 程式碼下載內容，請使用 Windows XP 背景智慧型傳送服務 (位) 。</span><span class="sxs-lookup"><span data-stu-id="87801-131">To download content using C++ code, use the Windows XP Background Intelligent Transfer Service (BITS).</span></span> <span data-ttu-id="87801-132">如需詳細資訊，請參閱 [BITS](bits.md)。</span><span class="sxs-lookup"><span data-stu-id="87801-132">For more information, see [BITS](bits.md).</span></span>

## <a name="about-background-and-real-time-downloading"></a><span data-ttu-id="87801-133">關於背景和即時下載</span><span class="sxs-lookup"><span data-stu-id="87801-133">About Background and Real-time Downloading</span></span>

<span data-ttu-id="87801-134">下載管理員提供兩種類型的下載：背景和即時。</span><span class="sxs-lookup"><span data-stu-id="87801-134">The Download Manager offers two types of downloading: background and real-time.</span></span> <span data-ttu-id="87801-135">您所使用的類型是由您負責，而且也可以讓使用者選取下載類型。</span><span class="sxs-lookup"><span data-stu-id="87801-135">Which type you use is up to you, and it is possible to allow the user to select the download type as well.</span></span> <span data-ttu-id="87801-136">如果您選擇允許使用者選取下載類型，請務必說明這兩種可用類型之間的差異。</span><span class="sxs-lookup"><span data-stu-id="87801-136">If you choose to allow the user to select the download type, be sure to explain the differences between the two available types.</span></span>

<span data-ttu-id="87801-137">即時下載會一次完成。</span><span class="sxs-lookup"><span data-stu-id="87801-137">Real-time downloading occurs all at once.</span></span> <span data-ttu-id="87801-138">當使用者開始下載檔案時，會以單一的連續串流將整個檔案傳送至使用者的電腦。</span><span class="sxs-lookup"><span data-stu-id="87801-138">When the user starts a file download, the entire file is transferred to the user's computer in a single, continuous stream.</span></span> <span data-ttu-id="87801-139">使用者無法暫停或以其他方式中斷下載。</span><span class="sxs-lookup"><span data-stu-id="87801-139">The user cannot pause or otherwise interrupt the download.</span></span> <span data-ttu-id="87801-140">如果使用者選擇在下載完成之前關閉 Windows Media Player，他或她會遺失任何未完成的檔案，而且必須從一開始就下載以取得內容。</span><span class="sxs-lookup"><span data-stu-id="87801-140">If the user chooses to close Windows Media Player before the download is finished, he or she loses any incomplete files and must download them from the beginning to acquire the content.</span></span>

<span data-ttu-id="87801-141">即時下載的主要優點是，它可讓使用者更快取得內容，而不是背景下載。</span><span class="sxs-lookup"><span data-stu-id="87801-141">The main advantage of real-time downloading is that it allows the user to acquire the content faster than background downloading.</span></span> <span data-ttu-id="87801-142">Windows XP 的使用者可以使用即時下載，但這是在 Windows XP 之前的 Windows 作業系統版本上唯一可用的下載類型。</span><span class="sxs-lookup"><span data-stu-id="87801-142">Real-time downloading is available to users of Windows XP, but it is the only type of downloading available on versions of the Windows operating system prior to Windows XP.</span></span>

<span data-ttu-id="87801-143">背景下載會以分次方式進行。</span><span class="sxs-lookup"><span data-stu-id="87801-143">Background downloading happens in a piecemeal fashion.</span></span> <span data-ttu-id="87801-144">當使用者啟動背景下載時，系統會在有可用的處理器時間時，將部分的檔案傳送至使用者的電腦。</span><span class="sxs-lookup"><span data-stu-id="87801-144">When the user starts a background download, parts of the file are transferred to the user's computer when processor time is available.</span></span> <span data-ttu-id="87801-145">您可以暫停並繼續背景下載。</span><span class="sxs-lookup"><span data-stu-id="87801-145">It is possible to pause and resume a background download.</span></span> <span data-ttu-id="87801-146">如果使用者選擇在背景下載完成之前關閉 Windows Media Player，則會儲存任何未完成檔案的條件，而且即使在重新開機電腦之後，下載也可以繼續在背景中繼續進行。</span><span class="sxs-lookup"><span data-stu-id="87801-146">If the user chooses to close Windows Media Player before background downloading is finished, the condition of any incomplete files is saved and the downloading can continue in the background, even after restarting the computer.</span></span>

<span data-ttu-id="87801-147">背景下載可能需要較長的時間才能下載，因為只有在處理器未執行其他工作時，才會進行下載程式。</span><span class="sxs-lookup"><span data-stu-id="87801-147">Background downloading can take longer than real-time downloading because the download process only happens when the processor is not performing other tasks.</span></span>

<span data-ttu-id="87801-148">只有在使用 Windows XP 時，才可使用背景下載。</span><span class="sxs-lookup"><span data-stu-id="87801-148">Background downloading is only available when using Windows XP.</span></span>

## <a name="about-library-integration"></a><span data-ttu-id="87801-149">關於程式庫整合</span><span class="sxs-lookup"><span data-stu-id="87801-149">About Library Integration</span></span>

<span data-ttu-id="87801-150">Windows Media Player 可以自動組織文件庫中的線上存放區內容。</span><span class="sxs-lookup"><span data-stu-id="87801-150">Windows Media Player can automatically organize online store content in the library.</span></span> <span data-ttu-id="87801-151">若要啟用這項程式，您必須為每個數位媒體檔案指定 **WM/ContentDistributor** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="87801-151">To enable this, you must specify a value for the **WM/ContentDistributor** attribute for each digital media file.</span></span> <span data-ttu-id="87801-152">當您將數位媒體檔案新增至程式庫時（當使用下載管理員時自動發生），檔案會自動列在 [已 **購買的音樂** ] 或 [已 **購買** 的影片] 節點中。</span><span class="sxs-lookup"><span data-stu-id="87801-152">When a digital media file is added to the library, which happens automatically when using the Download Manager, the file is listed in the **Purchased Music** or **Purchased Videos** node automatically.</span></span> <span data-ttu-id="87801-153">例如，如果 **WM/ContentDistributor** 的值是 "Proseware"，而數位媒體檔案包含音樂，則內容會顯示在程式庫中的下列位置：</span><span class="sxs-lookup"><span data-stu-id="87801-153">For example, if the value for **WM/ContentDistributor** is "Proseware" and the digital media file contains music, the content would appear in the library in the following location:</span></span>

<span data-ttu-id="87801-154">所有音樂/購買的音樂/Proseware</span><span class="sxs-lookup"><span data-stu-id="87801-154">All Music/Purchased Music/Proseware</span></span>

## <a name="related-topics"></a><span data-ttu-id="87801-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="87801-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87801-156">**下載管理員**</span><span class="sxs-lookup"><span data-stu-id="87801-156">**Download Manager**</span></span>](download-manager.md)
</dt> <dt>

[<span data-ttu-id="87801-157">**DownloadCollection.startDownload**</span><span class="sxs-lookup"><span data-stu-id="87801-157">**DownloadCollection.startDownload**</span></span>](downloadcollection-startdownload.md)
</dt> </dl>

 

 




