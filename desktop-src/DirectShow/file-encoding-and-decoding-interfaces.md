---
description: 檔案編碼和解碼介面
ms.assetid: 5456392d-2557-43b6-93b7-b2ebde218d12
title: 檔案編碼和解碼介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f73de2304f2b473a634127755ca900b99592ed63
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109897"
---
# <a name="file-encoding-and-decoding-interfaces"></a><span data-ttu-id="7b554-103">檔案編碼和解碼介面</span><span class="sxs-lookup"><span data-stu-id="7b554-103">File Encoding and Decoding Interfaces</span></span>

<span data-ttu-id="7b554-104">這些介面支援檔案編碼和解碼。</span><span class="sxs-lookup"><span data-stu-id="7b554-104">These interfaces support file encoding and decoding.</span></span>



| <span data-ttu-id="7b554-105">介面</span><span class="sxs-lookup"><span data-stu-id="7b554-105">Interface</span></span>                                                    | <span data-ttu-id="7b554-106">描述</span><span class="sxs-lookup"><span data-stu-id="7b554-106">Description</span></span>                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7b554-107">**IAMMediaContent**</span><span class="sxs-lookup"><span data-stu-id="7b554-107">**IAMMediaContent**</span></span>](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent)                   | <span data-ttu-id="7b554-108">從資料流程中取出中繼資料，例如作者和標題。</span><span class="sxs-lookup"><span data-stu-id="7b554-108">Retrieve meta-data from a stream, such as the author and title.</span></span>                                              |
| [<span data-ttu-id="7b554-109">**IAMOpenProgress**</span><span class="sxs-lookup"><span data-stu-id="7b554-109">**IAMOpenProgress**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress)                   | <span data-ttu-id="7b554-110">判斷檔案開啟操作的進度。</span><span class="sxs-lookup"><span data-stu-id="7b554-110">Determine the progress of a file-open operation.</span></span>                                                             |
| [<span data-ttu-id="7b554-111">**IAMParse**</span><span class="sxs-lookup"><span data-stu-id="7b554-111">**IAMParse**</span></span>](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse)                                 | <span data-ttu-id="7b554-112">查詢並設定 MPEG 資料流程中目前位置的剖析時間。</span><span class="sxs-lookup"><span data-stu-id="7b554-112">Query and set the parse time for the current position in an MPEG stream.</span></span>                                     |
| [<span data-ttu-id="7b554-113">**IAMStreamSelect**</span><span class="sxs-lookup"><span data-stu-id="7b554-113">**IAMStreamSelect**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect)                   | <span data-ttu-id="7b554-114">控制要播放的邏輯資料流程，並取得其相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7b554-114">Control which logical streams are played, and retrieve information about them.</span></span>                               |
| [<span data-ttu-id="7b554-115">**IAMVfwCompressDialogs**</span><span class="sxs-lookup"><span data-stu-id="7b554-115">**IAMVfwCompressDialogs**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs)       | <span data-ttu-id="7b554-116">VFW 編解碼器所提供的顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="7b554-116">Display dialog boxes provided by VFW codecs.</span></span>                                                                 |
| [<span data-ttu-id="7b554-117">**IAMVideoCompression**</span><span class="sxs-lookup"><span data-stu-id="7b554-117">**IAMVideoCompression**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)           | <span data-ttu-id="7b554-118">設定影片壓縮參數。</span><span class="sxs-lookup"><span data-stu-id="7b554-118">Set video compression parameters.</span></span>                                                                            |
| [<span data-ttu-id="7b554-119">**IConfigAsfWriter**</span><span class="sxs-lookup"><span data-stu-id="7b554-119">**IConfigAsfWriter**</span></span>](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter)                 | <span data-ttu-id="7b554-120">控制 [WM Asf 寫入](wm-asf-writer-filter.md) 器篩選器如何將 Advanced 系統格式寫入 (ASF) 檔。</span><span class="sxs-lookup"><span data-stu-id="7b554-120">Control how the [WM ASF Writer](wm-asf-writer-filter.md) filter writes Advanced Systems Format (ASF) files.</span></span> |
| [<span data-ttu-id="7b554-121">**IConfigAviMux**</span><span class="sxs-lookup"><span data-stu-id="7b554-121">**IConfigAviMux**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux)                       | <span data-ttu-id="7b554-122">控制 [Avi Mux](avi-mux-filter.md) 篩選寫入 avi 檔案的方式。</span><span class="sxs-lookup"><span data-stu-id="7b554-122">Control how the [AVI Mux](avi-mux-filter.md) filter writes AVI files.</span></span>                                       |
| [<span data-ttu-id="7b554-123">**IConfigInterleaving**</span><span class="sxs-lookup"><span data-stu-id="7b554-123">**IConfigInterleaving**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving)           | <span data-ttu-id="7b554-124">當 AVI Mux 篩選寫入 AVI 檔案時，請設定交錯。</span><span class="sxs-lookup"><span data-stu-id="7b554-124">Configure interleaving when the AVI Mux filter writes AVI files.</span></span>                                             |
| [<span data-ttu-id="7b554-125">**IDVEnc**</span><span class="sxs-lookup"><span data-stu-id="7b554-125">**IDVEnc**</span></span>](/windows/desktop/api/Strmif/nn-strmif-idvenc)                                     | <span data-ttu-id="7b554-126">在 [DV 影片編碼器](dv-video-encoder-filter.md) 篩選器上設定編碼解析度。</span><span class="sxs-lookup"><span data-stu-id="7b554-126">Set the encoding resolution on the [DV Video Encoder](dv-video-encoder-filter.md) filter.</span></span>                   |
| [<span data-ttu-id="7b554-127">**IDVSplitter**</span><span class="sxs-lookup"><span data-stu-id="7b554-127">**IDVSplitter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)                           | <span data-ttu-id="7b554-128"> (DV) 串流的數位視訊降級畫面播放速率</span><span class="sxs-lookup"><span data-stu-id="7b554-128">Downgrade the frame rate on a digital video (DV) stream</span></span>                                                      |
| [<span data-ttu-id="7b554-129">**IIPDVDec**</span><span class="sxs-lookup"><span data-stu-id="7b554-129">**IIPDVDec**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iipdvdec)                                 | <span data-ttu-id="7b554-130">在 [DV 影片解碼](dv-video-decoder-filter.md) 篩選器上設定解碼解析度。</span><span class="sxs-lookup"><span data-stu-id="7b554-130">Set the decoding resolution on the [DV Video Decoder](dv-video-decoder-filter.md) filter.</span></span>                   |
| [<span data-ttu-id="7b554-131">**IPersistMediaPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="7b554-131">**IPersistMediaPropertyBag**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag) | <span data-ttu-id="7b554-132">設定及取出 AVI 資料流程中的資訊並將區塊。</span><span class="sxs-lookup"><span data-stu-id="7b554-132">Set and retrieve INFO and DISP chunks in AVI streams.</span></span>                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="7b554-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="7b554-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b554-134">介面</span><span class="sxs-lookup"><span data-stu-id="7b554-134">Interfaces</span></span>](interfaces.md)
</dt> </dl>

 

 



