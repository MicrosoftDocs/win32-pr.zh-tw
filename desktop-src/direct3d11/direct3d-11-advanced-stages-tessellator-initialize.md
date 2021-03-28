---
title: 如何初始化鑲嵌階段
description: 本主題說明如何初始化鑲嵌階段。
ms.assetid: 81f5461a-0938-4c46-b3e8-bef2bea125a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cfe00a4d59396f0dc1b0157f84e57e9cabc4a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990594"
---
# <a name="how-to-initialize-the-tessellator-stage"></a>如何：初始化鑲嵌階段

一般而言，鑲嵌會將修補程式的精簡、使用者定義模型，以包含可程式化的詳細資料數量的幾何展開。 幾何通常是一組表示詳細表面幾何的三角形。 本主題說明如何初始化鑲嵌階段。

鑲嵌階段是三個階段的第二個，可共同運作以 tessellate 或磚化介面。 第一個階段是輪廓著色器階段;它會針對每個修補程式進行一次，並設定 (fixed function 鑲嵌) 行為的下一個階段。 輪廓著色器也會產生使用者定義輸出（例如輸出控制點），以及直接傳送至第三個階段（網域著色器階段）的鑲嵌的 patch 常數。 每個鑲嵌階段點都會叫用一次網域著色器，並評估介面位置。

鑲嵌階段是固定的函式階段，沒有可產生的著色器，也沒有要設定的狀態。 它會從輪廓-著色器階段接收所有的設定狀態;一旦將輪廓著色器階段初始化之後，就會自動初始化鑲嵌階段。

**若要初始化鑲嵌階段**

-   使用 [**>id3d11devicecoNtext：： HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader)，初始化輪廓著色器階段。

    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

    *ppClassInstances* 是指向著色器介面陣列的指標，並以 [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) 指標和介面數目（由 *NumClassInstances* 表示）來表示。 如果未使用，這些參數可以分別設定為 **Null** 和0。

在將輪廓著色器階段初始化之後，您也應該初始化網域著色器階段。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何使用 Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[鑲嵌式總覽](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




