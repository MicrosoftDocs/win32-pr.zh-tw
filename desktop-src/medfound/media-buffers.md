---
description: 媒體緩衝區
ms.assetid: 3ee073ea-7bac-4971-9167-93a4e541ab77
title: 媒體緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ef02570ab994f0a15a9b53f2df8a0ac0b96a91a3bf3f260c1bcc5f866ade87e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827508"
---
# <a name="media-buffers"></a>媒體緩衝區

媒體緩衝區是管理記憶體區塊的 COM 物件，通常是用來保存媒體資料。 媒體緩衝區可用來將資料從一個管線元件移至下一個管線元件。 大部分的應用程式不會直接使用媒體緩衝區，因為媒體會話會處理管線物件之間的所有資料流程。 如果您要撰寫自己的管線元件，或直接使用管線元件而不使用媒體會話，則必須使用媒體緩衝區。

媒體緩衝區會公開 [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) 介面。 這個介面是設計用來讀取或寫入任何類型的資料。 未壓縮的影片畫面需要特殊處理，因為它們可能會儲存在位於視訊記憶體的 Direct3D 介面中。

此章節包含下列主題。



| 主題                                                        | 描述                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------|
| [使用媒體緩衝區](working-with-media-buffers.md) | 描述所有媒體類型之媒體緩衝區的一般行為。 |
| [未壓縮的影片緩衝區](uncompressed-video-buffers.md) | 如何使用包含未壓縮影片畫面的媒體緩衝區。  |
| [DirectX 介面緩衝區](directx-surface-buffer.md)         | 說明如何將 Direct3D 介面儲存在媒體緩衝區中。         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎基本](media-foundation-primitives.md)
</dt> </dl>

 

 



