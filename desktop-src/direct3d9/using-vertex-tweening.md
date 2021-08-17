---
description: 若要判斷 Direct3D 是否支援頂點補間，請檢查 \_ D3DCAPS9 結構的 VertexProcessingCaps 成員中是否有 D3DVTXPCAPS 補間旗標。
ms.assetid: b60c7f96-3752-4703-9059-486d9906c508
title: 使用 (Direct3D 9) 的頂點補間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14c4d2da3f32698cc24e052a152b674ecb023f79e90541af23374c0903d54d55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797086"
---
# <a name="using-vertex-tweening-direct3d-9"></a>使用 (Direct3D 9) 的頂點補間

若要判斷 Direct3D 是否支援頂點補間，請檢查 \_ [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 VertexProcessingCaps 成員中是否有 D3DVTXPCAPS 補間旗標。 下列程式碼範例會使用 [**IDirect3DDevice9：： GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) 方法來判斷是否支援補間。


```
// This example assumes that m_pD3DDevice is 
// a valid pointer to a IDirect3DDevice9 interface.
//
D3DCAPS9 d3dCaps;

m_pD3DDevice->GetDeviceCaps( &d3dCaps );
if( 0 != (d3dCaps.VertexProcessingCaps & D3DVTXPCAPS_TWEENING) )
    // Vertex tweening is supported.
```



若要使用向量補間，您必須先設定使用第二個一般或第二個位置的自訂頂點型別。 下列程式碼範例顯示包含第二個點和第二個位置的範例宣告。


```
struct TEX_VERTEX
{
    D3DVECTOR position;
    D3DVECTOR normal;
    D3DVECTOR position2;
    D3DVECTOR normal2;
};

//Create a vertex buffer with the type TEX_VERTEX.
```



下一步是設定目前的宣告。 下列程式碼範例示範如何進行此動作。


```
// Create the shader declaration.
D3DVERTEXELEMENT9 decl[] = 
{
    { 0, 0,  D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
    { 0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0 },
    { 0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 1 },
    { 0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 1 },
    D3DDECL_END()
};
```



如需有關建立自訂頂點型別和頂點緩衝區的詳細資訊，請參閱 [建立 (Direct3D 9) 的頂點緩衝區 ](creating-a-vertex-buffer.md)。

> [!Note]  
> 啟用頂點補間時，目前的宣告中必須有第二個位置或第二個。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點 Tweening](vertex-tweening.md)
</dt> </dl>

 

 
