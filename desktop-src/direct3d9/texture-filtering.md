---
description: 當 Direct3D 轉譯原始物件時，會將 3D 原始物件對應到 2D 畫面上。
ms.assetid: vs|directx_sdk|~\texture_filtering.htm
title: " (Direct3D 9) 的材質篩選"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758ee51df65ffa4dddf793db83fe618107886cd4c20497f0e8090373a1415beb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118291173"
---
# <a name="texture-filtering-direct3d-9"></a> (Direct3D 9) 的材質篩選

當 Direct3D 轉譯原始物件時，會將 3D 原始物件對應到 2D 畫面上。 若原始物件帶有紋理，Direct3D 必須使用該紋理為原始物件的 2D 轉譯影像中的每個像素產生色彩。 針對畫面上原始物件影像的每個像素，程式必須從紋理中取得色彩值。 這個過程稱為「紋理篩選」。

執行紋理篩選作業時，通常也會放大或縮小使用的紋理。 換句話說，其會對應到比自身大或小的原始影像。 放大紋理可能會導致許多像素對應到一個材質。 其結果可能為外觀粗短。 縮小紋理通常表示一個像素會對應到許多材質。 其結果影像可能會顯得模糊或帶有鋸齒。 若要解決這些問題，您必須對材質色彩稍作混合，以達到像素的色彩。

Direct3D 將複雜的紋理篩選過程予以簡化。 Direct3D 提供您三種紋理篩選的類型：線性篩選、非等向性篩選，及 Mipmap 篩選。 如果您並未選擇任何紋理篩選方式，Direct3D 會使用一種稱作「最近點取樣」的技術。

每一種紋理篩選都有優點和缺點。 例如：線性紋理篩選可能會使最終影像產生鋸齒狀的邊緣，或是矮胖的外觀。 然而，其為運算上低負荷的一種紋理篩選方法。 使用 Mipmap 進行紋理篩選通常會產生最好的結果，特別是與非等向性篩選搭配使用時。 然而，其在 Direct3D 支援的技術中是最消耗記憶體的一種。

使用紋理介面指標的應用程式應該透過呼叫 [**IDirect3DDevice9：： SetSamplerState**](/windows/desktop/api) 方法來設定目前的材質篩選方法。 將第一個參數的值設定為您要選取材質篩選方法之材質 (0-7) 的整數索引編號。 \_ \_ 針對第二個參數傳遞 D3DSAMP MAGFILTER、D3DSAMP MINFILTER 或 D3DSAMP \_ MIPFILTER，以設定放大、縮制或 mipmap 篩選。 傳遞 [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) 列舉類型的成員作為第三個參數中的值。

本節提供 Direct3D 支援的材質篩選方法。 它會組織成下列主題。

-   [最接近點取樣 (Direct3D 9) ](nearest-point-sampling.md)
-   [ (Direct3D 9) 的線性材質篩選 ](linear-texture-filtering.md)
-   [ (Direct3D 9) 的雙線性材質篩選 ](bilinear-texture-filtering.md)
-   [ (Direct3D 9) 的非等向材質篩選 ](anisotropic-texture-filtering.md)
-   [使用 Mipmap (Direct3D 9) 的材質篩選 ](texture-filtering-with-mipmaps.md)

> [!Note]  
> 雖然 [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) 列舉型別中顯示的材質篩選轉譯狀態會被材質階段狀態取代，但 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)（相對於 IDirect3DDevice2 版本）不會在您嘗試使用時失敗。 相反地，系統會將這些轉譯狀態的效果對應至多紋理串聯（階段0）中的第一個階段。 應用程式不應該混用舊版轉譯狀態與其對應的材質階段狀態，因為可能會發生無法預期的結果。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 紋理](direct3d-textures.md)
</dt> </dl>

 

 
