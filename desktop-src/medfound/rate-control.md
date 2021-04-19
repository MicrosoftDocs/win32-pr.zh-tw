---
description: 速率控制
ms.assetid: 6529859f-cfb6-4983-a489-bcc2f04e721f
title: 速率控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f484a0469d96578ca1bb7e1d661d7e2319bd8bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974162"
---
# <a name="rate-control"></a><span data-ttu-id="b3634-103">速率控制</span><span class="sxs-lookup"><span data-stu-id="b3634-103">Rate Control</span></span>

<span data-ttu-id="b3634-104">[媒體會話](media-session.md)支援變更播放速率，應用程式可以使用此播放速率來執行快速向前和倒轉等播放功能。</span><span class="sxs-lookup"><span data-stu-id="b3634-104">The [Media Session](media-session.md) supports changing the playback rate, which an application can use to implement playback features such as fast-forward and rewind.</span></span> <span data-ttu-id="b3634-105">本節說明在使用媒體會話時，應用程式如何變更播放速度。</span><span class="sxs-lookup"><span data-stu-id="b3634-105">This section describes how applications can change the playback rate while using the Media Session.</span></span>

<span data-ttu-id="b3634-106">如需在您自己的管線元件中支援速率控制的詳細資訊，請參閱 [執行速率控制](implementing-rate-control.md)。</span><span class="sxs-lookup"><span data-stu-id="b3634-106">For information about supporting rate control in your own pipeline components, see [Implementing Rate Control](implementing-rate-control.md).</span></span>

<span data-ttu-id="b3634-107">此章節包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="b3634-107">This section contains the following topics.</span></span>



| <span data-ttu-id="b3634-108">主題</span><span class="sxs-lookup"><span data-stu-id="b3634-108">Topic</span></span>                                                                                                      | <span data-ttu-id="b3634-109">描述</span><span class="sxs-lookup"><span data-stu-id="b3634-109">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="b3634-110">關於速率控制</span><span class="sxs-lookup"><span data-stu-id="b3634-110">About Rate Control</span></span>](about-rate-control.md)                                                               | <span data-ttu-id="b3634-111">提供速率控制的一般總覽。</span><span class="sxs-lookup"><span data-stu-id="b3634-111">Gives a general overview of rate control.</span></span>                              |
| [<span data-ttu-id="b3634-112">如何判斷支援的費率</span><span class="sxs-lookup"><span data-stu-id="b3634-112">How to Determine Supported Rates</span></span>](how-to-determine-supported-rates.md)                                   | <span data-ttu-id="b3634-113">如何找出最快且最慢的支援播放速率。</span><span class="sxs-lookup"><span data-stu-id="b3634-113">How to find the fastest and slowest supported playback rates.</span></span>          |
| [<span data-ttu-id="b3634-114">如何設定媒體會話的播放率</span><span class="sxs-lookup"><span data-stu-id="b3634-114">How to Set the Playback Rate on the Media Session</span></span>](how-to-set-the-playback-rate-on-the-media-session.md) | <span data-ttu-id="b3634-115">如何變更播放速率。</span><span class="sxs-lookup"><span data-stu-id="b3634-115">How to change the playback rate.</span></span>                                       |
| [<span data-ttu-id="b3634-116">如何執行清理</span><span class="sxs-lookup"><span data-stu-id="b3634-116">How to Perform Scrubbing</span></span>](how-to-perform-scrubbing.md)                                                   | <span data-ttu-id="b3634-117">如何一次執行一個影片畫面。</span><span class="sxs-lookup"><span data-stu-id="b3634-117">How to step one video frame at a time.</span></span>                                 |
| [<span data-ttu-id="b3634-118">執行速率控制</span><span class="sxs-lookup"><span data-stu-id="b3634-118">Implementing Rate Control</span></span>](implementing-rate-control.md)                                                 | <span data-ttu-id="b3634-119">如何支援自訂管線元件中的變數播放速率。</span><span class="sxs-lookup"><span data-stu-id="b3634-119">How to support variable playback rates in a custom pipeline component.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b3634-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="b3634-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3634-121">媒體會話</span><span class="sxs-lookup"><span data-stu-id="b3634-121">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="b3634-122">搜尋、向前快轉及反向播放</span><span class="sxs-lookup"><span data-stu-id="b3634-122">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



