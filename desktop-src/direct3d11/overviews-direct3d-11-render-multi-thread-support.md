---
title: 如何檢查驅動程式支援
description: 本主題說明如何判斷多執行緒功能 (包括建立資源，以及硬體加速) 支援的命令清單。
ms.assetid: f577357c-c2e5-4e58-9870-2e995bdc6782
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae42bbb3eedb76d049479839d497a79db81b5697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990611"
---
# <a name="how-to-check-for-driver-support"></a>如何：檢查驅動程式支援

本主題說明如何判斷多執行緒功能 (包括 [建立資源](overviews-direct3d-11-render-multi-thread-intro.md) ，以及硬體加速) 支援的 [命令清單](overviews-direct3d-11-render-multi-thread-command-list.md) 。

建議應用程式檢查多執行緒的圖形硬體支援。 如果驅動程式和圖形硬體不支援多執行緒物件建立，效能可能會以下列方式受到限制：

-   同時建立多個物件 () 的不同類型可能會受到限制。
-   在使用 [立即內容](overviews-direct3d-11-render-multi-thread-render.md) 呈現圖形命令時建立物件可能會受到限制。 例如，如果硬體不支援多執行緒處理，則應用程式應該避免在背景執行緒上建立需要很長時間才能建立的物件。 需要很長時間的建立作業可以封鎖立即內容轉譯，並提高 visual 畫面播放速率斷斷續續的風險。

無論驅動程式和硬體支援為何，執行時間都支援多執行緒和命令清單;如果沒有任何 multithreads 或命令清單的驅動程式和硬體支援，則執行時間會模擬該功能。 如需多執行緒的詳細資訊，請參閱 [Direct3D 11 中的多執行緒簡介](overviews-direct3d-11-render-multi-thread-intro.md)。

**若要檢查多執行緒的驅動程式支援：**

1.  初始化 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 介面物件。 預設會啟用多執行緒處理。
2.  呼叫 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)。 將 **D3D11 \_ 功能 \_ 執行緒** 值傳遞給 *FEATURE* 參數、將 [**D3D11 \_ 功能 \_ 資料 \_ 執行緒**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) 結構傳遞至 *pFeatureSupportData* 參數，然後將 **D3D11 \_ 功能 \_ 資料 \_ 執行緒** 結構的大小傳遞給 *FeatureSupportDataSize* 參數。
3.  如果 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) 方法成功，則您在上一個步驟中傳遞的 [**D3D11 \_ 功能 \_ 資料 \_ 執行緒**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) 結構將會以多執行緒支援的相關資訊來初始化。
    -   如果 **DriverConcurrentCreates** 為 **TRUE**，驅動程式可以同時建立多個資源 (在不同的執行緒上同時) 。

        如果 **DriverCommandLists** 為 **TRUE**，則驅動程式支援命令清單。 也就是說，直接內容所發出的轉譯命令可能會同時在不同執行緒上建立物件，而且不會有畫面播放速率斷斷續續的風險。

    -   如果 **DriverConcurrentCreates** 為 **FALSE**，驅動程式不支援並行建立，這表示可能會有極大的平行存取量。 圖形硬體無法在不同的執行緒 simultanueously 上建立不同類型的物件。 此外，在圖形硬體嘗試在另一個執行緒上建立資源時，圖形硬體無法使用立即內容來發出轉譯命令。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何使用 Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[多執行緒](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




