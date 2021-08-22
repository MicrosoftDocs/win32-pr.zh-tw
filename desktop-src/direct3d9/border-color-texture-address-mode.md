---
description: 框線色彩材質位址模式（由 \_ D3DTEXTUREADDRESS 列舉型別的 D3DTADDRESS border 成員識別）會導致 Direct3D 針對0.0 到1.0 （含）範圍以外的任何材質座標，使用任意色彩（稱為框線色彩）。
ms.assetid: 689dbda1-0692-411d-9727-2fdf1df960ec
title: " (Direct3D 9) 的框線色彩材質位址模式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19e0685359227f80a847174157117e90116cffe8e61a48e172451a83aa8ec5fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496311"
---
# <a name="border-color-texture-address-mode-direct3d-9"></a> (Direct3D 9) 的框線色彩材質位址模式

框線色彩材質位址模式（由 \_ [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) 列舉型別的 D3DTADDRESS border 成員識別）會導致 Direct3D 針對0.0 到1.0 （含）範圍以外的任何材質座標，使用任意色彩（稱為框線色彩）。

在以下圖例中，應用程式指定紋理使用紅色的邊框並套用至原始物件。

![紋理及紅色邊框紋理的圖例](images/border.png)

應用程式會藉由呼叫 [**IDirect3DDevice9：： SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)來設定框線色彩。 將呼叫的第一個參數設定為所需的材質階段識別碼、將第二個參數設定為 [D3DSAMP] 的 [顏色組合] \_ 階段狀態值，以及將第三個參數設定為新的 RGBA 框線色彩。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[材質定址模式](texture-addressing-modes.md)
</dt> </dl>

 

 
