---
description: Per-Pixel Alpha 混色
ms.assetid: 68661dc5-1423-47b2-a0df-858e5eb7f02b
title: Per-Pixel Alpha 混色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df7e67084ae19df4a1aab81474dc8a9b1a313b9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "107000041"
---
# <a name="per-pixel-alpha-blending"></a>Per-Pixel Alpha 混色

已針對每個圖元的 Alpha 混色定義四個媒體子類型。 只有當 VMR 處於混合模式時，才支援這些子類型。 當上游篩選嘗試使用其中一個子類型進行連線時，如果連線不在混合模式中，VMR 將會拒絕連接。 這些子類型定義于 uuid 中：

-   MEDIASUBTYPE \_ ARGB1555
-   MEDIASUBTYPE \_ ARGB4444
-   MEDIASUBTYPE \_ ARGB32
-   MEDIASUBTYPE \_ AYUV

如需詳細資訊，請參閱 [未壓縮的 RGB 影片子類型](uncompressed-rgb-video-subtypes.md) 和 [**YUV 影片子類型**](yuv-video-subtypes.md)。

 

 



