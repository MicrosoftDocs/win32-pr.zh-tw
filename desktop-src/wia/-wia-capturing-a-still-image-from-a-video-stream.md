---
description: 開始預覽影片串流之後，請呼叫 IWiaVideo 介面的 IWiaVideo：： TakePicture 方法，以從串流影片中捕捉靜止影像。
ms.assetid: 2b8c465b-0dbf-4741-a701-200862cc3de3
title: 從影片串流捕捉靜止影像
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be475405f4aa9719514a531a6af0105d7a786f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192800"
---
# <a name="capturing-a-still-image-from-a-video-stream"></a><span data-ttu-id="7b350-103">從影片串流捕捉靜止影像</span><span class="sxs-lookup"><span data-stu-id="7b350-103">Capturing a Still Image from a Video Stream</span></span>

<span data-ttu-id="7b350-104">開始預覽影片串流之後，請呼叫 [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo)介面的 [**IWiaVideo：： TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture)方法，以從串流影片中捕捉靜止影像。</span><span class="sxs-lookup"><span data-stu-id="7b350-104">After beginning preview of a video stream, call the [**IWiaVideo::TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) method of the [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) interface to capture a still image from the streaming video.</span></span> <span data-ttu-id="7b350-105">如需如何取得 **IWiaVideo** 指標並開始預覽串流影片的指示，請參閱 [預覽影片](-wia-previewing-video.md)。</span><span class="sxs-lookup"><span data-stu-id="7b350-105">For instructions on how to get an **IWiaVideo** pointer and begin previewing streaming video, see [Previewing Video](-wia-previewing-video.md).</span></span>

<span data-ttu-id="7b350-106">當 [**IWiaVideo：： TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) 方法傳回時， *pbstrNewImageFilename* 參數會包含所產生影像檔案的完整路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="7b350-106">When the [**IWiaVideo::TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) method returns, the *pbstrNewImageFilename* parameter contains the full path and filename of the resulting image file.</span></span> <span data-ttu-id="7b350-107">檔案是 JPEG 格式。</span><span class="sxs-lookup"><span data-stu-id="7b350-107">The file is in JPEG format.</span></span> <span data-ttu-id="7b350-108">建立檔案的目錄是由 [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo)介面的 [**IWiaVideo：： ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory)屬性值所指定。</span><span class="sxs-lookup"><span data-stu-id="7b350-108">The directory in which the file is created is specified by the value of the [**IWiaVideo::ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) property of the [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) interface.</span></span>

> [!Note]  
> <span data-ttu-id="7b350-109">Windows 映像取得 (WIA) 不支援 Windows Server 2003、Windows Vista 或更新版本中的影片裝置。</span><span class="sxs-lookup"><span data-stu-id="7b350-109">Windows Image Acquisition (WIA) does not support video devices in Windows Server 2003, Windows Vista, or later.</span></span> <span data-ttu-id="7b350-110">針對這些版本的 Windows，請使用 [DirectShow](/previous-versions//ms783323(v=vs.85)) 從影片取得影像。</span><span class="sxs-lookup"><span data-stu-id="7b350-110">For those versions of the Windows, use [DirectShow](/previous-versions//ms783323(v=vs.85)) to acquire images from video.</span></span>

 

 

 
