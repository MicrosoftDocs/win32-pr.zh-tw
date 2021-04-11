---
description: 凹凸地圖是使用特製化像素格式的 IDirect3DTexture9 物件。
ms.assetid: 7f405cb9-9512-44da-8a85-4b7d22017284
title: " (Direct3D 9) 的凹凸地圖像素格式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21bbe4a9999d875e43d33389f86b35d22c81b3bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025985"
---
# <a name="bump-map-pixel-formats-direct3d-9"></a> (Direct3D 9) 的凹凸地圖像素格式

凹凸地圖是使用特製化像素格式的 [**IDirect3DTexture9**](/windows/desktop/api) 物件。 並不是儲存紅色、綠色和藍色色彩的元件，而是在 [放大] 地圖中的每個圖元都會儲存您和 v (D<sub>U</sub> 和<sub>D) 的</sub> 差異值，有時也會儲存亮度元件 L。這些值是由系統套用，如 (Direct3D 9 中的 [將 [對應公式 Direct3D 9) ](bump-mapping-formulas.md) 主題所述。

您可以藉由將格式設定為下列其中一種方式來指定 [凹凸地圖圖元] 格式： D3DFMT \_ CxV8U8、D3DFMT \_ V8U8、D3DFMT \_ L6V5U5、D3DFMT \_ X8L8V8U8、D3DFMT \_ Q8W8V8U8 或 D3DFMT \_ V16U16。 如需相關說明，請參閱 [D3DFORMAT](d3dformat.md)。

圖元的 D<sub>U</sub> 和 d<sub>V</sub> 元件是帶正負號的值，範圍從-1.0 到 + 1.0。 使用亮度元件時，是不帶正負號的整數值，範圍介於0到255之間。

> [!Note]  
> 在挑選「凸塊地圖圖元」格式之前，請先檢查是否支援特定的格式。 如需詳細資訊，請參閱 [使用 (Direct3D 9) 的 [凹凸對應 ](using-bump-mapping.md)]。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[凹凸對應](bump-mapping.md)
</dt> </dl>

 

 



