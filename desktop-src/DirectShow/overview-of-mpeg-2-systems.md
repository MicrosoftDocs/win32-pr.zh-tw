---
description: MPEG 2 系統總覽
ms.assetid: 1ebfb194-002f-40ac-9be5-267861b6687b
title: MPEG 2 系統總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4206b36db7b3172c6e161745922e83490855c73c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109517"
---
# <a name="overview-of-mpeg-2-systems"></a><span data-ttu-id="9581f-103">MPEG 2 系統總覽</span><span class="sxs-lookup"><span data-stu-id="9581f-103">Overview of MPEG-2 Systems</span></span>

<span data-ttu-id="9581f-104">本節提供 MPEG-2 系統層的一般非技術總覽。</span><span class="sxs-lookup"><span data-stu-id="9581f-104">This section gives a general, non-technical overview of the MPEG-2 Systems layer.</span></span> <span data-ttu-id="9581f-105">MPEG-2 系統是定義在 MPEG-2 中如何多工音訊和影片串流的標準。</span><span class="sxs-lookup"><span data-stu-id="9581f-105">MPEG-2 Systems is the standard that defines how audio and video streams are multiplexed in MPEG-2.</span></span>

<span data-ttu-id="9581f-106">**基本資料流程**</span><span class="sxs-lookup"><span data-stu-id="9581f-106">**Elementary Streams**</span></span>

<span data-ttu-id="9581f-107">MPEG-2 多工處理是以一或多個位元組串流（稱為基礎串流 (ES) ）開始，其中包含影片、音訊或其他資料。</span><span class="sxs-lookup"><span data-stu-id="9581f-107">MPEG-2 multiplexing starts with one or more byte streams, called elementary streams (ES), that contain video, audio, or other data.</span></span> <span data-ttu-id="9581f-108">例如，某段影片包含壓縮的影片畫面，加上序列標頭、圖片群組 (GOP) 標頭，以及將資料流程解碼所需的任何其他方法。</span><span class="sxs-lookup"><span data-stu-id="9581f-108">For example, a video ES contains compressed video frames, plus sequence headers, group-of-picture (GOP) headers, and anything else needed by the decoder to decode the stream.</span></span> <span data-ttu-id="9581f-109">系統層不會定義 ES 位元組資料流程的內容。</span><span class="sxs-lookup"><span data-stu-id="9581f-109">The Systems layer does not define the contents of the ES byte stream.</span></span>

<span data-ttu-id="9581f-110">基礎資料流程會細分成封包， (PE) 形成 *packetized 的基本資料流程* 。</span><span class="sxs-lookup"><span data-stu-id="9581f-110">An elementary stream is broken up into packets, forming a *packetized elementary stream* (PES).</span></span> <span data-ttu-id="9581f-111">PE 封包的長度不定。</span><span class="sxs-lookup"><span data-stu-id="9581f-111">PES packets have variable length.</span></span> <span data-ttu-id="9581f-112">封 *包的內容* 稱為「承載」。</span><span class="sxs-lookup"><span data-stu-id="9581f-112">The contents of the packet are called the *payload*.</span></span> <span data-ttu-id="9581f-113">每個 PE 封包也都包含一個標頭。</span><span class="sxs-lookup"><span data-stu-id="9581f-113">Each PES packet also includes a header.</span></span> <span data-ttu-id="9581f-114">多工器會將1位元組資料流程識別碼指派給每個 PE;個別的 PE 封包是由封包標頭中的資料流程識別碼所識別。</span><span class="sxs-lookup"><span data-stu-id="9581f-114">The multiplexer assigns a 1-byte stream ID to every PES; individual PES packets are identified by the stream ID in the packet header.</span></span> <span data-ttu-id="9581f-115">針對音訊串流，資料流程識別碼的格式為 110 *xxxxx*。</span><span class="sxs-lookup"><span data-stu-id="9581f-115">For audio streams, the stream ID has the form 110 *xxxxx*.</span></span> <span data-ttu-id="9581f-116">若為影片，資料流程識別碼的格式為 1110 *yyyy*。</span><span class="sxs-lookup"><span data-stu-id="9581f-116">For video, the stream ID has the form 1110 *yyyy*.</span></span>

<span data-ttu-id="9581f-117">MPEG-2 標準定義了兩種傳遞 packetized 基本資料流程的方式： *程式串流* 和 *傳輸資料流程*。</span><span class="sxs-lookup"><span data-stu-id="9581f-117">The MPEG-2 standard defines two ways to deliver packetized elementary streams: *program streams* and *transport streams*.</span></span>

<span data-ttu-id="9581f-118">**程式資料流程**</span><span class="sxs-lookup"><span data-stu-id="9581f-118">**Program Streams**</span></span>

<span data-ttu-id="9581f-119">程式資料流程是針對相對無錯誤的環境而設計，例如本機檔案儲存體。</span><span class="sxs-lookup"><span data-stu-id="9581f-119">Program streams are designed for environments that are relatively error-free, such as local file storage.</span></span> <span data-ttu-id="9581f-120">在程式資料流程中，會將 PE 封包多工化並組織成稱為「 *套件*」的單位。</span><span class="sxs-lookup"><span data-stu-id="9581f-120">In a program stream, the PES packets are multiplexed and organized into units called *packs*.</span></span> <span data-ttu-id="9581f-121">程式資料流程中的所有 PE 資料流程都會同步處理至相同的時鐘。</span><span class="sxs-lookup"><span data-stu-id="9581f-121">All of the PES streams in a program stream are synchronized to the same clock.</span></span>

<span data-ttu-id="9581f-122">**傳輸資料流程**</span><span class="sxs-lookup"><span data-stu-id="9581f-122">**Transport Streams**</span></span>

<span data-ttu-id="9581f-123"> (TS) 的傳輸串流是針對不可靠或容易出錯的環境所設計，例如網路廣播。</span><span class="sxs-lookup"><span data-stu-id="9581f-123">Transport streams (TS) are designed for unreliable or error-prone environments, such as network broadcasts.</span></span> <span data-ttu-id="9581f-124">此外，它們也可以包含多個同步處理至不同時鐘的程式。</span><span class="sxs-lookup"><span data-stu-id="9581f-124">Also, they can contain multiple programs that are synchronized to different clocks.</span></span> <span data-ttu-id="9581f-125">傳輸資料流程新增了第二層的 packetizing，也就是將 PE 資料流程封裝到傳輸資料流程封包內，每封包的大小都固定為188位元組。</span><span class="sxs-lookup"><span data-stu-id="9581f-125">A transport stream adds a second layer of packetizing — the PES streams are packaged inside transport stream packets, which have a fixed size of 188 bytes per packet.</span></span> <span data-ttu-id="9581f-126">TS 封包也可以包含程式資訊串流，如下一節所述。</span><span class="sxs-lookup"><span data-stu-id="9581f-126">TS packets can also contain program information streams, which are described in the following section.</span></span>

<span data-ttu-id="9581f-127">每個 TS 封包都有一個4位元組的標頭，再加上一個選擇性的調整欄位，其中包含額外的標頭資訊。</span><span class="sxs-lookup"><span data-stu-id="9581f-127">Each TS packet has a 4-byte header, plus an optional adaptation field that contains additional header information.</span></span> <span data-ttu-id="9581f-128">多工器會將程式識別碼 (PID) 指派給每個 PE 資料流程或程式資訊串流。</span><span class="sxs-lookup"><span data-stu-id="9581f-128">The multiplexer assigns a program ID (PID) to each PES stream or program information stream.</span></span> <span data-ttu-id="9581f-129">Pid 可用來識別 TS 封包，類似于串流識別碼識別 PE 封包的方式。</span><span class="sxs-lookup"><span data-stu-id="9581f-129">The PIDs are used to identify the TS packets, similar to the way stream IDs identify PES packets.</span></span> <span data-ttu-id="9581f-130"> (如果傳輸資料流程包含多個程式，則 *資料流程* 識別碼可能不是唯一的，但 PID 指派在傳輸資料流程中是唯一的。 ) </span><span class="sxs-lookup"><span data-stu-id="9581f-130">(If a transport stream contains multiple programs, the *stream* IDs might not be unique, but the PID assignments are unique within the transport stream.)</span></span>

<span data-ttu-id="9581f-131">**程式特定資訊**</span><span class="sxs-lookup"><span data-stu-id="9581f-131">**Program Specific Information**</span></span>

<span data-ttu-id="9581f-132">因為傳輸資料流程可以包含多個程式，所以必須有方法將各種 PE 封包與它們所屬的程式產生關聯。</span><span class="sxs-lookup"><span data-stu-id="9581f-132">Because a transport stream can carry multiple programs, there must be a way to associate the various PES packets with the programs they belong to.</span></span> <span data-ttu-id="9581f-133">這是使用可識別程式資料流程的資料表來完成的。</span><span class="sxs-lookup"><span data-stu-id="9581f-133">This is accomplished using tables that identify the program streams.</span></span> <span data-ttu-id="9581f-134">這項資料統稱為程式特定資訊 (PSI) 。</span><span class="sxs-lookup"><span data-stu-id="9581f-134">Collectively, this data is called Program Specific Information (PSI).</span></span> <span data-ttu-id="9581f-135">PSI 資料會隨附于 TS 封包，就像 PE 資料一樣。</span><span class="sxs-lookup"><span data-stu-id="9581f-135">The PSI data is carried in TS packets, just like the PES data.</span></span> <span data-ttu-id="9581f-136">有各種類型的 PSI 資料，包括：</span><span class="sxs-lookup"><span data-stu-id="9581f-136">There are various types of PSI data, including:</span></span>

-   <span data-ttu-id="9581f-137">程式關聯資料表 (PAT) 。</span><span class="sxs-lookup"><span data-stu-id="9581f-137">Program Association Table (PAT).</span></span> <span data-ttu-id="9581f-138">PAT 一律會指派給 PID 0x000。</span><span class="sxs-lookup"><span data-stu-id="9581f-138">The PAT is always assigned to PID 0x000.</span></span> <span data-ttu-id="9581f-139">PAT 中的每個專案都是用來識別該程式之 PMT 封包的 PID (請參閱下一個專案) 。</span><span class="sxs-lookup"><span data-stu-id="9581f-139">Each entry in the PAT is a PID that identifies the PMT packets for that program (see next item).</span></span>
-   <span data-ttu-id="9581f-140">程式對應表 (PMT) 。</span><span class="sxs-lookup"><span data-stu-id="9581f-140">Program Map Table (PMT).</span></span> <span data-ttu-id="9581f-141">每個 PMT 都會定義一個程式。</span><span class="sxs-lookup"><span data-stu-id="9581f-141">Each PMT defines one program.</span></span> <span data-ttu-id="9581f-142">PMT 包含資料流程清單;每個資料表專案都會提供該資料流程的 PID，以及可識別資料流程類型的程式碼。</span><span class="sxs-lookup"><span data-stu-id="9581f-142">The PMT contains a list of streams; each table entry gives the PID for that stream, plus a code that identifies the stream type.</span></span> <span data-ttu-id="9581f-143">ISO/IEC 13818-1 定義一些標準串流類型;下表顯示縮寫清單。</span><span class="sxs-lookup"><span data-stu-id="9581f-143">ISO/IEC 13818-1 defines some standard stream types; an abbreviated list is shown in the following table.</span></span>

    | <span data-ttu-id="9581f-144">資料流程 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="9581f-144">stream\_type</span></span> | <span data-ttu-id="9581f-145">Description</span><span class="sxs-lookup"><span data-stu-id="9581f-145">Description</span></span>  |
    |--------------|--------------|
    | <span data-ttu-id="9581f-146">0x01</span><span class="sxs-lookup"><span data-stu-id="9581f-146">0x01</span></span>         | <span data-ttu-id="9581f-147">MPEG-2 影片</span><span class="sxs-lookup"><span data-stu-id="9581f-147">MPEG-1 video</span></span> |
    | <span data-ttu-id="9581f-148">0x02</span><span class="sxs-lookup"><span data-stu-id="9581f-148">0x02</span></span>         | <span data-ttu-id="9581f-149">MPEG-2 影片</span><span class="sxs-lookup"><span data-stu-id="9581f-149">MPEG-2 video</span></span> |
    | <span data-ttu-id="9581f-150">0x03</span><span class="sxs-lookup"><span data-stu-id="9581f-150">0x03</span></span>         | <span data-ttu-id="9581f-151">MPEG-2 音訊</span><span class="sxs-lookup"><span data-stu-id="9581f-151">MPEG-1 audio</span></span> |
    | <span data-ttu-id="9581f-152">0x04</span><span class="sxs-lookup"><span data-stu-id="9581f-152">0x04</span></span>         | <span data-ttu-id="9581f-153">MPEG-2 音訊</span><span class="sxs-lookup"><span data-stu-id="9581f-153">MPEG-2 audio</span></span> |
    | <span data-ttu-id="9581f-154">0x80-0xFF</span><span class="sxs-lookup"><span data-stu-id="9581f-154">0x80 - 0xFF</span></span>  | <span data-ttu-id="9581f-155">使用者私用</span><span class="sxs-lookup"><span data-stu-id="9581f-155">User private</span></span> |

    

     

    <span data-ttu-id="9581f-156">以 MPEG-2 為基礎的其他標準（例如 ATSC）可能會在「使用者私用」範圍中定義其他串流類型。</span><span class="sxs-lookup"><span data-stu-id="9581f-156">Other standards that are based on MPEG-2, such as ATSC, may define additional stream types in the "user private" range.</span></span> <span data-ttu-id="9581f-157">例如，ATSC 將0x81 定義為杜比 AC-3 音訊。</span><span class="sxs-lookup"><span data-stu-id="9581f-157">For example, ATSC defines 0x81 as Dolby AC-3 audio.</span></span>

-   <span data-ttu-id="9581f-158">條件式存取資料表 (貓) </span><span class="sxs-lookup"><span data-stu-id="9581f-158">Conditional Access Tables (CAT)</span></span>
-   <span data-ttu-id="9581f-159">網路識別表 (NIT) </span><span class="sxs-lookup"><span data-stu-id="9581f-159">Network Identification Tables (NIT)</span></span>

## <a name="related-topics"></a><span data-ttu-id="9581f-160">相關主題</span><span class="sxs-lookup"><span data-stu-id="9581f-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9581f-161">DirectShow 中的 MPEG 2 支援</span><span class="sxs-lookup"><span data-stu-id="9581f-161">MPEG-2 Support in DirectShow</span></span>](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



