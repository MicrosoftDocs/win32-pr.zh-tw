---
description: 說明如何使用 Microsoft DirectX Video 加速 High Definition (DXVA-HD) 。
ms.assetid: dfd5cf5c-7d6e-4894-8d9b-41ef0293b3d3
title: DXVA-HD 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ae1945a98bc668aa12cc6cdf8d9e4693cbde27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847633"
---
# <a name="dxva-hd-sample"></a>DXVA-HD 範例

說明如何使用 Microsoft DirectX Video 加速 High Definition (DXVA-HD) 。

此範例本質上是 [DXVA2 \_ VideoProc 範例](dxva2-videoproc-sample.md)的埠。 它具有相同的基本功能，而大部分的鍵盤命令都相同。

此範例會以程式設計方式產生具有主要資料流程和子資料流程的影片。 主要資料流程會顯示 SMPTE 色軸。 子資料流程會使用 luma 金鑰混合在主要資料流程上進行 Alpha 混合。 使用者可以變更影片處理參數，包括平面 Alpha 值、來源和目的地矩形、色彩調整和色彩空間。 下圖顯示產生的影片。

![dxva-hd 範例的螢幕擷取畫面](images/dxva-hd-sample.png)

## <a name="apis-demonstrated"></a>示範的 Api

此範例示範下列 DXVA HD 介面：

-   [**IDXVAHD \_ 裝置**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device)
-   [**IDXVAHD \_ VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor)

## <a name="requirements"></a>規格需求



| 產品                                                        | 版本   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>下載範例

此範例可在 [Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/DXVA_HD)中取得。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> <dt>

[媒體基礎 SDK 範例](media-foundation-sdk-samples.md)
</dt> </dl>

 

 



