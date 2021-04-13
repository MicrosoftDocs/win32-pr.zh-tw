---
title: Windows Media Format SDK 範例應用程式
description: Windows Media Format SDK 範例應用程式
ms.assetid: 037741cb-c5fb-485f-bf62-79b5465abfe4
keywords:
- Windows Media Format SDK，範例應用程式
- 數位版權管理 (DRM) 、範例應用程式
- DRM (數位版權管理) 、範例應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ce7a9baf53c289e9420cf3c226bf21a3c6bd16
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464076"
---
# <a name="windows-media-format-sdk-sample-applications"></a><span data-ttu-id="16bea-106">Windows Media Format SDK 範例應用程式</span><span class="sxs-lookup"><span data-stu-id="16bea-106">Windows Media Format SDK Sample Applications</span></span>

<span data-ttu-id="16bea-107">此 SDK 提供的範例程式碼是 Microsoft Visual Studio 2005 的專案格式。</span><span class="sxs-lookup"><span data-stu-id="16bea-107">The sample code supplied with this SDK is in the form of projects for Microsoft Visual Studio 2005.</span></span> <span data-ttu-id="16bea-108">大部分的範例都是在 c + + 中，但 ManagedWMFSDKWrapper 和 ManagedMetadataEdit 需要 c #。</span><span class="sxs-lookup"><span data-stu-id="16bea-108">Most of the samples are in C++, but ManagedWMFSDKWrapper and ManagedMetadataEdit require C#.</span></span>

<span data-ttu-id="16bea-109">除非已安裝 Windows Media Format SDK 或 Windows Player SDK，否則這些範例將無法運作。</span><span class="sxs-lookup"><span data-stu-id="16bea-109">These samples will not work unless the Windows Media Format SDK or the Windows Player SDK has been installed.</span></span>

<span data-ttu-id="16bea-110">每個範例的使用資訊都包含在每個範例目錄的 readme.txt 檔案中。</span><span class="sxs-lookup"><span data-stu-id="16bea-110">Usage information for each sample is contained in a readme.txt file in each sample directory.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="16bea-111">範例</span><span class="sxs-lookup"><span data-stu-id="16bea-111">Samle</span></span></th>
<th><span data-ttu-id="16bea-112">Description</span><span class="sxs-lookup"><span data-stu-id="16bea-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="16bea-113">>audioplayer</span><span class="sxs-lookup"><span data-stu-id="16bea-113">AudioPlayer</span></span></td>
<td><span data-ttu-id="16bea-114">播放 Windows Media 檔案，包括受 DRM 保護的檔案。</span><span class="sxs-lookup"><span data-stu-id="16bea-114">Plays Windows Media files including DRM-protected files.</span></span> <span data-ttu-id="16bea-115">它是透過 GUI 來控制，而命令則包括播放、暫停、搜尋和停止。</span><span class="sxs-lookup"><span data-stu-id="16bea-115">It is controlled through a GUI, and commands include Play, Pause, Seek and Stop.</span></span> <span data-ttu-id="16bea-116">它可以播放從網際網路讀取的本機檔案或檔案 (包括使用 WMVNetWrite 範例) 的輸出到網際網路。</span><span class="sxs-lookup"><span data-stu-id="16bea-116">It can play local files or files read from the Internet (including those output to the Internet by using the WMVNetWrite sample).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="16bea-117">X64 版本的 Windows 不支援此範例的 DRM 部分。</span><span class="sxs-lookup"><span data-stu-id="16bea-117">The DRM portions of this sample are not supported on x64-based versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="16bea-118">DRMHeader</span><span class="sxs-lookup"><span data-stu-id="16bea-118">DRMHeader</span></span></td>
<td><span data-ttu-id="16bea-119">DRMHeader 是一種主控台應用程式，它會使用中繼資料編輯器的 <a href="/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor"><strong>IWMDRMEditor</strong></a> 介面，在不連結至 drm 靜態程式庫的情況下，讀取檔案的 drm 屬性。</span><span class="sxs-lookup"><span data-stu-id="16bea-119">DRMHeader is a console application that uses the metadata editor's <a href="/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor"><strong>IWMDRMEditor</strong></a> interface to read DRM attributes of files without linking to the DRM static library.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="16bea-120">X64 版本的 Windows 不支援這個範例。</span><span class="sxs-lookup"><span data-stu-id="16bea-120">This sample is not supported on x64-based versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="16bea-121">DRMShow</span><span class="sxs-lookup"><span data-stu-id="16bea-121">DRMShow</span></span></td>
<td><span data-ttu-id="16bea-122">DRMShow 是一個主控台應用程式，示範如何使用<strong>IWMDRMReader：： GetDRMProperty</strong>方法讀取 Windows Media 檔案的<a href="wmformat-glossary.md"><em>DRM</em></a>屬性。這個範例示範如何使用<strong>IWMDRMReader：： GetDRMProperty</strong>方法，以及可從 DRM 讀取器抓取的屬性。</span><span class="sxs-lookup"><span data-stu-id="16bea-122">DRMShow is a console application that shows how to read <a href="wmformat-glossary.md"><em>DRM</em></a> properties of a Windows Media file using the <strong>IWMDRMReader::GetDRMProperty</strong> method.This sample demonstrates the use of the <strong>IWMDRMReader::GetDRMProperty</strong> method and the properties that can be retrieved from the DRM reader.</span></span> <span data-ttu-id="16bea-123">它不會示範如何取得受 DRM 保護內容的授權。</span><span class="sxs-lookup"><span data-stu-id="16bea-123">It does not demonstrate how to acquire a license for DRM-protected content.</span></span> <span data-ttu-id="16bea-124">此範例需要 DRM 存根程式庫 WMStubDRM 來建立。</span><span class="sxs-lookup"><span data-stu-id="16bea-124">This sample requires the DRM stub library WMStubDRM.lib to build.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="16bea-125">X64 版本的 Windows 不支援這個範例。</span><span class="sxs-lookup"><span data-stu-id="16bea-125">This sample is not supported on x64-based versions of Windows.</span></span>
</blockquote>
<br/> <span data-ttu-id="16bea-126">當您從 Microsoft 取得 WMStubDRM 時，會將應用程式安全性層級指派給該程式庫。</span><span class="sxs-lookup"><span data-stu-id="16bea-126">When you acquire the WMStubDRM.lib from Microsoft, the library is assigned an application security level.</span></span> <span data-ttu-id="16bea-127">如果您收到的程式庫安全性層級不足以播放受保護的檔案，此範例將會顯示錯誤。</span><span class="sxs-lookup"><span data-stu-id="16bea-127">If the security level of the library you receive is not sufficient to play a protected file, this sample will display an error.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="16bea-128">DirectShowInterop/DSCopy</span><span class="sxs-lookup"><span data-stu-id="16bea-128">DirectShowInterop/DSCopy</span></span></td>
<td><span data-ttu-id="16bea-129">使用 DirectShow WM ASF 寫入器篩選器，將一或多個檔案轉碼至 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="16bea-129">Transcodes one or more files to an ASF file using the DirectShow  WM ASF Writer filter.</span></span> <span data-ttu-id="16bea-130">輸入檔可能是 DirectShow 支援的任何壓縮或未壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="16bea-130">The input file may be any compressed or uncompressed format supported by DirectShow.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="16bea-131">DirectShowInterop/DSPlay</span><span class="sxs-lookup"><span data-stu-id="16bea-131">DirectShowInterop/DSPlay</span></span></td>
<td><span data-ttu-id="16bea-132">此範例是互動式音訊/影片媒體檔案播放機（具有 <a href="wmformat-glossary.md"><em>DRM</em></a> 支援）。</span><span class="sxs-lookup"><span data-stu-id="16bea-132">This sample is an interactive audio/video media file player with <a href="wmformat-glossary.md"><em>DRM</em></a> support.</span></span> <span data-ttu-id="16bea-133">它會使用 DirectShow 的 WM ASF 讀取器篩選器來播放 Windows Media 檔案 (ASF、WMA、WMV) 沒有 DRM 保護，以及在100或更低層級使用 DRM 的檔案。</span><span class="sxs-lookup"><span data-stu-id="16bea-133">It uses DirectShow's WM ASF Reader filter to play Windows Media files (ASF, WMA, WMV) without DRM protection and files which use DRM at a level of 100 or below.</span></span> <span data-ttu-id="16bea-134">如需詳細資訊，請參閱範例目錄中的 readme.txt。</span><span class="sxs-lookup"><span data-stu-id="16bea-134">See readme.txt in the sample's directory for more information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="16bea-135">DirectShowInterop/DSSeekFm</span><span class="sxs-lookup"><span data-stu-id="16bea-135">DirectShowInterop/DSSeekFm</span></span></td>
<td><span data-ttu-id="16bea-136">此範例示範如何使用 DirectShow WM ASF 讀取器篩選器在 DirectShow 篩選圖形中播放 ASF 內容，以及如何使用 Windows Media 格式 SDK 中搜尋支援的畫面格。</span><span class="sxs-lookup"><span data-stu-id="16bea-136">This sample demonstrates how to use the DirectShow WM ASF Reader Filter to play ASF content in a DirectShow filter graph, and also how to use the frame seeking support in the Windows Media Format SDK.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="16bea-137">Managed/WMFSDKWrapper</span><span class="sxs-lookup"><span data-stu-id="16bea-137">Managed/WMFSDKWrapper</span></span></td>
<td><span data-ttu-id="16bea-138">此 managed 元件可作為 managed 程式碼範例所使用的包裝函式，以存取此 SDK 的一些中繼資料介面。</span><span class="sxs-lookup"><span data-stu-id="16bea-138">This managed assembly serves as a wrapper used by managed-code samples for accessing some metadata interfaces of this SDK.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="16bea-139">Managed/MetadataEdit</span><span class="sxs-lookup"><span data-stu-id="16bea-139">Managed/MetadataEdit</span></span></td>
<td><span data-ttu-id="16bea-140">您可以使用這個 c # 應用程式來查看和編輯來自 Windows Media 檔案的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="16bea-140">This C# application can be used to view and edit metadata from Windows Media files.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="16bea-141">MetaDataEdit</span><span class="sxs-lookup"><span data-stu-id="16bea-141">MetaDataEdit</span></span></td>
<td><span data-ttu-id="16bea-142">這是 Managed MetadataEdit 應用程式的 c + + 版本。</span><span class="sxs-lookup"><span data-stu-id="16bea-142">This is a C++ version of the Managed MetadataEdit application.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="16bea-143">ReadFromStream</span><span class="sxs-lookup"><span data-stu-id="16bea-143">ReadFromStream</span></span></td>
<td><span data-ttu-id="16bea-144">此主控台應用程式範例示範如何使用 WMReader 從 <strong>IStream</strong> 讀取資料。</span><span class="sxs-lookup"><span data-stu-id="16bea-144">This console application sample shows how to read data from <strong>IStream</strong> with WMReader.</span></span> <span data-ttu-id="16bea-145">已將<strong>IStream</strong>來源實作為使用 Windows Media 格式的檔案 (WMA/WMV/ASF) 。</span><span class="sxs-lookup"><span data-stu-id="16bea-145"><strong>IStream</strong> source has been implemented to use a file in Windows Media Format (WMA/WMV/ASF).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="16bea-146">此範例不會示範如何處理 WMReader 中所推出的媒體範例。</span><span class="sxs-lookup"><span data-stu-id="16bea-146">This sample does not show how to process the media samples coming out of WMReader.</span></span> <span data-ttu-id="16bea-147">如需有關如何處理音訊/影片或其他媒體範例類型的範例，請參閱 Windows Media Format SDK 隨附的其他範例，例如 >audioplayer。</span><span class="sxs-lookup"><span data-stu-id="16bea-147">For examples on how to process audio/video or other types of media samples, please refer to other samples, for instance AudioPlayer, that are included with the Windows Media Format SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="16bea-148">UncompAVIToWMV</span><span class="sxs-lookup"><span data-stu-id="16bea-148">UncompAVIToWMV</span></span></td>
<td><span data-ttu-id="16bea-149">此主控台應用程式範例會顯示將 AVI 檔案壓縮成 WMV 檔案的必要程式碼。</span><span class="sxs-lookup"><span data-stu-id="16bea-149">This console application sample shows the necessary code to compress an AVI file to a WMV file.</span></span> <span data-ttu-id="16bea-150">它會示範如何合併數個 AVI 檔案中的音訊和影片串流範例，並將其合併成類似的資料流程，或根據來來源資料流設定檔建立新的資料流程。</span><span class="sxs-lookup"><span data-stu-id="16bea-150">It shows how to merge samples for audio and video streams from several AVI files and either merge these into similar streams or create a new stream based on the source stream profile.</span></span> <span data-ttu-id="16bea-151">它也會示範如何建立任意資料流程、進行 multipass 編碼、新增 SMPTE 時間代碼，以及套用 DRM 第1版保護。</span><span class="sxs-lookup"><span data-stu-id="16bea-151">It also shows how to create an arbitrary stream, do multipass encoding, add SMPTE time code, and apply DRM version 1 protection.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="16bea-152">WMGenProfile/exe</span><span class="sxs-lookup"><span data-stu-id="16bea-152">WMGenProfile/exe</span></span></td>
<td><span data-ttu-id="16bea-153">此範例已從7.1 版本更新。</span><span class="sxs-lookup"><span data-stu-id="16bea-153">This sample has been updated from the 7.1 release.</span></span> <span data-ttu-id="16bea-154">它現在是 MFC 對話應用程式。</span><span class="sxs-lookup"><span data-stu-id="16bea-154">It is now an MFC Dialog application.</span></span> <span data-ttu-id="16bea-155">WMGenProfile 範例示範如何使用 WMGenProfile 靜態程式庫。</span><span class="sxs-lookup"><span data-stu-id="16bea-155">WMGenProfile sample demonstrates the use of the WMGenProfile static library.</span></span> <span data-ttu-id="16bea-156">它也可做為建立設定檔的工具。</span><span class="sxs-lookup"><span data-stu-id="16bea-156">It also serves as a tool for the creation of profiles.</span></span> <span data-ttu-id="16bea-157">這項工具適用于熟悉 Windows Media 格式的開發人員。</span><span class="sxs-lookup"><span data-stu-id="16bea-157">This tool is meant for developers familiar with the Windows Media Format.</span></span> <span data-ttu-id="16bea-158">UI 尚未經過測試以取得使用者經驗，也不是將此資訊提供給使用者的建議。</span><span class="sxs-lookup"><span data-stu-id="16bea-158">The UI has not been tested for user experience and is not meant as a recommendation about how to present this information to a user.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="16bea-159">WMGenProfile/lib</span><span class="sxs-lookup"><span data-stu-id="16bea-159">WMGenProfile/lib</span></span></td>
<td><span data-ttu-id="16bea-160">GenProfile 程式庫範例會示範如何建立設定檔。</span><span class="sxs-lookup"><span data-stu-id="16bea-160">The GenProfile library sample demonstrates the creation of profiles.</span></span> <span data-ttu-id="16bea-161">它會示範如何建立各種串流類型的媒體類型和資料流程 (音訊、影片、腳本、影像、檔案傳輸和 Web) 。</span><span class="sxs-lookup"><span data-stu-id="16bea-161">It shows how to create media types and streams for various stream types (audio, video, script, image, file transfer, and Web).</span></span> <span data-ttu-id="16bea-162">它不會示範如何使用系統設定檔，或是如何將系統設定檔轉換成指定 Windows Media 音訊和 Video 9 系列編解碼器的設定檔。</span><span class="sxs-lookup"><span data-stu-id="16bea-162">It does not demonstrate how to work with system profiles or how to convert system profiles to profiles that specify the Windows Media Audio and Video 9 Series codecs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="16bea-163">WMProp</span><span class="sxs-lookup"><span data-stu-id="16bea-163">WMProp</span></span></td>
<td><span data-ttu-id="16bea-164">此主控台應用程式示範如何使用「中繼資料編輯器」物件和「讀取器」中的設定檔資訊來取出屬性。</span><span class="sxs-lookup"><span data-stu-id="16bea-164">This console application demonstrates how to retrieve attributes by using the metadata editor object and profile information from the reader.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="16bea-165">WMStats</span><span class="sxs-lookup"><span data-stu-id="16bea-165">WMStats</span></span></td>
<td><span data-ttu-id="16bea-166">此主控台應用程式會顯示讀取器和寫入器統計資料。</span><span class="sxs-lookup"><span data-stu-id="16bea-166">This console application displays Reader and Writer statistics.</span></span> <span data-ttu-id="16bea-167">您也可以在一部電腦上同時使用多個 WMStats 實例。</span><span class="sxs-lookup"><span data-stu-id="16bea-167">Multiple instances of WMStats can also be used concurrently on one machine.</span></span> <span data-ttu-id="16bea-168">以伺服器的形式啟動一個實例，以將資料流程傳送至網路，然後以用戶端的形式執行第二個實例，以確認伺服器已正確串流處理。</span><span class="sxs-lookup"><span data-stu-id="16bea-168">Start one instance as a server to send the stream to the network and then run a second instance as a client to verify that server is streaming correctly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="16bea-169">WMSyncReader</span><span class="sxs-lookup"><span data-stu-id="16bea-169">WMSyncReader</span></span></td>
<td><span data-ttu-id="16bea-170">此主控台應用程式範例示範如何使用 <strong>IWMSyncReader</strong> 讀取媒體檔案，而不需要建立任何額外的執行緒或使用回呼。</span><span class="sxs-lookup"><span data-stu-id="16bea-170">This console application sample shows how to read a media file using <strong>IWMSyncReader</strong> without creating any extra thread or using callbacks.</span></span> <span data-ttu-id="16bea-171">會執行下列功能：讀取已壓縮或解壓縮的範例</span><span class="sxs-lookup"><span data-stu-id="16bea-171">The following features are implemented :Reading compressed or decompressed samples</span></span><br/> <span data-ttu-id="16bea-172">以時間為基礎的搜尋</span><span class="sxs-lookup"><span data-stu-id="16bea-172">Time-based seeking</span></span><br/> <span data-ttu-id="16bea-173">以框架為基礎的搜尋</span><span class="sxs-lookup"><span data-stu-id="16bea-173">Frame-based seeking</span></span><br/> <span data-ttu-id="16bea-174"><strong>IStream</strong> 衍生來源</span><span class="sxs-lookup"><span data-stu-id="16bea-174"><strong>IStream</strong> derived source</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="16bea-175">WMVAppend</span><span class="sxs-lookup"><span data-stu-id="16bea-175">WMVAppend</span></span></td>
<td><span data-ttu-id="16bea-176">此主控台應用程式會使用兩個 Windows Media 檔案進行輸入，並嘗試建立輸出檔案，其中包含第一個的內容，後面接著第二個。</span><span class="sxs-lookup"><span data-stu-id="16bea-176">This console application takes two Windows Media files for input, and attempts to create an output file with the contents of the first followed by the second.</span></span> <span data-ttu-id="16bea-177">此範例會比較兩個輸入檔的設定檔，以確保它們的相似之處。</span><span class="sxs-lookup"><span data-stu-id="16bea-177">The sample compares the profiles of the two input files to ensure they are similar enough to be appended.</span></span> <span data-ttu-id="16bea-178">如果不是這種情況，就會出現錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="16bea-178">If this is not the case, an error message appears.</span></span> <span data-ttu-id="16bea-179">例如，當一個檔案僅為音訊，第二個是音訊影片檔案，或兩個音訊檔案有不同的位速率時，就會出現錯誤訊息。此範例會 (VBR) 來源接受可變的位元速率。</span><span class="sxs-lookup"><span data-stu-id="16bea-179">For example, an error message occurs when one file is audio only and the second is an audio-video file, or when two audio files have different bit rates.The sample accepts variable bit rate (VBR) sources.</span></span> <span data-ttu-id="16bea-180">不過，在比較兩個 VBR 來源的設定檔時，此範例會忽略平均位元速率差異，因為兩個 VBR 資料流程會有不同的平均位速率，即使它們是使用相同的設定檔建立的。</span><span class="sxs-lookup"><span data-stu-id="16bea-180">However, when comparing the profiles of the two VBR sources, the sample ignores the average bit rate difference because two VBR streams will have different average bit rates even if they were created using the same profile.</span></span> <span data-ttu-id="16bea-181">WMVAppend 無法比較未受限制之以位速率為基礎的 VBR 資料流程或品質層級的 VBR 資料流程的尖峰位速率，因為這項資訊不存在於原始程式檔中。</span><span class="sxs-lookup"><span data-stu-id="16bea-181">WMVAppend cannot compare the peak bit rate of unconstrained bit-rate-based VBR streams, or the quality level of quality-based VBR streams, because this information does not exist in the source files.</span></span> <span data-ttu-id="16bea-182">因此，使用者必須負責確定兩個來源檔案是使用相同的設定檔所建立。</span><span class="sxs-lookup"><span data-stu-id="16bea-182">It is therefore the user's responsibility to make sure that two source files are created using the same profile.</span></span> <span data-ttu-id="16bea-183">否則，就可以建立不正確內容。</span><span class="sxs-lookup"><span data-stu-id="16bea-183">Otherwise, invalid content can be created.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="16bea-184">WMVCopy</span><span class="sxs-lookup"><span data-stu-id="16bea-184">WMVCopy</span></span></td>
<td><span data-ttu-id="16bea-185">此範例顯示覆制 WMV 檔案所需的程式碼。</span><span class="sxs-lookup"><span data-stu-id="16bea-185">This sample shows the code necessary to copy a WMV file.</span></span> <span data-ttu-id="16bea-186">它會顯示如何讀取和寫入壓縮的範例、讀取標頭屬性和腳本，以及修改標頭屬性。</span><span class="sxs-lookup"><span data-stu-id="16bea-186">It shows how to read and write compressed samples, read header attributes and scripts, and modify header attributes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="16bea-187">WMVNetWrite</span><span class="sxs-lookup"><span data-stu-id="16bea-187">WMVNetWrite</span></span></td>
<td><span data-ttu-id="16bea-188">此主控台應用程式顯示如何在網際網路上串流處理 Windows Media 檔案。</span><span class="sxs-lookup"><span data-stu-id="16bea-188">This console application shows how a Windows Media file is streamed across the Internet.</span></span> <span data-ttu-id="16bea-189">此範例需要指定埠，然後才能使用播放檔播放該檔案。</span><span class="sxs-lookup"><span data-stu-id="16bea-189">The sample requires a port to be specified, and then the file can be played using a player.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="16bea-190">WMVRecompress</span><span class="sxs-lookup"><span data-stu-id="16bea-190">WMVRecompress</span></span></td>
<td><span data-ttu-id="16bea-191">此主控台應用程式顯示如何重新壓縮 WMV 檔案。</span><span class="sxs-lookup"><span data-stu-id="16bea-191">This console application shows how to recompress a WMV file.</span></span> <span data-ttu-id="16bea-192">它會示範如何讀取未壓縮的範例、撰寫未壓縮的範例，以及進行多重傳遞編碼、多重通道輸出和智慧型 recompression。</span><span class="sxs-lookup"><span data-stu-id="16bea-192">It demonstrates reading uncompressed samples, writing uncompressed samples, and doing multi-pass encoding, multi-channel output, and smart recompression.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="16bea-193">相關主題</span><span class="sxs-lookup"><span data-stu-id="16bea-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16bea-194">**關於 Windows Media Format SDK**</span><span class="sxs-lookup"><span data-stu-id="16bea-194">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> <dt>

[<span data-ttu-id="16bea-195">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="16bea-195">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 





