---
title: 如何建立材質
description: 本主題說明如何建立材質。
ms.assetid: dfe88635-b2c2-48f8-a21e-cce845b518fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6539caec121f301dd89906f7cd78134d3b7cd79083c0d185af63d488ef1648eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565548"
---
# <a name="how-to-create-a-texture"></a>如何：建立材質

建立材質最簡單的方式是描述其屬性，並呼叫材質建立 API。 本主題說明如何建立材質。

**建立材質**

1.  以材質參數的描述填入 [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) 結構。
2.  藉由使用材質描述來呼叫 [**ID3D11Device：： CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) 來建立紋理。

這個範例會建立具有 [**動態使用量**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)的 256 x 256 材質，以做為具有 [**cpu 寫入存取**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag)的 [**著色器資源**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)。


```
D3D11_TEXTURE2D_DESC desc;
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D11_USAGE_DYNAMIC;
desc.BindFlags = D3D11_BIND_SHADER_RESOURCE;
desc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;
desc.MiscFlags = 0;

ID3D11Device *pd3dDevice; // Don't forget to initialize this
ID3D11Texture2D *pTexture = NULL;
pd3dDevice->CreateTexture2D( &desc, NULL, &pTexture );
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何使用 Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[紋理](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




