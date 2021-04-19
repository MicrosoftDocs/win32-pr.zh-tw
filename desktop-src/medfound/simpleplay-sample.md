---
description: 說明如何使用 MFPlay API 播放媒體檔案。
ms.assetid: 1acd6f98-af59-47fd-9a3e-38a668fb6acf
title: SimplePlay 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e02fee507ffed7bd91664f67ffb725565f47c721
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979751"
---
# <a name="simpleplay-sample"></a><span data-ttu-id="0c97b-103">SimplePlay 範例</span><span class="sxs-lookup"><span data-stu-id="0c97b-103">SimplePlay Sample</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0c97b-104">已取代。</span><span class="sxs-lookup"><span data-stu-id="0c97b-104">Deprecated.</span></span> <span data-ttu-id="0c97b-105">此 API 可能會從 Windows 的未來版本中移除。</span><span class="sxs-lookup"><span data-stu-id="0c97b-105">This API may be removed from future releases of Windows.</span></span> <span data-ttu-id="0c97b-106">應用程式應該使用 [媒體會話](media-session.md) 來播放。</span><span class="sxs-lookup"><span data-stu-id="0c97b-106">Applications should use the [Media Session](media-session.md) for playback.</span></span>

 

<span data-ttu-id="0c97b-107">說明如何使用 MFPlay API 播放媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="0c97b-107">Shows how to play a media file using the MFPlay API.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="0c97b-108">示範的 Api</span><span class="sxs-lookup"><span data-stu-id="0c97b-108">APIs Demonstrated</span></span>

<span data-ttu-id="0c97b-109">這個範例會示範下列 Microsoft 媒體基礎介面：</span><span class="sxs-lookup"><span data-stu-id="0c97b-109">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="0c97b-110">**IMFPMediaItem**</span><span class="sxs-lookup"><span data-stu-id="0c97b-110">**IMFPMediaItem**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem)
-   [<span data-ttu-id="0c97b-111">**IMFPMediaPlayer**</span><span class="sxs-lookup"><span data-stu-id="0c97b-111">**IMFPMediaPlayer**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)
-   [<span data-ttu-id="0c97b-112">**IMFPMediaPlayerCallback**</span><span class="sxs-lookup"><span data-stu-id="0c97b-112">**IMFPMediaPlayerCallback**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)

## <a name="requirements"></a><span data-ttu-id="0c97b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c97b-113">Requirements</span></span>



| <span data-ttu-id="0c97b-114">產品</span><span class="sxs-lookup"><span data-stu-id="0c97b-114">Product</span></span>                                                        | <span data-ttu-id="0c97b-115">版本</span><span class="sxs-lookup"><span data-stu-id="0c97b-115">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="0c97b-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="0c97b-116">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="0c97b-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0c97b-117">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="0c97b-118">下載範例</span><span class="sxs-lookup"><span data-stu-id="0c97b-118">Downloading the Sample</span></span>

<span data-ttu-id="0c97b-119">此範例可在 [Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/SimplePlay)中取得。</span><span class="sxs-lookup"><span data-stu-id="0c97b-119">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/SimplePlay).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c97b-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="0c97b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c97b-121">媒體基礎 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="0c97b-121">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="0c97b-122">使用 MFPlay 進行音訊/影片播放</span><span class="sxs-lookup"><span data-stu-id="0c97b-122">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



