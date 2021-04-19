---
description: 使用 EVR 媒體接收
ms.assetid: cd98266a-bc62-43da-b4d7-3561447d634f
title: 使用 EVR 媒體接收
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84f8c666e88b495ad2d2e53fb1de10364f91636f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106985515"
---
# <a name="using-the-evr-media-sink"></a><span data-ttu-id="8d267-103">使用 EVR 媒體接收</span><span class="sxs-lookup"><span data-stu-id="8d267-103">Using the EVR Media Sink</span></span>

<span data-ttu-id="8d267-104">增強型影片轉譯器 (EVR) 媒體接收器可作為獨立元件使用。</span><span class="sxs-lookup"><span data-stu-id="8d267-104">The enhanced video renderer (EVR) media sink can be used as a stand-alone component.</span></span> <span data-ttu-id="8d267-105">但是，應用程式通常會在拓撲內建立 EVR 媒體接收器，然後使用媒體會話來控制播放。</span><span class="sxs-lookup"><span data-stu-id="8d267-105">More often, however, an application will create the EVR media sink inside a topology, and then use the Media Session to control playback.</span></span>

<span data-ttu-id="8d267-106">有兩種方式可以建立 EVR 媒體接收器：</span><span class="sxs-lookup"><span data-stu-id="8d267-106">There are two ways to create the EVR media sink:</span></span>

-   <span data-ttu-id="8d267-107">[**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer)函式會建立媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="8d267-107">The [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) function creates the media sink.</span></span>

-   <span data-ttu-id="8d267-108">[**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate)函式會建立媒體接收器的啟用物件。</span><span class="sxs-lookup"><span data-stu-id="8d267-108">The [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function creates an activation object for the media sink.</span></span>

<span data-ttu-id="8d267-109">EVR 媒體接收器一開始會有一個對應至參考資料流的資料流程接收。</span><span class="sxs-lookup"><span data-stu-id="8d267-109">The EVR media sink initially has one stream sink, which corresponds to the reference stream.</span></span> <span data-ttu-id="8d267-110">若要加入新的資料流程接收，請呼叫 [**IMFMediaSink：： AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink)。</span><span class="sxs-lookup"><span data-stu-id="8d267-110">To add new stream sinks, call [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d267-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="8d267-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d267-112">增強的影片轉譯器</span><span class="sxs-lookup"><span data-stu-id="8d267-112">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="8d267-113">媒體接收器</span><span class="sxs-lookup"><span data-stu-id="8d267-113">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 



