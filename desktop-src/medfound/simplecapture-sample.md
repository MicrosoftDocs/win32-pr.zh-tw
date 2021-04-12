---
description: 說明如何使用 MFPlay API，從影片捕獲裝置預覽影片。
ms.assetid: 6e2b1636-9d24-40e6-9ed4-e17d1af6a044
title: SimpleCapture 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da6fd255ad4c69254eb6ff64bdb99731e0c5ba9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191750"
---
# <a name="simplecapture-sample"></a><span data-ttu-id="3c21b-103">SimpleCapture 範例</span><span class="sxs-lookup"><span data-stu-id="3c21b-103">SimpleCapture Sample</span></span>

<span data-ttu-id="3c21b-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="3c21b-104">\[Deprecated.</span></span> <span data-ttu-id="3c21b-105">MFPlay API 可能會從 Windows 的未來版本中移除。</span><span class="sxs-lookup"><span data-stu-id="3c21b-105">The MFPlay API may be removed from future releases of Windows.</span></span> <span data-ttu-id="3c21b-106">應用程式應該使用影片捕獲的 [來源讀取器](source-reader.md) 。\]</span><span class="sxs-lookup"><span data-stu-id="3c21b-106">Applications should use the [Source Reader](source-reader.md) for video capture.\]</span></span>

<span data-ttu-id="3c21b-107">說明如何使用 MFPlay API，從影片捕獲裝置預覽影片。</span><span class="sxs-lookup"><span data-stu-id="3c21b-107">Shows how to preview video from a video capture device, using the MFPlay API.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="3c21b-108">示範的 Api</span><span class="sxs-lookup"><span data-stu-id="3c21b-108">APIs Demonstrated</span></span>

<span data-ttu-id="3c21b-109">這個範例會示範下列 Microsoft 媒體基礎介面：</span><span class="sxs-lookup"><span data-stu-id="3c21b-109">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="3c21b-110">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="3c21b-110">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [<span data-ttu-id="3c21b-111">**IMFPMediaItem**</span><span class="sxs-lookup"><span data-stu-id="3c21b-111">**IMFPMediaItem**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem)
-   [<span data-ttu-id="3c21b-112">**IMFPMediaPlayer**</span><span class="sxs-lookup"><span data-stu-id="3c21b-112">**IMFPMediaPlayer**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)
-   [<span data-ttu-id="3c21b-113">**IMFPMediaPlayerCallback**</span><span class="sxs-lookup"><span data-stu-id="3c21b-113">**IMFPMediaPlayerCallback**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)

## <a name="requirements"></a><span data-ttu-id="3c21b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c21b-114">Requirements</span></span>



| <span data-ttu-id="3c21b-115">產品</span><span class="sxs-lookup"><span data-stu-id="3c21b-115">Product</span></span>                                                        | <span data-ttu-id="3c21b-116">版本</span><span class="sxs-lookup"><span data-stu-id="3c21b-116">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="3c21b-117">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="3c21b-117">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="3c21b-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3c21b-118">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="3c21b-119">下載範例</span><span class="sxs-lookup"><span data-stu-id="3c21b-119">Downloading the Sample</span></span>

<span data-ttu-id="3c21b-120">此範例可在 [Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/SimpleCapture)中取得。</span><span class="sxs-lookup"><span data-stu-id="3c21b-120">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/SimpleCapture).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c21b-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="3c21b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c21b-122">音訊/視訊擷取</span><span class="sxs-lookup"><span data-stu-id="3c21b-122">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="3c21b-123">媒體基礎 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="3c21b-123">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 



