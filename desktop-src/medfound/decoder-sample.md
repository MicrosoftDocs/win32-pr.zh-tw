---
description: 示範如何撰寫 Microsoft 媒體基礎的解碼器。
ms.assetid: 941e5400-e679-41f4-9830-3548dc6037aa
title: 解碼範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd7586534876cfa7f530e675b0342a92bf46b8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936557"
---
# <a name="decoder-sample"></a><span data-ttu-id="2aa3a-103">解碼範例</span><span class="sxs-lookup"><span data-stu-id="2aa3a-103">Decoder Sample</span></span>

<span data-ttu-id="2aa3a-104">示範如何撰寫 Microsoft 媒體基礎的解碼器。</span><span class="sxs-lookup"><span data-stu-id="2aa3a-104">Shows how to write a decoder for Microsoft Media Foundation.</span></span>

<span data-ttu-id="2aa3a-105">此範例會執行模擬的 MPEG-2 視頻解碼器，以顯示每個影片畫面的時間代碼。</span><span class="sxs-lookup"><span data-stu-id="2aa3a-105">This sample implements a mock MPEG-1 video decoder that displays the time code for each video frame.</span></span> <span data-ttu-id="2aa3a-106">它並不會實際解碼 MPEG 1 位流。</span><span class="sxs-lookup"><span data-stu-id="2aa3a-106">It does not actually decode the MPEG-1 bitstream.</span></span> <span data-ttu-id="2aa3a-107">下圖顯示來自解碼器的影片輸出。</span><span class="sxs-lookup"><span data-stu-id="2aa3a-107">The following image shows the video output from the decoder.</span></span>

![來自解碼器之影片畫面格的螢幕擷取畫面](images/decodersample.png)

> [!Note]  
> <span data-ttu-id="2aa3a-109">在 Windows 7 的 Windows SDK 之前，此範例包含在 [MPEG1Source 範例](mpeg1source-sample.md)中。</span><span class="sxs-lookup"><span data-stu-id="2aa3a-109">Prior to the Windows SDK for Windows 7, this sample was included as part of the [MPEG1Source Sample](mpeg1source-sample.md).</span></span>

 

## <a name="apis-demonstrated"></a><span data-ttu-id="2aa3a-110">示範的 Api</span><span class="sxs-lookup"><span data-stu-id="2aa3a-110">APIs Demonstrated</span></span>

<span data-ttu-id="2aa3a-111">這個範例會示範下列媒體基礎介面：</span><span class="sxs-lookup"><span data-stu-id="2aa3a-111">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="2aa3a-112">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="2aa3a-112">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="requirements"></a><span data-ttu-id="2aa3a-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2aa3a-113">Requirements</span></span>



| <span data-ttu-id="2aa3a-114">產品</span><span class="sxs-lookup"><span data-stu-id="2aa3a-114">Product</span></span>                                                        | <span data-ttu-id="2aa3a-115">版本</span><span class="sxs-lookup"><span data-stu-id="2aa3a-115">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="2aa3a-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="2aa3a-116">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="2aa3a-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2aa3a-117">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="2aa3a-118">下載範例</span><span class="sxs-lookup"><span data-stu-id="2aa3a-118">Downloading the Sample</span></span>

<span data-ttu-id="2aa3a-119">此範例可在 [Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/Decoder)中取得。</span><span class="sxs-lookup"><span data-stu-id="2aa3a-119">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/Decoder).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2aa3a-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="2aa3a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2aa3a-121">媒體基礎 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="2aa3a-121">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="2aa3a-122">媒體基礎轉換</span><span class="sxs-lookup"><span data-stu-id="2aa3a-122">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="2aa3a-123">撰寫自訂的 MFT</span><span class="sxs-lookup"><span data-stu-id="2aa3a-123">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 



