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
# <a name="capturing-a-still-image-from-a-video-stream"></a>從影片串流捕捉靜止影像

開始預覽影片串流之後，請呼叫 [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo)介面的 [**IWiaVideo：： TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture)方法，以從串流影片中捕捉靜止影像。 如需如何取得 **IWiaVideo** 指標並開始預覽串流影片的指示，請參閱 [預覽影片](-wia-previewing-video.md)。

當 [**IWiaVideo：： TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) 方法傳回時， *pbstrNewImageFilename* 參數會包含所產生影像檔案的完整路徑和檔案名。 檔案是 JPEG 格式。 建立檔案的目錄是由 [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo)介面的 [**IWiaVideo：： ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory)屬性值所指定。

> [!Note]  
> Windows 映像取得 (WIA) 不支援 Windows Server 2003、Windows Vista 或更新版本中的影片裝置。 針對這些版本的 Windows，請使用 [DirectShow](/previous-versions//ms783323(v=vs.85)) 從影片取得影像。

 

 

 
