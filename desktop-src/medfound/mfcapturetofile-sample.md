---
description: 說明如何從攝影機將影片捕獲到檔案。
ms.assetid: 910eb010-07df-4384-a489-3c268e4cd531
title: MFCaptureToFile 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a0f8d8bb71eabb1faeb72bd8ce345b7a3eea0fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691248"
---
# <a name="mfcapturetofile-sample"></a><span data-ttu-id="0e8be-103">MFCaptureToFile 範例</span><span class="sxs-lookup"><span data-stu-id="0e8be-103">MFCaptureToFile Sample</span></span>

<span data-ttu-id="0e8be-104">說明如何從攝影機將影片捕獲到檔案。</span><span class="sxs-lookup"><span data-stu-id="0e8be-104">Shows how to capture video from a video camera to a file.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="0e8be-105">示範的 Api</span><span class="sxs-lookup"><span data-stu-id="0e8be-105">APIs Demonstrated</span></span>

<span data-ttu-id="0e8be-106">此範例示範下列 Api。</span><span class="sxs-lookup"><span data-stu-id="0e8be-106">This sample demonstrates the following APIs.</span></span>

-   [<span data-ttu-id="0e8be-107">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="0e8be-107">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [<span data-ttu-id="0e8be-108">**IMFSinkWriter**</span><span class="sxs-lookup"><span data-stu-id="0e8be-108">**IMFSinkWriter**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
-   [<span data-ttu-id="0e8be-109">**IMFSourceReader**</span><span class="sxs-lookup"><span data-stu-id="0e8be-109">**IMFSourceReader**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
-   [<span data-ttu-id="0e8be-110">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="0e8be-110">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

## <a name="requirements"></a><span data-ttu-id="0e8be-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e8be-111">Requirements</span></span>



| <span data-ttu-id="0e8be-112">產品</span><span class="sxs-lookup"><span data-stu-id="0e8be-112">Product</span></span>                                                        | <span data-ttu-id="0e8be-113">版本</span><span class="sxs-lookup"><span data-stu-id="0e8be-113">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="0e8be-114">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="0e8be-114">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="0e8be-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0e8be-115">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="0e8be-116">下載範例</span><span class="sxs-lookup"><span data-stu-id="0e8be-116">Downloading the Sample</span></span>

<span data-ttu-id="0e8be-117">此範例可在 [Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/MFCaptureToFile)中取得。</span><span class="sxs-lookup"><span data-stu-id="0e8be-117">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/MFCaptureToFile).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e8be-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="0e8be-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e8be-119">音訊/視訊擷取</span><span class="sxs-lookup"><span data-stu-id="0e8be-119">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="0e8be-120">媒體基礎 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="0e8be-120">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 



