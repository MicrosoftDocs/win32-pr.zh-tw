---
title: " (Direct3D 11 圖形) 的資源介面"
description: 有一些介面適用于兩種基本類型的資源緩衝區和紋理。
ms.assetid: 8e40573a-b186-41ec-b2ff-81279d77bd3a
keywords:
- 介面，Direct3D 11 資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0896bd04a51a989e502676ee314e17d1bf94a110df8a5af9dfe82210dd1b6b71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119125342"
---
# <a name="resource-interfaces-direct3d-11-graphics"></a> (Direct3D 11 圖形) 的資源介面

有一些介面適用于兩種基本類型的資源：緩衝區和紋理。 另外還有一些介面可用於資源的查看。

應用程式會使用 view 將資源系結至管線階段。 此視圖會定義在轉譯期間存取資源的方式。 本節說明 view 介面。


## <a name="in-this-section"></a>本節內容



| 主題                                                                       | 描述                                                                                                                                                                                            |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)<br/>                             | 緩衝區介面會存取非結構化記憶體的緩衝區資源。 緩衝區通常會儲存頂點或索引資料。<br/>                                                                  |
| [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)<br/>         | 深度樣板視圖介面會在深度樣板測試期間存取材質資源。<br/>                                                                                                    |
| [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)<br/>         | 轉譯目標視圖介面會識別轉譯時可以存取的呈現目標子資源。<br/>                                                                             |
| [**ID3D11RenderTargetView1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rendertargetview1)<br/>       | 轉譯目標視圖介面代表可在轉譯期間存取的轉譯目標子資源。<br/>                                                                             |
| [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)<br/>                         | 資源介面可提供所有資源的一般動作。<br/>                                                                                                                              |
| [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)<br/>     | 著色器-資源檢視介面會指定著色器在轉譯期間可以存取的子資源。 著色器資源的範例包括常數緩衝區、材質緩衝區和材質。<br/>  |
| [**ID3D11ShaderResourceView1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11shaderresourceview1)<br/>   | 著色器-資源檢視介面代表著色器在轉譯期間可以存取的子資源。 著色器資源的範例包括常數緩衝區、材質緩衝區和材質。<br/> |
| [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d)<br/>                       | 1D 紋理介面會存取材質資料，也就是結構化的記憶體。<br/>                                                                                                                     |
| [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)<br/>                       | 2D 材質介面會管理材質資料，也就是結構化的記憶體。<br/>                                                                                                                      |
| [**ID3D11Texture2D1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11texture2d1)<br/>                     | 2D 材質介面代表材質資料，也就是結構化的記憶體。<br/>                                                                                                                   |
| [**ID3D11Texture3D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture3d)<br/>                       | 3D 紋理介面會存取材質資料，也就是結構化的記憶體。<br/>                                                                                                                     |
| [**ID3D11Texture3D1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11texture3d1)<br/>                     | 3D 紋理介面代表材質資料，也就是結構化的記憶體。<br/>                                                                                                                   |
| [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)<br/>   | View 介面會指定在轉譯期間，管線可以存取的資源部分。<br/>                                                                                                |
| [**ID3D11UnorderedAccessView1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11unorderedaccessview1)<br/> | 未排序的存取視圖介面代表管線在轉譯期間可以存取的資源部分。<br/>                                                                             |
| [**ID3D11View**](/windows/desktop/api/D3D11/nn-d3d11-id3d11view)<br/>                                 | View 介面會指定在轉譯期間，管線可以存取的資源部分。<br/>                                                                                                |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[資源參考](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

 





