---
description: Direct3D 在單一階段中最多可以將八個紋理混合到原始物件上。
ms.assetid: vs|directx_sdk|~\texture_blending.htm
title: " (Direct3D 9) 的材質混合"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 688be4c80fb87d0d96f8f930ed85c9cc934fc4392151196ec0c510a4cbe482bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118291598"
---
# <a name="texture-blending-direct3d-9"></a> (Direct3D 9) 的材質混合

Direct3D 在單一階段中最多可以將八個紋理混合到原始物件上。 使用多重紋理混合可大幅增加 Direct3D 應用程式的畫面播放速度。 應用程式藉由使用多重紋理混合，在單一階段中套用紋理、陰影、反射光源、擴散光源等其他特殊效果。

若要使用紋理混色，您的應用程式首先應該確認使用者的硬體是否支援該功能。 這項資訊可在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 TextureCaps 成員中找到。 如需有關如何查詢使用者硬體以進行紋理混合功能的詳細資訊，請參閱 [**IDirect3DDevice9：： GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps)。

## <a name="texture-stages-and-the-texture-blending-cascade"></a>紋理階段和材質混合式

Direct3D 透過使用紋理階段來支援一階段的多重紋理混合。 紋理階段取得兩個引數之後，對其進行混合運算，並且將結果傳回以供進一步處理或點陣化使用。 您可將紋理階段視覺化為以下圖例。

![紋理階段的簡圖](images/texstg.png)

如上方簡圖所示，紋理階段會利用一個指定的運算子將兩個引數混合。 常見的運算包括了簡單的調節，或是增加引數的色彩或 Alpha 元件，但應用程式支援超過 24 種運算。 階段的引數可以是關聯紋理、重複色彩及 Alpha (於 Gouraud Shading 中重複)、任意色彩及 Alpha，或是前一紋理階段的結果。 如需詳細資訊，請參閱 [ (Direct3D 9) 的材質混合作業和引數 ](texture-blending-operations-and-arguments.md)。

> [!Note]  
> Direct3D 會區分色彩與 Alpha 混色的混合。 應用程式會為色彩及 Alpha 個別設定混合運算及引數，並且其結果均各自獨立。

 

多重混合階段使用的引數及運算組合，定義了一個以流程為基礎的簡單混合語言。 一個階段的結果會流到另一個階段，並且再從該階段流至下一個階段，以此類推。 運算結果從一個階段流至另一個階段，並且最終在一個多邊形上進行點陣化的這項概念，通常稱作紋理混色串聯。 下列簡圖呈現了個別紋理階段組成紋理混色串聯的過程。

![紋理混色串聯中紋理階段的簡圖](images/tcascade.png)

裝置中的每個階段都有一個以 0 為基礎的索引。 Direct3D 雖然允許最多八個混合階段，我們仍建議您事先檢查裝置功能，以決定現有硬體支援的最大階段數量。 第一個混合階段位於索引 0 上，第二個則位於 1，以此類推直到索引 7 為止。 系統以遞增索引順序混合各階段。

建議您只使用您需要的階段數量。任何未使用的混合階段預設都會停用。 因此，若您的應用程式只會使用到前兩個階段，您只需要為階段 0 及階段 1 設定運算及引數。 系統會混合兩個階段，並且忽略所有停用的階段。

> [!Note]  
> 若您的應用程式根據不同的狀況，可能會使用不同數量的階段 (例如：針對一些物件設定四個階段，其他的則為兩個階段)，您不需要明確停用所有之前使用過的階段。 其中一個選項是停用第一個未使用階段的色彩運算，則所有具有更高索引值的階段皆不會啟用。 另一個選項是設定第一個材質階段的色彩作業， (階段 0) D3DTOP 停用，以停用材質對應 \_ 。 第三個選項是當材質階段具有 \_ 等於 D3DTA 材質的 D3DTSS COLORARG1， \_ 且階段的材質指標為 **Null** 時，這個階段和所有階段都不會處理。

 

下列主題包含其他資訊。

-   [ (Direct3D 9) 的材質混合作業和引數 ](texture-blending-operations-and-arguments.md)
-   [將目前的材質指派 (Direct3D 9) ](assigning-the-current-textures.md)
-   [ (Direct3D 9) 建立混合階段 ](creating-blending-stages.md)
-   [ (Direct3D 9) 的 Alpha 材質混合 ](alpha-texture-blending.md)
-   [Multipass (Direct3D 9) 的材質混合 ](multipass-texture-blending.md)
-   [使用 (Direct3D 9) 的材質進行淺色對應 ](light-mapping-with-textures.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 紋理](direct3d-textures.md)
</dt> </dl>

 

 
