---
title: 輸出格式列舉
description: 輸出格式列舉
ms.assetid: 53d5724b-f875-4b2e-92fa-279f46111f29
keywords:
- Windows Media Format SDK，輸出格式列舉
- Advanced Systems Format (ASF) ，輸出格式列舉
- ASF (Advanced Systems Format) ，輸出格式列舉
- Windows Media Format SDK，IWMReaderTypeNegotiation 介面
- Advanced Systems Format (ASF) ，IWMReaderTypeNegotiation 介面
- ASF (Advanced Systems Format) ，IWMReaderTypeNegotiation 介面
- 輸出格式列舉
- IWMReaderTypeNegotiation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d49999c3da2afd05b0d2231d259d24a50356eb4f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104022996"
---
# <a name="output-format-enumeration"></a><span data-ttu-id="f1469-111">輸出格式列舉</span><span class="sxs-lookup"><span data-stu-id="f1469-111">Output Format Enumeration</span></span>

<span data-ttu-id="f1469-112">讀取器物件和同步讀取器物件都會與編解碼器通訊，以列舉壓縮資料流程的可能輸出格式。</span><span class="sxs-lookup"><span data-stu-id="f1469-112">Both the reader object and the synchronous reader object communicate with the codecs to enumerate the possible output formats for compressed streams.</span></span> <span data-ttu-id="f1469-113">當您讀取包含以一或多個 Windows Media 編解碼器壓縮之內容的檔案時，您可以檢查可能的輸出格式，以選擇最適合您需求的輸出格式。</span><span class="sxs-lookup"><span data-stu-id="f1469-113">When you read a file containing content compressed with one or more of the Windows Media codecs, you can examine the possible output formats to choose the one that best suits your needs.</span></span> <span data-ttu-id="f1469-114">為了方便起見，每個編解碼器都有預設輸出格式，它會設定為最常用的格式。</span><span class="sxs-lookup"><span data-stu-id="f1469-114">For convenience, each codec has a default output format which is set to the most commonly used format.</span></span> <span data-ttu-id="f1469-115">如需有關輸出列舉的詳細資訊，請參閱 [使用輸出](working-with-outputs.md)。</span><span class="sxs-lookup"><span data-stu-id="f1469-115">For more information about output enumeration, see [Working with Outputs](working-with-outputs.md).</span></span>

<span data-ttu-id="f1469-116">您可以根據媒體類型，對輸出格式進行某些變更。</span><span class="sxs-lookup"><span data-stu-id="f1469-116">You can make certain changes to an output format depending upon the media type.</span></span> <span data-ttu-id="f1469-117">例如，您可以變更影片串流的畫面格大小和色彩深度。</span><span class="sxs-lookup"><span data-stu-id="f1469-117">For video streams, for example, you can change the frame size and color depth.</span></span> <span data-ttu-id="f1469-118">讀取物件都支援介面，以測試您對輸出格式（稱為 [**IWMReaderTypeNegotiation**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation)）所做的變更。</span><span class="sxs-lookup"><span data-stu-id="f1469-118">The reading objects both support an interface to test changes you make to the output format, called [**IWMReaderTypeNegotiation**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1469-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="f1469-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1469-120">**檔案讀取功能**</span><span class="sxs-lookup"><span data-stu-id="f1469-120">**File Reading Features**</span></span>](file-reading-features.md)
</dt> </dl>

 

 




