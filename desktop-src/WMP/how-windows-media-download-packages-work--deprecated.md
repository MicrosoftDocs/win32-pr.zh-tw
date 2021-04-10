---
title: 'Windows Media 下載套件的運作方式 (已淘汰) '
description: 'Windows Media 下載套件的運作方式 (已淘汰) '
ms.assetid: 8bab1764-93da-4abc-a8b7-17bc44b381ce
keywords:
- Windows Media 中繼檔，Windows Media 下載套件
- Windows Media Player，Windows Media 下載套件
- 中繼檔，Windows Media 下載套件
- Windows Media、Windows Media 下載套件
- Windows Media 下載套件，關於
- Windows Media 下載套件，封裝的運作方式
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1db477791bb93cd599dcef38a90b230c6cd7ddde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092252"
---
# <a name="how-windows-media-download-packages-work-deprecated"></a><span data-ttu-id="8f9f7-109">Windows Media 下載套件的運作方式 (已淘汰) </span><span class="sxs-lookup"><span data-stu-id="8f9f7-109">How Windows Media Download Packages Work (deprecated)</span></span>

<span data-ttu-id="8f9f7-110">本頁記載了未來版本的 Windows Media Player 和 Windows Media Player SDK 可能無法使用的功能。</span><span class="sxs-lookup"><span data-stu-id="8f9f7-110">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="8f9f7-111">當使用者按一下網頁瀏覽器中的連結（例如 Microsoft Internet Explorer）時，就會從網站啟動 Windows Media 下載套件。</span><span class="sxs-lookup"><span data-stu-id="8f9f7-111">A Windows Media Download package is launched from a website when a user clicks a link in a Web browser, such as Microsoft Internet Explorer.</span></span> <span data-ttu-id="8f9f7-112">此動作會開啟 Windows Media Player 然後在使用者的硬碟上，下載並取消封裝 Windows Media 下載套件（預設資料夾）。</span><span class="sxs-lookup"><span data-stu-id="8f9f7-112">This action opens Windows Media Player and then downloads and un-packages the Windows Media Download package on the user's hard disk in a default folder.</span></span>

<span data-ttu-id="8f9f7-113">從 Windows Media 下載套件解壓縮檔案之後，Windows Media Player 會在封裝的檔案之間找到副檔名為 .asx 的 Windows Media 中繼檔播放清單。</span><span class="sxs-lookup"><span data-stu-id="8f9f7-113">Once the files have been extracted from the Windows Media Download package, Windows Media Player locates a Windows Media metafile playlist with an .asx file name extension among the packaged files.</span></span> <span data-ttu-id="8f9f7-114">如果找到一個，播放清單會根據內含的中繼檔建立播放清單。</span><span class="sxs-lookup"><span data-stu-id="8f9f7-114">If it finds one, the Player creates a playlist based on the included metafile.</span></span> <span data-ttu-id="8f9f7-115">接著會將包含多媒體內容的檔案新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="8f9f7-115">Files that contain multimedia content are then added to the library.</span></span>

<span data-ttu-id="8f9f7-116">Windows Media Player 也會尋找中繼檔中的 **外觀** 元素。</span><span class="sxs-lookup"><span data-stu-id="8f9f7-116">Windows Media Player also looks for a **SKIN** element in the metafile.</span></span> <span data-ttu-id="8f9f7-117">如果面板 **元素包含** 副檔名為 wmz 的 border 檔案的參考，則播放機會將框線載入至 [ **現正播放** ] 窗格中。</span><span class="sxs-lookup"><span data-stu-id="8f9f7-117">If the **SKIN** element contains a reference to a border file with a .wmz file name extension, the Player loads the border into the **Now Playing** pane.</span></span> <span data-ttu-id="8f9f7-118">然後，玩家會開始播放套件中提供的內容。</span><span class="sxs-lookup"><span data-stu-id="8f9f7-118">The Player then starts to play the content provided in the package.</span></span>

<span data-ttu-id="8f9f7-119">下圖顯示如何將內容封裝在 Windows Media 下載檔案中、張貼至網站、在用戶端電腦上使用 Windows Media Player 進行下載及播放。</span><span class="sxs-lookup"><span data-stu-id="8f9f7-119">The following diagram shows how content is packaged in a Windows Media Download file, posted to a website, downloaded, and played on a client computer using Windows Media Player.</span></span>

![如何取得並播放 windows media 下載檔案。](images/wmd-image.png) <span data-ttu-id="8f9f7-121">Windows Media 下載</span><span class="sxs-lookup"><span data-stu-id="8f9f7-121">Windows Media Download</span></span>

<span data-ttu-id="8f9f7-122">下表說明組成 Windows Media 下載套件的三個元素。</span><span class="sxs-lookup"><span data-stu-id="8f9f7-122">The following table describes the three elements that make up a Windows Media Download package.</span></span>



| <span data-ttu-id="8f9f7-123">Package 元素</span><span class="sxs-lookup"><span data-stu-id="8f9f7-123">Package element</span></span>    | <span data-ttu-id="8f9f7-124">函式</span><span class="sxs-lookup"><span data-stu-id="8f9f7-124">Function</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="8f9f7-125">副檔名</span><span class="sxs-lookup"><span data-stu-id="8f9f7-125">File name extensions</span></span>                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="8f9f7-126">框線</span><span class="sxs-lookup"><span data-stu-id="8f9f7-126">Border</span></span>             | <span data-ttu-id="8f9f7-127">由內容擁有者所建立的固定自訂使用者介面，可顯示、連結及播放 Windows Media 下載套件中封裝的所有媒體。</span><span class="sxs-lookup"><span data-stu-id="8f9f7-127">A fixed, customized user interface created by the content owner for displaying, linking, and playing all media packaged in the Windows Media Download package.</span></span> <span data-ttu-id="8f9f7-128">用來建立框線的技巧，類似于用來建立外觀的技巧。</span><span class="sxs-lookup"><span data-stu-id="8f9f7-128">The techniques used to create borders are similar to those used to create skins.</span></span> | <span data-ttu-id="8f9f7-129">.wmz</span><span class="sxs-lookup"><span data-stu-id="8f9f7-129">.wmz</span></span>                                     |
| <span data-ttu-id="8f9f7-130">中繼檔播放清單</span><span class="sxs-lookup"><span data-stu-id="8f9f7-130">Metafile Playlist</span></span>  | <span data-ttu-id="8f9f7-131">Windows Media 中繼檔，其中包含 **專案專案** 、播放清單資訊，以及內容檔案的 **外觀** 元素識別。</span><span class="sxs-lookup"><span data-stu-id="8f9f7-131">A Windows Media metafile that contains **ENTRY** elements, playlist information, and a **SKIN** element identity for content files.</span></span>                                                                                                             | <span data-ttu-id="8f9f7-132">.asx</span><span class="sxs-lookup"><span data-stu-id="8f9f7-132">.asx</span></span>                                     |
| <span data-ttu-id="8f9f7-133">多媒體內容</span><span class="sxs-lookup"><span data-stu-id="8f9f7-133">Multimedia Content</span></span> | <span data-ttu-id="8f9f7-134">包含 Windows Media Player 所支援之任何音訊或影片格式的檔案。</span><span class="sxs-lookup"><span data-stu-id="8f9f7-134">A file containing any audio or video format that is supported by Windows Media Player.</span></span>                                                                                                                                                          | <span data-ttu-id="8f9f7-135">.wma、.wmv、.asf、.wav、.avi、. mpg、mp3</span><span class="sxs-lookup"><span data-stu-id="8f9f7-135">.wma, .wmv, .asf, .wav, .avi, .mpg, .mp3</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8f9f7-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="8f9f7-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f9f7-137">**(淘汰的 Windows Media 下載套件)**</span><span class="sxs-lookup"><span data-stu-id="8f9f7-137">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




