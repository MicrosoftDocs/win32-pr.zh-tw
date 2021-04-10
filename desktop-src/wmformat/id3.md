---
title: ID3 支援
description: ID3 是定義一組標準的組織，可在 MPEG 層-3 (MP3) 音訊檔案中包含中繼資料。
ms.assetid: 8c1f1114-48d8-4dce-b7ab-0293265a875c
keywords:
- Windows Media Format SDK，ID3 支援
- Advanced Systems Format (ASF) 、ID3 支援
- ASF (Advanced Systems Format) 、ID3 支援
- 中繼資料、ID3
- ID3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26f356dae63b1d3672b584bb61956f478b67a697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675112"
---
# <a name="id3-support"></a><span data-ttu-id="94114-108">ID3 支援</span><span class="sxs-lookup"><span data-stu-id="94114-108">ID3 Support</span></span>

<span data-ttu-id="94114-109">ID3 是定義一組標準的組織，可在 MPEG 層-3 (MP3) 音訊檔案中包含中繼資料。</span><span class="sxs-lookup"><span data-stu-id="94114-109">ID3 is an organization that has defined a set of standards for including metadata in MPEG Layer-3 (MP3) audio files.</span></span> <span data-ttu-id="94114-110">Windows Media 格式 SDK 的物件會提供 ID3 相容屬性的支援。</span><span class="sxs-lookup"><span data-stu-id="94114-110">The objects of the Windows Media Format SDK provide support for ID3 compatible attributes.</span></span> <span data-ttu-id="94114-111">支援三種不同的 ID3 版本： ID3v1. x、ID3v 2.2 和 ID3v 2.3/v2、4。</span><span class="sxs-lookup"><span data-stu-id="94114-111">Three distinct ID3 versions are supported: ID3v1.x, ID3v2.2, and ID3v2.3/v2,4.</span></span> <span data-ttu-id="94114-112">如需等同于 ID3 框架的屬性清單，請參閱 [Id3 標記支援](id3-tag-support.md)。</span><span class="sxs-lookup"><span data-stu-id="94114-112">For a list of the attributes that equate to ID3 frames, see [ID3 Tag Support](id3-tag-support.md).</span></span>

<span data-ttu-id="94114-113">除非另有說明，否則此 SDK 的物件不會執行 ID3 框架資料的驗證。</span><span class="sxs-lookup"><span data-stu-id="94114-113">Unless otherwise noted, no validation of ID3 frame data is performed by the objects of this SDK.</span></span> <span data-ttu-id="94114-114">例如，中繼資料屬性 [**WM/歌詞 \_ 內容**](wm-lyrics-synchronised.md) 會儲存歌曲歌詞與對應的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="94114-114">For example, the metadata attribute [**WM/Lyrics\_Synchronised**](wm-lyrics-synchronised.md) stores the song lyrics with corresponding time stamps.</span></span> <span data-ttu-id="94114-115">寫入 **WM/歌詞 \_ 內容** 屬性時，此 SDK 的物件將不會檢查，以確保時間戳記是以時間順序排列，或是執行任何種類的驗證。</span><span class="sxs-lookup"><span data-stu-id="94114-115">When writing a **WM/Lyrics\_Synchronised** attribute, the objects of this SDK will not check to ensure that the time stamps are in chronological order or perform validation of any kind.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94114-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="94114-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94114-117">**屬性**</span><span class="sxs-lookup"><span data-stu-id="94114-117">**Attributes**</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="94114-118">**中繼資料功能**</span><span class="sxs-lookup"><span data-stu-id="94114-118">**Metadata Features**</span></span>](metadata-features.md)
</dt> <dt>

[<span data-ttu-id="94114-119">**使用中繼資料**</span><span class="sxs-lookup"><span data-stu-id="94114-119">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




