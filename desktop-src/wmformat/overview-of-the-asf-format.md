---
title: ASF 格式的概觀
description: ASF 格式的概觀
ms.assetid: ef22a493-d6cf-40d2-ab17-d87159066d1d
keywords:
- Windows Media Format SDK，ASF 格式總覽
- Advanced Systems Format (ASF) ，格式總覽
- ASF (Advanced Systems Format) ，格式總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2858ae1845629c25b52d4c15b5ce7fbb5eb82146
ms.sourcegitcommit: d230e7720c0b566919f8ca11ff7fe3c6b32e028c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/26/2020
ms.locfileid: "104374829"
---
# <a name="overview-of-the-asf-format"></a><span data-ttu-id="f361b-106">ASF 格式的概觀</span><span class="sxs-lookup"><span data-stu-id="f361b-106">Overview of the ASF Format</span></span>

<span data-ttu-id="f361b-107">Advanced Systems Format (ASF) 是一種可延伸的檔案格式，主要是用來儲存及播放同步處理的數位媒體串流，並透過網路傳輸。</span><span class="sxs-lookup"><span data-stu-id="f361b-107">The Advanced Systems Format (ASF) is an extensible file format designed primarily for storing and playing synchronized digital media streams and transmitting them over networks.</span></span> <span data-ttu-id="f361b-108">ASF 是 Windows Media 音訊的容器格式，也是以 Windows Media 視訊為基礎的內容。</span><span class="sxs-lookup"><span data-stu-id="f361b-108">ASF is the container format for Windows Media Audio and Windows Media Video-based content.</span></span> <span data-ttu-id="f361b-109">副檔名 wma 或 wmv 可用來指定 ASF 檔案，其中包含以 Windows Media 音訊和/或 Windows Media 視訊編解碼器編碼的內容。</span><span class="sxs-lookup"><span data-stu-id="f361b-109">The extension wma or wmv is used to specify an ASF file that contains content encoded with the Windows Media Audio and/or Windows Media Video codecs.</span></span> <span data-ttu-id="f361b-110">Windows Media Format SDK 可以用來建立和讀取 Windows Media 檔案，以及包含其他類型壓縮或未壓縮資料的 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="f361b-110">The Windows Media Format SDK can be used to create and read Windows Media files, as well as ASF files that contain other types of compressed or uncompressed data.</span></span>

<span data-ttu-id="f361b-111">本節提供 ASF 格式的一般描述作為背景資訊。</span><span class="sxs-lookup"><span data-stu-id="f361b-111">This section provides a general description of the ASF format as background information.</span></span> <span data-ttu-id="f361b-112">由於讀取器和寫入器物件會處理所有的低層級檔案剖析和格式化工作，因此在使用此 SDK 建立 ASF 檔案之前，不需要先深入瞭解 ASF。</span><span class="sxs-lookup"><span data-stu-id="f361b-112">Because the reader and writer objects handle all low-level file parsing and formatting tasks, it is not necessary to have a detailed understanding of ASF before using this SDK to create ASF files.</span></span> <span data-ttu-id="f361b-113">您可以在 [Microsoft 網站](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)上找到完整的 ASF 規格。</span><span class="sxs-lookup"><span data-stu-id="f361b-113">The complete ASF specification can be found on the [Microsoft Web site](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).</span></span>

<span data-ttu-id="f361b-114">ASF 格式的主要目標是：</span><span class="sxs-lookup"><span data-stu-id="f361b-114">The primary goals of the ASF format are:</span></span>

-   <span data-ttu-id="f361b-115">支援從媒體伺服器、HTTP 伺服器和本機存放裝置進行有效率的播放。</span><span class="sxs-lookup"><span data-stu-id="f361b-115">To support efficient playback from media servers, HTTP servers, and local storage devices.</span></span>
-   <span data-ttu-id="f361b-116">支援可調整的媒體類型，例如音訊和影片。</span><span class="sxs-lookup"><span data-stu-id="f361b-116">To support scalable media types such as audio and video.</span></span>
-   <span data-ttu-id="f361b-117">允許在各式各樣的頻寬上呈現單一多媒體組合。</span><span class="sxs-lookup"><span data-stu-id="f361b-117">To permit a single multimedia composition to be presented over a wide range of bandwidths.</span></span>
-   <span data-ttu-id="f361b-118">允許撰寫媒體資料流程關聯性的控制權，特別是在受限頻寬的案例中。</span><span class="sxs-lookup"><span data-stu-id="f361b-118">To allow authoring control over media stream relationships, especially in constrained-bandwidth scenarios.</span></span>
-   <span data-ttu-id="f361b-119">獨立于任何特定的多媒體組合系統、電腦作業系統或資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="f361b-119">To be independent of any particular multimedia composition system, computer operating system, or data communications protocol.</span></span>

<span data-ttu-id="f361b-120">ASF 檔案可以包含多個獨立或相依的資料流程，包括多頻道音訊的多個音訊串流，或適用于透過不同頻寬傳輸的多重位元速率影片串流。</span><span class="sxs-lookup"><span data-stu-id="f361b-120">An ASF file can contain multiple independent or dependent streams, including multiple audio streams for multichannel audio, or multiple bit rate video streams suitable for transmission over different bandwidths.</span></span> <span data-ttu-id="f361b-121">資料流程可以採用任何壓縮或未壓縮的格式;不過，最佳壓縮可透過 Microsoft Windows Media 音訊和 Video 9 系列編解碼器來達成。</span><span class="sxs-lookup"><span data-stu-id="f361b-121">The streams can be in any compressed or uncompressed format; however, the best compression is achieved with the Microsoft Windows Media Audio and Video 9 Series codecs.</span></span> <span data-ttu-id="f361b-122">除了標準音頻和影片媒體資料流程類型之外，ASF 檔案也可以包含文字串流、網頁和指令碼命令，以及任何其他任意資料類型。</span><span class="sxs-lookup"><span data-stu-id="f361b-122">In addition to the standard audio and video media stream types, an ASF file can also contain text streams, Web pages and script commands, and any other arbitrary data type.</span></span> <span data-ttu-id="f361b-123">ASF 支援即時和隨選多媒體內容。</span><span class="sxs-lookup"><span data-stu-id="f361b-123">ASF supports live and on-demand multimedia content.</span></span> <span data-ttu-id="f361b-124">您可以使用它作為車輛來錄製或播放 32 (例如，h.264 和 h.) 或 MBONE 會議。</span><span class="sxs-lookup"><span data-stu-id="f361b-124">It can be used as a vehicle to record or play back H.32X (for example, H.323 and H.324) or MBONE conferences.</span></span>

<span data-ttu-id="f361b-125">ASF 檔會組織成稱為「物件」的區段。</span><span class="sxs-lookup"><span data-stu-id="f361b-125">An ASF file is organized into sections called "objects."</span></span> <span data-ttu-id="f361b-126">有三個最上層物件，標頭物件和資料物件 (需要的) ，再加上選擇性的索引物件。</span><span class="sxs-lookup"><span data-stu-id="f361b-126">There are three top-level objects, a Header object and a Data object (both required), plus an optional Index object.</span></span> <span data-ttu-id="f361b-127">標頭物件包含檔案的一般資訊，例如檔案大小、資料流程數目、錯誤修正方法，以及使用的編解碼器。</span><span class="sxs-lookup"><span data-stu-id="f361b-127">The Header object contains general information about the file, such as file size, number of streams, error correction methods, and codecs used.</span></span> <span data-ttu-id="f361b-128">中繼資料也會儲存在這裡。</span><span class="sxs-lookup"><span data-stu-id="f361b-128">Metadata is also stored here.</span></span> <span data-ttu-id="f361b-129">標頭物件是唯一可包含其他物件的最上層物件。</span><span class="sxs-lookup"><span data-stu-id="f361b-129">The Header object is the only top level object that can contain other objects.</span></span> <span data-ttu-id="f361b-130">資料物件包含資料流程資料，並組織成封包。</span><span class="sxs-lookup"><span data-stu-id="f361b-130">The Data object contains the stream data, organized in packets.</span></span> <span data-ttu-id="f361b-131">Simple Index 物件包含一份相關聯的索引/主要畫面格配對清單，可讓應用程式有效率地搜尋檔案。</span><span class="sxs-lookup"><span data-stu-id="f361b-131">The Simple Index object contains a list of associated index/key-frame pairs that enables applications to seek through a file efficiently.</span></span> <span data-ttu-id="f361b-132">與每個主要畫面格相關聯的索引可以是展示時間、影片畫面號碼或參考時間戳記。</span><span class="sxs-lookup"><span data-stu-id="f361b-132">The index associated with each key frame can be a presentation time, a video frame number, or a reference time stamp.</span></span>

<span data-ttu-id="f361b-133">每個最上層或較低層級的物件都是以全域唯一識別碼（ (GUID) 和大小值）作為開頭。</span><span class="sxs-lookup"><span data-stu-id="f361b-133">Each top-level or lower-level object begins with a globally unique identifier (GUID) and a size value.</span></span> <span data-ttu-id="f361b-134">這些數位可讓檔案讀取器將適當位置的資訊剖析成可辨識的物件。</span><span class="sxs-lookup"><span data-stu-id="f361b-134">These numbers allow the file reader to parse the information at appropriate places into identifiable objects.</span></span> <span data-ttu-id="f361b-135">因為這些 Guid，較低層級的物件可以依任何順序傳送，而且仍可辨識。</span><span class="sxs-lookup"><span data-stu-id="f361b-135">Because of these GUIDs, lower-level objects can be sent in any order and still be recognized.</span></span> <span data-ttu-id="f361b-136">ASF 格式的設計目的是克服不正確的資料接收。</span><span class="sxs-lookup"><span data-stu-id="f361b-136">The ASF format is designed to overcome inaccurate data reception.</span></span> <span data-ttu-id="f361b-137">部分下載的 ASF 檔案仍可讀取，只要其中包含標頭物件和至少一個資料物件。</span><span class="sxs-lookup"><span data-stu-id="f361b-137">A partially downloaded ASF file can still be read, as long as it contains the Header object and at least one Data object.</span></span>

<span data-ttu-id="f361b-138">ASF 規格中顯示之 ASF 的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f361b-138">Detailed information about ASF in presented in the ASF specification.</span></span> <span data-ttu-id="f361b-139">您可以從 [Microsoft 網站](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)下載規格。</span><span class="sxs-lookup"><span data-stu-id="f361b-139">You can download the specification from the [Microsoft Web site](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f361b-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="f361b-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f361b-141">**關於 Windows Media Format SDK**</span><span class="sxs-lookup"><span data-stu-id="f361b-141">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




