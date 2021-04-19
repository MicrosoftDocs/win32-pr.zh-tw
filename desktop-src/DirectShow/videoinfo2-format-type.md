---
description: VideoInfo2 格式類型
ms.assetid: edd2013a-f0c5-4176-ba3a-a3af719ce31d
title: VideoInfo2 格式類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74b0f435e0e2a1b5b1d948c42a881f19300a9c6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980731"
---
# <a name="videoinfo2-format-type"></a><span data-ttu-id="3d6f7-103">VideoInfo2 格式類型</span><span class="sxs-lookup"><span data-stu-id="3d6f7-103">VideoInfo2 Format Type</span></span>

<span data-ttu-id="3d6f7-104">預覽 pin 的慣用媒體類型可能是具有 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 格式的類型。</span><span class="sxs-lookup"><span data-stu-id="3d6f7-104">A preview pin's preferred media type might be a type with a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format.</span></span> <span data-ttu-id="3d6f7-105">此格式結構支援特殊功能，例如交錯式影片和圖片外觀比例。</span><span class="sxs-lookup"><span data-stu-id="3d6f7-105">This format structure supports special features such as interlaced video and picture aspect ratios.</span></span>

<span data-ttu-id="3d6f7-106">VMR-7 和 VMR-9 都支援直接 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 。</span><span class="sxs-lookup"><span data-stu-id="3d6f7-106">The VMR-7 and the VMR-9 both support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) directly.</span></span> <span data-ttu-id="3d6f7-107">當您將 VMR 連接到該解碼器時，它們將會協商最佳的格式。</span><span class="sxs-lookup"><span data-stu-id="3d6f7-107">When you connect the VMR to the decoder, they will negotiate the best format.</span></span> <span data-ttu-id="3d6f7-108">不過，較舊的影片轉譯器篩選器不支援 **VIDEOINFOHEADER2**。</span><span class="sxs-lookup"><span data-stu-id="3d6f7-108">The older Video Renderer filter, however, does not support **VIDEOINFOHEADER2**.</span></span> <span data-ttu-id="3d6f7-109">若要使用 **VIDEOINFOHEADER2** 格式類型搭配影片轉譯器篩選器，您必須將覆迭 [混音](overlay-mixer-filter.md) 器篩選插入圖形中。</span><span class="sxs-lookup"><span data-stu-id="3d6f7-109">To use **VIDEOINFOHEADER2** format types with the Video Renderer filter, you must insert the [Overlay Mixer](overlay-mixer-filter.md) filter into the graph.</span></span>

1.  <span data-ttu-id="3d6f7-110">使用 [**IPin：： EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) 方法，在解碼器篩選器的輸出釘選上列舉慣用的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3d6f7-110">Enumerate the preferred media types on the decoder filter's output pin, using the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>
2.  <span data-ttu-id="3d6f7-111">檢查列舉順序中的第一個媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3d6f7-111">Check the first media type in the enumeration sequence.</span></span>
3.  <span data-ttu-id="3d6f7-112">如果格式類型為 **\_ VideoInfo2 格式**，請將輸出釘選到重迭混音器。</span><span class="sxs-lookup"><span data-stu-id="3d6f7-112">If the format type is **FORMAT\_VideoInfo2**, connect the output pin to the Overlay Mixer.</span></span> <span data-ttu-id="3d6f7-113">然後將重迭混音器連線到影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="3d6f7-113">Then connect the Overlay Mixer to the video renderer.</span></span> <span data-ttu-id="3d6f7-114"> (查看 [影片埠釘](video-port-pins.md)選。 ) </span><span class="sxs-lookup"><span data-stu-id="3d6f7-114">(See [Video Port Pins](video-port-pins.md).)</span></span>

<span data-ttu-id="3d6f7-115">如果您不在意這些功能，就不需要使用重迭混音器。</span><span class="sxs-lookup"><span data-stu-id="3d6f7-115">If you do not care about these features, you do not have to use the Overlay Mixer.</span></span> <span data-ttu-id="3d6f7-116">將解碼器直接連接到影片轉譯器，它會改以 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 格式連接。</span><span class="sxs-lookup"><span data-stu-id="3d6f7-116">Connect the decoder directly to the Video Renderer, and it will connect with a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) format instead.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d6f7-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="3d6f7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d6f7-118">Advanced Capture 主題</span><span class="sxs-lookup"><span data-stu-id="3d6f7-118">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="3d6f7-119">使用影片捕獲中的重迭混音器</span><span class="sxs-lookup"><span data-stu-id="3d6f7-119">Using the Overlay Mixer in Video Capture</span></span>](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



