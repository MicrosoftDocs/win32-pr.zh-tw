---
title: 副檔名登錄設定
description: 副檔名登錄設定
ms.assetid: a5c31cf7-e1e1-4f1a-8e94-ed08f99ad973
keywords:
- Windows Media Player，登錄
- Windows Media Player、副檔名
- 登錄、副檔名
- 登錄，Windows Media Player 的設定
- 副檔名登錄設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c526e38ae1b2b76b942e0646df6f8aaa3b8e3417
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674835"
---
# <a name="file-name-extension-registry-settings"></a><span data-ttu-id="29f65-108">副檔名登錄設定</span><span class="sxs-lookup"><span data-stu-id="29f65-108">File Name Extension Registry Settings</span></span>

<span data-ttu-id="29f65-109">如果您的數位媒體檔案有自訂格式，您可以在使用者電腦的登錄中放入專案，以提供有關自訂格式的資訊 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="29f65-109">If your digital media files have a custom format, you can provide Windows Media Player with information about your custom format by placing entries in the registry on the user's computer.</span></span> <span data-ttu-id="29f65-110">Windows Media Player 會檢查您的登錄專案，以判斷它應該如何處理您的檔案。</span><span class="sxs-lookup"><span data-stu-id="29f65-110">Windows Media Player inspects your registry entries to determine how it should handle your files.</span></span> <span data-ttu-id="29f65-111">下列清單顯示您可以藉由建立與自訂媒體檔案格式相關的登錄專案來執行的一些動作。</span><span class="sxs-lookup"><span data-stu-id="29f65-111">The following list shows several of the things you can do by creating registry entries that pertain to your custom media file format.</span></span>

-   <span data-ttu-id="29f65-112">授與播放機播放、複製或轉碼檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="29f65-112">Grant permission for the Player to play, copy, or transcode your files.</span></span>
-   <span data-ttu-id="29f65-113">指定播放機用來播放檔案的基礎技術。</span><span class="sxs-lookup"><span data-stu-id="29f65-113">Specify the underlying technology that the Player should use to play your files.</span></span>
-   <span data-ttu-id="29f65-114">指定播放程式在文件庫視圖中顯示檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="29f65-114">Specify where the Player should display your files in its library view.</span></span>
-   <span data-ttu-id="29f65-115">指定播放機應用來將您的檔案轉換成標準格式的外掛程式。</span><span class="sxs-lookup"><span data-stu-id="29f65-115">Specify a plug-in that the Player should use to convert your files to a standard format.</span></span>
-   <span data-ttu-id="29f65-116">指定媒體傳輸通訊協定 (MTP) 格式的程式碼，讓播放程式可以用來判斷特定的可攜式裝置是否支援您的檔案格式。</span><span class="sxs-lookup"><span data-stu-id="29f65-116">Specify a Media Transport Protocol (MTP) format code that the Player can use to determine whether a particular portable device supports your file format.</span></span>

<span data-ttu-id="29f65-117">您提供的大部分專案都會在與自訂副檔名相關聯的子機碼下。</span><span class="sxs-lookup"><span data-stu-id="29f65-117">Most of the entries that you provide will be under a subkey that is associated with your custom file name extension.</span></span> <span data-ttu-id="29f65-118">您可以在 HKEY \_ 本機 \_ 電腦子樹和 [HKEY \_ 目前 \_ 使用者] 子樹中建立該子機碼。</span><span class="sxs-lookup"><span data-stu-id="29f65-118">You can create that subkey in the HKEY\_LOCAL\_MACHINE subtree and in the HKEY\_CURRENT\_USER subtree.</span></span> <span data-ttu-id="29f65-119">Windows Media Player 會先在 HKEY \_ 本機 \_ 電腦子樹中尋找。</span><span class="sxs-lookup"><span data-stu-id="29f65-119">Windows Media Player looks first in the HKEY\_LOCAL\_MACHINE subtree.</span></span> <span data-ttu-id="29f65-120">如果它在該處找不到它所需的內容，則會在 [HKEY \_ 目前 \_ 使用者] 子樹中尋找。</span><span class="sxs-lookup"><span data-stu-id="29f65-120">If it doesn't find what it needs there, it looks in the HKEY\_CURRENT\_USER subtree.</span></span> <span data-ttu-id="29f65-121">請注意，嘗試寫入使用者電腦上登錄的任何程式碼， \_ \_ 只有在目前的使用者具有系統管理許可權時，才可以寫入至 HKEY 本機電腦子樹。</span><span class="sxs-lookup"><span data-stu-id="29f65-121">Note that any code that attempts to write to the registry on the user's computer can write to the HKEY\_LOCAL\_MACHINE subtree only if the current user has administrative privileges.</span></span>

<span data-ttu-id="29f65-122">若要將自訂檔案格式的相關資訊寫入 HKEY \_ 本機 \_ 電腦子樹，請建立下列子機碼。</span><span class="sxs-lookup"><span data-stu-id="29f65-122">To write information about your custom file format to the HKEY\_LOCAL\_MACHINE subtree, create the following subkey.</span></span>

<span data-ttu-id="29f65-123">**HKEY \_本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ 多媒體 \\ WMPlayer \\ 延伸 \\** 模組 *customExtension*</span><span class="sxs-lookup"><span data-stu-id="29f65-123">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Extensions\\** *customExtension*</span></span>

<span data-ttu-id="29f65-124">其中 *customExtension* 是副檔名，包括點 (. ) 分隔符號。</span><span class="sxs-lookup"><span data-stu-id="29f65-124">where *customExtension* is the file name extension including the dot (.) separator.</span></span> <span data-ttu-id="29f65-125">例如，如果您自訂檔案格式的副檔名是 .xyz，請建立下列子機碼。</span><span class="sxs-lookup"><span data-stu-id="29f65-125">For example, if the extension for your custom file format is .xyz, create the following subkey.</span></span>

<span data-ttu-id="29f65-126">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ 多媒體 \\ WMPlayer \\ 擴充功能 \\ 。 xyz**</span><span class="sxs-lookup"><span data-stu-id="29f65-126">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Extensions\\.xyz**</span></span>

<span data-ttu-id="29f65-127">若要將自訂檔案格式的相關資訊寫入 HKEY \_ CURRENT \_ USER 子樹，請建立下列子機碼。</span><span class="sxs-lookup"><span data-stu-id="29f65-127">To write information about your custom file format to the HKEY\_CURRENT\_USER subtree, create the following subkey.</span></span>

<span data-ttu-id="29f65-128">**HKEY \_目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ MediaPlayer \\ Player \\ Extensions \\** *customExtension*</span><span class="sxs-lookup"><span data-stu-id="29f65-128">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Player\\Extensions\\** *customExtension*</span></span>

<span data-ttu-id="29f65-129">您可以在 *customExtension* 子機碼中寫入下列一或多個專案。</span><span class="sxs-lookup"><span data-stu-id="29f65-129">You can write one or more of the following entries in your *customExtension* subkey.</span></span>

-   <span data-ttu-id="29f65-130">**權限**</span><span class="sxs-lookup"><span data-stu-id="29f65-130">**Permissions**</span></span>
-   <span data-ttu-id="29f65-131">**執行階段**</span><span class="sxs-lookup"><span data-stu-id="29f65-131">**Runtime**</span></span>
-   <span data-ttu-id="29f65-132">**FormatCode**</span><span class="sxs-lookup"><span data-stu-id="29f65-132">**FormatCode**</span></span>

<span data-ttu-id="29f65-133">若要指定您自訂媒體檔案格式的轉換外掛程式，請在 *customExtension* 子機碼中建立 **ConvertPluginCLSID** 子機碼。</span><span class="sxs-lookup"><span data-stu-id="29f65-133">To specify conversion plug-ins for your custom media file format, create a **ConvertPluginCLSID** subkey in your *customExtension* subkey.</span></span>

<span data-ttu-id="29f65-134">若要指定 Windows Media Player 應該在其程式庫視圖中顯示檔案的位置，請在下列子機碼中寫入代表您自訂檔案格式的專案。</span><span class="sxs-lookup"><span data-stu-id="29f65-134">To specify where Windows Media Player should display your files in its library view, write an entry that represents your custom file format in the following subkey.</span></span>

<span data-ttu-id="29f65-135">**HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ MediaPlayer \\ MLS \\ Extensions**</span><span class="sxs-lookup"><span data-stu-id="29f65-135">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\MediaPlayer\\MLS\\Extensions**</span></span>

<span data-ttu-id="29f65-136">下列主題描述的登錄子機碼和專案可提供 Windows Media Player 有關自訂媒體檔案格式的資訊。</span><span class="sxs-lookup"><span data-stu-id="29f65-136">The following topics describe the registry subkeys and entries that provide Windows Media Player with information about custom media file formats.</span></span>

-   [<span data-ttu-id="29f65-137">許可權登錄專案</span><span class="sxs-lookup"><span data-stu-id="29f65-137">Permissions Registry Entry</span></span>](permissions-registry-entry.md)
-   [<span data-ttu-id="29f65-138">執行時間登錄專案</span><span class="sxs-lookup"><span data-stu-id="29f65-138">Runtime Registry Entry</span></span>](runtime-registry-entry.md)
-   [<span data-ttu-id="29f65-139">FormatCode 登錄專案</span><span class="sxs-lookup"><span data-stu-id="29f65-139">FormatCode Registry Entry</span></span>](formatcode-registry-entry.md)
-   [<span data-ttu-id="29f65-140">程式庫分類登錄專案</span><span class="sxs-lookup"><span data-stu-id="29f65-140">Library Classification Registry Entries</span></span>](library-classification-registry-entries.md)
-   [<span data-ttu-id="29f65-141">ConvertPluginCLSID 子機碼</span><span class="sxs-lookup"><span data-stu-id="29f65-141">ConvertPluginCLSID Subkey</span></span>](convertpluginclsid-subkey.md)

## <a name="related-topics"></a><span data-ttu-id="29f65-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="29f65-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29f65-143">**登錄設定**</span><span class="sxs-lookup"><span data-stu-id="29f65-143">**Registry Settings**</span></span>](registry-settings.md)
</dt> <dt>

[<span data-ttu-id="29f65-144">**Windows Media Player 轉換外掛程式**</span><span class="sxs-lookup"><span data-stu-id="29f65-144">**Windows Media Player Conversion Plug-ins**</span></span>](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




