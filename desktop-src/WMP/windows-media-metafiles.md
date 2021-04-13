---
title: Windows Media 中繼檔案  (可能為英文網頁)
description: Windows Media 中繼檔案  (可能為英文網頁)
ms.assetid: 77af7d15-52ac-496c-8037-51827adf0250
keywords:
- Windows Media 中繼檔，關於
- Windows Media Player，中繼檔
- Windows Media Player，Windows Media 中繼檔
- 中繼檔，關於
- Windows Media，中繼檔
- Windows Media 中繼檔播放清單，關於
- 播放清單，關於
- 中繼檔播放清單，關於
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 385b149e07e9d30df4e11a21f8e7aa4b05e06910
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300904"
---
# <a name="windows-media-metafiles"></a><span data-ttu-id="2cbe0-111">Windows Media 中繼檔案  (可能為英文網頁)</span><span class="sxs-lookup"><span data-stu-id="2cbe0-111">Windows Media Metafiles</span></span>

<span data-ttu-id="2cbe0-112">此參考檔記載 Windows Media 中繼檔，其使用地板蠟、. 300k.wvx、. wmx 和 .asx 副檔名。</span><span class="sxs-lookup"><span data-stu-id="2cbe0-112">This reference documents Windows Media metafiles, which use the .wax, .wvx, .wmx, and .asx file name extensions.</span></span> <span data-ttu-id="2cbe0-113">其中包含總覽和程式設計指南章節，以及中繼檔元素標記、其屬性和值，以及與每個專案相關的特殊條件的完整參考區段。</span><span class="sxs-lookup"><span data-stu-id="2cbe0-113">It contains overview and programming guide sections, and a full reference section on metafile element tags, their attributes and values, and special conditions related to each element.</span></span>

<span data-ttu-id="2cbe0-114">中繼檔是包含其他檔案相關資訊的檔案。</span><span class="sxs-lookup"><span data-stu-id="2cbe0-114">A metafile is a file that contains information about other files.</span></span> <span data-ttu-id="2cbe0-115">中繼檔可以用來列出要依序播放的媒體內容檔案群組。</span><span class="sxs-lookup"><span data-stu-id="2cbe0-115">A metafile can be used to list a group of media content files that are to be played in order.</span></span> <span data-ttu-id="2cbe0-116">Windows Media 中繼檔播放清單，在本參考檔中只是指播放清單，是 Microsoft Windows Media 技術最強大的功能之一。</span><span class="sxs-lookup"><span data-stu-id="2cbe0-116">Windows Media metafile playlists, simply referred to as playlists in this reference document, are one of the most powerful features of Microsoft Windows Media Technologies.</span></span> <span data-ttu-id="2cbe0-117">播放清單可讓您控制和自訂媒體內容。</span><span class="sxs-lookup"><span data-stu-id="2cbe0-117">Playlists allow you to control and customize your media content.</span></span> <span data-ttu-id="2cbe0-118">例如，有了播放清單，您可以將內容排程為連續播放，或是將廣告或特殊興趣剪輯插入簡報中。</span><span class="sxs-lookup"><span data-stu-id="2cbe0-118">For instance, with playlists you can schedule content to play in succession or insert advertising or special interest clips into a presentation.</span></span> <span data-ttu-id="2cbe0-119">播放清單的另一項好處是，不是播放資料流程、停止、啟動下一個資料流程，然後等候它完成緩衝處理，而 Windows Media Services 和 Windows Media Player 會一起運作，以最短的緩衝時間或其間的中斷來播放剪輯。</span><span class="sxs-lookup"><span data-stu-id="2cbe0-119">A further advantage of playlists is that instead of playing a stream, stopping, starting the next stream, and then waiting for it to finish buffering, Windows Media Services and Windows Media Player work together to play the clips one after the other with minimal buffering time or interruption between them.</span></span>

<span data-ttu-id="2cbe0-120">Windows Media 技術和其他網際網路產品提供您工具，以瞭解使用者人口統計，並針對個別使用者動態自訂廣播或訊息。</span><span class="sxs-lookup"><span data-stu-id="2cbe0-120">Windows Media Technologies and other Internet products provide you with the tools to understand user demographics and dynamically customize a broadcast or message for individual users.</span></span>

<span data-ttu-id="2cbe0-121">此參考分為下列各節。</span><span class="sxs-lookup"><span data-stu-id="2cbe0-121">This reference is divided into the following sections.</span></span>



| <span data-ttu-id="2cbe0-122">區段</span><span class="sxs-lookup"><span data-stu-id="2cbe0-122">Section</span></span>                                                                  | <span data-ttu-id="2cbe0-123">描述</span><span class="sxs-lookup"><span data-stu-id="2cbe0-123">Description</span></span>                                                                                                                                                                         |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2cbe0-124">關於 Windows Media 中繼檔</span><span class="sxs-lookup"><span data-stu-id="2cbe0-124">About Windows Media Metafiles</span></span>](about-windows-media-metafiles.md)       | <span data-ttu-id="2cbe0-125">介紹 Windows Media 中繼檔元素，並討論其用途。</span><span class="sxs-lookup"><span data-stu-id="2cbe0-125">Introduces Windows Media metafile elements and discusses their purpose.</span></span>                                                                                                             |
| [<span data-ttu-id="2cbe0-126">Windows Media 中繼檔指南</span><span class="sxs-lookup"><span data-stu-id="2cbe0-126">Windows Media Metafile Guide</span></span>](windows-media-metafile-guide.md)         | <span data-ttu-id="2cbe0-127">詳細說明建立中繼檔所需的步驟。</span><span class="sxs-lookup"><span data-stu-id="2cbe0-127">Details the steps necessary for creating metafiles.</span></span> <span data-ttu-id="2cbe0-128">範例說明如何針對特定工作使用元素標記。</span><span class="sxs-lookup"><span data-stu-id="2cbe0-128">Examples illustrate how to use element tags for specific tasks.</span></span>                                                                 |
| [<span data-ttu-id="2cbe0-129">Windows Media 中繼檔參考</span><span class="sxs-lookup"><span data-stu-id="2cbe0-129">Windows Media Metafile Reference</span></span>](windows-media-metafile-reference.md) | <span data-ttu-id="2cbe0-130">詳細說明每個中繼檔元素、其屬性和值，以及與每個專案相關的特殊條件。</span><span class="sxs-lookup"><span data-stu-id="2cbe0-130">Explains in detail each of the metafile elements, their attributes and values, and special conditions related to each.</span></span> <span data-ttu-id="2cbe0-131">說明中繼檔副檔名及其適當用途。</span><span class="sxs-lookup"><span data-stu-id="2cbe0-131">Explains metafile file name extensions and their proper use.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2cbe0-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="2cbe0-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cbe0-133">**Windows Media Player SDK**</span><span class="sxs-lookup"><span data-stu-id="2cbe0-133">**Windows Media Player SDK**</span></span>](windows-media-player-sdk.md)
</dt> </dl>

 

 




