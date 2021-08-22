---
title: 根簽章總覽
description: 根簽章是由應用程式設定，並將命令清單連結至著色器所需的資源。
ms.assetid: 2E649DA2-6CAC-4C2A-A420-D4EC0DD6EA73
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a44ed554156818d50526c5d3335eaa02cb57fec6e5b486882db4cab52eb8f8c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118806709"
---
# <a name="root-signatures-overview"></a>根簽章總覽

根簽章是由應用程式設定，並將命令清單連結至著色器所需的資源。 圖形命令清單同時具有圖形和計算根簽章。 計算命令清單只會有一個計算根簽章。 這些根簽章彼此獨立。

-   [根參數和引數](#root-parameters-and-arguments)
-   [根常數、描述元和資料表](#root-constants-descriptors-and-tables)
-   [相關主題](#related-topics)

## <a name="root-parameters-and-arguments"></a>根參數和引數

**根** 簽章類似于 API 函式簽章，它會決定著色器應該預期的資料類型，但不會定義實際的記憶體或資料。 **根參數** 是根簽章中的一個專案。 在執行時間設定和變更之根參數的實際值稱為 **根引數**。 變更根引數會變更著色器讀取的資料。

## <a name="root-constants-descriptors-and-tables"></a>根常數、描述元和資料表

根簽章可以包含三種類型的參數;根常數 (常數內嵌于根引數) 、根引數 (描述項內嵌于根引數) ，以及描述項資料表 (描述項堆積中的描述項範圍) 指標。

根常數是內嵌的32位值，在著色器中會顯示為常數緩衝區。

內嵌的根目錄描述項應該包含最常存取的描述元，但限制為 CBVs，以及原始或結構化 UAV 或 SRV 緩衝區。 較複雜的類型（例如2D 材質 SRV）不能用來做為根描述項。 根描述項不包含大小限制，因此不會有超出界限的檢查，與描述項堆積中的描述項不同，它包含大小。

根簽章內的描述項資料表專案包含描述元、HLSL 著色器系結名稱和可見度旗標。 請參閱 [著色器模型 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1) ，以取得著色器名稱的詳細資料。 在某些硬體上，只有在需要它們的著色器階段可以看見描述項時，才會有效能提升 (參考 [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)) 。

![根描述中繼資料表專案](images/root-descriptor-table.png)

根簽章的配置相當有彈性，而某些條件約束會強加于較少的可用硬體。 無論硬體層級為何，應用程式一律會盡可能地嘗試使根簽章盡可能小，以達到最高效率。 應用程式可以權衡根簽章中有更多描述中繼資料表，但不包含根常數的空間，反之亦然。

根簽章的內容 (描述中繼資料表、根常數和根描述元，) 當繪圖 (圖形) /dispatch (計算) 呼叫之間的任何內容變更時，D3D12 驅動程式會自動取得該應用程式的版本。 因此每個 draw/分派都會取得一組獨特的完整根簽章狀態。

在理想的情況下，會有 (Pso) 共用相同根簽章的管線狀態物件群組。 在管線上設定根簽章之後，它定義 (描述中繼資料表、描述元、常數) 的所有系結都可以個別設定或變更，包括對組合的繼承。

應用程式可以在其所需的兩個描述中繼資料表之間進行取捨，以取得更多空間，但會移除間接) 的內嵌常數 (，在根簽章中沒有間接) 的 (。 應用程式應該盡可能謹慎地使用根簽章，依賴應用程式控制的記憶體，例如指向它們的堆積和描述元，以代表大量資料。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[根簽章](root-signatures.md)
</dt> </dl>

 

 