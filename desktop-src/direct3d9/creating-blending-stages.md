---
description: 混合階段是一組定義紋理混合方式的紋理作業及其引數。
ms.assetid: 7f9e3041-a270-44a9-a8e1-bca5ea25a71e
title: " (Direct3D 9) 建立混合階段"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f5029d540433b22b1380435dd8092546917338
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110765"
---
# <a name="creating-blending-stages-direct3d-9"></a> (Direct3D 9) 建立混合階段

混合階段是一組定義紋理混合方式的紋理作業及其引數。 製作混合階段時，c + + 應用程式會叫用 [**IDirect3DDevice9：： SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) 方法。 第一個呼叫會指定執行的操作。 另外兩個調用會定義套用作業的引數。 下列程式碼範例說明如何建立混合階段。


```
// This example assumes that lpD3DDev is a valid pointer to an
// IDirect3DDevice9 interface.

// Set the operation for the first texture.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_ADD);

// Set argument 1 to the texture color.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE);

// Set argument 2 to the iterated diffuse color.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE);
```



材質中的材質資料包含色彩和 Alpha 值。 應用程式可以在單一混色階段中定義色彩和 Alpha 值的個別作業。 每個運算、色彩和 Alpha 都有自己的引數。 如需詳細資訊，請參閱 [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)。

雖然不是 Direct3D API 的一部分，但是您可以在應用程式中插入下列宏，以簡化建立紋理混合階段所需的程式碼。


```
#define SetTextureColorStage( dev, i, arg1, op, arg2 )     \
    dev->SetTextureStageState( i, D3DTSS_COLOROP, op);      \
    dev->SetTextureStageState( i, D3DTSS_COLORARG1, arg1 ); \
    dev->SetTextureStageState( i, D3DTSS_COLORARG2, arg2 );

#define SetTextureAlphaStage( dev, i, arg1, op, arg2 )     \
    dev->SetTextureStageState( i, D3DTSS_ALPHAOP, op);      \
    dev->SetTextureStageState( i, D3DTSS_ALPHAARG1, arg1 );  \
    dev->SetTextureStageState( i  D3DTSS_ALPHAARG2, arg2 );
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[材質混色](texture-blending.md)
</dt> </dl>

 

 
