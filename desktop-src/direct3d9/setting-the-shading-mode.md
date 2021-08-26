---
description: Direct3D 可以一次選取一種網底模式。
ms.assetid: 9531947d-4cd8-43c3-8825-4c48a0d69395
title: 設定 (Direct3D 9) 的陰影模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 769908513d4388fafae73f5a6788aef37c3ac9456a00f2e3280c57e04c18b462
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068958"
---
# <a name="setting-the-shading-mode-direct3d-9"></a>設定 (Direct3D 9) 的陰影模式

Direct3D 可以一次選取一種網底模式。 預設會選取 [Gouraud] 網底。 在 c + + 中，您可以藉由呼叫 [**IDirect3DDevice9：： graphicsdevice**](/windows/desktop/api) 方法來變更陰影模式。 將 *State* 參數設定為 D3DRS \_ SHADEMODE。 *State* 參數必須設定為 [**D3DSHADEMODE**](./d3dshademode.md)列舉的成員。 下列範例程式碼範例說明如何將 Direct3D 應用程式的目前網底模式設定為 [一般] 或 [Gouraud] 陰影模式。


```
// Set to flat shading.
// This code example assumes that pDev is a valid pointer to 
// an IDirect3DDevice9 interface.
hr = pDev->SetRenderState(D3DRS_SHADEMODE, D3DSHADE_FLAT);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}

// Set to Gouraud shading. This is the default for Direct3D.
hr = pDev->SetRenderState(D3DRS_SHADEMODE,
                            D3DSHADE_GOURAUD);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[陰影](shading.md)
</dt> </dl>

 

 
