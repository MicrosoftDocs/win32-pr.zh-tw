---
description: 使用時態壓縮的影片編碼
ms.assetid: df363017-97c5-45b0-b8a5-44ac73b7a0e7
title: 使用時態壓縮 (Microsoft 媒體基礎) 的影片編碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d663b0101353d9ce72dab45f0b85e594afcacf4aa8b8a99a6d61d2db0ae07d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721348"
---
# <a name="video-encoding-with-temporal-compression-microsoft-media-foundation"></a>使用時態壓縮 (Microsoft 媒體基礎) 的影片編碼

為了達到可能的最高壓縮率，Windows Media 視訊編解碼器會使用 *時態性壓縮*。 暫時壓縮是一種減少壓縮影片大小的技巧，而不會將每個畫面格編碼為完整影像。 完整編碼的框架 (像是靜態影像) ，稱為 *主要畫面* 格。 影片中的所有其他畫面格都會以指定最後一個畫面格之後變更的資料來表示。 這些框架稱為 *delta 框架*。

使用時態壓縮可達成的壓縮量取決於內容。 如果影片是靜態的，而沒有大量動作或影像中的其他變更，則可以為每個主要畫面格建立許多差異框架。 使用的差異畫面越多，編碼的影片資料流程就越小。 但是，如果影片是動態的，則有許多動作或變更色彩，使用時態壓縮的優點較小。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用影片](workingwithvideo.md)
</dt> </dl>

 

 



