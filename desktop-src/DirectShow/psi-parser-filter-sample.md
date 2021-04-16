---
description: PSI 剖析器篩選範例
ms.assetid: e815d57f-25e5-4a71-8f40-e7abec0db236
title: PSI 剖析器篩選範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1099375d2dbabf9ee6c8e891b0a1780bebbb599d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104571397"
---
# <a name="psi-parser-filter-sample"></a><span data-ttu-id="e5190-103">PSI 剖析器篩選範例</span><span class="sxs-lookup"><span data-stu-id="e5190-103">PSI Parser Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="e5190-104">Description</span><span class="sxs-lookup"><span data-stu-id="e5190-104">Description</span></span>

<span data-ttu-id="e5190-105">PSI 剖析器篩選器會接收從 MPEG-2 傳輸串流 (PSI) 的程式特定資訊，並從程式關聯資料表中解壓縮程式資訊 (PAT) 和程式對應表 (PMT) 。</span><span class="sxs-lookup"><span data-stu-id="e5190-105">The PSI Parser filter receives Program Specific Information (PSI) from an MPEG-2 transport stream and extracts program information from the Program Association Table (PAT) and Program Map Tables (PMT).</span></span> <span data-ttu-id="e5190-106">此資訊可讓應用程式設定 MPEG-2 信號信號。</span><span class="sxs-lookup"><span data-stu-id="e5190-106">This information enables an application to configure the MPEG-2 Demultiplexer.</span></span> <span data-ttu-id="e5190-107">篩選準則支援自訂介面 [**IMpeg2PsiParser**](impeg2psiparser.md)，可用於抓取 PSI 資訊。</span><span class="sxs-lookup"><span data-stu-id="e5190-107">The filter supports a custom interface, [**IMpeg2PsiParser**](impeg2psiparser.md), for retrieving the PSI information.</span></span>

<span data-ttu-id="e5190-108">此篩選器是針對 MPEG-2 裝置所設計，例如 IEEE 1394 MPEG 攝影機和 D VHS 裝置。</span><span class="sxs-lookup"><span data-stu-id="e5190-108">This filter is designed for MPEG-2 devices, such as IEEE 1394 MPEG-2 camcorders and D-VHS devices.</span></span> <span data-ttu-id="e5190-109">如需詳細資訊，請參閱 [MSTape 驅動程式](mstape-driver.md) 。</span><span class="sxs-lookup"><span data-stu-id="e5190-109">See [MSTape Driver](mstape-driver.md) for more information.</span></span> <span data-ttu-id="e5190-110">數位電視廣播來源應該使用 .TIF 篩選器來取得程式資訊。</span><span class="sxs-lookup"><span data-stu-id="e5190-110">Digital television broadcast sources should use a TIF filter to get program information.</span></span>

## <a name="usage"></a><span data-ttu-id="e5190-111">使用方式</span><span class="sxs-lookup"><span data-stu-id="e5190-111">Usage</span></span>

<span data-ttu-id="e5190-112">您可以在 GraphEdit 中測試 PSI 剖析器篩選器，如下所示：</span><span class="sxs-lookup"><span data-stu-id="e5190-112">You can test the PSI Parser filter in GraphEdit as follows:</span></span>

1.  <span data-ttu-id="e5190-113">啟動 GraphEdit。</span><span class="sxs-lookup"><span data-stu-id="e5190-113">Launch GraphEdit.</span></span>
2.  <span data-ttu-id="e5190-114">插入 MPEG 2 傳輸來源。</span><span class="sxs-lookup"><span data-stu-id="e5190-114">Insert an MPEG-2 transport source.</span></span> <span data-ttu-id="e5190-115">MPEG-2 攝影機和 D VHS 裝置在影片捕獲來源類別中會顯示為「Microsoft AV/C 磁帶次級裝置」。</span><span class="sxs-lookup"><span data-stu-id="e5190-115">MPEG-2 camcorders and D-VHS devices appear as "Microsoft AV/C Tape Subunit Device" in the Video Capture Sources category.</span></span>
3.  <span data-ttu-id="e5190-116">將來源篩選連接至 MPEG-2 信號篩選器。</span><span class="sxs-lookup"><span data-stu-id="e5190-116">Connect the source filter to the MPEG-2 Demultiplexer filter.</span></span>
4.  <span data-ttu-id="e5190-117">使用 demux 上的屬性頁面，建立具有 "MPEG-2 PSI" 媒體類型的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="e5190-117">Use the property page on the demux to create an output pin with an "MPEG-2 PSI" media type.</span></span> <span data-ttu-id="e5190-118">此 pin 會提供 PAT 和 PMT 區段。</span><span class="sxs-lookup"><span data-stu-id="e5190-118">This pin will deliver the PAT and PMT sections.</span></span>
5.  <span data-ttu-id="e5190-119">使用 [demux] 屬性頁可將 PID 0x00 對應到輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="e5190-119">Use the demux property page to map PID 0x00 to the output pin.</span></span> <span data-ttu-id="e5190-120">將內容類型設定為 [MPEG2 PSI 區段]。</span><span class="sxs-lookup"><span data-stu-id="e5190-120">Set the content type to "MPEG2 PSI Sections".</span></span>
6.  <span data-ttu-id="e5190-121">將 demux 輸出圖釘連接到 PSI 剖析器，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="e5190-121">Connect the demux output pin to PSI Parser, as shown in the following diagram.</span></span>

    ![psi 剖析器篩選圖形](images/psi-parser.png)

7.  <span data-ttu-id="e5190-123">執行圖形，以便將 PSI 資料摘要至 PSI 剖析器篩選器。</span><span class="sxs-lookup"><span data-stu-id="e5190-123">Run the graph, in order to feed PSI data to the PSI Parser filter.</span></span> <span data-ttu-id="e5190-124">當篩選器對 PAT 區段進行解碼時，它會自動將 PMT Pid 對應到 demux 上的相同輸出釘選，以便接收到 PMT 區段。</span><span class="sxs-lookup"><span data-stu-id="e5190-124">As the filter decodes the PAT sections, it automatically maps the PMT PIDs to the same output pin on the demux, so that it receives the PMT sections.</span></span>
8.  <span data-ttu-id="e5190-125">使用 [PSI 剖析器] 屬性頁選取程式編號。</span><span class="sxs-lookup"><span data-stu-id="e5190-125">Use the PSI Parser property page to select a program number.</span></span> <span data-ttu-id="e5190-126">[屬性] 頁面中的 [基本資料流程] 清單會顯示與所選程式中的每個基本資料流程相關聯的 PID 和資料流程類型。</span><span class="sxs-lookup"><span data-stu-id="e5190-126">The elementary stream list in the property page will show the PID and stream type associated with each elementary stream in the selected program.</span></span> <span data-ttu-id="e5190-127">屬性頁的設計目的是要辨識 ISO/IEC 13818-1 中定義的資料流程類型。</span><span class="sxs-lookup"><span data-stu-id="e5190-127">The property page is designed to recognize stream types defined in ISO/IEC 13818-1.</span></span>
9.  <span data-ttu-id="e5190-128">在 [ **音訊 pid** ] 編輯方塊中輸入音訊 pid 號碼，並在 [ **影片 pid** ] 編輯方塊中輸入影片 pid 號碼。</span><span class="sxs-lookup"><span data-stu-id="e5190-128">Enter the audio PID number in the **Audio PID** edit box, and the video PID number in the **Video PID** edit box.</span></span>
10. <span data-ttu-id="e5190-129">按一下 [ **視圖程式** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="e5190-129">Click the **View Program** button.</span></span> <span data-ttu-id="e5190-130">PSI 剖析器會在 demux 上設定輸出針腳，以符合程式串流資訊和轉譯釘選。</span><span class="sxs-lookup"><span data-stu-id="e5190-130">The PSI Parser will configure the output pins on the demux to match the program stream information and render the pins.</span></span>

> [!Note]  
> <span data-ttu-id="e5190-131">您可以利用 [PSI 剖析器] 屬性頁讓測試變得更容易，並提供可設定 MPEG-2 信號的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="e5190-131">The PSI Parser property page is provided to make testing easier, and to provide sample code that configures the MPEG-2 Demultiplexer.</span></span> <span data-ttu-id="e5190-132">不建議應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="e5190-132">It is not recommended for applications to use.</span></span> <span data-ttu-id="e5190-133">應用程式應該以程式設計的方式設定 demux。</span><span class="sxs-lookup"><span data-stu-id="e5190-133">Applications should configure the demux programmatically.</span></span>

 

<span data-ttu-id="e5190-134">若要在應用程式中使用 PSI 剖析器篩選器，請先從 MPEG-2 來源建立篩選圖形至 MPEG-2 demux。</span><span class="sxs-lookup"><span data-stu-id="e5190-134">To use the PSI Parser filter in an application, start by building the filter graph from the MPEG-2 source to the MPEG-2 demux.</span></span> <span data-ttu-id="e5190-135">此步驟的程式碼不會顯示在此處，因為確切的圖表設定將取決於來源。</span><span class="sxs-lookup"><span data-stu-id="e5190-135">Code for this step is not shown here, because the exact graph configuration will depend on the source.</span></span>

<span data-ttu-id="e5190-136">接下來，在 demux 上建立 PSI 資料的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="e5190-136">Next, create an output pin on the demux for the PSI data.</span></span> <span data-ttu-id="e5190-137">將 PID 0x00 （保留給 PAT 區段）對應至此 pin，如下列程式碼所示：</span><span class="sxs-lookup"><span data-stu-id="e5190-137">Map PID 0x00, which is reserved for PAT sections, to this pin, as shown in the following code:</span></span>


```C++
// Set the media type to MPEG-2 table sections.
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = KSDATAFORMAT_TYPE_MPEG2_SECTIONS;

// Create the pin.
IPin *pPsiPin;
hr = pDemux->CreateOutputPin(&mt, L"PSI", &pPsiPin);
if (SUCCEEDED(hr))
{
    // Map to PID 0.
    ULONG Pid = 0x00;
    hr = pPid->MapPID(1, &Pid, MEDIA_MPEG2_PSI);
}
```



<span data-ttu-id="e5190-138">如需詳細資訊，請參閱 [使用 Mpeg-2 信號](using-the-mpeg-2-demultiplexer.md)。</span><span class="sxs-lookup"><span data-stu-id="e5190-138">For more information, see [Using the MPEG-2 Demultiplexer](using-the-mpeg-2-demultiplexer.md).</span></span>

<span data-ttu-id="e5190-139">將 PSI 剖析器篩選器新增至圖形，並將它連接到 demux 上的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="e5190-139">Add the PSI Parser filter to the graph and connect it to the output pin on the demux.</span></span> <span data-ttu-id="e5190-140">查詢 [**IMpeg2PsiParser**](impeg2psiparser.md) 介面的 PSI 剖析器。</span><span class="sxs-lookup"><span data-stu-id="e5190-140">Query the PSI Parser for the [**IMpeg2PsiParser**](impeg2psiparser.md) interface.</span></span> <span data-ttu-id="e5190-141">現在，執行圖形並等候 EC \_ 程式 \_ 變更事件，以表示新的 PAT 或 PMT 區段。</span><span class="sxs-lookup"><span data-stu-id="e5190-141">Now run the graph and wait for EC\_PROGRAM\_CHANGED events, which signal a new PAT or PMT section.</span></span> <span data-ttu-id="e5190-142">此事件是由 PSI 剖析器篩選準則所定義的自訂事件。</span><span class="sxs-lookup"><span data-stu-id="e5190-142">This event is a custom event defined by the PSI Parser filter.</span></span> <span data-ttu-id="e5190-143">當您收到 EC \_ 程式 \_ 已變更事件時，您可以藉由呼叫 **IMpeg2PsiParser** 方法來取得可用的 PSI 資訊。</span><span class="sxs-lookup"><span data-stu-id="e5190-143">When you receive an EC\_PROGRAM\_CHANGED event, you can get the available PSI information by calling **IMpeg2PsiParser** methods.</span></span> <span data-ttu-id="e5190-144">本節將說明您最常需要的方法。</span><span class="sxs-lookup"><span data-stu-id="e5190-144">This section describes the methods you will need most often.</span></span>

<span data-ttu-id="e5190-145">若要取得程式的數目，請使用 [**IMpeg2PsiParser：： GetCountOfPrograms**](impeg2psiparser-getcountofprograms.md) 方法：</span><span class="sxs-lookup"><span data-stu-id="e5190-145">To get the number of programs, use the [**IMpeg2PsiParser::GetCountOfPrograms**](impeg2psiparser-getcountofprograms.md) method:</span></span>


```C++
int NumProgs = 0;
hr = pPsi->GetCountOfPrograms(&NumProgs);
```



<span data-ttu-id="e5190-146">若要取得特定程式的程式編號，請使用 [**IMpeg2PsiParser：： GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md) 方法：</span><span class="sxs-lookup"><span data-stu-id="e5190-146">To get the program number for a specific program, use the [**IMpeg2PsiParser::GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md) method:</span></span>


```C++
WORD ProgNum = 0;
for (int i = 0; i < NumProgs; i++)
{
    hr = pPsi->GetRecordProgramNumber(i, &ProgNum);
    ...
}
```



<span data-ttu-id="e5190-147">程式編號可用來取得個別程式的 PMT 專案。</span><span class="sxs-lookup"><span data-stu-id="e5190-147">The program number is used to obtain the PMT entries for individual programs.</span></span> <span data-ttu-id="e5190-148">若要取得程式中的基本資料流程數目，請使用 [**GetCountOfElementaryStreams**](impeg2psiparser-getcountofelementarystreams.md) 方法：</span><span class="sxs-lookup"><span data-stu-id="e5190-148">To get the number of elementary streams in a program, use the [**GetCountOfElementaryStreams**](impeg2psiparser-getcountofelementarystreams.md) method:</span></span>


```C++
WORD cElemStreams = 0;
hr = pPsi->GetCountOfElementaryStreams(ProgNum, &cElemStreams);
```



<span data-ttu-id="e5190-149">針對每個基本資料流程， [**IMpeg2PsiParser：： GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85)) 方法會傳回 PID，而 [**IMpeg2PsiParser：： GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85)) 方法會傳回資料流程類型：</span><span class="sxs-lookup"><span data-stu-id="e5190-149">For each elementary stream, the [**IMpeg2PsiParser::GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85)) method returns the PID, and the [**IMpeg2PsiParser::GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85)) method returns the stream type:</span></span>


```C++
BYTE ESType = 0;
WORD ESPid = 0;
for (WORD j = 0; j < cElemStreams; j++)
{
    hr = pPsi->GetRecordElementaryPid(ProgNum, j, &ESPid);
    hr = pPsi->GetRecordStreamType(ProgNum, j, &ESType);
}
```



<span data-ttu-id="e5190-150">PID 和 stream 型別可讓您設定新的輸出針腳（以 MPEG-2 信號的輸出）。</span><span class="sxs-lookup"><span data-stu-id="e5190-150">The PID and the stream type enable you to configure new output pins on the MPEG-2 Demultiplexer.</span></span> <span data-ttu-id="e5190-151">這可能需要對原始來源有所瞭解。</span><span class="sxs-lookup"><span data-stu-id="e5190-151">This may require some knowledge of the original source.</span></span> <span data-ttu-id="e5190-152">例如，ISO/IEC 13818-1 會將0x80 到0xFF 的資料流程類型定義為「使用者私用」，但以 MPEG-2 為基礎的其他標準可能會將其他意義指派給這些類型。</span><span class="sxs-lookup"><span data-stu-id="e5190-152">For example, ISO/IEC 13818-1 defines stream types 0x80 through 0xFF as "user private," but other standards that are based on MPEG-2 may assign other meanings to these types.</span></span>

<span data-ttu-id="e5190-153">當圖形正在執行時，MPEG-2 信號信號可以建立新的 pin 和新的 PID 對應，但您必須停止圖形來連接釘選。</span><span class="sxs-lookup"><span data-stu-id="e5190-153">The MPEG-2 Demultiplexer can create new pins and new PID mappings while the graph is running, but you must stop the graph to connect pins.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="e5190-154">下載範例</span><span class="sxs-lookup"><span data-stu-id="e5190-154">Downloading the Sample</span></span>

<span data-ttu-id="e5190-155">若要下載 DirectShow SDK 範例，請安裝最新版本的 [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="e5190-155">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="e5190-156">此範例安裝在下列路徑下： *\[ SDK \] 根* \\ 範例 \\ 多媒體 \\ DirectShow \\ 篩選 \\ PSIParser。</span><span class="sxs-lookup"><span data-stu-id="e5190-156">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\PSIParser.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5190-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="e5190-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5190-158">DirectShow 範例</span><span class="sxs-lookup"><span data-stu-id="e5190-158">DirectShow Samples</span></span>](directshow-samples.md)
</dt> <dt>

[<span data-ttu-id="e5190-159">**IMpeg2PsiParser 介面**</span><span class="sxs-lookup"><span data-stu-id="e5190-159">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> </dl>

 

 
