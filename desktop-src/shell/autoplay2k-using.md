---
description: 當 Shell 偵測到插入新媒體或熱插即用裝置的附件時，會決定裝置或媒體的內容。 [自動播放] （視其目前的設定而定）會執行下列其中一項動作。
title: 使用和設定自動播放
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 096c7042-8cf0-4e4f-934f-274564218f4c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 04a4f6dd09e03f26b13649e860beb7f2621ce952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689828"
---
# <a name="using-and-configuring-autoplay"></a><span data-ttu-id="991c8-104">使用和設定自動播放</span><span class="sxs-lookup"><span data-stu-id="991c8-104">Using and Configuring AutoPlay</span></span>

<span data-ttu-id="991c8-105">當 Shell 偵測到插入新媒體或熱插即用裝置的附件時，會決定裝置或媒體的內容。</span><span class="sxs-lookup"><span data-stu-id="991c8-105">When the Shell detects the insertion of new media or the attachment of a hot-plug device, the contents of the device or media are determined.</span></span> <span data-ttu-id="991c8-106">[自動播放] （視其目前的設定而定）會執行下列其中一項動作。</span><span class="sxs-lookup"><span data-stu-id="991c8-106">AutoPlay, depending on its current settings, does one of the following.</span></span>

-   <span data-ttu-id="991c8-107">自動播放內容。</span><span class="sxs-lookup"><span data-stu-id="991c8-107">Plays the content automatically.</span></span>
-   <span data-ttu-id="991c8-108">顯示對話方塊，提示使用者選擇單一內容類型的預設處理常式。</span><span class="sxs-lookup"><span data-stu-id="991c8-108">Displays a dialog box prompting the user to choose a default handler for a single content type.</span></span>
-   <span data-ttu-id="991c8-109">顯示混合內容的情況下，要啟動的可用處理程式應用程式清單。</span><span class="sxs-lookup"><span data-stu-id="991c8-109">Presents, in the case of mixed content, a list of available handler applications to launch.</span></span> <span data-ttu-id="991c8-110">然後，選擇的處理常式會自動播放其相關聯的內容類型。</span><span class="sxs-lookup"><span data-stu-id="991c8-110">The chosen handler then automatically plays its associated content type.</span></span>
-   <span data-ttu-id="991c8-111">顯示檔案的標準資料夾查看。</span><span class="sxs-lookup"><span data-stu-id="991c8-111">Displays a standard folder view of the files.</span></span>
-   <span data-ttu-id="991c8-112">如果之前使用者選擇的內容類型 **不採取任何動作** ，而且指定的 **一律執行選取的動作**，就不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="991c8-112">Does nothing if, earlier, the user had chosen **Take no action** for that content type as well as specified **Always do the selected action**.</span></span>

<span data-ttu-id="991c8-113">如果內容不符合自動播放的準則，則會將事件傳遞至 Windows 映像取得 (WIA) 。</span><span class="sxs-lookup"><span data-stu-id="991c8-113">If the contents do not meet the criteria for AutoPlay, the event is then passed to Windows Image Acquisition (WIA).</span></span>

<span data-ttu-id="991c8-114">下列主題討論自動播放的設定和使用。</span><span class="sxs-lookup"><span data-stu-id="991c8-114">The following topics discuss the setup and use of AutoPlay.</span></span>

-   [<span data-ttu-id="991c8-115">準備搭配自動播放使用的硬體和軟體</span><span class="sxs-lookup"><span data-stu-id="991c8-115">Preparing Hardware and Software for Use with AutoPlay</span></span>](#preparing-hardware-and-software-for-use-with-autoplay)
-   [<span data-ttu-id="991c8-116">自動播放如何搜尋媒體</span><span class="sxs-lookup"><span data-stu-id="991c8-116">How AutoPlay Searches Media</span></span>](#how-autoplay-searches-media)
-   [<span data-ttu-id="991c8-117">定義單一和混合內容類型</span><span class="sxs-lookup"><span data-stu-id="991c8-117">Defining Single and Mixed Content Types</span></span>](#defining-single-and-mixed-content-types)
-   [<span data-ttu-id="991c8-118">範例案例</span><span class="sxs-lookup"><span data-stu-id="991c8-118">Sample Scenarios</span></span>](#sample-scenarios)
    -   [<span data-ttu-id="991c8-119">使用圖片媒體自動播放存放裝置</span><span class="sxs-lookup"><span data-stu-id="991c8-119">AutoPlay for Storage Devices with Picture Media</span></span>](#autoplay-for-storage-devices-with-picture-media)
    -   [<span data-ttu-id="991c8-120">自動播放音樂檔案播放裝置，以及包含音樂媒體的儲存裝置</span><span class="sxs-lookup"><span data-stu-id="991c8-120">AutoPlay for Music File Playback Devices and Storage Devices Containing Music Media</span></span>](#autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media)
    -   [<span data-ttu-id="991c8-121">初次簡報時播放影片播放</span><span class="sxs-lookup"><span data-stu-id="991c8-121">AutoPlay for Video Playback on First Presentation</span></span>](#autoplay-for-video-playback-on-first-presentation)
-   [<span data-ttu-id="991c8-122">指派預設處理常式應用程式</span><span class="sxs-lookup"><span data-stu-id="991c8-122">Assigning Default Handler Applications</span></span>](#assigning-default-handler-applications)
-   [<span data-ttu-id="991c8-123">處理包含混合內容類型的媒體</span><span class="sxs-lookup"><span data-stu-id="991c8-123">Handling Media Containing Mixed Content Types</span></span>](#handling-media-containing-mixed-content-types)
-   [<span data-ttu-id="991c8-124">自動播放使用者介面</span><span class="sxs-lookup"><span data-stu-id="991c8-124">AutoPlay User Interfaces</span></span>](#autoplay-user-interfaces)
    -   [<span data-ttu-id="991c8-125">單一內容類型對話方塊</span><span class="sxs-lookup"><span data-stu-id="991c8-125">Single Content Type Dialog Box</span></span>](#single-content-type-dialog-box)
    -   [<span data-ttu-id="991c8-126">混合媒體對話方塊</span><span class="sxs-lookup"><span data-stu-id="991c8-126">Mixed Media Dialog Box</span></span>](#mixed-media-dialog-box)
    -   [<span data-ttu-id="991c8-127">屬性頁面</span><span class="sxs-lookup"><span data-stu-id="991c8-127">Property Page</span></span>](#property-page)

## <a name="preparing-hardware-and-software-for-use-with-autoplay"></a><span data-ttu-id="991c8-128">準備搭配自動播放使用的硬體和軟體</span><span class="sxs-lookup"><span data-stu-id="991c8-128">Preparing Hardware and Software for Use with AutoPlay</span></span>

<span data-ttu-id="991c8-129">有幾項資訊需要出現在登錄中，才能讓播放程式正常運作。</span><span class="sxs-lookup"><span data-stu-id="991c8-129">Several pieces of information need to appear in the registry for AutoPlay to function.</span></span> <span data-ttu-id="991c8-130">這些資訊片段會彼此互動並互相參考，以形成完整的自動播放環境。</span><span class="sxs-lookup"><span data-stu-id="991c8-130">These pieces of information interact and reference each other to form the full AutoPlay environment.</span></span> <span data-ttu-id="991c8-131">本檔將每一項資訊的設定以個別獨立程式的形式提供。</span><span class="sxs-lookup"><span data-stu-id="991c8-131">This document presents the setup of each of these pieces of information as an individual stand-alone procedure.</span></span>

<span data-ttu-id="991c8-132">如需其他指示，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="991c8-132">See the following topics for additional instructions.</span></span>

-   [<span data-ttu-id="991c8-133">如何將裝置處理常式指派給裝置</span><span class="sxs-lookup"><span data-stu-id="991c8-133">How To Assign a Device Handler to a Device</span></span>](how-to-assign-a-device-handler-to-a-device.md)
-   [<span data-ttu-id="991c8-134">如何使用裝置群組來指定裝置的圖示、標籤或裝置處理常式</span><span class="sxs-lookup"><span data-stu-id="991c8-134">How To Specify an Icon, Label, or Device Handler for a Device Using a Device Group</span></span>](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md)
-   [<span data-ttu-id="991c8-135">如何使用裝置類別指定裝置的圖示、標籤或裝置處理常式</span><span class="sxs-lookup"><span data-stu-id="991c8-135">How To Specify an Icon, Label, or Device Handler for a Device Using a Device Class</span></span>](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md)
-   [<span data-ttu-id="991c8-136">如何防止元件的自動播放</span><span class="sxs-lookup"><span data-stu-id="991c8-136">How To Prevent AutoPlay for a Component</span></span>](how-to-prevent-autoplay-for-a-component.md)
-   [<span data-ttu-id="991c8-137">如何註冊裝置事件的處理常式</span><span class="sxs-lookup"><span data-stu-id="991c8-137">How To Register a Handler for a Device Event</span></span>](how-to-register-a-handler-for-a-device-event.md)
-   [<span data-ttu-id="991c8-138">如何在執行中的應用程式中使用自動播放事件</span><span class="sxs-lookup"><span data-stu-id="991c8-138">How To Use AutoPlay Events in Running Applications</span></span>](how-to-use-autoplay-events-in-running-applications.md)
-   [<span data-ttu-id="991c8-139">如何註冊事件處理常式</span><span class="sxs-lookup"><span data-stu-id="991c8-139">How To Register an Event Handler</span></span>](how-to-register-an-event-handler.md)

## <a name="how-autoplay-searches-media"></a><span data-ttu-id="991c8-140">自動播放如何搜尋媒體</span><span class="sxs-lookup"><span data-stu-id="991c8-140">How AutoPlay Searches Media</span></span>

<span data-ttu-id="991c8-141">自動播放會搜尋根目錄下方的媒體四個目錄層級，以找出已知的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="991c8-141">AutoPlay searches for media four directory levels below the root directory to find known file types.</span></span> <span data-ttu-id="991c8-142">它會使用與登錄中的副檔名相關聯的 PerceivedType 值，來判斷檔案類別目錄，不論是影像、音訊檔案或影片檔案。</span><span class="sxs-lookup"><span data-stu-id="991c8-142">It uses the PerceivedType value associated with a file name extension in the registry to determine the file category, whether it is an image, an audio file, or a video file.</span></span> <span data-ttu-id="991c8-143">透過此資訊，自動播放會針對該裝置和檔案類型啟動適當的處理常式。</span><span class="sxs-lookup"><span data-stu-id="991c8-143">With this information, AutoPlay launches the appropriate handler for that device and file type.</span></span> <span data-ttu-id="991c8-144">如需詳細資訊，請參閱 [認知類型和應用程式註冊](fa-perceivedtypes.md)。</span><span class="sxs-lookup"><span data-stu-id="991c8-144">For more information, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

## <a name="defining-single-and-mixed-content-types"></a><span data-ttu-id="991c8-145">定義單一和混合內容類型</span><span class="sxs-lookup"><span data-stu-id="991c8-145">Defining Single and Mixed Content Types</span></span>

<span data-ttu-id="991c8-146">自動播放定義三個主要內容類別別。</span><span class="sxs-lookup"><span data-stu-id="991c8-146">AutoPlay defines three main content categories.</span></span>

-   <span data-ttu-id="991c8-147">圖片</span><span class="sxs-lookup"><span data-stu-id="991c8-147">Pictures</span></span>
-   <span data-ttu-id="991c8-148">音樂</span><span class="sxs-lookup"><span data-stu-id="991c8-148">Music</span></span>
-   <span data-ttu-id="991c8-149">影片</span><span class="sxs-lookup"><span data-stu-id="991c8-149">Video</span></span>

<span data-ttu-id="991c8-150">如果媒體上的所有檔案只屬於這三種類別的其中一種，則會將媒體視為包含單一內容類型。</span><span class="sxs-lookup"><span data-stu-id="991c8-150">A medium is considered to contain a single content type if all of the files on the medium fall into only one of these three categories.</span></span> <span data-ttu-id="991c8-151">請注意，這並不表示檔案必須是相同的 *檔* 類型，.jpg、.gif 和 .bmp 都是不同的檔案類型，但 (圖片) 一個內容類型。</span><span class="sxs-lookup"><span data-stu-id="991c8-151">Note that this does not mean that the files must be of the same *file* type; .jpg, .gif, and .bmp are different file types, but one content type (pictures).</span></span>

<span data-ttu-id="991c8-152">如果媒體上有支援的內容類型，但沒有單一內容類型可考慮總計的100%，則會將媒體視為包含混合的內容類型，並據以處理。</span><span class="sxs-lookup"><span data-stu-id="991c8-152">If supported content types are present on the medium, but no single content type can account for 100 percent of the total, then the medium is considered to contain mixed content type and is handled accordingly.</span></span> <span data-ttu-id="991c8-153">如需詳細資訊，請參閱 [處理包含混合內容類型的媒體](#handling-media-containing-mixed-content-types)。</span><span class="sxs-lookup"><span data-stu-id="991c8-153">For more information, see [Handling Media Containing Mixed Content Types](#handling-media-containing-mixed-content-types).</span></span>

## <a name="sample-scenarios"></a><span data-ttu-id="991c8-154">範例案例</span><span class="sxs-lookup"><span data-stu-id="991c8-154">Sample Scenarios</span></span>

<span data-ttu-id="991c8-155">下列案例可讓您對預期的自動播放功能有基本的瞭解。</span><span class="sxs-lookup"><span data-stu-id="991c8-155">The following scenarios provide a basic understanding of what to expect from AutoPlay.</span></span>

### <a name="autoplay-for-storage-devices-with-picture-media"></a><span data-ttu-id="991c8-156">使用圖片媒體自動播放存放裝置</span><span class="sxs-lookup"><span data-stu-id="991c8-156">AutoPlay for Storage Devices with Picture Media</span></span>

1.  <span data-ttu-id="991c8-157">使用者會將已經插入媒體的 USB SanDisk CompactFlash reader 裝置，以 .jpg 檔案的形式附加到包含 100% picture 內容類型的媒體。</span><span class="sxs-lookup"><span data-stu-id="991c8-157">The user attaches a USB SanDisk CompactFlash reader device that already has media inserted containing 100 percent picture content type in the form of .jpg files.</span></span>
2.  <span data-ttu-id="991c8-158">通知會顯示 **找到新的硬體 SanDisk ImageMate**。</span><span class="sxs-lookup"><span data-stu-id="991c8-158">Notification displays **Found New Hardware - SanDisk ImageMate**.</span></span>
3.  <span data-ttu-id="991c8-159">自動播放會啟動適當的映射應用程式。</span><span class="sxs-lookup"><span data-stu-id="991c8-159">AutoPlay launches the appropriate image application.</span></span>

<span data-ttu-id="991c8-160">同樣地，當讀取器已附加到系統時，當使用者將該相同的 CompactFlash 媒體插入讀取器時，media insert 事件也會導致自動播放啟動影像投影片放映應用程式。</span><span class="sxs-lookup"><span data-stu-id="991c8-160">Similarly, when the user inserts that same CompactFlash media into the reader when the reader is already attached to the system, the media insert event also causes AutoPlay to launch the image slide show application.</span></span> <span data-ttu-id="991c8-161">使用者可以選擇前往 SanDisk 媒體裝置的 [內容] 頁面，將預設值變更為另一個已註冊的自動播放應用程式，例如掃描器和攝影機的 [播放程式] 或圖片！。</span><span class="sxs-lookup"><span data-stu-id="991c8-161">The user has the option of going to the Properties page of the SanDisk media device to change the default to another registered AutoPlay application, such as the Scanner and Camera Wizard or Picture It!.</span></span>

### <a name="autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media"></a><span data-ttu-id="991c8-162">自動播放音樂檔案播放裝置，以及包含音樂媒體的儲存裝置</span><span class="sxs-lookup"><span data-stu-id="991c8-162">AutoPlay for Music File Playback Devices and Storage Devices Containing Music Media</span></span>

1.  <span data-ttu-id="991c8-163">使用者連接 USB 鑽石 Rio MP3 播放機。</span><span class="sxs-lookup"><span data-stu-id="991c8-163">The user attaches a USB Diamond Rio MP3 Player.</span></span>
2.  <span data-ttu-id="991c8-164">通知會顯示 **找到新的硬體鑽石 RIO MP3 播放機**。</span><span class="sxs-lookup"><span data-stu-id="991c8-164">Notification displays **Found New Hardware - Diamond Rio MP3 Player**.</span></span>
3.  <span data-ttu-id="991c8-165">自動播放會使用其註冊的預設處理常式（例如 Windows Media Player）來播放這些檔案。</span><span class="sxs-lookup"><span data-stu-id="991c8-165">AutoPlay plays the files using its registered default handler—for instance, Windows Media Player.</span></span>

<span data-ttu-id="991c8-166">同樣地，如果使用者插入包含 mp3 檔案的任何媒體 (例如，CompactFlash、SmartMedia、記憶杆或 CD-ROM) 將總支援內容的100% 儲存到儲存裝置，media insert 事件也會導致自動播放使用 Windows Media Player 播放檔案。</span><span class="sxs-lookup"><span data-stu-id="991c8-166">Similarly, if the user inserts any media containing .mp3 files (for example, CompactFlash, SmartMedia, Memory Stick, or CD-ROM) that account for 100 percent of the total supported content into a storage device, the media insert event would also cause AutoPlay to play the files using the Windows Media Player.</span></span> <span data-ttu-id="991c8-167">使用者可以存取儲存裝置的屬性工作表，並將預設動作變更為另一個已註冊的自動播放應用程式，例如說明或 Real Player。</span><span class="sxs-lookup"><span data-stu-id="991c8-167">The user can access the property sheet of the storage device and change the default action to another registered AutoPlay application, such as WinAmp or Real Player.</span></span>

### <a name="autoplay-for-video-playback-on-first-presentation"></a><span data-ttu-id="991c8-168">初次簡報時播放影片播放</span><span class="sxs-lookup"><span data-stu-id="991c8-168">AutoPlay for Video Playback on First Presentation</span></span>

1.  <span data-ttu-id="991c8-169">使用者第一次插入1394數位攝影機。</span><span class="sxs-lookup"><span data-stu-id="991c8-169">The user plugs in a 1394 digital video camera for the first time.</span></span>
2.  <span data-ttu-id="991c8-170">使用者會看到一個簡單的對話方塊，詢問要執行哪個應用程式。</span><span class="sxs-lookup"><span data-stu-id="991c8-170">The user is presented with a simple dialog box that asks what application to run.</span></span> <span data-ttu-id="991c8-171">選擇是執行其中一個已註冊的自動播放應用程式，或開啟資料夾以查看檔案。</span><span class="sxs-lookup"><span data-stu-id="991c8-171">The choices are to run one of the registered AutoPlay applications or to open a folder to view files.</span></span> <span data-ttu-id="991c8-172">使用者可以將選取的行為設定為要儲存為稍後數位攝影機熱插即用事件的預設動作。</span><span class="sxs-lookup"><span data-stu-id="991c8-172">The user may set the selected behavior to be saved as the default action for later digital video camera hot-plug events.</span></span>

## <a name="assigning-default-handler-applications"></a><span data-ttu-id="991c8-173">指派預設處理常式應用程式</span><span class="sxs-lookup"><span data-stu-id="991c8-173">Assigning Default Handler Applications</span></span>

<span data-ttu-id="991c8-174">全新安裝的 Windows 會使用一組已註冊的處理常式應用程式來尋找 [自動播放]。</span><span class="sxs-lookup"><span data-stu-id="991c8-174">A fresh installation of Windows finds AutoPlay with a set of registered handler applications.</span></span> <span data-ttu-id="991c8-175">依預設，在 Windows 安裝期間註冊的應用程式如下所示。</span><span class="sxs-lookup"><span data-stu-id="991c8-175">Applications registered by default during a Windows installation are as follows.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="991c8-176">媒體類型</span><span class="sxs-lookup"><span data-stu-id="991c8-176">Media Type</span></span></th>
<th><span data-ttu-id="991c8-177">應用程式</span><span class="sxs-lookup"><span data-stu-id="991c8-177">Applications</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="991c8-178">圖片</span><span class="sxs-lookup"><span data-stu-id="991c8-178">Pictures</span></span></td>
<td><ul>
<li><span data-ttu-id="991c8-179">投影片放映 (預設) </span><span class="sxs-lookup"><span data-stu-id="991c8-179">Slide Show (default)</span></span></li>
<li><span data-ttu-id="991c8-180">相機和掃描器的 Wizard</span><span class="sxs-lookup"><span data-stu-id="991c8-180">Camera and Scanner Wizard</span></span></li>
<li><span data-ttu-id="991c8-181">列印嚮導</span><span class="sxs-lookup"><span data-stu-id="991c8-181">Printing Wizard</span></span></li>
<li><span data-ttu-id="991c8-182">開啟資料夾</span><span class="sxs-lookup"><span data-stu-id="991c8-182">Open folder</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="991c8-183">音樂</span><span class="sxs-lookup"><span data-stu-id="991c8-183">Music</span></span></td>
<td><ul>
<li><span data-ttu-id="991c8-184">Windows Media Player (預設) </span><span class="sxs-lookup"><span data-stu-id="991c8-184">Windows Media Player (default)</span></span></li>
<li><span data-ttu-id="991c8-185">開啟資料夾</span><span class="sxs-lookup"><span data-stu-id="991c8-185">Open folder</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="991c8-186">影片</span><span class="sxs-lookup"><span data-stu-id="991c8-186">Video</span></span></td>
<td><ul>
<li><span data-ttu-id="991c8-187">Windows Media Player (預設) </span><span class="sxs-lookup"><span data-stu-id="991c8-187">Windows Media Player (default)</span></span></li>
<li><span data-ttu-id="991c8-188">開啟資料夾</span><span class="sxs-lookup"><span data-stu-id="991c8-188">Open folder</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="991c8-189">如果是不支援的類型，系統會要求使用者在第一次的系統簡介中，為與每個存放裝置相關聯的 [自動播放] 動作指派預設設定。</span><span class="sxs-lookup"><span data-stu-id="991c8-189">In the case of non-supported types, users are asked to assign the default setting for the AutoPlay action associated with each storage device on its first introduction to the system.</span></span> <span data-ttu-id="991c8-190">屆時，系統會提示使用者從提供的已註冊應用程式清單中選擇動作，或顯示列出媒體內容的資料夾檢視。</span><span class="sxs-lookup"><span data-stu-id="991c8-190">At that time, the user is prompted to choose an action from a provided list of registered applications or to display a folder view listing the media content.</span></span> <span data-ttu-id="991c8-191">使用者也可以選擇在每一次偵測到媒體類型時收到提示，而不是將任何特定的應用程式儲存為預設值。</span><span class="sxs-lookup"><span data-stu-id="991c8-191">The user also has the option of choosing to be prompted each time the media type is detected rather than saving any particular application as a default.</span></span>

> [!Note]  
> <span data-ttu-id="991c8-192">裝置製造商可以選擇註冊和指派預設應用程式，以搭配其特定產品使用。</span><span class="sxs-lookup"><span data-stu-id="991c8-192">Device manufacturers have the option of registering and assigning default applications to be used with their particular products.</span></span> <span data-ttu-id="991c8-193">在這些情況下，不會顯示為使用者提供選擇的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="991c8-193">In these cases, the dialog box offering a choice to the user is not displayed.</span></span>

 

<span data-ttu-id="991c8-194">新安裝的應用程式必須在登錄中自行註冊，才能以自動播放的形式提供給處理常式選項。</span><span class="sxs-lookup"><span data-stu-id="991c8-194">To be offered as a handler option by AutoPlay, newly installed applications must register themselves in the registry.</span></span> <span data-ttu-id="991c8-195">如需詳細資訊，請參閱 [準備搭配自動播放使用的硬體和軟體](#preparing-hardware-and-software-for-use-with-autoplay)。</span><span class="sxs-lookup"><span data-stu-id="991c8-195">For details, see [Preparing Hardware and Software for Use with AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).</span></span>

<span data-ttu-id="991c8-196">使用者一律可以變更任何儲存裝置或內容類型的預設自動播放處理常式。</span><span class="sxs-lookup"><span data-stu-id="991c8-196">Users can always change the default AutoPlay handler for any storage device or content type.</span></span> <span data-ttu-id="991c8-197">在 **我的電腦** 的儲存裝置的屬性工作表中，[自動播放] 屬性頁可供變更。</span><span class="sxs-lookup"><span data-stu-id="991c8-197">The AutoPlay property page is accessible for change in the property sheet of the storage device in **My Computer**.</span></span>

<span data-ttu-id="991c8-198">如需使用者提示和屬性頁的範例，請參閱 [自動播放使用者介面](#autoplay-user-interfaces)。</span><span class="sxs-lookup"><span data-stu-id="991c8-198">For examples of user prompts and property pages, see [AutoPlay User Interfaces](#autoplay-user-interfaces).</span></span>

## <a name="handling-media-containing-mixed-content-types"></a><span data-ttu-id="991c8-199">處理包含混合內容類型的媒體</span><span class="sxs-lookup"><span data-stu-id="991c8-199">Handling Media Containing Mixed Content Types</span></span>

<span data-ttu-id="991c8-200">當自動播放顯示混合的內容媒體時，需要使用者輸入才能執行動作。</span><span class="sxs-lookup"><span data-stu-id="991c8-200">When AutoPlay is presented with a mixed content medium, it requires user input before it can take action.</span></span> <span data-ttu-id="991c8-201">在此情況下，使用者會看到一個對話方塊，其中包含媒體上存在之內容類型可用的所有適當註冊應用程式篩選清單。</span><span class="sxs-lookup"><span data-stu-id="991c8-201">In this case, the user is presented with a dialog box containing a filtered list of all appropriate registered applications available for the content types present on the media.</span></span> <span data-ttu-id="991c8-202">使用者可以選擇其中一個應用程式來自動播放特定的內容類型，而其餘部分則保持不變。</span><span class="sxs-lookup"><span data-stu-id="991c8-202">The user can choose one of these applications to AutoPlay that particular content type, while the rest remain untouched.</span></span> <span data-ttu-id="991c8-203">由於混合內容媒體的組合因每個個別光碟而異，因此沒有任何選項可將此選項儲存為預設值。</span><span class="sxs-lookup"><span data-stu-id="991c8-203">As the composition of mixed content media varies with each individual disc, there is no option to save this choice as a default.</span></span>

<span data-ttu-id="991c8-204">如需使用者提示的範例，請參閱 [自動播放使用者介面](#autoplay-user-interfaces)。</span><span class="sxs-lookup"><span data-stu-id="991c8-204">For examples of user prompts, see [AutoPlay User Interfaces](#autoplay-user-interfaces).</span></span>

## <a name="autoplay-user-interfaces"></a><span data-ttu-id="991c8-205">自動播放使用者介面</span><span class="sxs-lookup"><span data-stu-id="991c8-205">AutoPlay User Interfaces</span></span>

<span data-ttu-id="991c8-206">有三個可能的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="991c8-206">There are three possible user interfaces.</span></span>

-   <span data-ttu-id="991c8-207">此對話方塊會提示使用者輸入單一內容類型的動作</span><span class="sxs-lookup"><span data-stu-id="991c8-207">A dialog box that prompts the user to enter an action for a single content type</span></span>
-   <span data-ttu-id="991c8-208">提示使用者輸入混合內容類型之動作的對話方塊</span><span class="sxs-lookup"><span data-stu-id="991c8-208">A dialog box that prompts the user to enter an action for mixed content types</span></span>
-   <span data-ttu-id="991c8-209">屬性頁</span><span class="sxs-lookup"><span data-stu-id="991c8-209">A property page</span></span>

### <a name="single-content-type-dialog-box"></a><span data-ttu-id="991c8-210">單一內容類型對話方塊</span><span class="sxs-lookup"><span data-stu-id="991c8-210">Single Content Type Dialog Box</span></span>

<span data-ttu-id="991c8-211">當任何尚未指派預設 [自動播放] 動作的支援媒體呈現給系統時，會顯示類似下面的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="991c8-211">A dialog box similar to the following is displayed when any supported media not yet assigned a default AutoPlay action is presented to the system.</span></span>

![[單一內容類型] 對話方塊的螢幕擷取畫面](images/pix.png)

<span data-ttu-id="991c8-213">使用者可以執行下列其中一項動作。</span><span class="sxs-lookup"><span data-stu-id="991c8-213">Users can do one of the following.</span></span>

-   <span data-ttu-id="991c8-214">從已註冊的應用程式清單中選擇動作。</span><span class="sxs-lookup"><span data-stu-id="991c8-214">Choose an action from the list of registered applications.</span></span>
-   <span data-ttu-id="991c8-215">以一般資料夾檢視列出媒體上的檔案。</span><span class="sxs-lookup"><span data-stu-id="991c8-215">List the files on the medium in a normal folder view.</span></span>
-   <span data-ttu-id="991c8-216">不採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="991c8-216">Take no action.</span></span>

<span data-ttu-id="991c8-217">使用者也可以按一下 [ **永遠執行選取的動作** ] 方塊，將選擇儲存為此媒體的預設動作。</span><span class="sxs-lookup"><span data-stu-id="991c8-217">A user can also save a choice as the default action for this medium by clicking the **Always do the selected action** box.</span></span> <span data-ttu-id="991c8-218">完成此選擇之後，對話方塊就不會再次顯示。</span><span class="sxs-lookup"><span data-stu-id="991c8-218">Once this choice is made, the dialog is not shown again.</span></span> <span data-ttu-id="991c8-219">不過，在 Windows XP Service Pack 1 (SP1) 中，如果可處理特定媒體類型的新應用程式已新增至電腦，則會再次向使用者顯示對話方塊，讓他們有機會選取新的應用程式做為預設的 [自動播放] 動作。</span><span class="sxs-lookup"><span data-stu-id="991c8-219">However, in Windows XP Service Pack 1 (SP1), if a new application that can handle a particular media type is added to the computer, the dialog is once again presented to the user, giving them the opportunity to select the new application as the default AutoPlay action.</span></span> <span data-ttu-id="991c8-220">應用程式安裝時，也可以將自己設定為預設選項。</span><span class="sxs-lookup"><span data-stu-id="991c8-220">Applications can also set themselves as the default selection when they are installed.</span></span>

<span data-ttu-id="991c8-221">Windows XP SP1 也加入了一項功能，可保留使用者選擇的 [自動播放] 動作（如果沒有按一下 [ **永遠執行選取的動作** ] 方塊）。</span><span class="sxs-lookup"><span data-stu-id="991c8-221">Windows XP SP1 also adds a feature that retains the user's choice of AutoPlay action if they do not click the **Always do the selected action** box.</span></span> <span data-ttu-id="991c8-222">如果使用者選擇單一實例的 [自動播放] 動作，則下次顯示該媒體類型的對話方塊時，相同的動作就是預設選項。</span><span class="sxs-lookup"><span data-stu-id="991c8-222">If a user chooses an AutoPlay action for a single instance, the next time that dialog is presented for that media type, the same action is the default selection.</span></span>

<span data-ttu-id="991c8-223">若要將應用程式包含在可能的動作清單中，則必須使用 [自動播放] 來註冊該應用程式。</span><span class="sxs-lookup"><span data-stu-id="991c8-223">For an application to be included in the list of possible actions, it must be registered with AutoPlay.</span></span> <span data-ttu-id="991c8-224">如需詳細資訊，請參閱 [準備搭配自動播放使用的硬體和軟體](#preparing-hardware-and-software-for-use-with-autoplay)。</span><span class="sxs-lookup"><span data-stu-id="991c8-224">For more information, see [Preparing Hardware and Software for Use with AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).</span></span>

### <a name="mixed-media-dialog-box"></a><span data-ttu-id="991c8-225">混合媒體對話方塊</span><span class="sxs-lookup"><span data-stu-id="991c8-225">Mixed Media Dialog Box</span></span>

<span data-ttu-id="991c8-226">當包含支援檔案類型混合的任何媒體呈現給系統時，會顯示下列對話方塊。</span><span class="sxs-lookup"><span data-stu-id="991c8-226">The following dialog box is displayed when any medium containing a mix of supported file types is presented to the system.</span></span> <span data-ttu-id="991c8-227">這基本上與單一 [內容媒體] 對話方塊相同，但是有兩個重要的差異。</span><span class="sxs-lookup"><span data-stu-id="991c8-227">This is essentially the same as the single content medium dialog box but with two significant differences.</span></span> <span data-ttu-id="991c8-228">首先，可用的動作選項包含與媒體上所有內容類型相關的應用程式篩選清單。</span><span class="sxs-lookup"><span data-stu-id="991c8-228">First, the available action options consist of a filtered list of applications relevant to all content types present on the medium.</span></span> <span data-ttu-id="991c8-229">其次，沒有選擇永久預設動作的選項，因為混合內容媒體的內容類型和百分比太無法預期。</span><span class="sxs-lookup"><span data-stu-id="991c8-229">Second, there is no option to choose a permanent default action because the content types and percentages of mixed content media are too unpredictable.</span></span>

![[混合媒體] 對話方塊的螢幕擷取畫面](images/mix.png)

<span data-ttu-id="991c8-231">若要將應用程式包含在可能的動作清單中，則必須使用 [自動播放] 來註冊該應用程式。</span><span class="sxs-lookup"><span data-stu-id="991c8-231">For an application to be included in the list of possible actions, it must be registered with AutoPlay.</span></span> <span data-ttu-id="991c8-232">如需詳細資訊，請參閱 [準備搭配自動播放使用的硬體和軟體](#preparing-hardware-and-software-for-use-with-autoplay)。</span><span class="sxs-lookup"><span data-stu-id="991c8-232">For more information, see [Preparing Hardware and Software for Use with AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).</span></span>

### <a name="property-page"></a><span data-ttu-id="991c8-233">屬性頁面</span><span class="sxs-lookup"><span data-stu-id="991c8-233">Property Page</span></span>

<span data-ttu-id="991c8-234">以下是 DVD/CD-ROM 裝置的 [自動播放] 屬性頁範例。</span><span class="sxs-lookup"><span data-stu-id="991c8-234">The following is a sample AutoPlay property page for a DVD/CD-ROM device.</span></span>

![屬性頁的螢幕擷取畫面](images/apdlg.png)

<span data-ttu-id="991c8-236">每種裝置類型都提供適當的內容類型子集，以供自動播放設定使用。</span><span class="sxs-lookup"><span data-stu-id="991c8-236">Each device type offers an appropriate subset of content types for AutoPlay configuration.</span></span> <span data-ttu-id="991c8-237">接著，每個內容類型在選取時，會在清單方塊中提供適當的動作選項清單。</span><span class="sxs-lookup"><span data-stu-id="991c8-237">In turn, each content type, when selected, offers an appropriate list of action options in the list box.</span></span> <span data-ttu-id="991c8-238">您可以為每個內容類型選擇不同的動作。</span><span class="sxs-lookup"><span data-stu-id="991c8-238">A different action can be chosen for each content type.</span></span>

 

 



