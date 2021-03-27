---
title: 統一記憶體架構
description: 查詢是否支援統一記憶體架構 (UMA) 可協助判斷如何處理某些資源。
ms.assetid: E43892F9-E7CD-4D18-BDDE-3C4F03F8F4EA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99baeab51838b9b3382884a681ec9b579fa700a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931965"
---
# <a name="unified-memory-architecture"></a>統一記憶體架構

查詢是否支援統一記憶體架構 (UMA) 可協助判斷如何處理某些資源。

您可以從 [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) 結構中讀取由驅動程式設定的布林值，以判斷硬體是否支援 UMA。

在 UMA 上執行的應用程式可能會想要讓 CPU 存取的資源超過可用的資源。 UMA 可讓應用程式避免複製資源資料，而不是只針對非 UMA 圖形介面卡保持有效率。 [Direct3D 11.3 功能](direct3d-11-3-features.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 11.3 功能](direct3d-11-3-features.md)
</dt> </dl>

 

 




