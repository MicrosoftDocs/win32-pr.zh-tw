---
description: 編碼是指將數位媒體從一種格式轉換成另一種格式的程式。 例如，將 MP3 音訊轉換成 Advanced Systems 格式所定義的 Windows Media 音訊格式 (ASF) 規格。
ms.assetid: 4fe202d8-c8f5-4e9a-ad40-1aea8f767362
title: 教學課程： 1-傳遞 Windows Media 編碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d670b107f315966a048a2f847183431f9a57bd4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103696262"
---
# <a name="tutorial-1-pass-windows-media-encoding"></a><span data-ttu-id="cbe10-104">教學課程： 1-傳遞 Windows Media 編碼</span><span class="sxs-lookup"><span data-stu-id="cbe10-104">Tutorial: 1-Pass Windows Media Encoding</span></span>

<span data-ttu-id="cbe10-105">編碼是指將數位媒體從一種格式轉換成另一種格式的程式。</span><span class="sxs-lookup"><span data-stu-id="cbe10-105">Encoding refers to the process of converting digital media from one format into another.</span></span> <span data-ttu-id="cbe10-106">例如，將 MP3 音訊轉換成 Advanced Systems 格式所定義的 Windows Media 音訊格式 (ASF) 規格。</span><span class="sxs-lookup"><span data-stu-id="cbe10-106">For example, converting MP3 audio into Windows Media Audio format as defined by the Advanced Systems Format (ASF) specification.</span></span>

<span data-ttu-id="cbe10-107">**注意**  ASF 規格會定義輸出檔的容器類型 ( .wma 或 .wmv) 可包含任何格式、壓縮或未壓縮的媒體資料。</span><span class="sxs-lookup"><span data-stu-id="cbe10-107">**Note**  The ASF specification defines a container type for the output file (.wma or .wmv) that can contain media data in any format, compressed or uncompressed.</span></span> <span data-ttu-id="cbe10-108">例如，一個 ASF 容器（例如 .wma 檔）可以包含 MP3 格式的媒體資料。</span><span class="sxs-lookup"><span data-stu-id="cbe10-108">For example, an ASF container such as a .wma file can contain media data in MP3 format.</span></span> <span data-ttu-id="cbe10-109">編碼程式會轉換檔案中包含的實際資料格式。</span><span class="sxs-lookup"><span data-stu-id="cbe10-109">The encoding process converts the actual format of the data contained within the file.</span></span>

<span data-ttu-id="cbe10-110">本教學課程示範如何將純 (的非 DRM 保護) 輸入來源編碼為 Windows Media 內容，並將資料寫入新的 ASF 檔案 ( \* 使用管線層級 ASF 元件) wm。</span><span class="sxs-lookup"><span data-stu-id="cbe10-110">This tutorial demonstrates encoding clear content (non DRM-protected) input source into Windows Media content and writing the data in a new ASF file (.wm\*) by using Pipeline Layer ASF Components.</span></span> <span data-ttu-id="cbe10-111">這些元件將用來建立部分編碼拓撲，這會由媒體會話的實例控制。</span><span class="sxs-lookup"><span data-stu-id="cbe10-111">These components will be used to build a partial encoding topology, which will be controlled by an instance of the Media Session.</span></span>

<span data-ttu-id="cbe10-112">在本教學課程中，您將建立主控台應用程式，該應用程式會採用輸入和輸出檔案名，並使用編碼模式作為引數。</span><span class="sxs-lookup"><span data-stu-id="cbe10-112">In this tutorial, you will create a console application that takes the input and output filenames, and the encoding mode as arguments.</span></span> <span data-ttu-id="cbe10-113">輸入檔案可以是壓縮或未壓縮的媒體格式。</span><span class="sxs-lookup"><span data-stu-id="cbe10-113">The input file can be in a compressed or an uncompressed media format.</span></span> <span data-ttu-id="cbe10-114">有效的編碼模式為 "CBR" (常數位元速率) 或 "VBR" (變數位元速率) 。</span><span class="sxs-lookup"><span data-stu-id="cbe10-114">The valid encoding modes are "CBR" (constant bit rate) or "VBR" (variable bit rate).</span></span> <span data-ttu-id="cbe10-115">應用程式會建立媒體來源以代表輸入檔案名所指定的來源，以及使用 ASF 檔案接收，將原始程式檔的編碼內容封存到 ASF 檔案中。</span><span class="sxs-lookup"><span data-stu-id="cbe10-115">The application creates a media source to represent the source specified by the input filename, and the ASF file sink to archive the encoded contents of source file into an ASF file.</span></span> <span data-ttu-id="cbe10-116">為了讓案例更容易執行，輸出檔只會有一個音訊串流和一個影片串流。</span><span class="sxs-lookup"><span data-stu-id="cbe10-116">To keep the scenario simple to implement, the output file will have only one audio stream and one video stream.</span></span> <span data-ttu-id="cbe10-117">應用程式會插入適用于音訊串流格式轉換的 Windows Media 音訊 9.1 Professional 編解碼器，以及適用于影片串流的 Windows Media 視訊9編解碼器。</span><span class="sxs-lookup"><span data-stu-id="cbe10-117">The application inserts the Windows Media Audio 9.1 Professional codec for the audio stream format conversion and Windows Media Video 9 codec for the video stream.</span></span>

<span data-ttu-id="cbe10-118">針對常數的位元速率編碼，編碼會話開始之前，編碼器必須知道它必須達到的目標位元速率。</span><span class="sxs-lookup"><span data-stu-id="cbe10-118">For constant bit rate encoding, before the encoding session begins, the encoder must know the target bit rate that it must achieve.</span></span> <span data-ttu-id="cbe10-119">在本教學課程中，針對「CBR」模式，應用程式會使用在媒體類型協商期間從編碼器抓取的第一個輸出媒體類型所提供的位元速率，以做為目標位元速率。</span><span class="sxs-lookup"><span data-stu-id="cbe10-119">In this tutorial, for "CBR" mode, the application uses the bit rate available with the first output media type that is retrieved from the encoder during media type negotiation as the target bit rate.</span></span> <span data-ttu-id="cbe10-120">針對變數位元速率編碼，本教學課程會藉由設定品質等級來示範如何使用變數位元速率進行編碼。</span><span class="sxs-lookup"><span data-stu-id="cbe10-120">For variable bit rate encoding, this tutorial demonstrates encoding with variable bit rate by setting a quality level.</span></span> <span data-ttu-id="cbe10-121">音訊串流的編碼品質為98，而視頻串流的品質等級為95。</span><span class="sxs-lookup"><span data-stu-id="cbe10-121">The audio streams are encoded at the quality level of 98 and video streams at the quality level of 95.</span></span>

<span data-ttu-id="cbe10-122">下列程式摘要說明在 ASF 容器中使用1傳遞編碼模式來編碼 Windows Media 內容的步驟。</span><span class="sxs-lookup"><span data-stu-id="cbe10-122">The following procedure summarizes the steps for encoding Windows Media content in an ASF container by using a 1-pass encoding mode.</span></span>

1.  <span data-ttu-id="cbe10-123">使用來源解析程式建立所指定的媒體來源。</span><span class="sxs-lookup"><span data-stu-id="cbe10-123">Create a media source for the specified by using the source resolver.</span></span>
2.  <span data-ttu-id="cbe10-124">列舉媒體來源中的串流。</span><span class="sxs-lookup"><span data-stu-id="cbe10-124">Enumerate the streams in the media source.</span></span>
3.  <span data-ttu-id="cbe10-125">根據媒體來源中需要編碼的資料流程，建立 ASF 媒體接收器並新增資料流程接收器。</span><span class="sxs-lookup"><span data-stu-id="cbe10-125">Create the ASF media sink and add stream sinks depending on the streams in the media source that need to be encoded.</span></span>
4.  <span data-ttu-id="cbe10-126">使用必要的編碼屬性來設定媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="cbe10-126">Configure the media sink with the required encoding properties.</span></span>
5.  <span data-ttu-id="cbe10-127">在輸出檔中建立資料流程的 Windows Media 編碼器。</span><span class="sxs-lookup"><span data-stu-id="cbe10-127">Create the Windows Media encoders for the streams in the output file.</span></span>
6.  <span data-ttu-id="cbe10-128">使用在媒體接收上設定的屬性來設定編碼器。</span><span class="sxs-lookup"><span data-stu-id="cbe10-128">Configure the encoders with the properties that are set on the media sink.</span></span>
7.  <span data-ttu-id="cbe10-129">建立部分編碼拓撲。</span><span class="sxs-lookup"><span data-stu-id="cbe10-129">Build a partial encoding topology.</span></span>
8.  <span data-ttu-id="cbe10-130">將媒體會話具現化，並在媒體會話上設定拓撲。</span><span class="sxs-lookup"><span data-stu-id="cbe10-130">Instantiate the Media Session and set the topology on the Media Session.</span></span>
9.  <span data-ttu-id="cbe10-131">藉由控制媒體會話並從媒體會話取得所有相關事件，來啟動編碼會話。</span><span class="sxs-lookup"><span data-stu-id="cbe10-131">Start the encoding session by controlling the Media Session and getting all the relevant events from the Media Session.</span></span>
10. <span data-ttu-id="cbe10-132">針對 VBR 編碼，從編碼器取得編碼屬性值，並在媒體接收器上進行設定。</span><span class="sxs-lookup"><span data-stu-id="cbe10-132">For VBR encoding, get the encoding property values from the encoder and set them on the media sink.</span></span>
11. <span data-ttu-id="cbe10-133">關閉並關閉編碼會話。</span><span class="sxs-lookup"><span data-stu-id="cbe10-133">Close and shutdown the encoding session.</span></span>

<span data-ttu-id="cbe10-134">本教學課程包含下列各節：</span><span class="sxs-lookup"><span data-stu-id="cbe10-134">This tutorial contains the following sections:</span></span>

-   [<span data-ttu-id="cbe10-135">先決條件</span><span class="sxs-lookup"><span data-stu-id="cbe10-135">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="cbe10-136">設定專案</span><span class="sxs-lookup"><span data-stu-id="cbe10-136">Set up the Project</span></span>](#set-up-the-project)
-   [<span data-ttu-id="cbe10-137">建立媒體來源</span><span class="sxs-lookup"><span data-stu-id="cbe10-137">Create the Media Source</span></span>](#create-the-media-source)
-   [<span data-ttu-id="cbe10-138">建立 ASF File 接收器</span><span class="sxs-lookup"><span data-stu-id="cbe10-138">Create the ASF File Sink</span></span>](#create-the-asf-file-sink)
    -   [<span data-ttu-id="cbe10-139">建立 ASF 設定檔物件</span><span class="sxs-lookup"><span data-stu-id="cbe10-139">Create the ASF Profile Object</span></span>](#create-the-asf-profile-object)
    -   [<span data-ttu-id="cbe10-140">建立壓縮的音訊媒體類型</span><span class="sxs-lookup"><span data-stu-id="cbe10-140">Create a Compressed Audio Media Type</span></span>](#create-a-compressed-audio-media-type)
    -   [<span data-ttu-id="cbe10-141">建立壓縮的影片媒體類型</span><span class="sxs-lookup"><span data-stu-id="cbe10-141">Create a Compressed Video Media Type</span></span>](#create-a-compressed-video-media-type)
    -   [<span data-ttu-id="cbe10-142">建立 ASF ContentInfo 物件</span><span class="sxs-lookup"><span data-stu-id="cbe10-142">Create the ASF ContentInfo Object</span></span>](#create-the-asf-contentinfo-object)
    -   [<span data-ttu-id="cbe10-143">建立 ASF File 接收器</span><span class="sxs-lookup"><span data-stu-id="cbe10-143">Create the ASF File Sink</span></span>](#create-the-asf-file-sink)
-   [<span data-ttu-id="cbe10-144">建立部分編碼拓撲</span><span class="sxs-lookup"><span data-stu-id="cbe10-144">Build the Partial Encoding Topology</span></span>](#build-the-partial-encoding-topology)
    -   [<span data-ttu-id="cbe10-145">建立媒體來源的來源拓撲節點</span><span class="sxs-lookup"><span data-stu-id="cbe10-145">Create the Source Topology Node for the Media Source</span></span>](#create-the-source-topology-node-for-the-media-source)
    -   [<span data-ttu-id="cbe10-146">具現化所需的編碼器，並建立轉換節點</span><span class="sxs-lookup"><span data-stu-id="cbe10-146">Instantiate the Required Encoders and Create the Transform Nodes</span></span>](#instantiate-the-required-encoders-and-create-the-transform-nodes)
    -   [<span data-ttu-id="cbe10-147">建立檔案接收的輸出拓撲節點</span><span class="sxs-lookup"><span data-stu-id="cbe10-147">Create the Output Topology Nodes for the File Sink</span></span>](#create-the-output-topology-nodes-for-the-file-sink)
    -   [<span data-ttu-id="cbe10-148">連接來源、轉換和接收節點</span><span class="sxs-lookup"><span data-stu-id="cbe10-148">Connect the Source, Transform, and Sink Nodes</span></span>](#connect-the-source-transform-and-sink-nodes)
-   [<span data-ttu-id="cbe10-149">處理編碼會話</span><span class="sxs-lookup"><span data-stu-id="cbe10-149">Handling the Encoding Session</span></span>](#handling-the-encoding-session)
-   [<span data-ttu-id="cbe10-150">更新 File 接收器中的編碼屬性</span><span class="sxs-lookup"><span data-stu-id="cbe10-150">Update Encoding Properties in the File Sink</span></span>](#update-encoding-properties-in-the-file-sink)
-   [<span data-ttu-id="cbe10-151">執行 Main</span><span class="sxs-lookup"><span data-stu-id="cbe10-151">Implement Main</span></span>](#implement-main)
-   [<span data-ttu-id="cbe10-152">測試輸出檔案</span><span class="sxs-lookup"><span data-stu-id="cbe10-152">Test the Output File</span></span>](#test-the-output-file)
-   [<span data-ttu-id="cbe10-153">常見的錯誤碼和調試秘訣</span><span class="sxs-lookup"><span data-stu-id="cbe10-153">Common Error Codes and Debugging Tips</span></span>](#common-error-codes-and-debugging-tips)
-   [<span data-ttu-id="cbe10-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="cbe10-154">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="cbe10-155">必要條件</span><span class="sxs-lookup"><span data-stu-id="cbe10-155">Prerequisites</span></span>

<span data-ttu-id="cbe10-156">本教學課程假設您已句備下列條件：</span><span class="sxs-lookup"><span data-stu-id="cbe10-156">This tutorial assumes the following:</span></span>

-   <span data-ttu-id="cbe10-157">您已熟悉 Asf 檔案 [結構](asf-file-structure.md)，媒體基礎提供的 [管線層 ASF 元件](pipeline-layer-asf-components.md) ，可與 asf 物件搭配使用。</span><span class="sxs-lookup"><span data-stu-id="cbe10-157">You are familiar with the [ASF File Structure](asf-file-structure.md), the [Pipeline Layer ASF Components](pipeline-layer-asf-components.md) provided by Media Foundation to work with ASF Objects.</span></span> <span data-ttu-id="cbe10-158">這些元件包括下列物件：</span><span class="sxs-lookup"><span data-stu-id="cbe10-158">These components include the following objects:</span></span>
    -   [<span data-ttu-id="cbe10-159">媒體來源</span><span class="sxs-lookup"><span data-stu-id="cbe10-159">Media Sources</span></span>](media-sources.md)

        <span data-ttu-id="cbe10-160">**注意**  如果您正在執行 transrating (將較高的位元速率檔案轉換成較低的位元速率檔案，而不變更) 的格式，則會使用 [ASF 媒體來源](asf-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="cbe10-160">**Note**  If you are performing transrating (converting a higher bit-rate file to a lower bit-rate file without changing formats), you will use the [ASF Media Source](asf-media-source.md).</span></span>

    -   [<span data-ttu-id="cbe10-161">Windows Media 編碼器</span><span class="sxs-lookup"><span data-stu-id="cbe10-161">Windows Media Encoders</span></span>](windows-media-encoders.md)
    -   [<span data-ttu-id="cbe10-162">ASF 媒體接收</span><span class="sxs-lookup"><span data-stu-id="cbe10-162">ASF Media Sinks</span></span>](asf-media-sinks.md)
    -   [<span data-ttu-id="cbe10-163">ASF ContentInfo 物件</span><span class="sxs-lookup"><span data-stu-id="cbe10-163">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
    -   [<span data-ttu-id="cbe10-164">ASF 設定檔</span><span class="sxs-lookup"><span data-stu-id="cbe10-164">ASF Profile</span></span>](asf-profile.md)

-   <span data-ttu-id="cbe10-165">您已熟悉 Windows Media 編碼器，以及各種編碼類型，尤其是 [常數的位元速率編碼](constant-bit-rate-encoding.md) 和 [品質型變數位元速率編碼](quality-based-variable-bit-rate--vbr--encoding.md)。</span><span class="sxs-lookup"><span data-stu-id="cbe10-165">You are familiar with Windows Media encoders, and the various encoding types, particularly [Constant Bit Rate Encoding](constant-bit-rate-encoding.md) and [Quality-Based Variable Bit Rate Encoding](quality-based-variable-bit-rate--vbr--encoding.md).</span></span>
-   <span data-ttu-id="cbe10-166">您已熟悉編碼器 MFT 作業。</span><span class="sxs-lookup"><span data-stu-id="cbe10-166">You are familiar with encoder MFT operations.</span></span> <span data-ttu-id="cbe10-167">具體而言，就是建立編碼器的實例，並在編碼器上設定輸入和輸出類型。</span><span class="sxs-lookup"><span data-stu-id="cbe10-167">Specifically, creating an instance of the encoder and setting input and output types on the encoder.</span></span>
-   <span data-ttu-id="cbe10-168">您已熟悉拓撲物件，以及如何建立編碼拓撲。</span><span class="sxs-lookup"><span data-stu-id="cbe10-168">You are familiar with topology objects and how to build an encoding topology.</span></span> <span data-ttu-id="cbe10-169">如需拓撲與拓撲節點的詳細資訊，請參閱 [建立拓撲](creating-topologies.md)。</span><span class="sxs-lookup"><span data-stu-id="cbe10-169">For more information about topologies and topology nodes, see [Creating Topologies](creating-topologies.md).</span></span>
-   <span data-ttu-id="cbe10-170">您已熟悉 [媒體會話](media-session.md)的事件模型和流程式控制製作業。</span><span class="sxs-lookup"><span data-stu-id="cbe10-170">You are familiar with [Media Session](media-session.md)'s event model and the flow control operations.</span></span> <span data-ttu-id="cbe10-171">如需詳細資訊，請參閱 [媒體會話事件](media-session-events.md)。</span><span class="sxs-lookup"><span data-stu-id="cbe10-171">For information, see [Media Session Events](media-session-events.md).</span></span>

## <a name="set-up-the-project"></a><span data-ttu-id="cbe10-172">設定專案</span><span class="sxs-lookup"><span data-stu-id="cbe10-172">Set up the Project</span></span>

1.  <span data-ttu-id="cbe10-173">在原始程式檔中包含下列標頭：</span><span class="sxs-lookup"><span data-stu-id="cbe10-173">Include the following headers in your source file:</span></span>

    ```C++
    #include <new>
    #include <mfidl.h>            // Media Foundation interfaces
    #include <mfapi.h>            // Media Foundation platform APIs
    #include <mferror.h>        // Media Foundation error codes
    #include <wmcontainer.h>    // ASF-specific components
    #include <wmcodecdsp.h>        // Windows Media DSP interfaces
    #include <Dmo.h>            // DMO objects
    #include <uuids.h>            // Definition for FORMAT_VideoInfo
    #include <propvarutil.h>
    
    ```

    

2.  <span data-ttu-id="cbe10-174">連結至下列程式庫檔案：</span><span class="sxs-lookup"><span data-stu-id="cbe10-174">Link to the following library files:</span></span>

    ```C++
    // The required link libraries 
    #pragma comment(lib, "mfplat")
    #pragma comment(lib, "mf")
    #pragma comment(lib, "mfuuid")
    #pragma comment(lib, "msdmo")
    #pragma comment(lib, "strmiids")
    #pragma comment(lib, "propsys")
    
    ```

    

3.  <span data-ttu-id="cbe10-175">宣告 [SafeRelease](saferelease.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="cbe10-175">Declare the [SafeRelease](saferelease.md) function.</span></span>

    ```C++
    template <class T> void SafeRelease(T **ppT)
    {
        if (*ppT)
        {
            (*ppT)->Release();
            *ppT = NULL;
        }
    }
    ```

    

4.  <span data-ttu-id="cbe10-176">宣告編碼 \_ 模式列舉來定義 CBR 和 VBR 編碼類型。</span><span class="sxs-lookup"><span data-stu-id="cbe10-176">Declare the ENCODING\_MODE enumeration to define CBR and VBR encoding types.</span></span>

    ```C++
    // Encoding mode
    typedef enum ENCODING_MODE {
      NONE  = 0x00000000,
      CBR   = 0x00000001,
      VBR   = 0x00000002,
    } ;
    
    ```

    

5.  <span data-ttu-id="cbe10-177">為影片資料流程定義緩衝區視窗的常數。</span><span class="sxs-lookup"><span data-stu-id="cbe10-177">Define a constant for buffer window for a video stream.</span></span>

    ```C++
    // Video buffer window
    const INT32 VIDEO_WINDOW_MSEC = 3000;
    
    ```

    

## <a name="create-the-media-source"></a><span data-ttu-id="cbe10-178">建立媒體來源</span><span class="sxs-lookup"><span data-stu-id="cbe10-178">Create the Media Source</span></span>

<span data-ttu-id="cbe10-179">建立輸入來源的媒體來源。</span><span class="sxs-lookup"><span data-stu-id="cbe10-179">Create a media source for the input source.</span></span> <span data-ttu-id="cbe10-180">媒體基礎提供各種媒體格式的內建媒體來源： MP3、3GP、AVI/WAVE。</span><span class="sxs-lookup"><span data-stu-id="cbe10-180">Media Foundation provides built-in media sources for various media formats: MP3, MP4/3GP, AVI/WAVE.</span></span> <span data-ttu-id="cbe10-181">如需媒體基礎所支援之格式的相關資訊，請參閱 [媒體基礎中支援的媒體格式](supported-media-formats-in-media-foundation.md)。</span><span class="sxs-lookup"><span data-stu-id="cbe10-181">For information about the formats supported by Media Foundation, see [Supported Media Formats in Media Foundation](supported-media-formats-in-media-foundation.md).</span></span>

<span data-ttu-id="cbe10-182">若要建立媒體來源，請使用 [來源解析程式](source-resolver.md)。</span><span class="sxs-lookup"><span data-stu-id="cbe10-182">To create the media source, use the [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="cbe10-183">這個物件會分析針對原始程式檔所指定的 URL，並建立適當的媒體來源。</span><span class="sxs-lookup"><span data-stu-id="cbe10-183">This object analyzes the URL that was specified for the source file and creates the appropriate media source.</span></span>

<span data-ttu-id="cbe10-184">進行下列呼叫：</span><span class="sxs-lookup"><span data-stu-id="cbe10-184">Make the following calls:</span></span>

-   [<span data-ttu-id="cbe10-185">**MFCreateSourceResolver**</span><span class="sxs-lookup"><span data-stu-id="cbe10-185">**MFCreateSourceResolver**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver)
-   [<span data-ttu-id="cbe10-186">**IMFSourceResolver::CreateObjectFromURL**</span><span class="sxs-lookup"><span data-stu-id="cbe10-186">**IMFSourceResolver::CreateObjectFromURL**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)

    <span data-ttu-id="cbe10-187">如需這些呼叫的詳細資訊，請參閱 [使用來源解析程式](using-the-source-resolver.md)。</span><span class="sxs-lookup"><span data-stu-id="cbe10-187">For more information about these calls, see [Using the Source Resolver](using-the-source-resolver.md).</span></span>

    <span data-ttu-id="cbe10-188">如果您的輸入檔是 ASF 格式，而且您想要將它轉換成不同的位元速率檔案而不變更格式，來源規劃求解會建立 [Asf 媒體來源](asf-media-source.md)的實例。</span><span class="sxs-lookup"><span data-stu-id="cbe10-188">If your input file is in ASF format and you want to convert it to a different bit-rate file without changing formats, the source solver creates an instance of the [ASF Media Source](asf-media-source.md).</span></span>

<span data-ttu-id="cbe10-189">下列程式碼範例顯示的函式 CreateMediaSource 會建立指定檔案的媒體來源。</span><span class="sxs-lookup"><span data-stu-id="cbe10-189">The following code example shows a function CreateMediaSource that creates a media source for the specified file.</span></span>


```C++
//  Create a media source from a URL.
HRESULT CreateMediaSource(PCWSTR sURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source.

    // Note: For simplicity this sample uses the synchronous method to create 
    // the media source. However, creating a media source can take a noticeable
    // amount of time, especially for a network source. For a more responsive 
    // UI, use the asynchronous BeginCreateObjectFromURL method.

    hr = pSourceResolver->CreateObjectFromURL(
        sURL,                       // URL of the source.
        MF_RESOLUTION_MEDIASOURCE,  // Create a source object.
        NULL,                       // Optional property store.
        &ObjectType,        // Receives the created object type. 
        &pSource            // Receives a pointer to the media source.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



## <a name="create-the-asf-file-sink"></a><span data-ttu-id="cbe10-190">建立 ASF File 接收器</span><span class="sxs-lookup"><span data-stu-id="cbe10-190">Create the ASF File Sink</span></span>

<span data-ttu-id="cbe10-191">建立 ASF 檔案接收的實例，將編碼的媒體資料封存至編碼會話結尾的 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="cbe10-191">Create an instance of the ASF file sink that will archive encoded media data to an ASF file at the end of the encoding session.</span></span>

<span data-ttu-id="cbe10-192">在本教學課程中，您將建立 ASF 檔案接收的啟用物件。</span><span class="sxs-lookup"><span data-stu-id="cbe10-192">In this tutorial, you will create an activation object for the ASF file sink.</span></span> <span data-ttu-id="cbe10-193">檔案接收需要下列資訊，才能建立必要的資料流程接收。</span><span class="sxs-lookup"><span data-stu-id="cbe10-193">The file sink needs the following information in order to create the required stream sinks.</span></span>

-   <span data-ttu-id="cbe10-194">要在最後一個檔案中編碼和寫入的資料流程。</span><span class="sxs-lookup"><span data-stu-id="cbe10-194">The streams to be encoded and written in the final file.</span></span>
-   <span data-ttu-id="cbe10-195">用來編碼媒體內容的編碼屬性，例如編碼類型、編碼次數和相關屬性。</span><span class="sxs-lookup"><span data-stu-id="cbe10-195">The encoding properties that are used to encode the media content, such as, type of encoding, number of encoding passes, and the related properties.</span></span>
-   <span data-ttu-id="cbe10-196">通用檔案屬性，指出媒體接收是否應該自動調整有漏洞值區參數 (位速率和緩衝區大小) 。</span><span class="sxs-lookup"><span data-stu-id="cbe10-196">The global file properties that indicate to the media sink whether it should adjust the leaky bucket parameters (bit rate and buffer size) automatically.</span></span>

<span data-ttu-id="cbe10-197">資料流程資訊是在 ASF 設定檔物件中設定，而且編碼和全域屬性是在 ASF ContentInfo 物件所管理的屬性存放區中設定。</span><span class="sxs-lookup"><span data-stu-id="cbe10-197">The stream information is configured in the ASF Profile object and the encoding and global properties are set in a property store managed by the ASF ContentInfo Object.</span></span>

<span data-ttu-id="cbe10-198">如需 ASF 檔案接收的總覽，請參閱 [Asf 媒體接收器](asf-media-sinks.md)。</span><span class="sxs-lookup"><span data-stu-id="cbe10-198">For an overview of the ASF file sink, see [ASF Media Sinks](asf-media-sinks.md).</span></span>

### <a name="create-the-asf-profile-object"></a><span data-ttu-id="cbe10-199">建立 ASF 設定檔物件</span><span class="sxs-lookup"><span data-stu-id="cbe10-199">Create the ASF Profile Object</span></span>

<span data-ttu-id="cbe10-200">若要讓 ASF 檔案接收將編碼的媒體資料寫入 ASF 檔案，接收端必須知道要建立串流接收器的資料流程數目和資料流程類型。</span><span class="sxs-lookup"><span data-stu-id="cbe10-200">For the ASF file sink to write encoded media data into an ASF file, the sink needs to know the number of streams and the type of streams for which to create stream sinks.</span></span> <span data-ttu-id="cbe10-201">在本教學課程中，您將從媒體來源解壓縮該資訊，並建立對應的輸出資料流程。</span><span class="sxs-lookup"><span data-stu-id="cbe10-201">In this tutorial you will extract that information from the media source and create corresponding output streams.</span></span> <span data-ttu-id="cbe10-202">將您的輸出資料流程限制為一個音訊串流和一個影片串流。</span><span class="sxs-lookup"><span data-stu-id="cbe10-202">Restrict your output streams to one audio stream and one video stream.</span></span> <span data-ttu-id="cbe10-203">針對來源中的每個選取的資料流程，建立目標資料流程並將它新增至設定檔。</span><span class="sxs-lookup"><span data-stu-id="cbe10-203">For each selected stream in the source, create a target stream and add it to the profile.</span></span>

<span data-ttu-id="cbe10-204">若要執行此步驟，您需要下列物件。</span><span class="sxs-lookup"><span data-stu-id="cbe10-204">To implement this step, you need the following objects.</span></span>

-   [<span data-ttu-id="cbe10-205">ASF 設定檔</span><span class="sxs-lookup"><span data-stu-id="cbe10-205">ASF Profile</span></span>](asf-profile.md)
-   <span data-ttu-id="cbe10-206">媒體來源的簡報描述項</span><span class="sxs-lookup"><span data-stu-id="cbe10-206">Presentation Descriptor for the media source</span></span>
-   <span data-ttu-id="cbe10-207">媒體來源中所選取資料流程的資料流程描述項。</span><span class="sxs-lookup"><span data-stu-id="cbe10-207">Stream descriptors for the selected streams in the media source.</span></span>
-   <span data-ttu-id="cbe10-208">所選資料流程的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="cbe10-208">Media Types for the selected streams.</span></span>

<span data-ttu-id="cbe10-209">下列步驟說明建立 ASF 設定檔和目標資料流程的程式。</span><span class="sxs-lookup"><span data-stu-id="cbe10-209">The following steps describe the process of creating the ASF profile and the target streams.</span></span>

<span data-ttu-id="cbe10-210">**建立 ASF 設定檔**</span><span class="sxs-lookup"><span data-stu-id="cbe10-210">**To create the ASF profile**</span></span>

1.  <span data-ttu-id="cbe10-211">呼叫 [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) 以建立空的設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="cbe10-211">Call [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) to create an empty profile object.</span></span>
2.  <span data-ttu-id="cbe10-212">呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) ，以建立本教學課程的「建立媒體來源」一節所述步驟中所建立之媒體來源的簡報描述項。</span><span class="sxs-lookup"><span data-stu-id="cbe10-212">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) to create the presentation descriptor for the media source created in the step described in the "Create the Media Source" section of this tutorial.</span></span>
3.  <span data-ttu-id="cbe10-213">呼叫 [**IMFPresentationDescriptor：： GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) 來取得媒體來源中的資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="cbe10-213">Call [**IMFPresentationDescriptor::GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) to get the number of streams in the media source.</span></span>
4.  <span data-ttu-id="cbe10-214">針對媒體來源中的每個資料流程呼叫 [**IMFPresentationDescriptor：： GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) ，取得資料流程的資料流程描述項。</span><span class="sxs-lookup"><span data-stu-id="cbe10-214">Call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) for each stream in the media source, get the stream's stream descriptor.</span></span>
5.  <span data-ttu-id="cbe10-215">呼叫 [**IMFStreamDescriptor：： GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) ，後面接著 [**IMFMediaTypeHandler：： GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) ，並取得資料流程的第一個媒體類型。</span><span class="sxs-lookup"><span data-stu-id="cbe10-215">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) followed by [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) and get the first media type for the stream.</span></span>

    <span data-ttu-id="cbe10-216">**注意**   若要避免複雜的呼叫，請假設每個資料流程只有一個媒體類型，並選取資料流程的第一個媒體類型。</span><span class="sxs-lookup"><span data-stu-id="cbe10-216">**Note**   To avoid complex calls, assume that only one media type exists per stream and select the first media type of the stream.</span></span> <span data-ttu-id="cbe10-217">針對複雜的資料流程，您需要從媒體類型處理常式列舉每個媒體類型，並選擇您要編碼的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="cbe10-217">For complex streams, you need to enumerate each media type from the media type handler and choose the media type that you would like to encode.</span></span>

6.  <span data-ttu-id="cbe10-218">呼叫 I [**IMFMediaType：： GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) 來取得資料流程的主要類型，以判斷資料流程是否包含音訊或影片。</span><span class="sxs-lookup"><span data-stu-id="cbe10-218">Call I [**IMFMediaType::GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) to get the major type of the stream to determine whether the stream is contains audio or video.</span></span>
7.  <span data-ttu-id="cbe10-219">視資料流程的主要類型而定，建立目標媒體類型。</span><span class="sxs-lookup"><span data-stu-id="cbe10-219">Depending on the major type of the stream, create target media types.</span></span> <span data-ttu-id="cbe10-220">這些媒體類型會保存編碼器將在編碼會話期間使用的格式資訊。</span><span class="sxs-lookup"><span data-stu-id="cbe10-220">These media types will hold format information that the encoder will use during the encoding session.</span></span> <span data-ttu-id="cbe10-221">本教學課程的下列各節將說明建立目標媒體類型的程式。</span><span class="sxs-lookup"><span data-stu-id="cbe10-221">The following sections of this tutorial describe the process of creating the target media types.</span></span>
    -   <span data-ttu-id="cbe10-222">建立壓縮的音訊媒體類型</span><span class="sxs-lookup"><span data-stu-id="cbe10-222">Create a Compressed Audio Media Type</span></span>
    -   <span data-ttu-id="cbe10-223">建立壓縮的影片媒體類型</span><span class="sxs-lookup"><span data-stu-id="cbe10-223">Create a Compressed Video Media Type</span></span>
8.  <span data-ttu-id="cbe10-224">根據目標媒體類型建立資料流程，根據應用程式的需求設定資料流程，然後將資料流程新增至設定檔。</span><span class="sxs-lookup"><span data-stu-id="cbe10-224">Create a stream based on the target media type, configure the stream according to the application's requirements, and add the stream to the profile.</span></span> <span data-ttu-id="cbe10-225">如需詳細資訊，請參閱 [將資料流程資訊新增至 ASF 檔案接收](adding-stream-information-to-the-asf-file-sink.md)。</span><span class="sxs-lookup"><span data-stu-id="cbe10-225">For more information, see [Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md).</span></span>

    1.  <span data-ttu-id="cbe10-226">呼叫 [**IMFASFProfile：： CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) ，並傳遞目標媒體類型以建立輸出資料流程。</span><span class="sxs-lookup"><span data-stu-id="cbe10-226">Call [**IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) and pass the target media type to create the output stream.</span></span> <span data-ttu-id="cbe10-227">方法會捕獲資料流程物件的 IMFASFStreamConfig 介面。</span><span class="sxs-lookup"><span data-stu-id="cbe10-227">The method retrieves the IMFASFStreamConfig interface of the stream object.</span></span>
    2.  <span data-ttu-id="cbe10-228">設定資料流程。</span><span class="sxs-lookup"><span data-stu-id="cbe10-228">Configure the stream.</span></span>
        -   <span data-ttu-id="cbe10-229">呼叫 [**IMFASFStreamConfig：： SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) ，將數位指派給資料流程。</span><span class="sxs-lookup"><span data-stu-id="cbe10-229">Call [**IMFASFStreamConfig::SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) to assign a number to the stream.</span></span> <span data-ttu-id="cbe10-230">這是必要設定。</span><span class="sxs-lookup"><span data-stu-id="cbe10-230">This setting is mandatory.</span></span>
        -   <span data-ttu-id="cbe10-231">藉由呼叫 [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) 方法和相關的資料流程設定屬性，選擇性地設定每個資料流程的有漏洞值區參數、承載延伸模組、互斥。</span><span class="sxs-lookup"><span data-stu-id="cbe10-231">Optionally configure the leaky bucket parameters, payload extension, mutual exclusion on each stream by calling [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) methods and relevant stream configuration attributes.</span></span>
    3.  <span data-ttu-id="cbe10-232">使用 ASF ContentInfo 物件來新增串流層級編碼屬性。</span><span class="sxs-lookup"><span data-stu-id="cbe10-232">Add the stream level encoding properties by using the ASF ContentInfo object.</span></span> <span data-ttu-id="cbe10-233">如需此步驟的詳細資訊，請參閱本教學課程中的「建立 ASF ContentInfo 物件」一節。</span><span class="sxs-lookup"><span data-stu-id="cbe10-233">For more information about this step, see the "Create the ASF ContentInfo Object" section in this tutorial.</span></span>
    4.  <span data-ttu-id="cbe10-234">呼叫 [**IMFASFProfile：： SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) ，將資料流程新增至設定檔。</span><span class="sxs-lookup"><span data-stu-id="cbe10-234">Call [**IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) to add the stream to the profile.</span></span>

    <span data-ttu-id="cbe10-235">下列程式碼範例會建立輸出音訊串流。</span><span class="sxs-lookup"><span data-stu-id="cbe10-235">The following code example creates an output audio stream.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  CreateAudioStream
    //  Create an audio stream and add it to the profile.
    //
    //  pProfile: A pointer to the ASF profile.
    //  wStreamNumber: Stream number to assign for the new stream.
    //-------------------------------------------------------------------

    HRESULT CreateAudioStream(IMFASFProfile* pProfile, WORD wStreamNumber)
    {
        if (!pProfile)
        {
            return E_INVALIDARG;
        }
        if (wStreamNumber < 1 || wStreamNumber > 127 )
        {
            return MF_E_INVALIDSTREAMNUMBER;
        }

        IMFMediaType* pAudioType = NULL;
        IMFASFStreamConfig* pAudioStream = NULL;
        
        //Create an output type from the encoder
        HRESULT hr = GetOutputTypeFromWMAEncoder(&pAudioType);
        if (FAILED(hr))
        {
            goto done;
        }
        
        //Create a new stream with the audio type
        hr = pProfile->CreateStream(pAudioType, &pAudioStream);
        if (FAILED(hr))
        {
            goto done;
        }

        //Set stream number
        hr = pAudioStream->SetStreamNumber(wStreamNumber);
        if (FAILED(hr))
        {
            goto done;
        }
        
        //Add the stream to the profile
        hr = pProfile->SetStream(pAudioStream);
        if (FAILED(hr))
        {
            goto done;
        }

        wprintf_s(L"Audio Stream created. Stream Number: %d.\n", wStreamNumber);

    done:
        SafeRelease(&pAudioStream);
        SafeRelease(&pAudioType);
        return hr;
    }
    ```

    

    <span data-ttu-id="cbe10-236">下列程式碼範例會建立輸出影片串流。</span><span class="sxs-lookup"><span data-stu-id="cbe10-236">The following code example creates an output video stream.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  CreateVideoStream
    //  Create an video stream and add it to the profile.
    //
    //  pProfile: A pointer to the ASF profile.
    //  wStreamNumber: Stream number to assign for the new stream.
    //    pType: A pointer to the source's video media type.
    //-------------------------------------------------------------------

    HRESULT CreateVideoStream(IMFASFProfile* pProfile, WORD wStreamNumber, IMFMediaType* pType)
    {
        if (!pProfile)
        {
            return E_INVALIDARG;
        }
        if (wStreamNumber < 1 || wStreamNumber > 127 )
        {
            return MF_E_INVALIDSTREAMNUMBER;
        }

        HRESULT hr = S_OK;

        
        IMFMediaType* pVideoType = NULL;
        IMFASFStreamConfig* pVideoStream = NULL;

        UINT32 dwBitRate = 0;
            
        //Create a new video type from the source type
        hr = CreateCompressedVideoType(pType, &pVideoType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Create a new stream with the video type
        hr = pProfile->CreateStream(pVideoType, &pVideoStream);
        if (FAILED(hr))
        {
            goto done;
        }
        

        //Set a valid stream number
        hr = pVideoStream->SetStreamNumber(wStreamNumber);
        if (FAILED(hr))
        {
            goto done;
        }

        //Add the stream to the profile
        hr = pProfile->SetStream(pVideoStream);
        if (FAILED(hr))
        {
            goto done;
        }

        wprintf_s(L"Video Stream created. Stream Number: %d .\n", wStreamNumber);

    done:

        SafeRelease(&pVideoStream);
        SafeRelease(&pVideoType);

        return hr;
    }
    ```

    

<span data-ttu-id="cbe10-237">下列程式碼範例會根據來源中的資料流程建立輸出資料流程。</span><span class="sxs-lookup"><span data-stu-id="cbe10-237">The following code example creates output streams depending on the streams in the source.</span></span>


```C++
    //For each stream in the source, add target stream information in the profile
    for (DWORD iStream = 0; iStream < dwSrcStream; iStream++)
    {
        hr = pPD->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);
        if (FAILED(hr))
        {
            goto done;
        }

        if (!fSelected)
        {
            continue;
        }

        //Get the media type handler
        hr = pStreamDesc->GetMediaTypeHandler(&pHandler);
        if (FAILED(hr))
        {
            goto done;
        }

        //Get the first media type 
        hr = pHandler->GetMediaTypeByIndex(0, &pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Get the major type
        hr = pMediaType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        // If this is a video stream, create the target video stream
        if (guidMajor == MFMediaType_Video)
        {
            //The stream level encoding properties will be set in this call
            hr = CreateVideoStream(pProfile, wStreamID, pMediaType);

            if (FAILED(hr))
            {
                goto done;
            }
        }
        
        // If this is an audio stream, create the target audio stream
        if (guidMajor == MFMediaType_Audio)
        {
            //The stream level encoding properties will be set in this call
            hr = CreateAudioStream(pProfile, wStreamID);

            if (FAILED(hr))
            {
                goto done;
            }
        }

        //Get stream's encoding property
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamID, &pContentInfoProps);
        if (FAILED(hr))
        {
            goto done;
        }

        //Set the stream-level encoding properties
        hr = SetEncodingProperties(guidMajor, pContentInfoProps);       
        if (FAILED(hr))
        {
            goto done;
        }


        SafeRelease(&pMediaType);
        SafeRelease(&pStreamDesc);
        SafeRelease(&pContentInfoProps);
        wStreamID++;
    }
```



### <a name="create-a-compressed-audio-media-type"></a><span data-ttu-id="cbe10-238">建立壓縮的音訊媒體類型</span><span class="sxs-lookup"><span data-stu-id="cbe10-238">Create a Compressed Audio Media Type</span></span>

<span data-ttu-id="cbe10-239">如果您想要在輸出檔中包含音訊串流，請設定所需的屬性，藉由指定編碼類型的特性來建立音訊類型。</span><span class="sxs-lookup"><span data-stu-id="cbe10-239">If you want to include an audio stream in the output file, create an audio type by specifying the characteristics of the encoded type by setting the required attributes.</span></span> <span data-ttu-id="cbe10-240">為確保音訊類型與 Windows Media 音訊編碼器相容，請具現化編碼器 MFT、設定編碼屬性，然後呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)來取得媒體類型。</span><span class="sxs-lookup"><span data-stu-id="cbe10-240">To make sure that the audio type is compatible with the Windows Media audio encoder, instantiate the encoder MFT, set the encoding properties, and get a media type by calling [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span></span> <span data-ttu-id="cbe10-241">藉由逐一查看所有可用的類型、取得每個媒體類型的屬性，以及選取最接近您需求的類型，來取得所需的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="cbe10-241">Get the required output type by looping through all the available types, getting the attributes of each media type, and selecting the type that is closest to your requirements.</span></span> <span data-ttu-id="cbe10-242">在本教學課程中，從編碼器支援的輸出媒體類型清單取得第一個可用類型。</span><span class="sxs-lookup"><span data-stu-id="cbe10-242">In this tutorial, get the first available type from the list of output media types supported by the encoder.</span></span>

<span data-ttu-id="cbe10-243">**注意**  針對 Windows 7，媒體基礎提供新的函式 [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) ，以抓取相容音訊類型的清單。</span><span class="sxs-lookup"><span data-stu-id="cbe10-243">**Note**  For Windows 7, Media Foundation provides a new function, [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) that retrieves a list of the compatible audio types.</span></span> <span data-ttu-id="cbe10-244">此函數只會取得 CBR 編碼的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="cbe10-244">This function only gets media types for CBR encoding.</span></span>

<span data-ttu-id="cbe10-245">完整的音訊類型必須設定下列屬性：</span><span class="sxs-lookup"><span data-stu-id="cbe10-245">A complete audio type must have the following attributes set:</span></span>

-   [<span data-ttu-id="cbe10-246">**MF \_ MT \_ 主要 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="cbe10-246">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)
-   [<span data-ttu-id="cbe10-247">**MF \_ MT \_ 子類型**</span><span class="sxs-lookup"><span data-stu-id="cbe10-247">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)
-   [<span data-ttu-id="cbe10-248">**MF \_ MT \_ 音訊 \_ 數目 \_ 通道**</span><span class="sxs-lookup"><span data-stu-id="cbe10-248">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)
-   [<span data-ttu-id="cbe10-249">**\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cbe10-249">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)
-   [<span data-ttu-id="cbe10-250">**MF \_ MT \_ 音訊 \_ 區塊 \_ 對齊**</span><span class="sxs-lookup"><span data-stu-id="cbe10-250">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)
-   [<span data-ttu-id="cbe10-251">**\_每秒的 MF MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cbe10-251">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [<span data-ttu-id="cbe10-252">**\_ \_ \_ \_ 每個 \_ 樣本的 MF MT 音訊位數**</span><span class="sxs-lookup"><span data-stu-id="cbe10-252">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)

<span data-ttu-id="cbe10-253">下列程式碼範例會從 Windows Media 音訊編碼器取得相容的類型，以建立壓縮的音訊類型。</span><span class="sxs-lookup"><span data-stu-id="cbe10-253">The following code example creates a compressed audio type by getting a compatible type from the Windows Media Audio encoder.</span></span> <span data-ttu-id="cbe10-254">SetEncodingProperties 的實作為本教學課程的「建立 ASF ContentInfo 物件」一節所示。</span><span class="sxs-lookup"><span data-stu-id="cbe10-254">The implementation for SetEncodingProperties is shown in the "Create the ASF ContentInfo Object" section of this tutorial.</span></span>


```C++
//-------------------------------------------------------------------
//  GetOutputTypeFromWMAEncoder
//  Gets a compatible output type from the Windows Media audio encoder.
//
//  ppAudioType: Receives a pointer to the media type.
//-------------------------------------------------------------------

HRESULT GetOutputTypeFromWMAEncoder(IMFMediaType** ppAudioType)
{
    if (!ppAudioType)
    {
        return E_POINTER;
    }

    IMFTransform* pMFT = NULL;
    IMFMediaType* pType = NULL;
    IPropertyStore* pProps = NULL;

    //We need to find a suitable output media type
    //We need to create the encoder to get the available output types
    //and discard the instance.

    CLSID *pMFTCLSIDs = NULL;   // Pointer to an array of CLISDs. 
    UINT32 cCLSID = 0;            // Size of the array.

    MFT_REGISTER_TYPE_INFO tinfo;
    
    tinfo.guidMajorType = MFMediaType_Audio;
    tinfo.guidSubtype = MFAudioFormat_WMAudioV9;

    // Look for an encoder.
    HRESULT hr = MFTEnum(
        MFT_CATEGORY_AUDIO_ENCODER,
        0,                  // Reserved
        NULL,                // Input type to match. None.
        &tinfo,             // WMV encoded type.
        NULL,               // Attributes to match. (None.)
        &pMFTCLSIDs,        // Receives a pointer to an array of CLSIDs.
        &cCLSID             // Receives the size of the array.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // MFTEnum can return zero matches.
    if (cCLSID == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
        goto done;
    }
    else
    {
        // Create the MFT decoder
        hr = CoCreateInstance(pMFTCLSIDs[0], NULL,
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pMFT));

        if (FAILED(hr))
        {
            goto done;
        }

    }

    // Get the encoder's property store

    hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
    if (FAILED(hr))
    {
        goto done;
    }
    
    //Set encoding properties
    hr = SetEncodingProperties(MFMediaType_Audio, pProps);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get the first output type
    //You can loop through the available output types to choose 
    //the one that meets your target requirements
    hr = pMFT->GetOutputAvailableType(0, 0, &pType);
    if (FAILED(hr))
    {
        goto done;
    }

    //Return to the caller
    *ppAudioType = pType;
    (*ppAudioType)->AddRef();
    
done:
    SafeRelease(&pProps);
    SafeRelease(&pType);
    SafeRelease(&pMFT);
    CoTaskMemFree(pMFTCLSIDs);
    return hr;
}
```



### <a name="create-a-compressed-video-media-type"></a><span data-ttu-id="cbe10-255">建立壓縮的影片媒體類型</span><span class="sxs-lookup"><span data-stu-id="cbe10-255">Create a Compressed Video Media Type</span></span>

<span data-ttu-id="cbe10-256">如果您想要在輸出檔中包含影片串流，請建立完整編碼的影片類型。</span><span class="sxs-lookup"><span data-stu-id="cbe10-256">If you want to include a video stream in the output file, create a complete-encoded video type.</span></span> <span data-ttu-id="cbe10-257">完整的媒體類型必須包含所需的位元速率和編解碼器私用資料。</span><span class="sxs-lookup"><span data-stu-id="cbe10-257">The complete media type must include the desired bit rate and codec private data.</span></span>

<span data-ttu-id="cbe10-258">有兩種方式可以建立完整的影片媒體類型。</span><span class="sxs-lookup"><span data-stu-id="cbe10-258">There are two ways you can create a complete video media type.</span></span>

-   <span data-ttu-id="cbe10-259">建立空的媒體類型，並從來源影片類型複製媒體類型屬性，然後以 GUID 常數 MFVideoFormat WMV3 覆寫 [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md) 屬性 \_ 。</span><span class="sxs-lookup"><span data-stu-id="cbe10-259">Create an empty media type and copy the media type attributes from the source video type and overwrite the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute with the GUID constant MFVideoFormat\_WMV3.</span></span>

    <span data-ttu-id="cbe10-260">完整的影片類型必須設定下列屬性：</span><span class="sxs-lookup"><span data-stu-id="cbe10-260">A complete video type must have the following attributes set:</span></span>

    -   <span data-ttu-id="cbe10-261">MF \_ MT \_ 主要 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="cbe10-261">MF\_MT\_MAJOR\_TYPE</span></span>
    -   <span data-ttu-id="cbe10-262">MF \_ MT \_ 子類型</span><span class="sxs-lookup"><span data-stu-id="cbe10-262">MF\_MT\_SUBTYPE</span></span>
    -   <span data-ttu-id="cbe10-263">MF \_ MT \_ 幀 \_ 速率</span><span class="sxs-lookup"><span data-stu-id="cbe10-263">MF\_MT\_FRAME\_RATE</span></span>
    -   <span data-ttu-id="cbe10-264">MF \_ MT \_ 框架 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="cbe10-264">MF\_MT\_FRAME\_SIZE</span></span>
    -   <span data-ttu-id="cbe10-265">MF \_ MT \_ 交錯 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="cbe10-265">MF\_MT\_INTERLACE\_MODE</span></span>
    -   <span data-ttu-id="cbe10-266">MF \_ MT \_ 圖元 \_ 外觀 \_ 比例</span><span class="sxs-lookup"><span data-stu-id="cbe10-266">MF\_MT\_PIXEL\_ASPECT\_RATIO</span></span>
    -   <span data-ttu-id="cbe10-267">MF \_ MT \_ 平均 \_ 位元速率</span><span class="sxs-lookup"><span data-stu-id="cbe10-267">MF\_MT\_AVG\_BITRATE</span></span>
    -   <span data-ttu-id="cbe10-268">MF \_ MT \_ 使用者 \_ 資料</span><span class="sxs-lookup"><span data-stu-id="cbe10-268">MF\_MT\_USER\_DATA</span></span>

    <span data-ttu-id="cbe10-269">下列程式碼範例會從來源的影片類型建立壓縮的影片類型。</span><span class="sxs-lookup"><span data-stu-id="cbe10-269">The following code example creates a compressed video type from the source's video type.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  CreateCompressedVideoType
    //  Creates an output type from source's video media type.
    //
    //    pType: A pointer to the source's video media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT CreateCompressedVideoType(
            IMFMediaType* pType, 
            IMFMediaType** ppVideoType)
    {
        if (!pType)
        {
            return E_INVALIDARG;
        }
        if (!ppVideoType)
        {
            return E_POINTER;
        }
        
        HRESULT hr = S_OK;
        MFRatio fps = { 0 };
        MFRatio par = { 0 };
        UINT32 width = 0, height = 0;
        UINT32 interlace = MFVideoInterlace_Unknown;
        UINT32 fSamplesIndependent = 0;
        UINT32 cBitrate = 0;

        IMFMediaType* pMediaType = NULL;

        GUID guidMajor = GUID_NULL;

        hr = pType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMajor != MFMediaType_Video )
        {
            hr = MF_E_INVALID_FORMAT;
            goto done;
        }

        hr = MFCreateMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pType->CopyAllItems(pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Fill the missing attributes
        //1. Frame rate
        hr = MFGetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, (UINT32*)&fps.Numerator, (UINT32*)&fps.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            fps.Numerator = 30000;
            fps.Denominator = 1001;

            hr = MFSetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, fps.Numerator, fps.Denominator);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        ////2. Frame size
        hr = MFGetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, &width, &height);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            width = 1280;
            height = 720;
                
            hr = MFSetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, width, height);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        ////3. Interlace mode
        
        if (FAILED(pMediaType->GetUINT32(MF_MT_INTERLACE_MODE, &interlace)))
        {
            hr = pMediaType->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        ////4. Pixel aspect Ratio
        hr = MFGetAttributeRatio(pMediaType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32*)&par.Numerator, (UINT32*)&par.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            par.Numerator = par.Denominator = 1;
            hr = MFSetAttributeRatio(pMediaType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32)par.Numerator, (UINT32)par.Denominator);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        //6. bit rate
        if (FAILED(pMediaType->GetUINT32(MF_MT_AVG_BITRATE, &cBitrate)))
        {
            hr = pMediaType->SetUINT32(MF_MT_AVG_BITRATE, 1000000);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        hr = pMediaType->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_WMV3);
        if (FAILED(hr))
        {
            goto done;
        }

        // Return the pointer to the caller.
        *ppVideoType = pMediaType;
        (*ppVideoType)->AddRef();


    done:
        SafeRelease(&pMediaType);
        return hr;
    }
    
    ```

    

-   <span data-ttu-id="cbe10-270">藉由設定編碼屬性，然後呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)，從 Windows media video 編碼器取得相容的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="cbe10-270">Get a compatible media type from the Windows Media video encoder by setting the encoding properties and then calling [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span></span> <span data-ttu-id="cbe10-271">這個方法會傳回部分型別。</span><span class="sxs-lookup"><span data-stu-id="cbe10-271">This method returns the partial type.</span></span> <span data-ttu-id="cbe10-272">藉由新增下列資訊，請務必將部分類型轉換成完整的類型：</span><span class="sxs-lookup"><span data-stu-id="cbe10-272">Make sure you convert the partial type to a complete type by adding the following information:</span></span>

    -   <span data-ttu-id="cbe10-273">設定 [ [**MF \_ MT \_ 平均 \_ 位元速率**](mf-mt-avg-bitrate-attribute.md) ] 屬性中的 [影片位率]。</span><span class="sxs-lookup"><span data-stu-id="cbe10-273">Set the video bit rate in the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute.</span></span>
    -   <span data-ttu-id="cbe10-274">藉由設定 [**MF \_ MT \_ 使用者 \_ 資料**](mf-mt-user-data-attribute.md) 屬性來新增編解碼器私用資料。</span><span class="sxs-lookup"><span data-stu-id="cbe10-274">Add codec private data by setting the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute.</span></span> <span data-ttu-id="cbe10-275">如需詳細指示，請參閱設定 [WMV 編碼器](configuring-a-wmv-encoder.md)中的「私用編解碼器資料」。</span><span class="sxs-lookup"><span data-stu-id="cbe10-275">For detailed instructions, see "Private Codec Data" in [Configuring a WMV Encoder](configuring-a-wmv-encoder.md).</span></span>

    <span data-ttu-id="cbe10-276">因為 [**IWMCodecPrivateData：： GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) 會在傳回編解碼器私用資料之前檢查位元速率，所以請確定您在取得編解碼器私用資料之前，先設定位元速率。</span><span class="sxs-lookup"><span data-stu-id="cbe10-276">Because [**IWMCodecPrivateData::GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) checks the bit rate before returning the codec private data, make sure that you set the bit rate before getting the codec private data.</span></span>

    <span data-ttu-id="cbe10-277">下列程式碼範例會從 Windows Media 視訊編碼器取得相容的類型，以建立壓縮的影片類型。</span><span class="sxs-lookup"><span data-stu-id="cbe10-277">The following code example creates a compressed video type by getting a compatible type from the Windows Media Video encoder.</span></span> <span data-ttu-id="cbe10-278">它也會建立未壓縮的影片類型，並將它設定為編碼器的輸入。</span><span class="sxs-lookup"><span data-stu-id="cbe10-278">It also creates an uncompressed video type and sets it as the encoder's input.</span></span> <span data-ttu-id="cbe10-279">這會在 helper 函式 CreateUncompressedVideoType 中執行。</span><span class="sxs-lookup"><span data-stu-id="cbe10-279">This is implemented in the helper function CreateUncompressedVideoType.</span></span> <span data-ttu-id="cbe10-280">GetOutputTypeFromWMVEncoder 藉由新增編解碼器私用資料，將傳回的部分型別轉換成完整型別。</span><span class="sxs-lookup"><span data-stu-id="cbe10-280">GetOutputTypeFromWMVEncoder converts the returned partial type into a complete type by adding codec private data.</span></span> <span data-ttu-id="cbe10-281">SetEncodingProperties 的實作為本教學課程的「建立 ASF ContentInfo 物件」一節所示。</span><span class="sxs-lookup"><span data-stu-id="cbe10-281">The implementation for SetEncodingProperties is shown in the "Create the ASF ContentInfo Object" section of this tutorial.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  GetOutputTypeFromWMVEncoder
    //  Gets a compatible output type from the Windows Media video encoder.
    //
    //  pType: A pointer to the source video stream's media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT GetOutputTypeFromWMVEncoder(IMFMediaType* pType, IMFMediaType** ppVideoType)
    {
        if (!ppVideoType)
        {
            return E_POINTER;
        }

        IMFTransform* pMFT = NULL;
        IPropertyStore* pProps = NULL;
        IMFMediaType* pInputType = NULL;
        IMFMediaType* pOutputType = NULL;
        
        UINT32 cBitrate = 0;

        //We need to find a suitable output media type
        //We need to create the encoder to get the available output types
        //and discard the instance.

        CLSID *pMFTCLSIDs = NULL;   // Pointer to an array of CLISDs. 
        UINT32 cCLSID = 0;          // Size of the array.

        MFT_REGISTER_TYPE_INFO tinfo;
        
        tinfo.guidMajorType = MFMediaType_Video;
        tinfo.guidSubtype = MFVideoFormat_WMV3;

        // Look for an encoder.
        HRESULT hr = MFTEnum(
            MFT_CATEGORY_VIDEO_ENCODER,
            0,                  // Reserved
            NULL,               // Input type to match. None.
            &tinfo,             // WMV encoded type.
            NULL,               // Attributes to match. (None.)
            &pMFTCLSIDs,        // Receives a pointer to an array of CLSIDs.
            &cCLSID             // Receives the size of the array.
            );
        if (FAILED(hr))
        {
            goto done;
        }

        // MFTEnum can return zero matches.
        if (cCLSID == 0)
        {
            hr = MF_E_TOPO_CODEC_NOT_FOUND;
            goto done;
        }
        else
        {
            //Create the MFT decoder
            hr = CoCreateInstance(pMFTCLSIDs[0], NULL,
                CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pMFT));
            if (FAILED(hr))
            {
                goto done;
            }

        }
        
        //Get the video encoder property store
        hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
        if (FAILED(hr))
        {
            goto done;
        }

        //Set encoding properties
        hr = SetEncodingProperties(MFMediaType_Video, pProps);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = CreateUncompressedVideoType(pType, &pInputType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMFT->SetInputType(0, pInputType, 0);

        //Get the first output type
        //You can loop through the available output types to choose 
        //the one that meets your target requirements
        hr =  pMFT->GetOutputAvailableType(0, 0, &pOutputType);
        if (FAILED(hr))
        {
            goto done;
        }
        
        hr = pType->GetUINT32(MF_MT_AVG_BITRATE, &cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        //Now set the bit rate
        hr = pOutputType->SetUINT32(MF_MT_AVG_BITRATE, cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = AddPrivateData(pMFT, pOutputType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Return to the caller
        *ppVideoType = pOutputType;
        (*ppVideoType)->AddRef();
        
    done:
        SafeRelease(&pProps);
        SafeRelease(&pOutputType);
        SafeRelease(&pInputType);
        SafeRelease(&pMFT);
        CoTaskMemFree(pMFTCLSIDs);
        return hr;
    }
    ```

    

    <span data-ttu-id="cbe10-282">下列程式碼範例會建立未壓縮的影片類型。</span><span class="sxs-lookup"><span data-stu-id="cbe10-282">The following code example creates an uncompressed video type.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  CreateUncompressedVideoType
    //  Creates an uncompressed video type.
    //
    //    pType: A pointer to the source's video media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT CreateUncompressedVideoType(IMFMediaType* pType, IMFMediaType** ppMediaType)
    {
        if (!pType)
        {
            return E_INVALIDARG;
        }
        if (!ppMediaType)
        {
            return E_POINTER;
        }
        
        MFRatio fps = { 0 };
        MFRatio par = { 0 };
        UINT32 width = 0, height = 0;
        UINT32 interlace = MFVideoInterlace_Unknown;
        UINT32 cBitrate = 0;

        IMFMediaType* pMediaType = NULL;

        GUID guidMajor = GUID_NULL;

        HRESULT hr = pType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMajor != MFMediaType_Video )
        {
            hr = MF_E_INVALID_FORMAT;
            goto done;
        }

        hr = MFGetAttributeRatio(pType, MF_MT_FRAME_RATE, (UINT32*)&fps.Numerator, (UINT32*)&fps.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            fps.Numerator = 30000;
            fps.Denominator = 1001;

        }
        hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            width = 1280;
            height = 720;

        }

        interlace = MFGetAttributeUINT32(pType, MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);

        hr = MFGetAttributeRatio(pType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32*)&par.Numerator, (UINT32*)&par.Denominator);
        if (FAILED(hr))
        {
            par.Numerator = par.Denominator = 1;
        }

        cBitrate = MFGetAttributeUINT32(pType, MF_MT_AVG_BITRATE, 1000000);

        hr = MFCreateMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetGUID(MF_MT_MAJOR_TYPE, guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_RGB32);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = MFSetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, fps.Numerator, fps.Denominator);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = MFSetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, width, height);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetUINT32(MF_MT_INTERLACE_MODE, 2);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaType->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaType->SetUINT32(MF_MT_AVG_BITRATE, cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        // Return the pointer to the caller.
        *ppMediaType = pMediaType;
        (*ppMediaType)->AddRef();


    done:
        SafeRelease(&pMediaType);
        return hr;
    }
    ```

    

    <span data-ttu-id="cbe10-283">下列程式碼範例會將編解碼器私用資料新增至指定的影片媒體類型。</span><span class="sxs-lookup"><span data-stu-id="cbe10-283">The following code example adds codec private data to the specified video media type.</span></span>

    ```C++
    //
    // AddPrivateData
    // Appends the private codec data to a media type.
    //
    // pMFT: The video encoder
    // pTypeOut: A video type from the encoder's type list.
    //
    // The function modifies pTypeOut by adding the codec data.
    //

    HRESULT AddPrivateData(IMFTransform *pMFT, IMFMediaType *pTypeOut)
    {
        HRESULT hr = S_OK;
        ULONG cbData = 0;
        BYTE *pData = NULL;

        IWMCodecPrivateData *pPrivData = NULL;

        DMO_MEDIA_TYPE mtOut = { 0 };

        // Convert the type to a DMO type.
        hr = MFInitAMMediaTypeFromMFMediaType(
            pTypeOut, 
            FORMAT_VideoInfo, 
            (AM_MEDIA_TYPE*)&mtOut
            );
        
        if (SUCCEEDED(hr))
        {
            hr = pMFT->QueryInterface(IID_PPV_ARGS(&pPrivData));
        }

        if (SUCCEEDED(hr))
        {
            hr = pPrivData->SetPartialOutputType(&mtOut);
        }

        //
        // Get the private codec data
        //

        // First get the buffer size.
        if (SUCCEEDED(hr))
        {
            hr = pPrivData->GetPrivateData(NULL, &cbData);
        }

        if (SUCCEEDED(hr))
        {
            pData = new BYTE[cbData];

            if (pData == NULL)
            {
                hr = E_OUTOFMEMORY;
            }
        }

        // Now get the data.
        if (SUCCEEDED(hr))
        {
            hr = pPrivData->GetPrivateData(pData, &cbData);
        }

        // Add the data to the media type.
        if (SUCCEEDED(hr))
        {
            hr = pTypeOut->SetBlob(MF_MT_USER_DATA, pData, cbData);
        }

        delete [] pData;
        MoFreeMediaType(&mtOut);
        SafeRelease(&pPrivData);
        return hr;
    }
    ```

    

### <a name="create-the-asf-contentinfo-object"></a><span data-ttu-id="cbe10-284">建立 ASF ContentInfo 物件</span><span class="sxs-lookup"><span data-stu-id="cbe10-284">Create the ASF ContentInfo Object</span></span>

<span data-ttu-id="cbe10-285">ASF ContentInfo 物件是 WMContainer 層級元件，主要是設計用來儲存 ASF 標頭物件資訊。</span><span class="sxs-lookup"><span data-stu-id="cbe10-285">The ASF ContentInfo object is a WMContainer level component that is primarily designed to store ASF Header Object information.</span></span> <span data-ttu-id="cbe10-286">ASF 檔案接收會執行 ContentInfo 物件，以便將資訊儲存 (在屬性存放區中，) ，此屬性存放區會用來寫入編碼檔案的 ASF 標頭物件。</span><span class="sxs-lookup"><span data-stu-id="cbe10-286">The ASF file sink, implements the ContentInfo object in order to store information (in a property store) that will be used to write the ASF Header Object of the encoded file.</span></span> <span data-ttu-id="cbe10-287">若要這樣做，您必須在啟動編碼會話之前，先在 ContentInfo 物件上建立並設定下列資訊集。</span><span class="sxs-lookup"><span data-stu-id="cbe10-287">To do so, you must create and configure the following set of information on the ContentInfo object before starting the encoding session.</span></span>

1.  <span data-ttu-id="cbe10-288">呼叫 [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) 以建立空的 ContentInfo 物件。</span><span class="sxs-lookup"><span data-stu-id="cbe10-288">Call [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) to create an empty ContentInfo object.</span></span>

    <span data-ttu-id="cbe10-289">下列程式碼範例會建立空的 ContentInfo 物件。</span><span class="sxs-lookup"><span data-stu-id="cbe10-289">The following code example creates an empty ContentInfo object.</span></span>

    ```C++
        // Create an empty ContentInfo object
        hr = MFCreateASFContentInfo(&pContentInfo);
        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

2.  <span data-ttu-id="cbe10-290">呼叫 [**IMFASFContentInfo：： GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) ，以取得 file 接收器的資料流程層級屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="cbe10-290">Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) to get the file sink's stream-level property store.</span></span> <span data-ttu-id="cbe10-291">在此呼叫中，您必須在建立 ASF 設定檔時，傳遞您為串流指派的串流號碼。</span><span class="sxs-lookup"><span data-stu-id="cbe10-291">In this call, you need to pass the stream number that you assigned for the stream while creating the ASF profile.</span></span>
3.  <span data-ttu-id="cbe10-292">在 file 接收器的資料流程屬性存放區中設定資料流程層級 [編碼屬性](configuring-the-encoder.md) 。</span><span class="sxs-lookup"><span data-stu-id="cbe10-292">Set the stream-level [Encoding Properties](configuring-the-encoder.md) in the file sink's stream property store.</span></span> <span data-ttu-id="cbe10-293">如需詳細資訊，請參閱在檔案接收中 [設定屬性](setting-properties-in-the-file-sink.md)的「資料流程編碼屬性」。</span><span class="sxs-lookup"><span data-stu-id="cbe10-293">For more information, see "Stream Encoding Properties" in [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>

    <span data-ttu-id="cbe10-294">下列程式碼範例會在 file 接收器的屬性存放區中設定資料流程層級屬性。</span><span class="sxs-lookup"><span data-stu-id="cbe10-294">The following code example sets the stream level properties in the file sink's property store.</span></span>

    ```C++
            //Get stream's encoding property
            hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamID, &pContentInfoProps);
            if (FAILED(hr))
            {
                goto done;
            }

            //Set the stream-level encoding properties
            hr = SetEncodingProperties(guidMajor, pContentInfoProps);       
            if (FAILED(hr))
            {
                goto done;
            }

    
    ```

    

    <span data-ttu-id="cbe10-295">下列程式碼範例顯示 SetEncodingProperties 的執行。</span><span class="sxs-lookup"><span data-stu-id="cbe10-295">The following code example shows the implementation for SetEncodingProperties.</span></span> <span data-ttu-id="cbe10-296">此函式會設定 CBR 和 VBR 的資料流程層級編碼屬性。</span><span class="sxs-lookup"><span data-stu-id="cbe10-296">This function sets stream level encoding properties for CBR and VBR.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  SetEncodingProperties
    //  Create a media source from a URL.
    //
    //  guidMT:  Major type of the stream, audio or video
    //  pProps:  A pointer to the property store in which 
    //           to set the required encoding properties.
    //-------------------------------------------------------------------

    HRESULT SetEncodingProperties (const GUID guidMT, IPropertyStore* pProps)
    {
        if (!pProps)
        {
            return E_INVALIDARG;
        }

        if (EncodingMode == NONE)
        {
            return MF_E_NOT_INITIALIZED;
        }
       
        HRESULT hr = S_OK;

        PROPVARIANT var;

        switch (EncodingMode)
        {
            case CBR:
                // Set VBR to false.
                hr = InitPropVariantFromBoolean(FALSE, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Set the video buffer window.
                if (guidMT == MFMediaType_Video)
                {
                    hr = InitPropVariantFromInt32(VIDEO_WINDOW_MSEC, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_VIDEOWINDOW, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                break;

            case VBR:
                //Set VBR to true.
                hr = InitPropVariantFromBoolean(TRUE, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Number of encoding passes is 1.

                hr = InitPropVariantFromInt32(1, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_PASSESUSED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Set the quality level.

                if (guidMT == MFMediaType_Audio)
                {
                    hr = InitPropVariantFromUInt32(98, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_DESIRED_VBRQUALITY, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                else if (guidMT == MFMediaType_Video)
                {
                    hr = InitPropVariantFromUInt32(95, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_VBRQUALITY, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                break;

            default:
                hr = E_UNEXPECTED;
                break;
        }    

    done:
        PropVariantClear(&var);
        return hr;
    }
    ```

    

4.  <span data-ttu-id="cbe10-297">呼叫 [**IMFASFContentInfo：： GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) 來取得 file 接收器的全域屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="cbe10-297">Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) to get the file sink's global property store.</span></span> <span data-ttu-id="cbe10-298">在此呼叫中，您必須在第一個參數中傳遞0。</span><span class="sxs-lookup"><span data-stu-id="cbe10-298">In this call, you need to pass 0 in the first parameter.</span></span> <span data-ttu-id="cbe10-299">如需詳細資訊，請參閱在檔案 [接收中設定屬性](setting-properties-in-the-file-sink.md)的「通用檔案接收屬性」。</span><span class="sxs-lookup"><span data-stu-id="cbe10-299">For more information, see "Global File Sink Properties" in [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>
5.  <span data-ttu-id="cbe10-300">將 [**MFPKEY \_ ASFMEDIASINK \_ AUTOADJUST \_ 位元速率**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) 設定為 VARIANT \_ TRUE，以確保正確地調整 ASF 多工器的有漏洞 bucket 值。</span><span class="sxs-lookup"><span data-stu-id="cbe10-300">Set the [**MFPKEY\_ASFMEDIASINK\_AUTOADJUST\_BITRATE**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) to VARIANT\_TRUE to ensure the leaky bucket values in the ASF multiplexer are adjusted properly.</span></span> <span data-ttu-id="cbe10-301">如需此屬性的相關資訊，請參閱建立多工器 [物件](creating-the-multiplexer-object.md)中的「多工器初始化和有漏洞 Bucket 設定」。</span><span class="sxs-lookup"><span data-stu-id="cbe10-301">For information about this property, see "Multiplexer Initialization and Leaky Bucket Settings" in [Creating the Multiplexer Object](creating-the-multiplexer-object.md).</span></span>

    <span data-ttu-id="cbe10-302">下列程式碼範例會在 file 接收器的屬性存放區中設定資料流程層級屬性。</span><span class="sxs-lookup"><span data-stu-id="cbe10-302">The following code example sets the stream level properties in the file sink's property store.</span></span>

    ```C++
        //Now we need to set global properties that will be set on the media sink
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(0, &pContentInfoProps);
        if (FAILED(hr))
        {
            goto done;
        }

        //Auto adjust Bitrate
        var.vt = VT_BOOL;
        var.boolVal = VARIANT_TRUE;

        hr = pContentInfoProps->SetValue(MFPKEY_ASFMEDIASINK_AUTOADJUST_BITRATE, var);
        
        //Initialize with the profile
        hr = pContentInfo->SetProfile(pProfile);
        if (FAILED(hr))
        {
            goto done;
        }
    ```

    

    > [!Note]  
    > <span data-ttu-id="cbe10-303">您可以在全域層級設定檔案接收的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="cbe10-303">There are other properties that you can set at the global level for the file sink.</span></span> <span data-ttu-id="cbe10-304">如需詳細資訊，請參閱在 [ContentInfo 物件中設定屬性](setting-properties-in-the-contentinfo-object.md)（property）中的「使用編碼器設定設定 ContentInfo 物件」。</span><span class="sxs-lookup"><span data-stu-id="cbe10-304">For more information, see "Configuring the ContentInfo Object with Encoder Settings" in [Setting Properties in the ContentInfo Object](setting-properties-in-the-contentinfo-object.md).</span></span>

     

<span data-ttu-id="cbe10-305">您將使用設定的 ASF ContentInfo 來建立 ASF 檔案接收的啟用物件 (下一節) 所述。</span><span class="sxs-lookup"><span data-stu-id="cbe10-305">You will use the configured ASF ContentInfo to create an activation object for the ASF file sink (described in the next section).</span></span>

<span data-ttu-id="cbe10-306">如果您要建立跨進程的檔案接收 ([**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)) ，也就是使用啟始物件，您可以使用已設定的 ContentInfo 物件，將 ASF 媒體接收器具現化， (下一節) 所述。</span><span class="sxs-lookup"><span data-stu-id="cbe10-306">If you are creating an out-of-process file sink ([**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)), that is by using an activation object, you can use the configured ContentInfo object to instantiate the ASF media sink (described in the next section).</span></span> <span data-ttu-id="cbe10-307">如果您要建立同進程檔案接收 ([**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)) ，而不是依照步驟1中所述建立空的 ContentInfo 物件，請在檔案接收上呼叫 **IMFMediaSink：： QueryInterface** ，以取得 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)介面的參考。</span><span class="sxs-lookup"><span data-stu-id="cbe10-307">If you are creating an in-process file sink ([**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)), instead of creating the empty ContentInfo object as described in step 1, get a reference to the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface by calling **IMFMediaSink::QueryInterface** on the file sink.</span></span> <span data-ttu-id="cbe10-308">接著，您必須設定 ContentInfo 物件，如本節所述。</span><span class="sxs-lookup"><span data-stu-id="cbe10-308">You must then configure the ContentInfo object as described in this section.</span></span>

### <a name="create-the-asf-file-sink"></a><span data-ttu-id="cbe10-309">建立 ASF File 接收器</span><span class="sxs-lookup"><span data-stu-id="cbe10-309">Create the ASF File Sink</span></span>

<span data-ttu-id="cbe10-310">在本教學課程的這個步驟中，您將使用您在上一個步驟中建立的已設定 ASF ContentInfo，透過呼叫 [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) 函式來建立 asf 檔案接收的啟用物件。</span><span class="sxs-lookup"><span data-stu-id="cbe10-310">In this step of the tutorial, you will use the configured ASF ContentInfo, which you created in the previous step, to create an activation object for the ASF file sink by calling the [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) function.</span></span> <span data-ttu-id="cbe10-311">如需詳細資訊，請參閱 [建立 ASF File 接收器](creating-the-asf-file-sink.md)。</span><span class="sxs-lookup"><span data-stu-id="cbe10-311">For more information, see [Creating the ASF File Sink](creating-the-asf-file-sink.md).</span></span>

<span data-ttu-id="cbe10-312">下列程式碼範例會建立檔案接收的啟用物件。</span><span class="sxs-lookup"><span data-stu-id="cbe10-312">The following code example creates the activation object for the file sink.</span></span>


```C++
    //Create the activation object for the  file sink
    hr = MFCreateASFMediaSinkActivate(sURL, pContentInfo, &pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

```



## <a name="build-the-partial-encoding-topology"></a><span data-ttu-id="cbe10-313">建立部分編碼拓撲</span><span class="sxs-lookup"><span data-stu-id="cbe10-313">Build the Partial Encoding Topology</span></span>

<span data-ttu-id="cbe10-314">接下來，您將建立部分編碼拓撲，方法是建立媒體來源的拓撲節點、必要的 Windows Media 編碼器，以及 ASF 檔案接收。</span><span class="sxs-lookup"><span data-stu-id="cbe10-314">Next, you will build a partial encoding topology by creating topology nodes for the media source, the required Windows Media encoders, and the ASF file sink.</span></span> <span data-ttu-id="cbe10-315">新增拓撲節點之後，您將連接來源、轉換和接收節點。</span><span class="sxs-lookup"><span data-stu-id="cbe10-315">After adding the topology nodes, you will connect the source, transform, and the sink nodes.</span></span> <span data-ttu-id="cbe10-316">在新增拓撲節點之前，您必須藉由呼叫 [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology)來建立空白拓撲物件。</span><span class="sxs-lookup"><span data-stu-id="cbe10-316">Before adding topology nodes, you must create an empty topology object by calling [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).</span></span>

### <a name="create-the-source-topology-node-for-the-media-source"></a><span data-ttu-id="cbe10-317">建立媒體來源的來源拓撲節點</span><span class="sxs-lookup"><span data-stu-id="cbe10-317">Create the Source Topology Node for the Media Source</span></span>

<span data-ttu-id="cbe10-318">在此步驟中，您將建立媒體來源的來源拓撲節點。</span><span class="sxs-lookup"><span data-stu-id="cbe10-318">In this step, you will create the source topology node for the media source.</span></span>

<span data-ttu-id="cbe10-319">若要建立此節點，您需要下列參考：</span><span class="sxs-lookup"><span data-stu-id="cbe10-319">To create this node you need the following references:</span></span>

-   <span data-ttu-id="cbe10-320">您在本教學課程的「建立媒體來源」一節所述的步驟中所建立之媒體來源的指標。</span><span class="sxs-lookup"><span data-stu-id="cbe10-320">A pointer to the media source that you created in the step described in the "Create the Media Source" section of this tutorial.</span></span>
-   <span data-ttu-id="cbe10-321">媒體來源的簡報描述元指標。</span><span class="sxs-lookup"><span data-stu-id="cbe10-321">A pointer to the presentation descriptor for the media source.</span></span> <span data-ttu-id="cbe10-322">您可以藉由呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)，取得媒體來源之 IMFPresentationDescriptor 介面的參考。</span><span class="sxs-lookup"><span data-stu-id="cbe10-322">You can get a reference to IMFPresentationDescriptor interface of the media source by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span>
-   <span data-ttu-id="cbe10-323">在此教學課程的「建立 ASF 設定檔物件」一節所述的步驟中，您已建立目標資料流程之媒體來源中每個資料流程的資料流程描述元指標。</span><span class="sxs-lookup"><span data-stu-id="cbe10-323">A pointer to the stream descriptor for each stream in the media source for which you have created a target stream in the step described in the "Create the ASF Profile Object" section of this tutorial.</span></span>

<span data-ttu-id="cbe10-324">如需有關建立來源節點和程式碼範例的詳細資訊，請參閱 [建立來源節點](creating-source-nodes.md)。</span><span class="sxs-lookup"><span data-stu-id="cbe10-324">For more information about creating source nodes and code example, see [Creating Source Nodes](creating-source-nodes.md).</span></span>

<span data-ttu-id="cbe10-325">下列程式碼範例會藉由新增來源節點和必要的轉換節點來建立部分拓撲。</span><span class="sxs-lookup"><span data-stu-id="cbe10-325">The following code example creates a partial topology by adding the source node and the required transform nodes.</span></span> <span data-ttu-id="cbe10-326">此程式碼會呼叫 helper 函式 AddSourceNode 和 AddTransformOutputNodes。</span><span class="sxs-lookup"><span data-stu-id="cbe10-326">This code calls the helper functions AddSourceNode, and AddTransformOutputNodes.</span></span> <span data-ttu-id="cbe10-327">本教學課程稍後會包含這些函數。</span><span class="sxs-lookup"><span data-stu-id="cbe10-327">These functions are included later in this tutorial.</span></span>


```C++
//-------------------------------------------------------------------
//  BuildPartialTopology
//  Create a partial encoding topology by adding the source and the sink.
//
//  pSource:  A pointer to the media source to enumerate the source streams.
//  pSinkActivate: A pointer to the activation object for ASF file sink.
//  ppTopology:  Receives a pointer to the topology.
//-------------------------------------------------------------------

HRESULT BuildPartialTopology(
       IMFMediaSource *pSource, 
       IMFActivate* pSinkActivate,
       IMFTopology** ppTopology)
{
    if (!pSource || !pSinkActivate)
    {
        return E_INVALIDARG;
    }
    if (!ppTopology)
    {
        return E_POINTER;
    }

    HRESULT hr = S_OK;

    IMFPresentationDescriptor* pPD = NULL;
    IMFStreamDescriptor *pStreamDesc = NULL;
    IMFMediaTypeHandler* pMediaTypeHandler = NULL;
    IMFMediaType* pSrcType = NULL;

    IMFTopology* pTopology = NULL;
    IMFTopologyNode* pSrcNode = NULL;
    IMFTopologyNode* pEncoderNode = NULL;
    IMFTopologyNode* pOutputNode = NULL;


    DWORD cElems = 0;
    DWORD dwSrcStream = 0;
    DWORD StreamID = 0;
    GUID guidMajor = GUID_NULL;
    BOOL fSelected = FALSE;


    //Create the topology that represents the encoding pipeline
    hr = MFCreateTopology (&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

        
    hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pPD->GetStreamDescriptorCount(&dwSrcStream);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD iStream = 0; iStream < dwSrcStream; iStream++)
    {
        hr = pPD->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);
        if (FAILED(hr))
        {
            goto done;
        }

        if (!fSelected)
        {
            continue;
        }

        hr = AddSourceNode(pTopology, pSource, pPD, pStreamDesc, &pSrcNode);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStreamDesc->GetMediaTypeHandler (&pMediaTypeHandler);
        if (FAILED(hr))
        {
            goto done;
        }
        
        hr = pStreamDesc->GetStreamIdentifier(&StreamID);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaTypeHandler->GetMediaTypeByIndex(0, &pSrcType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pSrcType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = AddTransformOutputNodes(pTopology, pSinkActivate, pSrcType, &pEncoderNode);
        if (FAILED(hr))
        {
            goto done;
        }

        //now we have the transform node, connect it to the source node
        hr = pSrcNode->ConnectOutput(0, pEncoderNode, 0);
        if (FAILED(hr))
        {
            goto done;
        }
                

        SafeRelease(&pStreamDesc);
        SafeRelease(&pMediaTypeHandler);
        SafeRelease(&pSrcType);
        SafeRelease(&pEncoderNode);
        SafeRelease(&pOutputNode);
        guidMajor = GUID_NULL;
    }

    *ppTopology = pTopology;
   (*ppTopology)->AddRef();


    wprintf_s(L"Partial Topology Built.\n");

done:
    SafeRelease(&pStreamDesc);
    SafeRelease(&pMediaTypeHandler);
    SafeRelease(&pSrcType);
    SafeRelease(&pEncoderNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pTopology);

    return hr;
}
```



<span data-ttu-id="cbe10-328">下列程式碼範例會建立來源拓撲節點，並將其加入至編碼拓撲中。</span><span class="sxs-lookup"><span data-stu-id="cbe10-328">The following code example creates and adds the source topology node to the encoding topology.</span></span> <span data-ttu-id="cbe10-329">它會採用先前拓撲物件的指標、用來列舉來來源資料流的媒體來源、媒體來源的展示描述項，以及媒體來源的資料流程描述項。</span><span class="sxs-lookup"><span data-stu-id="cbe10-329">It takes pointers to a previously topology object, the media source to enumerate the source streams, the media source's presentation descriptor, and the media source's stream descriptor.</span></span> <span data-ttu-id="cbe10-330">呼叫端會收到來源拓撲節點的指標。</span><span class="sxs-lookup"><span data-stu-id="cbe10-330">The caller receives a pointer to the source topology node.</span></span>


```C++
// Add a source node to a topology.
HRESULT AddSourceNode(
    IMFTopology *pTopology,           // Topology.
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    IMFStreamDescriptor *pSD,         // Stream descriptor.
    IMFTopologyNode **ppNode)         // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_SOURCESTREAM_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the attributes.
    hr = pNode->SetUnknown(MF_TOPONODE_SOURCE, pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_PRESENTATION_DESCRIPTOR, pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_STREAM_DESCRIPTOR, pSD);
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



### <a name="instantiate-the-required-encoders-and-create-the-transform-nodes"></a><span data-ttu-id="cbe10-331">具現化所需的編碼器，並建立轉換節點</span><span class="sxs-lookup"><span data-stu-id="cbe10-331">Instantiate the Required Encoders and Create the Transform Nodes</span></span>

<span data-ttu-id="cbe10-332">媒體基礎管線不會自動插入必須編碼的資料流程所需的 Windows Media 編碼器。</span><span class="sxs-lookup"><span data-stu-id="cbe10-332">The Media Foundation pipeline does not automatically insert the required Windows Media encoders for the streams that it must encode.</span></span> <span data-ttu-id="cbe10-333">應用程式必須手動新增編碼器。</span><span class="sxs-lookup"><span data-stu-id="cbe10-333">The application must add the encoders manually.</span></span> <span data-ttu-id="cbe10-334">若要這樣做，請在本教學課程的「建立 ASF 設定檔物件」一節所述的步驟中，列舉在您建立的 ASF 設定檔中的串流。</span><span class="sxs-lookup"><span data-stu-id="cbe10-334">To do so, enumerate the streams in the ASF profile that you created in the step described in the "Create the ASF Profile Object" section of this tutorial.</span></span> <span data-ttu-id="cbe10-335">針對來源中的每個資料流程和設定檔中的對應資料流程，將所需的編碼器具現化。</span><span class="sxs-lookup"><span data-stu-id="cbe10-335">For each stream in the source and the corresponding stream in the profile, instantiate the required encoders.</span></span> <span data-ttu-id="cbe10-336">針對此步驟，您需要在本教學課程的「建立 ASF 檔案接收」一節所述的步驟中所建立之檔案接收的啟用物件指標。</span><span class="sxs-lookup"><span data-stu-id="cbe10-336">For this step, you need a pointer to the activation object for the file sink that you created in the step described in the "Create the ASF File Sink" section of this tutorial.</span></span>

<span data-ttu-id="cbe10-337">如需透過啟用物件建立編碼器的總覽，請參閱 [使用編碼器的啟用物件](using-an-encoder-s-activation-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="cbe10-337">For an overview on creating encoders through activation objects, see [Using an Encoder's Activation Objects](using-an-encoder-s-activation-objects.md).</span></span>

<span data-ttu-id="cbe10-338">下列程式說明具現化必要編碼器所需的步驟。</span><span class="sxs-lookup"><span data-stu-id="cbe10-338">The following procedure describes the steps required to instantiate the required encoders.</span></span>

1.  <span data-ttu-id="cbe10-339">藉由呼叫 **QueryInterface** 來取得接收之 ContentInfo 物件的參考，方法是在檔案接收啟動時呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) ，然後從檔案接收查詢 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) 。</span><span class="sxs-lookup"><span data-stu-id="cbe10-339">Get a reference to the sink's ContentInfo object by calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) on the file sink activate and then querying for [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) from the file sink by calling **QueryInterface**.</span></span>
2.  <span data-ttu-id="cbe10-340">藉由呼叫 [**IMFASFContentInfo：： GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile)，取得與 ContentInfo 物件相關聯的 ASF 設定檔。</span><span class="sxs-lookup"><span data-stu-id="cbe10-340">Get the ASF profile associated with the ContentInfo object by calling [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span></span>
3.  <span data-ttu-id="cbe10-341">列舉設定檔中的資料流程。</span><span class="sxs-lookup"><span data-stu-id="cbe10-341">Enumerate the streams in the profile.</span></span> <span data-ttu-id="cbe10-342">針對這一點，您將需要串流計數和每個資料流程 [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) 介面的參考。</span><span class="sxs-lookup"><span data-stu-id="cbe10-342">For this you will need the stream count and a reference to each stream's [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span>

    <span data-ttu-id="cbe10-343">呼叫下列方法：</span><span class="sxs-lookup"><span data-stu-id="cbe10-343">Call the following methods:</span></span>

    -   [<span data-ttu-id="cbe10-344">**IMFASFProfile::GetStreamCount**</span><span class="sxs-lookup"><span data-stu-id="cbe10-344">**IMFASFProfile::GetStreamCount**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)
    -   [<span data-ttu-id="cbe10-345">**IMFASFProfile：： GetStream**</span><span class="sxs-lookup"><span data-stu-id="cbe10-345">**IMFASFProfile::GetStream**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream)

4.  <span data-ttu-id="cbe10-346">針對每個資料流程，從 ContentInfo 物件取得主要類型和資料流程的編碼屬性。</span><span class="sxs-lookup"><span data-stu-id="cbe10-346">For each stream get the major type and the stream's encoding properties from the ContentInfo object.</span></span>

    <span data-ttu-id="cbe10-347">呼叫下列方法：</span><span class="sxs-lookup"><span data-stu-id="cbe10-347">Call the following methods:</span></span>

    -   [<span data-ttu-id="cbe10-348">**IMFASFStreamConfig::GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="cbe10-348">**IMFASFStreamConfig::GetMediaType**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype)
    -   [<span data-ttu-id="cbe10-349">**IMFMediaType::GetMajorType**</span><span class="sxs-lookup"><span data-stu-id="cbe10-349">**IMFMediaType::GetMajorType**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype)
    -   [<span data-ttu-id="cbe10-350">**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="cbe10-350">**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore)

        <span data-ttu-id="cbe10-351">針對此呼叫，您需要 [**IMFASFProfile：： GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) 呼叫所取出的串流號碼。</span><span class="sxs-lookup"><span data-stu-id="cbe10-351">For this call you need the stream number retrieved by the [**IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) call.</span></span>

5.  <span data-ttu-id="cbe10-352">根據串流、音訊或影片的類型，藉由呼叫 [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) 或 [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate)，將編碼器的啟用物件具現化。</span><span class="sxs-lookup"><span data-stu-id="cbe10-352">Depending on the type of the stream, audio or video, instantiate the activation object for the encoder by calling [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) or [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate).</span></span>

    <span data-ttu-id="cbe10-353">若要呼叫這些函式，您需要下列參考：</span><span class="sxs-lookup"><span data-stu-id="cbe10-353">To call these functions, you need the following references:</span></span>

    -   <span data-ttu-id="cbe10-354">上一個步驟中由 [**IMFASFStreamConfig：： GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) 所抓取資料流程的媒體類型指標。</span><span class="sxs-lookup"><span data-stu-id="cbe10-354">A pointer to the stream's media type retrieved by [**IMFASFStreamConfig::GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) in the previous step.</span></span>
    -   <span data-ttu-id="cbe10-355">[**IMFASFContentInfo：： GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore)所抓取資料流程的編碼屬性存放區指標。</span><span class="sxs-lookup"><span data-stu-id="cbe10-355">A pointer to the stream's encoding property store retrieved by [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore).</span></span> <span data-ttu-id="cbe10-356">藉由將指標傳遞至屬性存放區，就會將檔案接收中設定的資料流程屬性複製到編碼器 MFT 上。</span><span class="sxs-lookup"><span data-stu-id="cbe10-356">By passing a pointer to the property store, the stream properties set in the file sink are copied on the encoder MFT.</span></span>

6.  <span data-ttu-id="cbe10-357">更新音訊串流的有漏洞 bucket 參數。</span><span class="sxs-lookup"><span data-stu-id="cbe10-357">Update the leaky bucket parameter for the audio stream.</span></span>

    <span data-ttu-id="cbe10-358">[**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) 會針對 Windows Media 音訊編解碼器，設定基礎編碼器 MFT 的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="cbe10-358">[**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) sets the output type on the underlying encoder MFT for the Windows Media audio codec.</span></span> <span data-ttu-id="cbe10-359">設定輸出媒體類型之後，編碼器會從輸出媒體類型取得平均位元速率、計算緩衝區視窗開始風行位速率，以及設定要在編碼會話期間使用的有漏洞值區值。</span><span class="sxs-lookup"><span data-stu-id="cbe10-359">After the output media type is set, the encoder gets the average bit rate from the output media type, calculates the buffer window rage bit rate, and sets the leaky bucket values that will be used during the encoding session.</span></span> <span data-ttu-id="cbe10-360">您可以藉由查詢編碼器或設定自訂值，更新檔案接收中的這些值。</span><span class="sxs-lookup"><span data-stu-id="cbe10-360">You can update these values in the file sink by either querying the encoder or setting custom values.</span></span> <span data-ttu-id="cbe10-361">若要更新值，您需要下列一組資訊：</span><span class="sxs-lookup"><span data-stu-id="cbe10-361">To update values you need the following set of information:</span></span>

    -   <span data-ttu-id="cbe10-362">平均位元速率：從在媒體類型協商期間選取的輸出媒體類型上，取得 [**MF \_ MT \_ 音訊 \_ \_ \_ 每 \_ 秒平均位元組數**](mf-mt-audio-avg-bytes-per-second-attribute.md) 屬性的平均位元速率。</span><span class="sxs-lookup"><span data-stu-id="cbe10-362">Average bit rate: Get the average bit rate from the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute set on the output media type that is selected during media type negotiation.</span></span>
    -   <span data-ttu-id="cbe10-363">緩衝區視窗：您可以藉由呼叫 [**IWMCodecLeakyBucket：： GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md)來取得它。</span><span class="sxs-lookup"><span data-stu-id="cbe10-363">Buffer window: you can retrieve it by calling [**IWMCodecLeakyBucket::GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).</span></span>
    -   <span data-ttu-id="cbe10-364">初始緩衝區大小：設定為0。</span><span class="sxs-lookup"><span data-stu-id="cbe10-364">Initial buffer size: Set to 0.</span></span>

    <span data-ttu-id="cbe10-365">建立 Dword 陣列，並在音訊串流接收器的 [**MFPKEY \_ ASFSTREAMSINK \_ 更正 \_ LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) 屬性中設定值。</span><span class="sxs-lookup"><span data-stu-id="cbe10-365">Create an array of DWORDs and set the value in the [**MFPKEY\_ASFSTREAMSINK\_CORRECTED\_LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) property of the audio stream sink.</span></span> <span data-ttu-id="cbe10-366">如果您未提供更新的值，媒體會話就會適當地設定這些值。</span><span class="sxs-lookup"><span data-stu-id="cbe10-366">If you do not provide the updated values, the Media Session sets them appropriately.</span></span>

    <span data-ttu-id="cbe10-367">如需詳細資訊，請參閱 [有漏洞 Bucket 緩衝區模型](the-leaky-bucket-buffer-model.md)。</span><span class="sxs-lookup"><span data-stu-id="cbe10-367">For more information, see [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md).</span></span>

<span data-ttu-id="cbe10-368">在步驟5中建立的啟用物件必須新增至拓撲，作為轉換拓撲節點。</span><span class="sxs-lookup"><span data-stu-id="cbe10-368">The activation objects created in step 5 must be added to the topology as transform topology nodes.</span></span> <span data-ttu-id="cbe10-369">如需詳細資訊和程式碼範例，請參閱 [建立轉換節點](creating-transform-nodes.md)中的「從啟用物件建立轉換節點」。</span><span class="sxs-lookup"><span data-stu-id="cbe10-369">For more information and code example, see "Creating a Transform Node from an Activation Object" in [Creating Transform Nodes](creating-transform-nodes.md).</span></span>

<span data-ttu-id="cbe10-370">下列程式碼範例會建立並新增所需的編碼器啟用。</span><span class="sxs-lookup"><span data-stu-id="cbe10-370">The following code example creates and adds the required encoder activates.</span></span> <span data-ttu-id="cbe10-371">它會使用先前建立之拓撲物件的指標、檔案接收的啟用物件和來來源資料流的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="cbe10-371">It takes pointers to a previously created topology object, the file sink's activation object and the source stream's media type.</span></span> <span data-ttu-id="cbe10-372">它也會呼叫 AddOutputNode (請參閱下一個程式碼範例) ，此範例會建立接收節點並將其加入至編碼拓撲中。</span><span class="sxs-lookup"><span data-stu-id="cbe10-372">It also calls AddOutputNode (see next code example) that creates and adds the sink node to the encoding topology.</span></span> <span data-ttu-id="cbe10-373">呼叫端會收到來源拓撲節點的指標。</span><span class="sxs-lookup"><span data-stu-id="cbe10-373">It The caller receives a pointer to the source topology node.</span></span>


```C++
//-------------------------------------------------------------------
//  AddTransformOutputNodes
//  Creates and adds the sink node to the encoding topology.
//  Creates and adds the required encoder activates.

//  pTopology:  A pointer to the topology.
//  pSinkActivate:  A pointer to the file sink's activation object.
//  pSourceType: A pointer to the source stream's media type.
//  ppNode:  Receives a pointer to the topology node.
//-------------------------------------------------------------------

HRESULT AddTransformOutputNodes(
    IMFTopology* pTopology,
    IMFActivate* pSinkActivate,
    IMFMediaType* pSourceType,
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    if (!pTopology || !pSinkActivate || !pSourceType)
    {
        return E_INVALIDARG;
    }

    IMFTopologyNode* pEncNode = NULL;
    IMFTopologyNode* pOutputNode = NULL;
    IMFASFContentInfo* pContentInfo = NULL;
    IMFASFProfile* pProfile = NULL;
    IMFASFStreamConfig* pStream = NULL;
    IMFMediaType* pMediaType = NULL;
    IPropertyStore* pProps = NULL;
    IMFActivate *pEncoderActivate = NULL;
    IMFMediaSink *pSink = NULL; 

    GUID guidMT = GUID_NULL;
    GUID guidMajor = GUID_NULL;

    DWORD cStreams = 0;
    WORD wStreamNumber = 0;

    HRESULT hr = S_OK;
        
    hr = pSourceType->GetMajorType(&guidMajor);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the node.
    hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pEncNode);
    if (FAILED(hr))
    {
        goto done;
    }
    
    //Activate the sink
    hr = pSinkActivate->ActivateObject(__uuidof(IMFMediaSink), (void**)&pSink);
    if (FAILED(hr))
    {
        goto done;
    }
    //find the media type in the sink
    //Get content info from the sink
    hr = pSink->QueryInterface(__uuidof(IMFASFContentInfo), (void**)&pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }
    

    hr = pContentInfo->GetProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->GetStreamCount(&cStreams);
    if (FAILED(hr))
    {
        goto done;
    }

    for(DWORD index = 0; index < cStreams ; index++)
    {
        hr = pProfile->GetStream(index, &wStreamNumber, &pStream);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pStream->GetMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->GetMajorType(&guidMT);
        if (FAILED(hr))
        {
            goto done;
        }
        if (guidMT!=guidMajor)
        {
            SafeRelease(&pStream);
            SafeRelease(&pMediaType);
            guidMT = GUID_NULL;

            continue;
        }
        //We need to activate the encoder
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamNumber, &pProps);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMT == MFMediaType_Audio)
        {
             hr = MFCreateWMAEncoderActivate(pMediaType, pProps, &pEncoderActivate);
            if (FAILED(hr))
            {
                goto done;
            }
            wprintf_s(L"Audio Encoder created. Stream Number: %d .\n", wStreamNumber);

            break;
        }
        if (guidMT == MFMediaType_Video)
        {
            hr = MFCreateWMVEncoderActivate(pMediaType, pProps, &pEncoderActivate);
            if (FAILED(hr))
            {
                goto done;
            }
            wprintf_s(L"Video Encoder created. Stream Number: %d .\n", wStreamNumber);

            break;
        }
    }

    // Set the object pointer.
    hr = pEncNode->SetObject(pEncoderActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pEncNode);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the output node to this node.
    hr = AddOutputNode(pTopology, pSinkActivate, wStreamNumber, &pOutputNode);
    if (FAILED(hr))
    {
        goto done;
    }

    //now we have the output node, connect it to the transform node
    hr = pEncNode->ConnectOutput(0, pOutputNode, 0);
    if (FAILED(hr))
    {
        goto done;
    }

   // Return the pointer to the caller.
    *ppNode = pEncNode;
    (*ppNode)->AddRef();


done:
    SafeRelease(&pEncNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pEncoderActivate);
    SafeRelease(&pMediaType);
    SafeRelease(&pProps);
    SafeRelease(&pStream);
    SafeRelease(&pProfile);
    SafeRelease(&pContentInfo);
    SafeRelease(&pSink);
    return hr;
}
```



### <a name="create-the-output-topology-nodes-for-the-file-sink"></a><span data-ttu-id="cbe10-374">建立檔案接收的輸出拓撲節點</span><span class="sxs-lookup"><span data-stu-id="cbe10-374">Create the Output Topology Nodes for the File Sink</span></span>

<span data-ttu-id="cbe10-375">在此步驟中，您將建立 ASF 檔案接收的輸出拓撲節點。</span><span class="sxs-lookup"><span data-stu-id="cbe10-375">In this step, you will create the output topology node for the ASF file sink.</span></span>

<span data-ttu-id="cbe10-376">若要建立此節點，您需要下列參考：</span><span class="sxs-lookup"><span data-stu-id="cbe10-376">To create this node you need the following references:</span></span>

-   <span data-ttu-id="cbe10-377">您在本教學課程的「建立 ASF 檔案接收」一節所述的步驟中所建立之啟用物件的指標。</span><span class="sxs-lookup"><span data-stu-id="cbe10-377">A pointer to the activation object that you created in the step described in the "Create the ASF File Sink" section of this tutorial.</span></span>
-   <span data-ttu-id="cbe10-378">用來識別已新增至檔案接收之資料流程接收器的資料流程號碼。</span><span class="sxs-lookup"><span data-stu-id="cbe10-378">The stream numbers to identify the stream sinks added to the file sink.</span></span> <span data-ttu-id="cbe10-379">串流號碼符合資料流程建立時所設定的資料流程識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbe10-379">The stream numbers match the stream's identification that was set during stream creation.</span></span>

<span data-ttu-id="cbe10-380">如需有關建立輸出節點和程式碼範例的詳細資訊，請參閱 [建立輸出節點](creating-output-nodes.md)中的「從啟用物件建立輸出節點」。</span><span class="sxs-lookup"><span data-stu-id="cbe10-380">For more information about creating output nodes and code example, see "Creating an Output Node from an Activation Object" in [Creating Output Nodes](creating-output-nodes.md).</span></span>

<span data-ttu-id="cbe10-381">如果您不是使用檔案接收的啟用物件，您必須列舉 ASF 檔案接收中的串流接收器，並將每個資料流程接收設定為拓撲中的輸出節點。</span><span class="sxs-lookup"><span data-stu-id="cbe10-381">If you are not using activation object for the file sink, you must enumerate the stream sinks in the ASF file sink and set each stream sink as the output node in the topology.</span></span> <span data-ttu-id="cbe10-382">如需資料流程接收列舉的詳細資訊，請參閱 [將資料流程資訊新增至 ASF 檔案接收](adding-stream-information-to-the-asf-file-sink.md)中的「列舉資料流程接收器」。</span><span class="sxs-lookup"><span data-stu-id="cbe10-382">For information about stream sink enumeration, see "Enumerating Stream Sinks" in [Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md).</span></span>

<span data-ttu-id="cbe10-383">下列程式碼範例會建立接收節點，並將其加入至編碼拓撲。</span><span class="sxs-lookup"><span data-stu-id="cbe10-383">The following code example creates and adds the sink node to the encoding topology.</span></span> <span data-ttu-id="cbe10-384">它會使用先前建立之拓撲物件的指標、檔案接收的啟用物件和資料流程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbe10-384">It takes pointers to a previously created topology object, the file sink's activation object and the stream's identification number.</span></span> <span data-ttu-id="cbe10-385">呼叫端會收到來源拓撲節點的指標。</span><span class="sxs-lookup"><span data-stu-id="cbe10-385">It The caller receives a pointer to the source topology node.</span></span>


```C++
// Add an output node to a topology.
HRESULT AddOutputNode(
    IMFTopology *pTopology,     // Topology.
    IMFActivate *pActivate,     // Media sink activation object.
    DWORD dwId,                 // Identifier of the stream sink.
    IMFTopologyNode **ppNode)   // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_OUTPUT_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the object pointer.
    hr = pNode->SetObject(pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the stream sink ID attribute.
    hr = pNode->SetUINT32(MF_TOPONODE_STREAMID, dwId);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUINT32(MF_TOPONODE_NOSHUTDOWN_ON_REMOVE, FALSE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



<span data-ttu-id="cbe10-386">下列程式碼範例會列舉指定媒體接收器的資料流程接收。</span><span class="sxs-lookup"><span data-stu-id="cbe10-386">The following code example enumerates the stream sinks for a given media sink.</span></span>


```C++
//-------------------------------------------------------------------
//  EnumerateStreamSinks
//  Enumerates the stream sinks within the specified media sink.
//
//  pSink:  A pointer to the media sink.
//-------------------------------------------------------------------
HRESULT EnumerateStreamSinks (IMFMediaSink* pSink)
{
    if (!pSink)
    {
        return E_INVALIDARG;
    }
    
    IMFStreamSink* pStreamSink = NULL;
    DWORD cStreamSinks = 0;

    HRESULT hr = pSink->GetStreamSinkCount(&cStreamSinks);
    if (FAILED(hr))
    {
        goto done;
    }

    for(DWORD index = 0; index < cStreamSinks; index++)
    {
        hr = pSink->GetStreamSinkByIndex (index, &pStreamSink);
        if (FAILED(hr))
        {
            goto done;
        }

        //Use the stream sink
        //Not shown.
    }
done:
    SafeRelease(&pStreamSink);

    return hr;
}
```



### <a name="connect-the-source-transform-and-sink-nodes"></a><span data-ttu-id="cbe10-387">連接來源、轉換和接收節點</span><span class="sxs-lookup"><span data-stu-id="cbe10-387">Connect the Source, Transform, and Sink Nodes</span></span>

<span data-ttu-id="cbe10-388">在此步驟中，您會將來源節點連接到參考該編碼的轉換節點，並啟用您在本教學課程的 < 具現化必要的編碼器和建立轉換節點的步驟中所述的步驟中所建立的轉換節點。</span><span class="sxs-lookup"><span data-stu-id="cbe10-388">In this step, you will connect the source node to the transform node referencing the encoding activates that you created in the step described in the "Instantiate the Required Encoders and Create the Transform Nodes" section of this tutorial.</span></span> <span data-ttu-id="cbe10-389">[轉換] 節點將連接至輸出節點，其中包含 file 接收的啟用物件。</span><span class="sxs-lookup"><span data-stu-id="cbe10-389">The transform node will be connected to the output node containing the activation object for the file sink.</span></span>

## <a name="handling-the-encoding-session"></a><span data-ttu-id="cbe10-390">處理編碼會話</span><span class="sxs-lookup"><span data-stu-id="cbe10-390">Handling the Encoding Session</span></span>

<span data-ttu-id="cbe10-391">在步驟中，您將執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="cbe10-391">In the step, you will perform the following steps:</span></span>

1.  <span data-ttu-id="cbe10-392">呼叫 [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) 來建立編碼會話。</span><span class="sxs-lookup"><span data-stu-id="cbe10-392">Call [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create an encoding session.</span></span>
2.  <span data-ttu-id="cbe10-393">呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) 來設定會話的編碼拓撲。</span><span class="sxs-lookup"><span data-stu-id="cbe10-393">Call [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) to set the encoding topology on the session.</span></span> <span data-ttu-id="cbe10-394">如果呼叫完成，媒體會話就會評估拓撲節點，並插入其他轉換物件，例如將指定的壓縮來源轉換成未壓縮樣本的解碼器，以作為編碼器的輸入。</span><span class="sxs-lookup"><span data-stu-id="cbe10-394">If the call completes, the Media Session evaluates the topology nodes and inserts additional transform objects such as a decoder that converts the specified compressed source to uncompressed samples to feed as input to the encoder.</span></span>
3.  <span data-ttu-id="cbe10-395">呼叫 [**IMFMediaSession：： GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) ，以要求媒體會話所引發的事件。</span><span class="sxs-lookup"><span data-stu-id="cbe10-395">Call [**IMFMediaSession::GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) to request for the events raised by the Media Session.</span></span>

    <span data-ttu-id="cbe10-396">在事件迴圈中，您將會根據媒體會話所引發的事件，啟動並關閉編碼會話。</span><span class="sxs-lookup"><span data-stu-id="cbe10-396">In the event loop you will start and close the encoding session depending on the events raised by the Media Session.</span></span> <span data-ttu-id="cbe10-397">[**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)呼叫會產生媒體會話，並使用已設定的 MF [](mesessiontopologystatus.md) \_ TOPOSTATUS 就緒旗標來引發 MESessionTopologyStatus 事件 \_ 。</span><span class="sxs-lookup"><span data-stu-id="cbe10-397">The [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) call results in Media Session raising the [MESessionTopologyStatus](mesessiontopologystatus.md) event with the MF\_TOPOSTATUS\_READY flag set.</span></span> <span data-ttu-id="cbe10-398">所有事件都是以非同步方式產生，而應用程式可以同步或非同步方式抓取這些事件。</span><span class="sxs-lookup"><span data-stu-id="cbe10-398">All events are generated asynchronously and an application can retrieve these events synchronously or asynchronously.</span></span> <span data-ttu-id="cbe10-399">因為本教學課程中的應用程式是主控台應用程式，而且封鎖使用者介面執行緒並不是問題，所以我們會以同步方式從媒體會話取得事件。</span><span class="sxs-lookup"><span data-stu-id="cbe10-399">Because the application in this tutorial is a console application and blocking user interface threads is not a concern, we will get the events from Media Session synchronously.</span></span>

    <span data-ttu-id="cbe10-400">若要以非同步方式取得事件，您的應用程式必須執行 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面。</span><span class="sxs-lookup"><span data-stu-id="cbe10-400">To get the events asynchronously, your application must implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> <span data-ttu-id="cbe10-401">如需此介面的詳細資訊和範例執行，請參閱 [如何使用媒體基礎播放媒體](how-to-play-unprotected-media-files.md)檔案中的「處理會話事件」。</span><span class="sxs-lookup"><span data-stu-id="cbe10-401">For more information and an example implementation of this interface, see "Handling Session Events" in [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span>

<span data-ttu-id="cbe10-402">在取得媒體會話事件的事件迴圈中，等候 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)完成且拓撲已解決時所引發的 [MESessionTopologyStatus](mesessiontopologystatus.md)事件。</span><span class="sxs-lookup"><span data-stu-id="cbe10-402">In the event loop for getting Media Session events, wait for the [MESessionTopologyStatus](mesessiontopologystatus.md) event that is raised when the [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) completes and the topology is resolved.</span></span> <span data-ttu-id="cbe10-403">取得 MESessionTopologyStatus 事件時，請呼叫 [**IMFMediaSession：： start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)來啟動編碼會話。</span><span class="sxs-lookup"><span data-stu-id="cbe10-403">Upon getting the MESessionTopologyStatus event, start the encoding session by calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span> <span data-ttu-id="cbe10-404">當所有編碼作業都完成時，媒體會話就會產生 [MEEndOfPresentation](meendofpresentation.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="cbe10-404">The Media Session generates the [MEEndOfPresentation](meendofpresentation.md) event when all of the encoding operations are complete.</span></span> <span data-ttu-id="cbe10-405">此事件必須針對 VBR 編碼進行處理，並在本教學課程的下一節「針對 VBR 編碼的檔案接收更新編碼屬性」中加以討論。</span><span class="sxs-lookup"><span data-stu-id="cbe10-405">This event must be handled for VBR encoding and is discussed in the next section "Update Encoding Properties on the File Sink for VBR Encoding" of this tutorial.</span></span>

<span data-ttu-id="cbe10-406">媒體會話會產生 ASF 標頭物件，並在編碼會話完成時完成檔案，然後引發 [MESessionClosed](mesessionclosed.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="cbe10-406">The Media Session generates the ASF Header Object and finalizes the file when the encoding session completes and then raises the [MESessionClosed](mesessionclosed.md) event.</span></span> <span data-ttu-id="cbe10-407">此事件必須透過在媒體會話執行適當的關機操作來處理。</span><span class="sxs-lookup"><span data-stu-id="cbe10-407">This event must be handled by performing proper shutdown operations on the Media Session.</span></span> <span data-ttu-id="cbe10-408">若要開始關機作業，請呼叫 [**IMFMediaSession：： shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown)。</span><span class="sxs-lookup"><span data-stu-id="cbe10-408">To begin the shutdown operations, call [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span> <span data-ttu-id="cbe10-409">在編碼會話關閉之後，您就無法在相同的媒體會話實例上設定另一個要進行編碼的拓朴。</span><span class="sxs-lookup"><span data-stu-id="cbe10-409">After the encoding session is closed, you cannot set another topology for encoding on the same Media Session instance.</span></span> <span data-ttu-id="cbe10-410">若要編碼另一個檔案，必須關閉並釋放目前的媒體會話，且必須在新建立的媒體會話上設定新的拓撲。</span><span class="sxs-lookup"><span data-stu-id="cbe10-410">To encode another file, the current Media Session must be closed and released and the new topology must be set on a newly created Media Session.</span></span> <span data-ttu-id="cbe10-411">下列程式碼範例會建立媒體會話、設定編碼拓撲，以及處理媒體會話事件。</span><span class="sxs-lookup"><span data-stu-id="cbe10-411">The following code example creates the Media Session, sets the encoding topology and handles the Media Session events.</span></span>

<span data-ttu-id="cbe10-412">下列程式碼範例會建立媒體會話、設定編碼拓撲，以及藉由處理來自媒體會話的事件來控制編碼會話。</span><span class="sxs-lookup"><span data-stu-id="cbe10-412">The following code example creates the Media Session, sets the encoding topology, and controls the encoding session by handling events from the Media Session.</span></span>


```C++
//-------------------------------------------------------------------
//  Encode
//  Controls the encoding session and handles events from the media session.
//
//  pTopology:  A pointer to the encoding topology.
//-------------------------------------------------------------------

HRESULT Encode(IMFTopology *pTopology)
{
    if (!pTopology)
    {
        return E_INVALIDARG;
    }
    
    IMFMediaSession *pSession = NULL;
    IMFMediaEvent* pEvent = NULL;
    IMFTopology* pFullTopology = NULL;
    IUnknown* pTopoUnk = NULL;


    MediaEventType meType = MEUnknown;  // Event type

    HRESULT hr = S_OK;
    HRESULT hrStatus = S_OK;            // Event status
                
    MF_TOPOSTATUS TopoStatus = MF_TOPOSTATUS_INVALID; // Used with MESessionTopologyStatus event.    
        

    hr = MFCreateMediaSession(NULL, &pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSession->SetTopology(MFSESSION_SETTOPOLOGY_IMMEDIATE, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get media session events synchronously
    while (1)
    {
        hr = pSession->GetEvent(0, &pEvent);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEvent->GetType(&meType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEvent->GetStatus(&hrStatus);
        if (FAILED(hr))
        {
            goto done;
        }
        if (FAILED(hrStatus))
        {
            hr = hrStatus;
            goto done;
        }

       switch(meType)
        {
            case MESessionTopologyStatus:
                {
                    // Get the status code.
                    MF_TOPOSTATUS status = (MF_TOPOSTATUS)MFGetAttributeUINT32(
                                             pEvent, MF_EVENT_TOPOLOGY_STATUS, MF_TOPOSTATUS_INVALID);

                    if (status == MF_TOPOSTATUS_READY)
                    {
                        PROPVARIANT var;
                        PropVariantInit(&var);
                        wprintf_s(L"Topology resolved and set on the media session.\n");

                        hr = pSession->Start(NULL, &var);
                        if (FAILED(hr))
                        {
                            goto done;
                        }

                    }
                    if (status == MF_TOPOSTATUS_STARTED_SOURCE)
                    {
                        wprintf_s(L"Encoding started.\n");
                        break;
                    }
                    if (status == MF_TOPOSTATUS_ENDED)
                    {
                        wprintf_s(L"Encoding complete.\n");
                        hr = pSession->Close();
                        if (FAILED(hr))
                        {
                            goto done;
                        }

                        break;
                    }
                }
                break;


            case MESessionEnded:
                wprintf_s(L"Encoding complete.\n");
                hr = pSession->Close();
                if (FAILED(hr))
                {
                    goto done;
                }
                break;

            case MEEndOfPresentation:
                {
                    if (EncodingMode == VBR)
                    {
                        hr = pSession->GetFullTopology(MFSESSION_GETFULLTOPOLOGY_CURRENT, 0, &pFullTopology);
                        if (FAILED(hr))
                        {
                            goto done;
                        }
                        hr = PostEncodingUpdate(pFullTopology);
                        if (FAILED(hr))
                        {
                            goto done;
                        }
                        wprintf_s(L"Updated sinks for VBR. \n");
                    }
                }
                break;

            case MESessionClosed:
                wprintf_s(L"Encoding session closed.\n");

                hr = pSession->Shutdown();
                goto done;
        }
        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pEvent);

    }
done:
    SafeRelease(&pEvent);
    SafeRelease(&pSession);
    SafeRelease(&pFullTopology);
    SafeRelease(&pTopoUnk);
    return hr;
}
```



## <a name="update-encoding-properties-in-the-file-sink"></a><span data-ttu-id="cbe10-413">更新 File 接收器中的編碼屬性</span><span class="sxs-lookup"><span data-stu-id="cbe10-413">Update Encoding Properties in the File Sink</span></span>

<span data-ttu-id="cbe10-414">某些編碼屬性（例如編碼位元速率和精確的有漏洞值區值）在編碼完成之前都是未知的，特別是針對 VBR 編碼。</span><span class="sxs-lookup"><span data-stu-id="cbe10-414">Certain encoding properties such as the encoding bit rate and the accurate leaky bucket values are not known until the encoding is complete, especially for VBR encoding.</span></span> <span data-ttu-id="cbe10-415">若要取得正確的值，應用程式必須等待 [MEEndOfPresentation](meendofpresentation.md) 事件，指出編碼會話已完成。</span><span class="sxs-lookup"><span data-stu-id="cbe10-415">To get the correct values the application must wait for the [MEEndOfPresentation](meendofpresentation.md) event that indicates that the encoding session is complete.</span></span> <span data-ttu-id="cbe10-416">有漏洞值區值必須在接收中更新，如此 ASF 標頭物件才能反映正確的值。</span><span class="sxs-lookup"><span data-stu-id="cbe10-416">The leaky bucket values must be updated in the sink so that the ASF Header Object can reflect the accurate values.</span></span>

<span data-ttu-id="cbe10-417">下列程式說明在編碼拓撲中執行節點以取得 file sink 節點，並設定必要的有漏洞 bucket 屬性所需的步驟。</span><span class="sxs-lookup"><span data-stu-id="cbe10-417">The following procedure describes the steps required to traverse the nodes in the encoding topology to get the file sink node and set the required leaky bucket properties.</span></span>

<span data-ttu-id="cbe10-418">**更新 ASF 檔案接收的 post 編碼屬性值**</span><span class="sxs-lookup"><span data-stu-id="cbe10-418">**To update the post encoding property values on the ASF file sink**</span></span>

1.  <span data-ttu-id="cbe10-419">呼叫 [**IMFTopology：： GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) ，以從編碼拓撲取得輸出節點集合。</span><span class="sxs-lookup"><span data-stu-id="cbe10-419">Call [**IMFTopology::GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) to get the output node collection from the encoding topology.</span></span>
2.  <span data-ttu-id="cbe10-420">針對每個節點，藉由呼叫 [**IMFTopologyNode：： GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject)來取得節點中資料流程接收的指標。</span><span class="sxs-lookup"><span data-stu-id="cbe10-420">For each node, get a pointer to the stream sink in the node by calling [**IMFTopologyNode::GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject).</span></span> <span data-ttu-id="cbe10-421">在 **IMFTopologyNode：： GetObject** 傳回的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)指標上查詢 [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)介面。</span><span class="sxs-lookup"><span data-stu-id="cbe10-421">Query for the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface on the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer returned by **IMFTopologyNode::GetObject**.</span></span>
3.  <span data-ttu-id="cbe10-422">針對每個串流接收，藉由呼叫 [**IMFTopologyNode：： >getinput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinput)取得下游節點 (編碼器) 。</span><span class="sxs-lookup"><span data-stu-id="cbe10-422">For each stream sink get the downstream node (encoder) by calling [**IMFTopologyNode::GetInput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinput).</span></span>
4.  <span data-ttu-id="cbe10-423">查詢節點，以從編碼器節點取得 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 指標。</span><span class="sxs-lookup"><span data-stu-id="cbe10-423">Query the node to get the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) pointer from the encoder node.</span></span>
5.  <span data-ttu-id="cbe10-424">查詢 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 指標的編碼器，以從編碼器取得編碼屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="cbe10-424">Query the encoder for the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to get the encoding property store from the encoder.</span></span>
6.  <span data-ttu-id="cbe10-425">查詢 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 指標的串流接收器，以取得資料流程接收的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="cbe10-425">Query the stream sink for the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to get the stream sink's property store.</span></span>
7.  <span data-ttu-id="cbe10-426">呼叫 [**IPropertyStore：： GetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 以從編碼器的屬性存放區取得必要的屬性值，並藉由呼叫 **IPropertyStore：： SetValue**，將它們複製到資料流程接收器的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="cbe10-426">Call [**IPropertyStore::GetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore) to get the required property values from the encoder's property store and copy them to the stream sink's property store by calling **IPropertyStore::SetValue**.</span></span>

<span data-ttu-id="cbe10-427">下表顯示必須在影片資料流程的串流接收上設定的 post 編碼屬性值。</span><span class="sxs-lookup"><span data-stu-id="cbe10-427">The following table shows the post encoding property values that must be set on the stream sink for the video stream.</span></span>



| <span data-ttu-id="cbe10-428">編碼類型</span><span class="sxs-lookup"><span data-stu-id="cbe10-428">Encoding type</span></span>                                                                                  | <span data-ttu-id="cbe10-429">屬性名稱 (GetValue) </span><span class="sxs-lookup"><span data-stu-id="cbe10-429">Property name (GetValue)</span></span>                                                                        | <span data-ttu-id="cbe10-430">屬性名稱 (SetValue) </span><span class="sxs-lookup"><span data-stu-id="cbe10-430">Property name (SetValue)</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbe10-431">常數位元速率編碼</span><span class="sxs-lookup"><span data-stu-id="cbe10-431">Constant Bit Rate Encoding</span></span>](constant-bit-rate-encoding.md)                                   | <span data-ttu-id="cbe10-432">MFPKEY \_ BAVG</span><span class="sxs-lookup"><span data-stu-id="cbe10-432">MFPKEY\_BAVG</span></span><br/> <span data-ttu-id="cbe10-433">MFPKEY \_ RAVG</span><span class="sxs-lookup"><span data-stu-id="cbe10-433">MFPKEY\_RAVG</span></span><br/>                                                 | <span data-ttu-id="cbe10-434">MFPKEY \_ STAT \_ BAVG</span><span class="sxs-lookup"><span data-stu-id="cbe10-434">MFPKEY\_STAT\_BAVG</span></span><br/> <span data-ttu-id="cbe10-435">MFPKEY \_ STAT \_ RAVG</span><span class="sxs-lookup"><span data-stu-id="cbe10-435">MFPKEY\_STAT\_RAVG</span></span><br/>                                                             |
| [<span data-ttu-id="cbe10-436">以品質為基礎的變數位元速率編碼</span><span class="sxs-lookup"><span data-stu-id="cbe10-436">Quality-Based Variable Bit Rate Encoding</span></span>](quality-based-variable-bit-rate--vbr--encoding.md) | <span data-ttu-id="cbe10-437">MFPKEY \_ BAVG</span><span class="sxs-lookup"><span data-stu-id="cbe10-437">MFPKEY\_BAVG</span></span><br/> <span data-ttu-id="cbe10-438">MFPKEY \_ RAVG</span><span class="sxs-lookup"><span data-stu-id="cbe10-438">MFPKEY\_RAVG</span></span><br/> <span data-ttu-id="cbe10-439">MFPKEY \_ BMAX</span><span class="sxs-lookup"><span data-stu-id="cbe10-439">MFPKEY\_BMAX</span></span><br/> <span data-ttu-id="cbe10-440">MFPKEY \_ RMAX</span><span class="sxs-lookup"><span data-stu-id="cbe10-440">MFPKEY\_RMAX</span></span><br/> | <span data-ttu-id="cbe10-441">MFPKEY \_ STAT \_ BAVG</span><span class="sxs-lookup"><span data-stu-id="cbe10-441">MFPKEY\_STAT\_BAVG</span></span><br/> <span data-ttu-id="cbe10-442">MFPKEY \_ STAT \_ RAVG</span><span class="sxs-lookup"><span data-stu-id="cbe10-442">MFPKEY\_STAT\_RAVG</span></span><br/> <span data-ttu-id="cbe10-443">MFPKEY \_ STAT \_ BMAX</span><span class="sxs-lookup"><span data-stu-id="cbe10-443">MFPKEY\_STAT\_BMAX</span></span><br/> <span data-ttu-id="cbe10-444">MFPKEY \_ STAT \_ RMAX</span><span class="sxs-lookup"><span data-stu-id="cbe10-444">MFPKEY\_STAT\_RMAX</span></span><br/> |



 

<span data-ttu-id="cbe10-445">下列程式碼範例會設定編碼後屬性值。</span><span class="sxs-lookup"><span data-stu-id="cbe10-445">The following code example sets the post-encoding property values.</span></span>


```C++
//-------------------------------------------------------------------
//  PostEncodingUpdate
//  Updates the file sink with encoding properties set on the encoder
//  during the encoding session.
    //1. Get the output nodes
    //2. For each node, get the downstream node
    //3. For the downstream node, get the MFT
    //4. Get the property store
    //5. Get the required values
    //6. Set them on the stream sink
//
//  pTopology: A pointer to the full topology retrieved from the media session.
//-------------------------------------------------------------------

HRESULT PostEncodingUpdate(IMFTopology *pTopology)
{
    if (!pTopology)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_OK;

    IMFCollection* pOutputColl = NULL;
    IUnknown* pNodeUnk = NULL;
    IMFMediaType* pType = NULL;
    IMFTopologyNode* pNode = NULL;
    IUnknown* pSinkUnk = NULL;
    IMFStreamSink* pStreamSink = NULL;
    IMFTopologyNode* pEncoderNode = NULL;
    IUnknown* pEncoderUnk = NULL;
    IMFTransform* pEncoder = NULL;
    IPropertyStore* pStreamSinkProps = NULL;
    IPropertyStore* pEncoderProps = NULL;

    GUID guidMajorType = GUID_NULL;

    PROPVARIANT var;
    PropVariantInit( &var );

    DWORD cElements = 0;

    hr = pTopology->GetOutputNodeCollection( &pOutputColl);
    if (FAILED(hr))
    {
        goto done;
    }


    hr = pOutputColl->GetElementCount(&cElements);
    if (FAILED(hr))
    {
        goto done;
    }


    for(DWORD index = 0; index < cElements; index++)
    {
        hr = pOutputColl->GetElement(index, &pNodeUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNodeUnk->QueryInterface(IID_IMFTopologyNode, (void**)&pNode);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetInputPrefType(0, &pType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pType->GetMajorType( &guidMajorType );
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetObject(&pSinkUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pSinkUnk->QueryInterface(IID_IMFStreamSink, (void**)&pStreamSink);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetInput( 0, &pEncoderNode, NULL );
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoderNode->GetObject(&pEncoderUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoderUnk->QueryInterface(IID_IMFTransform, (void**)&pEncoder);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStreamSink->QueryInterface(IID_IPropertyStore, (void**)&pStreamSinkProps);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoder->QueryInterface(IID_IPropertyStore, (void**)&pEncoderProps);
        if (FAILED(hr))
        {
            goto done;
        }

        if( guidMajorType == MFMediaType_Video )
        {            
            hr = pEncoderProps->GetValue( MFPKEY_BAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_RAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RAVG, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_BMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_RMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }
        }
        else if( guidMajorType == MFMediaType_Audio )
        {      
            hr = pEncoderProps->GetValue( MFPKEY_STAT_BAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }
            
            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_RAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }
            
            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_BMAX, &var);
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_RMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RMAX, var );         
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_WMAENC_AVGBYTESPERSEC, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_WMAENC_AVGBYTESPERSEC, var );         
            if (FAILED(hr))
            {
                goto done;
            }
        } 
        PropVariantClear( &var ); 
   }
done:
    SafeRelease (&pOutputColl);
    SafeRelease (&pNodeUnk);
    SafeRelease (&pType);
    SafeRelease (&pNode);
    SafeRelease (&pSinkUnk);
    SafeRelease (&pStreamSink);
    SafeRelease (&pEncoderNode);
    SafeRelease (&pEncoderUnk);
    SafeRelease (&pEncoder);
    SafeRelease (&pStreamSinkProps);
    SafeRelease (&pEncoderProps);

    return hr;
   
}
```



## <a name="implement-main"></a><span data-ttu-id="cbe10-446">執行 Main</span><span class="sxs-lookup"><span data-stu-id="cbe10-446">Implement Main</span></span>

<span data-ttu-id="cbe10-447">下列程式碼範例顯示主控台應用程式的主要功能。</span><span class="sxs-lookup"><span data-stu-id="cbe10-447">The following code example shows the main function of your console application.</span></span>


```C++
int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 4)
    {
        wprintf_s(L"Usage: %s inputaudio.mp3, %s output.wm*, %Encoding Type: CBR, VBR\n");
        return 0;
    }


    HRESULT             hr = S_OK;

    IMFMediaSource* pSource = NULL;
    IMFTopology* pTopology = NULL;
    IMFActivate* pFileSinkActivate = NULL;

    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
    if (FAILED(hr))
    {
        goto done;
    }

    //Set the requested encoding mode
    if (wcscmp(argv[3], L"CBR")==0)
    {
        EncodingMode = CBR;
    }
    else if (wcscmp(argv[3], L"VBR")==0)
    {
        EncodingMode = VBR;
    }
    else
    {
        EncodingMode = CBR;
    }

    // Start up Media Foundation platform.
    hr = MFStartup(MF_VERSION);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the media source
    hr = CreateMediaSource(argv[1], &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the file sink activate
    hr = CreateMediaSink(argv[2], pSource, &pFileSinkActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    //Build the encoding topology.
    hr = BuildPartialTopology(pSource, pFileSinkActivate, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Instantiate the media session and start encoding
    hr = Encode(pTopology);
    if (FAILED(hr))
    {
        goto done;
    }


done:
    // Clean up.
    SafeRelease(&pSource);
    SafeRelease(&pTopology);
    SafeRelease(&pFileSinkActivate);

    MFShutdown();
    CoUninitialize();

    if (FAILED(hr))
    {
        wprintf_s(L"Could not create the output file due to 0x%X\n", hr);
    }
    return 0;
}
```



## <a name="test-the-output-file"></a><span data-ttu-id="cbe10-448">測試輸出檔案</span><span class="sxs-lookup"><span data-stu-id="cbe10-448">Test the Output File</span></span>

<span data-ttu-id="cbe10-449">下列清單描述測試編碼檔案的檢查清單。</span><span class="sxs-lookup"><span data-stu-id="cbe10-449">The following list describes a check list for testing the encoded file.</span></span> <span data-ttu-id="cbe10-450">您可以在 [檔案屬性] 對話方塊中選取這些值，方法是以滑鼠右鍵按一下編碼的檔案，然後從內容功能表中選取 [ **屬性** ]。</span><span class="sxs-lookup"><span data-stu-id="cbe10-450">These values can be checked in the file properties dialog box that you can display by right-clicking the encoded file and selecting **Properties** from the context menu.</span></span>

-   <span data-ttu-id="cbe10-451">編碼檔案的路徑是正確的。</span><span class="sxs-lookup"><span data-stu-id="cbe10-451">The path of the encoded file is accurate.</span></span>
-   <span data-ttu-id="cbe10-452">檔案大小超過零 KB，且播放持續時間符合原始程式檔的持續時間。</span><span class="sxs-lookup"><span data-stu-id="cbe10-452">The size of the file is more than zero KB and the play duration matches the source file's duration.</span></span>
-   <span data-ttu-id="cbe10-453">若為影片串流，請檢查框架寬度和高度（畫面播放速率）。</span><span class="sxs-lookup"><span data-stu-id="cbe10-453">For the video stream, check the frame width and height, frame rate.</span></span> <span data-ttu-id="cbe10-454">這些值應該符合您在「建立 ASF 設定檔物件」一節所述的步驟中所建立的 ASF 設定檔中所指定的值。</span><span class="sxs-lookup"><span data-stu-id="cbe10-454">These values should match the values that you specified in the ASF profile that you created in the step described in the section "Create the ASF Profile Object".</span></span>
-   <span data-ttu-id="cbe10-455">若為音訊串流，位元速率必須接近您在目標媒體類型上所指定的值。</span><span class="sxs-lookup"><span data-stu-id="cbe10-455">For the audio stream, the bit rate must be close to the value you specified on the target media type.</span></span>
-   <span data-ttu-id="cbe10-456">在 Windows Media Player 中開啟檔案，並檢查編碼的品質。</span><span class="sxs-lookup"><span data-stu-id="cbe10-456">Open the file in Windows Media Player and check the quality of the encoding.</span></span>
-   <span data-ttu-id="cbe10-457">在 ASFViewer 中開啟 ASF 檔案，以查看 ASF 檔案的結構。</span><span class="sxs-lookup"><span data-stu-id="cbe10-457">Open the ASF file in ASFViewer to see the structure of an ASF file.</span></span> <span data-ttu-id="cbe10-458">您可以從這個 [Microsoft 網站](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea)下載此工具。</span><span class="sxs-lookup"><span data-stu-id="cbe10-458">This tool can be downloaded from this [Microsoft website](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span></span>

## <a name="common-error-codes-and-debugging-tips"></a><span data-ttu-id="cbe10-459">常見的錯誤碼和調試秘訣</span><span class="sxs-lookup"><span data-stu-id="cbe10-459">Common Error Codes and Debugging Tips</span></span>

<span data-ttu-id="cbe10-460">下列清單描述您可能會收到的一般錯誤碼和偵錯工具提示。</span><span class="sxs-lookup"><span data-stu-id="cbe10-460">The following list describes the common error codes that your might receive and the debugging tips.</span></span>

-   <span data-ttu-id="cbe10-461">呼叫 [**IMFSourceResolver：： CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) 會停止應用程式。</span><span class="sxs-lookup"><span data-stu-id="cbe10-461">The call to [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) stalls the application.</span></span>

    <span data-ttu-id="cbe10-462">藉由呼叫 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup)，確定您已初始化媒體基礎平臺。</span><span class="sxs-lookup"><span data-stu-id="cbe10-462">Make sure that you have initialized the Media Foundation platform by calling [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span></span> <span data-ttu-id="cbe10-463">此函式會設定非同步平臺，以供所有在內部啟動非同步作業的方法（例如 [**IMFSourceResolver：： CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)）使用。</span><span class="sxs-lookup"><span data-stu-id="cbe10-463">This function sets up the asynchronous platform that is used by all methods that start asynchronous operations, such as [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), internally.</span></span>

-   <span data-ttu-id="cbe10-464">[**IMFSourceResolver：： CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) 會傳回 HRESULT 0X80070002」，系統找不到指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="cbe10-464">[**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) returns HRESULT 0x80070002 "The system cannot find the file specified.</span></span>

    <span data-ttu-id="cbe10-465">請確定使用者在第一個引數中所指定的輸入檔名稱是否存在。</span><span class="sxs-lookup"><span data-stu-id="cbe10-465">Make sure that the input file name specified by the user in the first argument exists.</span></span>

-   <span data-ttu-id="cbe10-466">HRESULT 0x80070020 「進程無法存取檔案，因為另一個進程正在使用該檔案。</span><span class="sxs-lookup"><span data-stu-id="cbe10-466">HRESULT 0x80070020 "The process cannot access the file because it is being used by another process.</span></span> <span data-ttu-id="cbe10-467">"</span><span class="sxs-lookup"><span data-stu-id="cbe10-467">"</span></span>

    <span data-ttu-id="cbe10-468">請確定系統中的其他資源目前並未使用輸入和輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="cbe10-468">Make sure that the input and the output files are not currently in use by another resource in the system.</span></span>

-   <span data-ttu-id="cbe10-469">呼叫 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 方法會傳回 MF \_ E \_ INVALIDMEDIATYPE。</span><span class="sxs-lookup"><span data-stu-id="cbe10-469">Calls to [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) methods return MF\_E\_INVALIDMEDIATYPE.</span></span>

    <span data-ttu-id="cbe10-470">請確定下列條件成立：</span><span class="sxs-lookup"><span data-stu-id="cbe10-470">Make sure that the following conditions are true:</span></span>

    -   <span data-ttu-id="cbe10-471">輸入類型或您指定的輸出類型與編碼器支援的媒體類型相容。</span><span class="sxs-lookup"><span data-stu-id="cbe10-471">The input type or the output type that you specified is compatible with media types that the encoder supports.</span></span>
    -   <span data-ttu-id="cbe10-472">您指定的媒體類型已完成。</span><span class="sxs-lookup"><span data-stu-id="cbe10-472">The media types that you specified are complete.</span></span> <span data-ttu-id="cbe10-473">若要完成媒體類型，請參閱本教學課程的「建立壓縮的音訊媒體類型」和「建立壓縮的影片媒體類型」一節中的必要屬性。</span><span class="sxs-lookup"><span data-stu-id="cbe10-473">For media types to be complete, see the required attributes in the "Create a Compressed Audio Media Type" and "Create a Compressed Video Media Type" sections of this tutorial.</span></span>
    -   <span data-ttu-id="cbe10-474">請確定您已在要新增編解碼器私用資料的部分媒體類型上設定目標位速率。</span><span class="sxs-lookup"><span data-stu-id="cbe10-474">Make sure that you have set the target bit rate on the partial media type to which you are adding the codec private data.</span></span>

-   <span data-ttu-id="cbe10-475">媒體會話會 \_ \_ 在事件狀態中傳回 MF E 不支援 \_ \_ 的 D3D 類型。</span><span class="sxs-lookup"><span data-stu-id="cbe10-475">The Media Session returns MF\_E\_UNSUPPORTED\_D3D\_TYPE in the event status.</span></span>

    <span data-ttu-id="cbe10-476">當來源的媒體類型指出 Windows Media 視訊編碼器不支援的混合交錯模式時，會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="cbe10-476">This error is returned when the source's media type indicates a mixed interlace mode that is not supported by Windows Media Video encoder.</span></span> <span data-ttu-id="cbe10-477">如果您的壓縮影片媒體類型設定為使用漸進模式，則管線必須使用取消交錯轉換。</span><span class="sxs-lookup"><span data-stu-id="cbe10-477">If your compressed video media type is set to use progressive mode, the pipeline must use a de-interlacing transform.</span></span> <span data-ttu-id="cbe10-478">因為管線找不到符合 (此錯誤碼) 指出的相符，所以您必須手動在解碼器和編碼器節點之間插入 interlacer (轉碼 video 處理器) 。</span><span class="sxs-lookup"><span data-stu-id="cbe10-478">Because the pipeline is unable to find a match (indicated by this error code), you must insert a de-interlacer (transcode video processor) between the decoder and encoder nodes manually.</span></span>

-   <span data-ttu-id="cbe10-479">媒體會話會傳回 \_ 事件狀態中的 E INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="cbe10-479">The Media Session returns E\_INVALIDARG in the event status.</span></span>

    <span data-ttu-id="cbe10-480">當來源的媒體類型屬性與 Windows Media 編碼器上設定之輸出媒體類型的屬性不相容時，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="cbe10-480">This error is returned when the source's media type attributes are not compatible with the attributes of the output media type set on the Windows Media encoder.</span></span>

-   <span data-ttu-id="cbe10-481">[**IWMCodecPrivateData：： GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) 會傳回 HRESULT 0x80040203 「嘗試評估查詢字串時發生語法錯誤」</span><span class="sxs-lookup"><span data-stu-id="cbe10-481">[**IWMCodecPrivateData::GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) returns HRESULT 0x80040203 "A syntax error occurred trying to evaluate a query string"</span></span>

    <span data-ttu-id="cbe10-482">請確定已在編碼器 MFT 上設定輸入類型。</span><span class="sxs-lookup"><span data-stu-id="cbe10-482">Make sure that the input type is set on the encoder MFT.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbe10-483">相關主題</span><span class="sxs-lookup"><span data-stu-id="cbe10-483">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbe10-484">管線層 ASF 元件</span><span class="sxs-lookup"><span data-stu-id="cbe10-484">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> </dl>

 

 
