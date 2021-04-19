---
description: 本節說明如何使用 Microsoft 媒體基礎，在您的應用程式中執行音訊/影片播放。
ms.assetid: 6efadfe6-013a-4942-9df5-bed557d9af8b
title: 音訊/視訊播放
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6781c531bc7e5c595125d5353a381cc44c08fd5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970945"
---
# <a name="audiovideo-playback"></a><span data-ttu-id="511ff-103">音訊/視訊播放</span><span class="sxs-lookup"><span data-stu-id="511ff-103">Audio/Video Playback</span></span>

<span data-ttu-id="511ff-104">本節說明如何使用 Microsoft 媒體基礎，在您的應用程式中執行音訊/影片播放。</span><span class="sxs-lookup"><span data-stu-id="511ff-104">This section describes how to implement audio/video playback in your application, using Microsoft Media Foundation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="511ff-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="511ff-105">In this section</span></span>



| <span data-ttu-id="511ff-106">主題</span><span class="sxs-lookup"><span data-stu-id="511ff-106">Topic</span></span>                                                                                               | <span data-ttu-id="511ff-107">描述</span><span class="sxs-lookup"><span data-stu-id="511ff-107">Description</span></span>                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="511ff-108">如何使用媒體基礎播放媒體檔案</span><span class="sxs-lookup"><span data-stu-id="511ff-108">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)<br/> | <span data-ttu-id="511ff-109">本教學課程說明如何使用 [Media Session](media-session.md) 物件播放媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="511ff-109">This tutorial shows how to play media files using the [Media Session](media-session.md) object.</span></span> <br/>                                 |
| [<span data-ttu-id="511ff-110">如何播放受保護的媒體檔案</span><span class="sxs-lookup"><span data-stu-id="511ff-110">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)<br/>               | <span data-ttu-id="511ff-111">如何播放包含受 DRM 保護之媒體的檔案。</span><span class="sxs-lookup"><span data-stu-id="511ff-111">How to play files that contain DRM-protected media.</span></span><br/>                                                                               |
| [<span data-ttu-id="511ff-112">如何尋找媒體檔案的持續時間</span><span class="sxs-lookup"><span data-stu-id="511ff-112">How to Find the Duration of a Media File</span></span>](how-to-find-the-duration-of-a-media-file.md)<br/> | <span data-ttu-id="511ff-113">如何尋找媒體檔案的持續時間。</span><span class="sxs-lookup"><span data-stu-id="511ff-113">How to find the duration of a media file.</span></span><br/>                                                                                         |
| [<span data-ttu-id="511ff-114">搜尋、向前快轉及反向播放</span><span class="sxs-lookup"><span data-stu-id="511ff-114">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)<br/>   | <span data-ttu-id="511ff-115">本主題說明使用 [媒體會話](media-session.md) 進行播放時，管理搜尋和速率變更的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="511ff-115">This topic shows example code to manage seeking and rate changes, when using the [Media Session](media-session.md) for playback.</span></span><br/> |
| [<span data-ttu-id="511ff-116">如何設定播放停止時間</span><span class="sxs-lookup"><span data-stu-id="511ff-116">How to Set the Playback Stop Time</span></span>](how-to-set-the-playback-stop-time-.md)<br/>              | <span data-ttu-id="511ff-117">本主題說明如何設定在使用 [媒體會話](media-session.md)時播放的停止時間。</span><span class="sxs-lookup"><span data-stu-id="511ff-117">This topic describes how to set a stop time for playback when using the [Media Session](media-session.md).</span></span><br/>                       |
| [<span data-ttu-id="511ff-118">增強的影片轉譯器</span><span class="sxs-lookup"><span data-stu-id="511ff-118">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)<br/>                                   | <span data-ttu-id="511ff-119">增強型影片轉譯器 (EVR) 是在使用者的監視器上顯示影片的元件。</span><span class="sxs-lookup"><span data-stu-id="511ff-119">The enhanced video renderer (EVR) is a component that displays video on the user's monitor.</span></span><br/>                                       |
| [<span data-ttu-id="511ff-120">串流音訊轉譯器</span><span class="sxs-lookup"><span data-stu-id="511ff-120">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)<br/>                                 | <span data-ttu-id="511ff-121">串流音訊轉譯器 (特別行政區) 是可轉譯音訊的媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="511ff-121">The streaming audio renderer (SAR) is a media sink that renders audio.</span></span><br/>                                                            |
| [<span data-ttu-id="511ff-122">MFPlay</span><span class="sxs-lookup"><span data-stu-id="511ff-122">MFPlay</span></span>](using-mfplay-for-audio-video-playback.md)<br/>                                      | <span data-ttu-id="511ff-123">MFPlay API 已淘汰。</span><span class="sxs-lookup"><span data-stu-id="511ff-123">The MFPlay API is deprecated.</span></span><br/>                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="511ff-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="511ff-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="511ff-125">媒體基礎架構</span><span class="sxs-lookup"><span data-stu-id="511ff-125">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="511ff-126">媒體基礎程式設計指南</span><span class="sxs-lookup"><span data-stu-id="511ff-126">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="511ff-127">媒體基礎中的 MPEG 4 支援</span><span class="sxs-lookup"><span data-stu-id="511ff-127">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> </dl>

 

 




