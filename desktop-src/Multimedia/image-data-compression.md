---
title: Image-Data 壓縮
description: Image-Data 壓縮
ms.assetid: 689cf403-cbb5-4ccb-a05b-0caa617430ed
keywords:
- 影片壓縮管理員 (BC-VCM-LVM-HYPERV) 、影像資料壓縮
- BC-VCM-LVM-HYPERV (視訊壓縮管理員) 、影像資料壓縮
- ICCompress 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8f59a163a9b5a74d2d2fe984417069985fa86a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375080"
---
# <a name="image-data-compression"></a><span data-ttu-id="4b363-106">Image-Data 壓縮</span><span class="sxs-lookup"><span data-stu-id="4b363-106">Image-Data Compression</span></span>

<span data-ttu-id="4b363-107">您的應用程式可以使用一系列的 [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) 函式和宏來壓縮資料。</span><span class="sxs-lookup"><span data-stu-id="4b363-107">Your application can use a series of [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) functions and macros to compress data.</span></span> <span data-ttu-id="4b363-108">函式和宏可協助您執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="4b363-108">The functions and macros can help you perform the following tasks:</span></span>

-   <span data-ttu-id="4b363-109">判斷要用於指定之輸入格式的壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="4b363-109">Determine the compression format to use for a specified input format.</span></span>
-   <span data-ttu-id="4b363-110">準備壓縮。</span><span class="sxs-lookup"><span data-stu-id="4b363-110">Prepare the compressor.</span></span>
-   <span data-ttu-id="4b363-111">壓縮資料。</span><span class="sxs-lookup"><span data-stu-id="4b363-111">Compress the data.</span></span>
-   <span data-ttu-id="4b363-112">結束壓縮。</span><span class="sxs-lookup"><span data-stu-id="4b363-112">End compression.</span></span>

<span data-ttu-id="4b363-113">您的應用程式可以使用 [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) 函式和宏，來加強對壓縮進程的控制權。</span><span class="sxs-lookup"><span data-stu-id="4b363-113">Your application can increase control over the compression process by using the [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) functions and macros.</span></span> <span data-ttu-id="4b363-114">這組函式和宏會處理個別的畫面，而不是整個序列。</span><span class="sxs-lookup"><span data-stu-id="4b363-114">This group of functions and macros handles individual frames, rather than the sequence as a whole.</span></span> <span data-ttu-id="4b363-115">例如，您的應用程式可以使用 **ICCompress** 函式來識別要壓縮為主要畫面格的畫面格。</span><span class="sxs-lookup"><span data-stu-id="4b363-115">For example, your application can identify the frames to compress as key frames by using the **ICCompress** function.</span></span>

<span data-ttu-id="4b363-116">壓縮程式會以一種格式接收資料、壓縮資料，並使用指定的格式傳回壓縮的資料版本。</span><span class="sxs-lookup"><span data-stu-id="4b363-116">A compressor receives data in one format, compresses the data, and returns a compressed version of the data using a specified format.</span></span> <span data-ttu-id="4b363-117">一般輸入格式會使用 [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) 結構來指定 dib。</span><span class="sxs-lookup"><span data-stu-id="4b363-117">The typical input format specifies DIBs using the [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure.</span></span> <span data-ttu-id="4b363-118">一般輸出格式會指定壓縮的 Dib，同時也會使用 **BITMAPINFO** 結構。</span><span class="sxs-lookup"><span data-stu-id="4b363-118">The typical output format specifies compressed DIBs, also using the **BITMAPINFO** structure.</span></span>

> [!Note]  
> <span data-ttu-id="4b363-119">若要將播放期間的影像和音訊降低效能降至最低，請避免壓縮 AVI 檔案一次以上。</span><span class="sxs-lookup"><span data-stu-id="4b363-119">To minimize image and audio degradation during playback, avoid compressing an AVI file more than once.</span></span> <span data-ttu-id="4b363-120">在編輯系統中結合未壓縮的部分影片，然後壓縮最終產品。</span><span class="sxs-lookup"><span data-stu-id="4b363-120">Combine uncompressed pieces of video in your editing system and then compress the final product.</span></span>

 

## <a name="compressor-and-compression-format-selection"></a><span data-ttu-id="4b363-121">壓縮和壓縮格式選取專案</span><span class="sxs-lookup"><span data-stu-id="4b363-121">Compressor and Compression Format Selection</span></span>

<span data-ttu-id="4b363-122">如果您想要壓縮資料，而您的應用程式需要特定的輸出格式，請將 [**ICM \_ 壓縮 \_ 查詢**](icm-compress-query.md) 訊息 (，或使用 [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) 宏) 來查詢壓縮程式，以判斷它是否支援輸入和輸出格式。</span><span class="sxs-lookup"><span data-stu-id="4b363-122">If you want to compress data and your application requires a specific output format, send the [**ICM\_COMPRESS\_QUERY**](icm-compress-query.md) message (or use the [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) macro) to query the compressor to determine if it supports the input and output formats.</span></span>

<span data-ttu-id="4b363-123">如果輸出格式對您的應用程式而言並不重要，您只需要尋找可以處理輸入格式的壓縮程式。</span><span class="sxs-lookup"><span data-stu-id="4b363-123">If the output format is not important to your application, you need only find a compressor that can handle the input format.</span></span> <span data-ttu-id="4b363-124">若要判斷壓縮程式是否可以處理輸入格式，您可以傳送 **ICM \_ 壓縮 \_ 查詢**，為 *lParam* 參數指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="4b363-124">To determine if a compressor can handle the input format, you can send **ICM\_COMPRESS\_QUERY**, specifying **NULL** for the *lParam* parameter.</span></span> <span data-ttu-id="4b363-125">此訊息不會將輸出格式傳回給您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="4b363-125">This message does not return the output format to your application.</span></span> <span data-ttu-id="4b363-126">您的應用程式可以藉由傳送 [**ICM \_ 壓縮 \_ 取得 \_ 格式**](icm-compress-get-format.md) 訊息 (或使用 [**ICCompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) 宏) ，判斷指定壓縮格式的資料所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="4b363-126">Your application can determine the buffer size needed for the data specifying the compression format by sending the [**ICM\_COMPRESS\_GET\_FORMAT**](icm-compress-get-format.md) message (or use the [**ICCompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) macro).</span></span> <span data-ttu-id="4b363-127">您也可以藉由傳送 ICM \_ 壓縮 \_ 取得 \_ 格式 (或 [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) 宏) 來取得格式資料。</span><span class="sxs-lookup"><span data-stu-id="4b363-127">You can also retrieve the format data by sending ICM\_COMPRESS\_GET\_FORMAT (or the [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) macro).</span></span>

<span data-ttu-id="4b363-128">如果您想要判斷壓縮程式可能需要壓縮的最大緩衝區，請傳送 [**ICM \_ 壓縮 \_ 取得 \_ 大小**](icm-compress-get-size.md) 訊息 (或使用 [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) 宏) 。</span><span class="sxs-lookup"><span data-stu-id="4b363-128">If you want to determine the largest buffer that the compressor could require for compression, send the [**ICM\_COMPRESS\_GET\_SIZE**](icm-compress-get-size.md) message (or use the [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) macro).</span></span> <span data-ttu-id="4b363-129">您可以使用 [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) 函式所傳回的位元組數目，為後續的影像壓縮配置緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4b363-129">You can use the number of bytes returned by the [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) function to allocate a buffer for subsequent image compressions.</span></span>

## <a name="compressor-initialization"></a><span data-ttu-id="4b363-130">壓縮的初始化</span><span class="sxs-lookup"><span data-stu-id="4b363-130">Compressor Initialization</span></span>

<span data-ttu-id="4b363-131">當您的應用程式選取可以處理其所需之輸入和輸出格式的壓縮程式之後，您可以使用 [**ICM \_ 壓縮 \_ 開始**](icm-compress-begin.md) 訊息 (，或使用 [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) 宏) 來初始化壓縮程式。</span><span class="sxs-lookup"><span data-stu-id="4b363-131">After your application selects a compressor that can handle the input and output formats it needs, you can initialize the compressor by using the [**ICM\_COMPRESS\_BEGIN**](icm-compress-begin.md) message (or use the [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) macro).</span></span> <span data-ttu-id="4b363-132">此訊息需要壓縮的控制碼以及輸入和輸出格式。</span><span class="sxs-lookup"><span data-stu-id="4b363-132">This message requires the compressor handle and the input and output formats.</span></span>

## <a name="data-compression"></a><span data-ttu-id="4b363-133">資料壓縮</span><span class="sxs-lookup"><span data-stu-id="4b363-133">Data Compression</span></span>

<span data-ttu-id="4b363-134">您可以使用 [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) 函式來壓縮框架。</span><span class="sxs-lookup"><span data-stu-id="4b363-134">You can use the [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) function to compress a frame.</span></span> <span data-ttu-id="4b363-135">您的應用程式必須重複使用這個函式，直到序列中的所有框架都經過壓縮為止。</span><span class="sxs-lookup"><span data-stu-id="4b363-135">Your application must use this function repeatedly until all the frames in a sequence are compressed.</span></span> <span data-ttu-id="4b363-136">您的應用程式也必須追蹤和遞增以 **ICCompress** 壓縮的每個畫面格的數目。</span><span class="sxs-lookup"><span data-stu-id="4b363-136">Your application must also track and increment the number of each frame compressed with **ICCompress**.</span></span> <span data-ttu-id="4b363-137">壓縮程式會使用此值來檢查是否在快速時態壓縮期間依序傳送框架， (儲存後續畫面格) 之間的差異。</span><span class="sxs-lookup"><span data-stu-id="4b363-137">The compressor uses this value to check if frames are sent out of order during fast temporal compression (storing differences between successive frames).</span></span> <span data-ttu-id="4b363-138">如果您的應用程式此舉將框架，則應該使用與第一次壓縮框架時相同的框架編號。</span><span class="sxs-lookup"><span data-stu-id="4b363-138">If your application recompresses a frame, it should use the same frame number as when the frame was first compressed.</span></span> <span data-ttu-id="4b363-139">如果您的應用程式會壓縮仍框架的影像，則可以將畫面格編號指定為零。</span><span class="sxs-lookup"><span data-stu-id="4b363-139">If your application compresses a still-frame image, it can specify a frame number of zero.</span></span>

<span data-ttu-id="4b363-140">您的應用程式可以使用 ICCOMPRESS 的主要畫面格旗標，藉由 [**ICCOMPRESS**](/windows/desktop/api/Vfw/nf-vfw-iccompress)主要畫面格來將框架壓縮。 **\_**</span><span class="sxs-lookup"><span data-stu-id="4b363-140">Your application can use the **ICCOMPRESS\_KEYFRAME** flag to make the frame compressed by [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) a key frame.</span></span>

<span data-ttu-id="4b363-141">當 BC-VCM-LVM-HYPERV 在壓縮框架之後將控制權傳回給您的應用程式時，BC-VCM-LVM-HYPERV 會將壓縮的資料儲存在 *lpbiOutput* 和 *lpData* 參數所參考的結構中。</span><span class="sxs-lookup"><span data-stu-id="4b363-141">When VCM returns control to your application after compressing a frame, VCM stores the compressed data in the structures referenced by the *lpbiOutput* and *lpData* parameters.</span></span> <span data-ttu-id="4b363-142">如果您的應用程式需要移動壓縮的資料，它會在 *lpbiOutput* 中指定之 [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構的 *biSizeImage* 成員中找到其大小。</span><span class="sxs-lookup"><span data-stu-id="4b363-142">If your application needs to move the compressed data, it can find its size in the *biSizeImage* member of the [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure specified in *lpbiOutput*.</span></span>

> [!Note]  
> <span data-ttu-id="4b363-143">您的應用程式必須配置儲存未壓縮和壓縮資料的結構和緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4b363-143">Your application must allocate the structures and buffers that store the uncompressed and compressed data.</span></span> <span data-ttu-id="4b363-144">如果壓縮程式支援時態壓縮，則您的應用程式也必須配置結構和緩衝區，以保存先前資訊框架的格式和資料。</span><span class="sxs-lookup"><span data-stu-id="4b363-144">If the compressor supports temporal compression, your application must also allocate a structure and buffer to hold the format and data for the previous frame of information.</span></span>

 

## <a name="ending-compression"></a><span data-ttu-id="4b363-145">結束壓縮</span><span class="sxs-lookup"><span data-stu-id="4b363-145">Ending Compression</span></span>

<span data-ttu-id="4b363-146">當您的應用程式壓縮資料之後，它就可以使用 [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) 宏通知壓縮程式已完成。</span><span class="sxs-lookup"><span data-stu-id="4b363-146">After your application has compressed the data, it can use the [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) macro to notify the compressor that it has finished.</span></span> <span data-ttu-id="4b363-147">如果您想要在使用此函式之後重新開機壓縮，您的應用程式必須透過傳送 [**ICM \_ 壓縮 \_ 開始**](icm-compress-begin.md) 訊息 (或使用 [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) 宏) 來重新初始化壓縮程式。</span><span class="sxs-lookup"><span data-stu-id="4b363-147">If you want to restart compression after using this function, your application must reinitialize the compressor by sending the [**ICM\_COMPRESS\_BEGIN**](icm-compress-begin.md) message (or use the [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) macro).</span></span>

 

 