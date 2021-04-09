---
title: 使用輸出
description: 使用輸出
ms.assetid: e2e14e88-dddc-496d-8087-1455da0821e3
keywords:
- Windows Media Format SDK，使用輸出
- Advanced Systems Format (ASF) ，使用輸出
- ASF (Advanced Systems Format) ，使用輸出
- Advanced Systems Format (ASF) 、output 數位和格式
- ASF (Advanced Systems Format) 、output 數位和格式
- 輸出數位和格式，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d089a645838a295e07eb740927d75238473cc4f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681398"
---
# <a name="working-with-outputs"></a><span data-ttu-id="719b2-109">使用輸出</span><span class="sxs-lookup"><span data-stu-id="719b2-109">Working with Outputs</span></span>

<span data-ttu-id="719b2-110">根據預設，您從任一個 reader 物件收到的每個範例都會與一個輸出編號相關聯。</span><span class="sxs-lookup"><span data-stu-id="719b2-110">As a default, every sample you receive from either reader object is associated with an output number.</span></span> <span data-ttu-id="719b2-111">每個輸出編號都會對應到 ASF 檔案中的資料流程。</span><span class="sxs-lookup"><span data-stu-id="719b2-111">Each output number corresponds to a stream in the ASF file.</span></span> <span data-ttu-id="719b2-112">當檔案開啟時，讀取器會將輸出編號指派給檔案中的資料流程。</span><span class="sxs-lookup"><span data-stu-id="719b2-112">The reader assigns output numbers to the streams in the file when the file is opened.</span></span> <span data-ttu-id="719b2-113">一般來說，檔案中的每個資料流程都會有一個輸出。</span><span class="sxs-lookup"><span data-stu-id="719b2-113">Normally there is one output for each stream in a file.</span></span> <span data-ttu-id="719b2-114">但是，如果檔案使用相互排除，則會為每個互斥資料流程群組指派一個輸出編號。</span><span class="sxs-lookup"><span data-stu-id="719b2-114">If the file uses mutual exclusion, however, each group of mutually exclusive streams is assigned a single output number.</span></span> <span data-ttu-id="719b2-115">對應至互斥資料流程輸出數目的資料流程是由讀取器所決定，在多個位速率 (MBR) 檔，或您的應用程式中，如果您使用手動資料流程選取專案的話。</span><span class="sxs-lookup"><span data-stu-id="719b2-115">The stream that corresponds to the output number of the mutually exclusive streams is determined either by the reader, in the case of multiple bit rate (MBR) files, or by your application, if you are using manual stream selection.</span></span>

<span data-ttu-id="719b2-116">因為設定檔中設定的連接名稱不會保存在檔案中，所以讀取器會為每個輸出建立預設的連接名稱，而這只是輸出數位的字串表示，例如 "1"、"2"、"3" 等等。</span><span class="sxs-lookup"><span data-stu-id="719b2-116">Because the connection name set in the profile is not persisted in the file, the reader creates a default connection name for each output that is simply a string representation of the output number, for example "1", "2", "3" and so on.</span></span> <span data-ttu-id="719b2-117">連接名稱可讓應用程式和讀取器本身將輸出與資料流程產生相互關聯。</span><span class="sxs-lookup"><span data-stu-id="719b2-117">The connection names enable applications, and the reader itself, to correlate outputs to streams.</span></span> <span data-ttu-id="719b2-118">在多位元率檔案中，有數個串流共用一個連接名稱。</span><span class="sxs-lookup"><span data-stu-id="719b2-118">In a multiple bit rate file, several streams share a connection name.</span></span> <span data-ttu-id="719b2-119">這對讀取器並不重要，因為每個 MBR 資料流程的輸出屬性都相同。</span><span class="sxs-lookup"><span data-stu-id="719b2-119">This does not matter to the reader, because the output properties for each MBR stream are identical.</span></span>

<span data-ttu-id="719b2-120">每個輸出都有一或多個支援的輸出格式。</span><span class="sxs-lookup"><span data-stu-id="719b2-120">Each output has one or more supported output formats.</span></span> <span data-ttu-id="719b2-121">輸出格式是由讀取器所提供的未壓縮範例所使用的格式。</span><span class="sxs-lookup"><span data-stu-id="719b2-121">An output format is the format that the uncompressed samples delivered by the reader use.</span></span> <span data-ttu-id="719b2-122">當讀取器開啟檔案時，它會將每個輸出的格式設定為媒體子類型的預設值。</span><span class="sxs-lookup"><span data-stu-id="719b2-122">When the reader opens a file, it sets the format of each output to the default for the media subtype.</span></span> <span data-ttu-id="719b2-123">支援的輸出格式數目和類型是由解壓縮媒體資料的編解碼器所決定。</span><span class="sxs-lookup"><span data-stu-id="719b2-123">The number and type of output formats supported is determined by the codec that decompresses the media data.</span></span>

<span data-ttu-id="719b2-124">下列主題說明如何使用輸出：</span><span class="sxs-lookup"><span data-stu-id="719b2-124">The following topics explain how to work with outputs:</span></span>

-   [<span data-ttu-id="719b2-125">識別輸出編號</span><span class="sxs-lookup"><span data-stu-id="719b2-125">To Identify Output Numbers</span></span>](to-identify-output-numbers.md)
-   [<span data-ttu-id="719b2-126">指派輸出格式</span><span class="sxs-lookup"><span data-stu-id="719b2-126">Assigning Output Formats</span></span>](assigning-output-formats.md)

## <a name="related-topics"></a><span data-ttu-id="719b2-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="719b2-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="719b2-128">**IWMReader 介面**</span><span class="sxs-lookup"><span data-stu-id="719b2-128">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="719b2-129">**IWMSyncReader 介面**</span><span class="sxs-lookup"><span data-stu-id="719b2-129">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="719b2-130">**讀取 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="719b2-130">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




