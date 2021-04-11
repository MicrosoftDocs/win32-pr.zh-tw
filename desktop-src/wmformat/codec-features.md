---
title: 編解碼器功能
description: 編解碼器功能
ms.assetid: e0bbdf75-2369-4080-ae8e-aabaa8401dcf
keywords:
- Windows Media Format SDK，編解碼器功能
- Windows Media Format SDK，功能
- 編解碼器，功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e3623bcb6f338fe11bef3089705801dc3ea047
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183497"
---
# <a name="codec-features"></a><span data-ttu-id="c2d81-106">編解碼器功能</span><span class="sxs-lookup"><span data-stu-id="c2d81-106">Codec Features</span></span>

<span data-ttu-id="c2d81-107">Windows Media Format SDK 會以數個音訊和影片編解碼器傳遞。</span><span class="sxs-lookup"><span data-stu-id="c2d81-107">The Windows Media Format SDK is delivered with several audio and video codecs.</span></span> <span data-ttu-id="c2d81-108">您可以使用提供的編解碼器來壓縮和解壓縮內容，以符合各種需求。</span><span class="sxs-lookup"><span data-stu-id="c2d81-108">You can use the codecs provided to compress and decompress content to suit a variety of needs.</span></span> <span data-ttu-id="c2d81-109">寫入器用來壓縮資料的編解碼器是由設定檔中的串流設定資訊所指定。</span><span class="sxs-lookup"><span data-stu-id="c2d81-109">The codec that is used by the writer to compress data is specified by stream configuration information in the profile.</span></span> <span data-ttu-id="c2d81-110">然後，來自設定檔的資訊會儲存在寫入器所建立之檔案的標頭中。</span><span class="sxs-lookup"><span data-stu-id="c2d81-110">Information from the profile is then stored in the header of the file created by the writer.</span></span> <span data-ttu-id="c2d81-111">然後，當讀取器或同步讀取器開啟檔案時，標頭中的設定檔資訊就會識別解壓縮資料所需的編解碼器。</span><span class="sxs-lookup"><span data-stu-id="c2d81-111">Then, when the file is opened by the reader or synchronous reader, the profile information in the header identifies the codec needed to decompress the data.</span></span>

<span data-ttu-id="c2d81-112">本節將討論下列功能。</span><span class="sxs-lookup"><span data-stu-id="c2d81-112">The following features are discussed in this section.</span></span>

-   [<span data-ttu-id="c2d81-113">支援的編解碼器</span><span class="sxs-lookup"><span data-stu-id="c2d81-113">Supported Codecs</span></span>](supported-codecs.md)
-   [<span data-ttu-id="c2d81-114">固定位元速率 (CBR) 編碼</span><span class="sxs-lookup"><span data-stu-id="c2d81-114">Constant Bit Rate (CBR) Encoding</span></span>](constant-bit-rate--cbr--encoding.md)
-   [<span data-ttu-id="c2d81-115">變數位速率 (VBR) 編碼</span><span class="sxs-lookup"><span data-stu-id="c2d81-115">Variable Bit Rate (VBR) Encoding</span></span>](variable-bit-rate--vbr--encoding.md)
-   [<span data-ttu-id="c2d81-116">雙通路編碼</span><span class="sxs-lookup"><span data-stu-id="c2d81-116">Two-Pass Encoding</span></span>](two-pass-encoding.md)
-   [<span data-ttu-id="c2d81-117">高解析度音訊支援</span><span class="sxs-lookup"><span data-stu-id="c2d81-117">High-Resolution Audio Support</span></span>](high-resolution-audio-support.md)
-   [<span data-ttu-id="c2d81-118">低延遲音訊</span><span class="sxs-lookup"><span data-stu-id="c2d81-118">Low-Delay Audio</span></span>](low-delay-audio.md)
-   [<span data-ttu-id="c2d81-119">S/PDIF 音訊輸出</span><span class="sxs-lookup"><span data-stu-id="c2d81-119">S/PDIF Audio Output</span></span>](s-pdif-audio-output.md)
-   [<span data-ttu-id="c2d81-120">視訊影像</span><span class="sxs-lookup"><span data-stu-id="c2d81-120">Video Image</span></span>](video-image.md)
-   [<span data-ttu-id="c2d81-121">裝置一致性範本</span><span class="sxs-lookup"><span data-stu-id="c2d81-121">Device Conformance Templates</span></span>](device-conformance-templates.md)
-   [<span data-ttu-id="c2d81-122">影片複雜性設定</span><span class="sxs-lookup"><span data-stu-id="c2d81-122">Video Complexity Settings</span></span>](video-complexity-settings.md)
-   [<span data-ttu-id="c2d81-123">框架插補</span><span class="sxs-lookup"><span data-stu-id="c2d81-123">Frame Interpolation</span></span>](frame-interpolation.md)

## <a name="related-topics"></a><span data-ttu-id="c2d81-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="c2d81-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2d81-125">**特性**</span><span class="sxs-lookup"><span data-stu-id="c2d81-125">**Features**</span></span>](features.md)
</dt> </dl>

 

 




