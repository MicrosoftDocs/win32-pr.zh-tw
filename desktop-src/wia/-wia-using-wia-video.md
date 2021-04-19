---
description: WIA 提供 IWiaVideo 介面，可讓應用程式在視窗中顯示串流影片、從影片串流捕捉靜止影像，並將這些影像儲存為 JPEG 檔案。
ms.assetid: b0785f3e-78b1-4044-99f4-0617ce18e095
title: 使用 WIA 影片
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37c7c82d7b82aa45f864496fb2b74cb53b8dcbd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972640"
---
# <a name="using-wia-video"></a><span data-ttu-id="d70c9-103">使用 WIA 影片</span><span class="sxs-lookup"><span data-stu-id="d70c9-103">Using WIA Video</span></span>

<span data-ttu-id="d70c9-104">WIA 提供 [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) 介面，可讓應用程式在視窗中顯示串流影片、從影片串流捕捉靜止影像，並將這些影像儲存為 JPEG 檔案。</span><span class="sxs-lookup"><span data-stu-id="d70c9-104">WIA provides the [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) interface to enable applications to display streaming video in a window, capture still images from the video stream, and save those images as JPEG files.</span></span>

<span data-ttu-id="d70c9-105">下列各節說明如何使用 Windows 映像取得 (WIA) 影片功能：</span><span class="sxs-lookup"><span data-stu-id="d70c9-105">The following sections explain how to use Windows Image Acquisition (WIA) video capabilities:</span></span>

-   [<span data-ttu-id="d70c9-106">預覽影片</span><span class="sxs-lookup"><span data-stu-id="d70c9-106">Previewing Video</span></span>](-wia-previewing-video.md)
-   [<span data-ttu-id="d70c9-107">從影片串流捕捉靜止影像</span><span class="sxs-lookup"><span data-stu-id="d70c9-107">Capturing a Still Image from a Video Stream</span></span>](-wia-capturing-a-still-image-from-a-video-stream.md)

> [!Note]  
> <span data-ttu-id="d70c9-108">WIA 不支援 Windows Server 2003、Windows Vista 或更新版本中的影片裝置。</span><span class="sxs-lookup"><span data-stu-id="d70c9-108">WIA does not support video devices in Windows Server 2003, Windows Vista, or later.</span></span> <span data-ttu-id="d70c9-109">針對這些版本的 Windows，請使用 [DirectShow](/previous-versions//ms783323(v=vs.85)) 從影片取得影像。</span><span class="sxs-lookup"><span data-stu-id="d70c9-109">For those versions of the Windows, use [DirectShow](/previous-versions//ms783323(v=vs.85)) to acquire images from video.</span></span>

 

 

 
