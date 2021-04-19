---
title: 建立 Windows Media 裝置管理員應用程式
description: 建立 Windows Media 裝置管理員應用程式
ms.assetid: 6a200bd9-19dd-4130-acb4-e038b469c334
keywords:
- Windows Media 裝置管理員，建立應用程式
- 裝置管理員，建立應用程式
- Windows Media 裝置管理員，程式設計手冊
- 裝置管理員，程式設計手冊
- 桌面應用程式程式設計指南
- Windows Media 裝置管理員程式設計指南
- 程式設計指南，外掛程式
- 程式設計指南，建立應用程式
- Windows Media 裝置管理員，桌面應用程式
- 裝置管理員，桌面應用程式
- Windows Media 裝置管理員、外掛程式
- 裝置管理員、外掛程式 insp
- 外掛程式，建立
- 外掛程式，程式設計指南
- 桌面應用程式，建立
- 建立 Windows Media 裝置管理員應用程式，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b50a2dfce057b993f84c0aca4c8f45796f67ba8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967411"
---
# <a name="creating-a-windows-media-device-manager-application"></a><span data-ttu-id="48265-119">建立 Windows Media 裝置管理員應用程式</span><span class="sxs-lookup"><span data-stu-id="48265-119">Creating a Windows Media Device Manager Application</span></span>

<span data-ttu-id="48265-120">本節說明如何在您的應用程式中使用 Windows Media 裝置管理員。</span><span class="sxs-lookup"><span data-stu-id="48265-120">This section describes how to use Windows Media Device Manager in your application.</span></span> <span data-ttu-id="48265-121">這裡的「應用程式」一詞是指可執行檔（例如，媒體播放機）或 COM 外掛程式（例如計量外掛程式）。</span><span class="sxs-lookup"><span data-stu-id="48265-121">The term "application" here means either an executable, such as a media player, or a COM plug-in, such as a metering plug-in.</span></span>

<span data-ttu-id="48265-122">Microsoft 包含數個 Windows XP 和 Windows Media Player 10 的服務提供者，包括 MTP 服務提供者、Windows CE 服務提供者 (適用于執行 Windows CE 和使用 RAPI 通訊協定的裝置，例如 Pocket PC) 和大型儲存體類別 (SERVICES.MSC) 裝置的服務提供者。</span><span class="sxs-lookup"><span data-stu-id="48265-122">Microsoft includes several service providers with Windows XP and Windows Media Player 10, including an MTP service provider, a Windows CE service provider (for devices running Windows CE and using the RAPI protocol, such as the Pocket PC), and a service provider for mass-storage category (MSC) devices.</span></span> <span data-ttu-id="48265-123">您也可以建立自己的服務提供者，以確保與您自己的裝置進行通訊;如需詳細資訊，請參閱 [建立服務提供者](creating-a-service-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="48265-123">You can also create your own service provider to ensure communication with your own device; for more information, see [Creating a Service Provider](creating-a-service-provider.md).</span></span>

<span data-ttu-id="48265-124">有一些協力廠商舊版服務提供者，可處理特定制造商的非 MTP、非 RAPI 或非 SERVICES.MSC 裝置。</span><span class="sxs-lookup"><span data-stu-id="48265-124">There are a number of third-party legacy service providers that address a particular manufacturer's non-MTP, non-RAPI, or non-MSC device.</span></span> <span data-ttu-id="48265-125">這些服務提供者包含在隨附于這些裝置的驅動程式磁片中。</span><span class="sxs-lookup"><span data-stu-id="48265-125">These service providers are included on the driver disk shipped with these devices.</span></span>

<span data-ttu-id="48265-126">使用 Windows Media 裝置管理員的應用程式必須執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="48265-126">An application that uses Windows Media Device Manager must perform the following steps.</span></span>

1.  <span data-ttu-id="48265-127">**留意與開發應用程式相關的隱私權問題。**</span><span class="sxs-lookup"><span data-stu-id="48265-127">**Become aware of privacy issues involved with developing an application.**</span></span> <span data-ttu-id="48265-128">若要瞭解有關開發 Windows Media 裝置管理員應用程式的一些隱私權問題，請參閱 [隱私權聲明](privacy-statement.md) 。</span><span class="sxs-lookup"><span data-stu-id="48265-128">See [Privacy Statement](privacy-statement.md) to learn about some privacy issues involving developing a Windows Media Device Manager application.</span></span>
2.  <span data-ttu-id="48265-129">**包含應用程式所需的程式庫和標頭檔。**</span><span class="sxs-lookup"><span data-stu-id="48265-129">**Include the required library and header files for your application.**</span></span> <span data-ttu-id="48265-130">請參閱 [應用程式所需的程式庫和標頭檔](required-library-and-header-files-for-an-application.md) ，以瞭解您需要將哪些檔案包含在專案中。</span><span class="sxs-lookup"><span data-stu-id="48265-130">See [Required Library and Header Files for an Application](required-library-and-header-files-for-an-application.md) to learn what files you will need to include in your project.</span></span>
3.  <span data-ttu-id="48265-131">**驗證應用程式並取得根 IWMDMDevice 介面。**</span><span class="sxs-lookup"><span data-stu-id="48265-131">**Authenticate the application and acquire the root IWMDMDevice interface.**</span></span> <span data-ttu-id="48265-132">應用程式必須執行才能使用 Windows Media 裝置管理員的第一項工作是自行驗證。</span><span class="sxs-lookup"><span data-stu-id="48265-132">The first task an application must do to use Windows Media Device Manager is to authenticate itself.</span></span> <span data-ttu-id="48265-133">此程式會使用適用于有限 Windows Media 裝置管理員功能的虛擬憑證，或使用正式的憑證來取得完整功能，以驗證 Windows Media 裝置管理員應用程式的身分識別。</span><span class="sxs-lookup"><span data-stu-id="48265-133">This process verifies the identity of the application to Windows Media Device Manager using a dummy certificate for limited Windows Media Device Manager functionality, or using an official certificate for full functionality.</span></span> <span data-ttu-id="48265-134">如需詳細資訊，請參閱 [驗證應用程式](authenticating-the-application.md)。</span><span class="sxs-lookup"><span data-stu-id="48265-134">For more information, see [Authenticating the Application](authenticating-the-application.md).</span></span>
4.  <span data-ttu-id="48265-135">**列舉已連線的裝置。**</span><span class="sxs-lookup"><span data-stu-id="48265-135">**Enumerate the connected devices.**</span></span> <span data-ttu-id="48265-136">與裝置通訊的第一個步驟是找出哪些裝置已連線，且可供 Windows Media 裝置管理員存取。</span><span class="sxs-lookup"><span data-stu-id="48265-136">The first step in communicating with devices is to find out what devices are connected and accessible to Windows Media Device Manager.</span></span> <span data-ttu-id="48265-137">如需詳細資訊，請參閱 [列舉裝置](enumerating-devices.md)。</span><span class="sxs-lookup"><span data-stu-id="48265-137">For more information, see [Enumerating Devices](enumerating-devices.md).</span></span>
5.  <span data-ttu-id="48265-138">**檢查裝置 DRM 元件的狀態。**</span><span class="sxs-lookup"><span data-stu-id="48265-138">**Check the status of the device's DRM components.**</span></span> <span data-ttu-id="48265-139">若要使用受 DRM 保護的檔案，裝置必須建立在可攜式裝置的某些 Windows Media DRM 版本上，而且 DRM 元件必須是最新的。</span><span class="sxs-lookup"><span data-stu-id="48265-139">To use DRM-protected files, a device must be built on some version of Windows Media DRM for Portable Devices, and the DRM components must be up to date.</span></span> <span data-ttu-id="48265-140">在您開始處理裝置上的檔案之前，最好先查看裝置是否支援受 DRM 保護的檔案，以及是否需要更新裝置。</span><span class="sxs-lookup"><span data-stu-id="48265-140">Before you begin handling files on the device, it is best to see if the device supports DRM-protected files, and whether the device needs to be updated.</span></span> <span data-ttu-id="48265-141">如需詳細資訊，請參閱 [在應用程式中處理受保護的內容](handling-protected-content-in-the-application.md)。</span><span class="sxs-lookup"><span data-stu-id="48265-141">For more information, see [Handling Protected Content in the Application](handling-protected-content-in-the-application.md).</span></span>
6.  <span data-ttu-id="48265-142">**探索裝置。**</span><span class="sxs-lookup"><span data-stu-id="48265-142">**Explore a device.**</span></span> <span data-ttu-id="48265-143">找到您想要的裝置之後，您可以流覽該裝置的內容。</span><span class="sxs-lookup"><span data-stu-id="48265-143">After you have found the device you want, you can explore the contents of that device.</span></span> <span data-ttu-id="48265-144">如需詳細資訊，請參閱 [探索裝置](exploring-a-device.md)。</span><span class="sxs-lookup"><span data-stu-id="48265-144">For more information, see [Exploring a Device](exploring-a-device.md).</span></span>
7.  <span data-ttu-id="48265-145">**從裝置讀取檔案，並將檔案寫入至裝置。**</span><span class="sxs-lookup"><span data-stu-id="48265-145">**Read files from the device, and write files to the device.**</span></span> <span data-ttu-id="48265-146">當您知道裝置的版面配置之後，就可以開始在裝置之間傳輸檔案。</span><span class="sxs-lookup"><span data-stu-id="48265-146">After you know about the layout of the device, you can begin transferring files to and from the device.</span></span> <span data-ttu-id="48265-147">如需詳細資訊，請參閱 [從裝置讀取](reading-files-from-the-device.md) 檔案，並 [將檔案寫入至裝置](writing-files-to-the-device.md)。</span><span class="sxs-lookup"><span data-stu-id="48265-147">For more information, see [Reading Files from the Device](reading-files-from-the-device.md) and [Writing Files to the Device](writing-files-to-the-device.md).</span></span>
8.  <span data-ttu-id="48265-148">**在裝置上建立播放清單。**</span><span class="sxs-lookup"><span data-stu-id="48265-148">**Create playlists on the device.**</span></span> <span data-ttu-id="48265-149">您可以寫入至裝置的一種檔案是抽象檔，也就是其他檔案的參考集合。</span><span class="sxs-lookup"><span data-stu-id="48265-149">One kind of file you can write to the device is an abstract file, which is a collection of references to other files.</span></span> <span data-ttu-id="48265-150">雖然將抽象檔寫入裝置的功能取決於服務提供者和裝置，但通常只有 MTP 裝置具有這項功能。</span><span class="sxs-lookup"><span data-stu-id="48265-150">Although the ability to write abstract files to a device depends on the service provider and the device, generally only MTP devices have this capability.</span></span> <span data-ttu-id="48265-151">如需詳細資訊，請參閱在 [裝置上建立播放清單](creating-a-playlist-on-the-device.md)。</span><span class="sxs-lookup"><span data-stu-id="48265-151">For more information, see [Creating a Playlist on the Device](creating-a-playlist-on-the-device.md).</span></span>

<span data-ttu-id="48265-152">除了這些步驟之外，您還可以在應用程式中啟用數個功能：</span><span class="sxs-lookup"><span data-stu-id="48265-152">In addition to these steps, there are several more features that you can enable in your application:</span></span>

-   <span data-ttu-id="48265-153">**通知。**</span><span class="sxs-lookup"><span data-stu-id="48265-153">**Notifications.**</span></span> <span data-ttu-id="48265-154">您可以讓應用程式在裝置與電腦連線或中斷連線時接收通知。</span><span class="sxs-lookup"><span data-stu-id="48265-154">You can enable your application to receive notifications when devices connect or disconnect from the computer.</span></span> <span data-ttu-id="48265-155">如需詳細資訊，請參閱 [啟用通知](enabling-notifications.md)。</span><span class="sxs-lookup"><span data-stu-id="48265-155">For more information, see [Enabling Notifications](enabling-notifications.md).</span></span>
-   <span data-ttu-id="48265-156">**測 井。**</span><span class="sxs-lookup"><span data-stu-id="48265-156">**Logging.**</span></span> <span data-ttu-id="48265-157">Windows Media 裝置管理員使用記錄物件，將其動作的記錄儲存至本機文字檔。</span><span class="sxs-lookup"><span data-stu-id="48265-157">Windows Media Device Manager uses a logging object that saves a record of its actions to a local text file.</span></span> <span data-ttu-id="48265-158">您可以將訊息新增至此記錄檔，以協助您分析應用程式中的錯誤或效能。</span><span class="sxs-lookup"><span data-stu-id="48265-158">You can add messages to this log to help you analyze errors or performance in your application.</span></span> <span data-ttu-id="48265-159">如需詳細資訊，請參閱 [啟用記錄](enabling-logging.md)。</span><span class="sxs-lookup"><span data-stu-id="48265-159">For more information, see [Enabling Logging](enabling-logging.md).</span></span>
-   <span data-ttu-id="48265-160">**計量內容使用方式。**</span><span class="sxs-lookup"><span data-stu-id="48265-160">**Metering content usage.**</span></span> <span data-ttu-id="48265-161">您可以針對授與此許可權的授權，取得其內容使用統計資料。</span><span class="sxs-lookup"><span data-stu-id="48265-161">You can retrieve content usage statistics for licenses that grant this right.</span></span> <span data-ttu-id="48265-162">然後可以將這些統計資料傳送到 Web 服務器，以計算內容擁有者的專利款項。</span><span class="sxs-lookup"><span data-stu-id="48265-162">These statistics can then be sent up to a Web server to calculate royalty payments to content owners.</span></span> <span data-ttu-id="48265-163">如需詳細資訊，請參閱 [計量內容使用](metering-content-usage.md)方式。</span><span class="sxs-lookup"><span data-stu-id="48265-163">For more information, see [Metering Content Usage](metering-content-usage.md).</span></span>

<span data-ttu-id="48265-164">**注意事項**</span><span class="sxs-lookup"><span data-stu-id="48265-164">**A note of caution**</span></span>

<span data-ttu-id="48265-165">您的應用程式可能需要使用各種不同的裝置，包括您未開發的某些裝置，而且從未針對您的程式碼進行測試。</span><span class="sxs-lookup"><span data-stu-id="48265-165">Your application may need to work with a variety of devices, including some that you have not developed and have never tested your code against.</span></span> <span data-ttu-id="48265-166">這些裝置可能會或可能無法精確地回應查詢和命令，或執行 MTP 或其他規格。</span><span class="sxs-lookup"><span data-stu-id="48265-166">These devices might or might not accurately respond to queries and commands, or implement MTP or other specifications.</span></span> <span data-ttu-id="48265-167">請務必包含健全的錯誤檢查和回溯功能來處理非預期的。</span><span class="sxs-lookup"><span data-stu-id="48265-167">Be sure to include robust error checking and fallback functionality to deal with the unexpected.</span></span> <span data-ttu-id="48265-168">程式依舊撰寫,。</span><span class="sxs-lookup"><span data-stu-id="48265-168">Program defensively.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48265-169">相關主題</span><span class="sxs-lookup"><span data-stu-id="48265-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48265-170">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="48265-170">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




