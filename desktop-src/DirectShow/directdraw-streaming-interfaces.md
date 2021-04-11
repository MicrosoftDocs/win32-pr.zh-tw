---
description: DirectDraw 串流介面
ms.assetid: 8f91d90d-0b9f-4d04-bc10-4b82c1b0e062
title: DirectDraw 串流介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc922bfed03fd2fac3581168bda35f072871a52
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025705"
---
# <a name="directdraw-streaming-interfaces"></a><span data-ttu-id="a8b00-103">DirectDraw 串流介面</span><span class="sxs-lookup"><span data-stu-id="a8b00-103">DirectDraw Streaming Interfaces</span></span>

> [!Note]  
> <span data-ttu-id="a8b00-104">這些 Api 已被取代。</span><span class="sxs-lookup"><span data-stu-id="a8b00-104">These APIs are deprecated.</span></span> <span data-ttu-id="a8b00-105">應用程式應該使用 [**範例捕獲**](sample-grabber-filter.md) 篩選器或執行自訂篩選，以從 DirectShow 篩選圖形取得資料。</span><span class="sxs-lookup"><span data-stu-id="a8b00-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="a8b00-106">如果您在資料流程中使用支援 DirectDraw 的影片格式，下列介面可讓您更有效地控制資料，而不是更多泛型基底介面。</span><span class="sxs-lookup"><span data-stu-id="a8b00-106">If you use DirectDraw-supported video formats in your streams, the following interfaces give you more powerful control over the data than the more generic base interfaces.</span></span>



| <span data-ttu-id="a8b00-107">介面</span><span class="sxs-lookup"><span data-stu-id="a8b00-107">Interface</span></span>                                                  | <span data-ttu-id="a8b00-108">描述</span><span class="sxs-lookup"><span data-stu-id="a8b00-108">Description</span></span>                                                                                                                                                                                                                 |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8b00-109">**IDirectDrawMediaStream**</span><span class="sxs-lookup"><span data-stu-id="a8b00-109">**IDirectDrawMediaStream**</span></span>](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | <span data-ttu-id="a8b00-110">設定和抓取資料流程格式以及與媒體資料流程相關聯的 DirectDraw 物件;這個介面衍生自 [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)。</span><span class="sxs-lookup"><span data-stu-id="a8b00-110">Sets and retrieves the stream format and the DirectDraw object associated with the media stream; this interface derives from [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream).</span></span> <span data-ttu-id="a8b00-111">您也可以使用此介面來建立影片範例。</span><span class="sxs-lookup"><span data-stu-id="a8b00-111">You can also use this interface to create video samples.</span></span> |
| [<span data-ttu-id="a8b00-112">**IDirectDrawStreamSample**</span><span class="sxs-lookup"><span data-stu-id="a8b00-112">**IDirectDrawStreamSample**</span></span>](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | <span data-ttu-id="a8b00-113">可讓您將影片範例附加至 DirectDraw 表面;這個介面衍生自 [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) 介面。</span><span class="sxs-lookup"><span data-stu-id="a8b00-113">Enables you to attach video samples to DirectDraw surfaces; this interface derives from the [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) interface.</span></span> <span data-ttu-id="a8b00-114">每個附加表面都包含裁剪矩形，讓轉譯更容易。</span><span class="sxs-lookup"><span data-stu-id="a8b00-114">Each attached surface includes a clipping rectangle to make rendering easier.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a8b00-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="a8b00-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8b00-116">多媒體串流介面的清單</span><span class="sxs-lookup"><span data-stu-id="a8b00-116">List of Multimedia Streaming Interfaces</span></span>](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



