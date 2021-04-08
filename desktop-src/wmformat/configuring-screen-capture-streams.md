---
title: 設定畫面抓取資料流程
description: 設定畫面抓取資料流程
ms.assetid: 974e679f-0bf6-412b-9e80-43370de7605a
keywords:
- 串流，設定畫面抓取資料流程
- 編解碼器，設定畫面抓取資料流程
- 畫面抓取資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8200c4a6e733c2bb7f908b79cb73dbb2c3244dc4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103932908"
---
# <a name="configuring-screen-capture-streams"></a><span data-ttu-id="3ec9b-106">設定畫面抓取資料流程</span><span class="sxs-lookup"><span data-stu-id="3ec9b-106">Configuring Screen Capture Streams</span></span>

<span data-ttu-id="3ec9b-107">使用 Windows Media® Video 9 螢幕編解碼器的資料流程，是由應用程式以與一般影片串流相同的方式進行設定。</span><span class="sxs-lookup"><span data-stu-id="3ec9b-107">Streams that use the Windows Media® Video 9 Screen codec are configured by applications in the same way as normal video streams.</span></span> <span data-ttu-id="3ec9b-108">但是，如果您將影片複雜性等級設定為0，則寫入器會忽略任何以 [**IWMVideoMediaProps：： SetQuality**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setquality)設定的影片品質值。</span><span class="sxs-lookup"><span data-stu-id="3ec9b-108">However, if you set the video complexity level to 0, the writer will ignore any video quality value set with [**IWMVideoMediaProps::SetQuality**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setquality).</span></span> <span data-ttu-id="3ec9b-109">如需詳細資訊，請參閱 [使用 Windows Media 視訊9螢幕編解碼器取得良好的結果](getting-good-results-with-the-windows-media-video-9-screen-codec.md)。</span><span class="sxs-lookup"><span data-stu-id="3ec9b-109">For more information, see [Getting Good Results with the Windows Media Video 9 Screen Codec](getting-good-results-with-the-windows-media-video-9-screen-codec.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ec9b-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="3ec9b-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ec9b-111">**設定資料流程**</span><span class="sxs-lookup"><span data-stu-id="3ec9b-111">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="3ec9b-112">**所有資料流程通用的設定**</span><span class="sxs-lookup"><span data-stu-id="3ec9b-112">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="3ec9b-113">**設定影片串流**</span><span class="sxs-lookup"><span data-stu-id="3ec9b-113">**Configuring Video Streams**</span></span>](configuring-video-streams.md)
</dt> </dl>

 

 




