---
description: 在 DirectShow 中使用 Windows Media
ms.assetid: 2fae0504-d1da-413a-80dd-de7818f506ef
title: 在 DirectShow 中使用 Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e73726f0d7251f1c19beee05cfd8f335d3fdd7a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104386324"
---
# <a name="using-windows-media-in-directshow"></a><span data-ttu-id="6347a-103">在 DirectShow 中使用 Windows Media</span><span class="sxs-lookup"><span data-stu-id="6347a-103">Using Windows Media in DirectShow</span></span>

<span data-ttu-id="6347a-104">本節說明如何使用 DirectShow 來播放和寫入 Advanced 系統格式 (ASF) 檔。</span><span class="sxs-lookup"><span data-stu-id="6347a-104">This section describes how to use DirectShow to play and write Advanced Systems Format (ASF) files.</span></span> <span data-ttu-id="6347a-105">ASF 檔案通常包含使用 Windows Media 音訊和影片編解碼器編碼的音訊和影片內容。</span><span class="sxs-lookup"><span data-stu-id="6347a-105">ASF files commonly contain audio and video content encoded using the Windows Media Audio and Video codecs.</span></span> <span data-ttu-id="6347a-106">不過，ASF 可以包含任何類型的資料。</span><span class="sxs-lookup"><span data-stu-id="6347a-106">However, ASF can contain any type of data.</span></span>

<span data-ttu-id="6347a-107">下列 DirectShow 篩選器支援讀取和寫入 ASF 檔案：</span><span class="sxs-lookup"><span data-stu-id="6347a-107">The following DirectShow filters support reading and writing ASF files:</span></span>

-   <span data-ttu-id="6347a-108">[WM ASF 讀取器篩選器](wm-asf-reader-filter.md)。</span><span class="sxs-lookup"><span data-stu-id="6347a-108">[WM ASF Reader Filter](wm-asf-reader-filter.md).</span></span> <span data-ttu-id="6347a-109">讀取 ASF 檔。</span><span class="sxs-lookup"><span data-stu-id="6347a-109">Reads ASF files.</span></span>
-   <span data-ttu-id="6347a-110">[WM ASF 寫入器篩選器](wm-asf-writer-filter.md)。</span><span class="sxs-lookup"><span data-stu-id="6347a-110">[WM ASF Writer Filter](wm-asf-writer-filter.md).</span></span> <span data-ttu-id="6347a-111">Wrties ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="6347a-111">Wrties ASF files.</span></span>
-   <span data-ttu-id="6347a-112">[Sql-dmo 包裝](dmo-wrapper-filter.md)函式篩選。</span><span class="sxs-lookup"><span data-stu-id="6347a-112">[DMO Wrapper Filter](dmo-wrapper-filter.md).</span></span> <span data-ttu-id="6347a-113">包裝 Windows Media 編碼器和解碼器 DMOs。</span><span class="sxs-lookup"><span data-stu-id="6347a-113">Wraps the Windows Media encoder and decoder DMOs.</span></span>

### <a name="versions"></a><span data-ttu-id="6347a-114">版本</span><span class="sxs-lookup"><span data-stu-id="6347a-114">Versions</span></span>

<span data-ttu-id="6347a-115">WM ASF 讀取器和 WM ASF 寫入器篩選器封裝在名為 qasf.dll 的 DLL 中，而篩選器統稱為「QASF 元件」。</span><span class="sxs-lookup"><span data-stu-id="6347a-115">The WM ASF Reader and WM ASF Writer filters are packaged in the DLL named qasf.dll, and the filters are collectively named "QASF components."</span></span> <span data-ttu-id="6347a-116">這些篩選器是 Windows Media Format SDK 的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="6347a-116">These filters are wrappers for the Windows Media Format SDK.</span></span> <span data-ttu-id="6347a-117">DLL (qasf.dll) 先在 DirectX SDK 中發佈，但稍後會在 Windows Media Format SDK 中更新。</span><span class="sxs-lookup"><span data-stu-id="6347a-117">The DLL (qasf.dll) was first published in the DirectX SDK but was later updated in the Windows Media Format SDK.</span></span> <span data-ttu-id="6347a-118">以下是 QASF 篩選的版本歷程記錄：</span><span class="sxs-lookup"><span data-stu-id="6347a-118">Here is the version history of the QASF filters:</span></span>

-   <span data-ttu-id="6347a-119">DirectShow 8.1 支援 Windows Media Format SDK 7.0 版。</span><span class="sxs-lookup"><span data-stu-id="6347a-119">DirectShow 8.1 supports Windows Media Format SDK version 7.0.</span></span>
-   <span data-ttu-id="6347a-120">DirectShow 9.0 支援 Windows Media Format SDK 7.1 版。</span><span class="sxs-lookup"><span data-stu-id="6347a-120">DirectShow 9.0 supports Windows Media Format SDK version 7.1.</span></span>
-   <span data-ttu-id="6347a-121">Windows XP Service Pack 2 支援 Windows Media Format 9 SDK。</span><span class="sxs-lookup"><span data-stu-id="6347a-121">Windows XP Service Pack 2 supports Windows Media Format 9 SDK.</span></span>
-   <span data-ttu-id="6347a-122">Windows Vista 支援 Windows Media Format 11 SDK。</span><span class="sxs-lookup"><span data-stu-id="6347a-122">Windows Vista supports Windows Media Format 11 SDK.</span></span>
-   <span data-ttu-id="6347a-123">Windows Media Format 9 SDK 和更新版本包含 QASF 的對應版本。</span><span class="sxs-lookup"><span data-stu-id="6347a-123">Windows Media Format 9 SDK and later contain corresponding versions of QASF.</span></span>

<span data-ttu-id="6347a-124">若要取得最新版本的 QASF，請一律下載最新的 Windows Media Format SDK。</span><span class="sxs-lookup"><span data-stu-id="6347a-124">To get the latest version of QASF, always download the latest Windows Media Format SDK.</span></span>

### <a name="legacy-windows-media-source-filter"></a><span data-ttu-id="6347a-125">舊版 Windows Media 來源篩選</span><span class="sxs-lookup"><span data-stu-id="6347a-125">Legacy Windows Media Source Filter</span></span>

<span data-ttu-id="6347a-126">在 Windows XP Service Pack 1 及更早版本中，適用于 ASF 檔案的預設來源篩選 ( .asf、.wmv 和 .wma 副檔名) 是過時的 [Windows Media 來源篩選](windows-media-source-filter.md)。</span><span class="sxs-lookup"><span data-stu-id="6347a-126">In Windows XP Service Pack 1 and earlier, the default source filter for ASF files (.asf, .wmv, and .wma file extensions) is the obsolete [Windows Media Source Filter](windows-media-source-filter.md).</span></span> <span data-ttu-id="6347a-127">維護此行為的目的，是為了確保與使用 Windows Media Player 6.4 的應用程式回溯相容。</span><span class="sxs-lookup"><span data-stu-id="6347a-127">This behavior was maintained to ensure backward compatibility with applications that used the Windows Media Player 6.4.</span></span> <span data-ttu-id="6347a-128">新的應用程式應該使用較新版本的 QASF，這會讓 WM ASF 讀取器篩選播放 ASF 檔案的預設篩選器。</span><span class="sxs-lookup"><span data-stu-id="6347a-128">New applications should use the newer versions of QASF, which make the WM ASF Reader filter the default filter for playing ASF files.</span></span>

<span data-ttu-id="6347a-129">如需有關 Windows Media 套件軟體發展工具組的詳細資訊，請參閱 MDSN 文件庫的 [音訊和影片](../audio-and-video.md) 章節。</span><span class="sxs-lookup"><span data-stu-id="6347a-129">For more information on the Windows Media suite of software development kits, see the [Audio and Video](../audio-and-video.md) section of the MDSN Library.</span></span>

<span data-ttu-id="6347a-130">本文包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="6347a-130">This article contains the following topics:</span></span>

-   [<span data-ttu-id="6347a-131">在 DirectShow 中讀取 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="6347a-131">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
-   [<span data-ttu-id="6347a-132">在 DirectShow 中建立 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="6347a-132">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)

## <a name="related-topics"></a><span data-ttu-id="6347a-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="6347a-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6347a-134">使用 DirectShow</span><span class="sxs-lookup"><span data-stu-id="6347a-134">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 
