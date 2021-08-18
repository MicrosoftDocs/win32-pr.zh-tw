---
description: 使用影片畫面
ms.assetid: a5ad74dd-abfd-4810-a512-42e4b98a6c59
title: 使用影片畫面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86407f99138e0b38b67468668fc963bd1bcd7b65e875571643bc7727b4d0d339
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870928"
---
# <a name="working-with-video-frames"></a>使用影片畫面

未壓縮的影片是快速連續播放的一系列點陣圖，通常是每秒大約30個畫面格的速率。 因為大部分的影片都會以壓縮的格式進入 DirectShow 的篩選圖形，所以影片串流通常會通過用於解壓縮的解碼器。 許多的解碼器都會以 YUV 格式輸出資料，並在轉譯之前，將最後轉換成 RGB 的影片硬體。 如果解碼器使用 DirectX Video 加速，則影片硬體會執行額外的工作來將映射解碼。 因此，在資料到達影片硬體之前，可能不會執行點陣圖的最終解壓縮。

但是，若要執行許多類型的影片分析、處理或編輯，通常必須使用某種 RGB 或 YUV 格式的未壓縮點陣圖，才能轉譯或寫入至檔案。 這項工作通常是在以 [**CTransformFilter**](ctransformfilter.md) 基類為基礎的轉換篩選準則中完成，特別是在 **轉換** 方法中。 這個方法會接收封裝影片資料之 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 物件的指標。 **IMediaSample：： GetPointer** 方法會傳回原始資料之第一個位元組的指標。 針對未壓縮的框架，此資料包含可由篩選準則直接存取或修改的圖元。 下列各節提供的背景資訊可協助您以這種方式有效地使用 DIB 資料。

> [!Note]  
> 您也可以使用 GDI、GDI+、DirectDraw 或 Direct3D 函數來修改位，但這些技術已超出本文的範圍。

 

本節包含下列主題：

-   [由上而下與 Bottom-Up Dib](top-down-vs--bottom-up-dibs.md)
-   [使用16位 RGB](working-with-16-bit-rgb.md)

 

 



