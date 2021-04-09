---
description: 如果場景包含許多使用相同幾何的物件，您可以藉由減少您需要提供給轉譯器的資料量，以不同的方向、大小、色彩等來繪製該幾何的許多實例，並大幅提升效能。
ms.assetid: d8d9b0c8-b1c4-406d-bf2a-9716d725aec7
title: '有效率地繪製多個 Geometry 實例 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9981dff913b704fca5e6b211b57e3647fddd28c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845972"
---
# <a name="efficiently-drawing-multiple-instances-of-geometry-direct3d-9"></a>有效率地繪製多個 Geometry 實例 (Direct3D 9) 

如果場景包含許多使用相同幾何的物件，您可以藉由減少您需要提供給轉譯器的資料量，以不同的方向、大小、色彩等來繪製該幾何的許多實例，並大幅提升效能。

您可以使用兩種方法來完成這項作業：第一個用於繪製索引幾何，第二個用於非索引幾何。 這兩種技術都使用兩個頂點緩衝區：一個用來提供幾何資料，另一個用來提供每個物件的實例資料。 實例資料可以是各種不同的資訊，例如轉換、色彩資料或光來源資料-基本上，您可以在頂點宣告中描述的任何內容。 使用這些技術來繪製許多幾何實例，可以大幅減少傳送至轉譯器的資料量。

-   [繪圖索引幾何](#drawing-indexed-geometry)
    -   [索引幾何效能比較](#indexed-geometry-performance-comparison)
-   [繪圖非索引幾何](#drawing-non-indexed-geometry)
    -   [非索引幾何效能比較](#non-indexed-geometry-performance-comparison)
-   [相關主題](#related-topics)

## <a name="drawing-indexed-geometry"></a>繪圖索引幾何

頂點緩衝區包含頂點宣告所定義的每個頂點資料。 假設每個頂點的部分包含幾何資料，而每個頂點的一部分包含每個物件的實例資料，如下圖所示。

![索引幾何的頂點緩衝區圖表](images/drawingmultipleinstances.png)

這項技術需要支援 3 \_ 0 頂點著色器模型的裝置。 這項技術適用于任何可程式化的著色器，但不適用於固定函式管線。

針對上方所示的頂點緩衝區，以下是對應的頂點緩衝區宣告：


```
const D3DVERTEXELEMENT9 g_VBDecl_Geometry[] =
{
{0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
{0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL,   0},
{0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TANGENT,  0},
{0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BINORMAL, 0},
{0, 48, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0},
D3DDECL_END()
};

const D3DVERTEXELEMENT9 g_VBDecl_InstanceData[] =
{
{1, 0,  D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1},
{1, 16, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 2},
{1, 32, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 3},
{1, 48, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 4},
{1, 64, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_COLOR,    0},
D3DDECL_END()
};
```



這些宣告會定義兩個頂點緩衝區。 資料流程0的第一個宣告 (（以資料行1中的零表示）) 定義由： position、normal、正切、binormal 和材質座標資料組成的幾何資料。

資料流程1的第二個宣告 (，由資料行1中的宣告所表示) 定義每個物件的實例資料。 每個實例都是由 4 4-元件浮點數和四個元件的色彩所定義。 前四個值可用來初始化4x4 矩陣，這表示此資料將會唯一調整、定位和旋轉幾何的每個實例。 前四個元件使用紋理座標語義，在此案例中表示「這是一般四個元件的數位」。 當您在頂點宣告中使用任意資料時，請使用材質座標語義來標示它。 資料流程中的最後一個元素用於色彩資料。 這可以套用在頂點著色器中，為每個實例提供獨特的色彩。

轉譯之前，您必須呼叫 [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) ，以將頂點緩衝區資料流程系結至裝置。 以下是系結兩個頂點緩衝區的範例：


```
// Set up the geometry data stream
pd3dDevice->SetStreamSourceFreq(0,
    (D3DSTREAMSOURCE_INDEXEDDATA | g_numInstancesToDraw));
pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
    D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

// Set up the instance data stream
pd3dDevice->SetStreamSourceFreq(1,
    (D3DSTREAMSOURCE_INSTANCEDATA | 1));
pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
    D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));
```



[**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) 會使用 [D3DSTREAMSOURCE \_ INDEXEDDATA](other-direct3d-constants.md) 來識別索引幾何資料。 在此情況下，stream 0 包含描述物件幾何的索引資料。 此值會以邏輯方式結合要繪製之幾何的實例數目。

請注意，D3DSTREAMSOURCE \_ INDEXEDDATA 和要繪製的實例數目必須一律設定在資料流程零中。

在第二個呼叫中， [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) 會使用 [D3DSTREAMSOURCE \_ INSTANCEDATA](other-direct3d-constants.md) 來識別包含實例資料的資料流程。 此值會以邏輯方式結合1，因為每個頂點都包含一組實例資料。

[**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource)的最後兩個呼叫會將頂點緩衝區指標系結至裝置。

當您完成轉譯實例資料時，請務必將頂點資料流程頻率重設回其預設狀態 (而不會使用實例) 。 因為此範例使用兩個數據流，所以請設定這兩個數據流，如下所示：


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="indexed-geometry-performance-comparison"></a>索引幾何效能比較

雖然這項技術可能會降低每個應用程式中轉譯時間的結果，但請考慮串流處理到執行時間的資料量差異，以及如果您使用實例技術將會降低的狀態變更數目。 此轉譯順序會利用繪製相同幾何之多個實例的優點：


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    // Set up the geometry data stream
    pd3dDevice->SetStreamSourceFreq(0,
                (D3DSTREAMSOURCE_INDEXEDDATA | g_numInstancesToDraw));
    pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

    // Set up the instance data stream
    pd3dDevice->SetStreamSourceFreq(1,
                (D3DSTREAMSOURCE_INSTANCEDATA | 1));
    pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
                D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));

    pd3dDevice->SetVertexDeclaration( ... );
    pd3dDevice->SetVertexShader( ... );
    pd3dDevice->SetIndices( ... );

    pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    
    pd3dDevice->EndScene();
}
```



請注意，轉譯迴圈會呼叫一次，而幾何資料會串流處理一次，而 n 個實例則會進行一次資料流程處理。 下一個轉譯順序與功能相同，但不會利用實例：


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    for(int i=0; i < g_numObjects; i++)
    {
        pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));


        pd3dDevice->SetVertexDeclaration( ... );
        pd3dDevice->SetVertexShader( ... );
        pd3dDevice->SetIndices( ... );

        pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    }                             
    
    pd3dDevice->EndScene();
}
```



請注意，整個轉譯迴圈是由第二個迴圈所包裝，以繪製每個物件。 現在幾何資料會串流處理到轉譯器 n 次 (而不是一次) 而且任何管線狀態也可能會針對每個繪製的物件進行重複設定。 此轉譯順序很可能會變得很慢。 另外也請注意，在這兩個轉譯迴圈之間， [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) 的參數並未變更。

## <a name="drawing-non-indexed-geometry"></a>繪圖非索引幾何

在 [繪圖索引幾何](#drawing-indexed-geometry)中，頂點緩衝區已設定為以較高的效率繪製多個索引幾何的實例。 您也可以使用 [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) 來繪製非索引的幾何。 這需要不同的頂點緩衝區配置，且具有不同的條件約束。 若要繪製非索引幾何，請準備您的頂點緩衝區，如下圖所示。

![非索引幾何的頂點緩衝區圖表](images/olderstyleinstancing.png)

任何裝置上的硬體加速都不支援此技術。 它僅受軟體頂點處理的支援，而且只適用于 [vs \_ 3 \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-vs-3-0.md) 著色器。

因為這項技術適用于非索引幾何，所以沒有索引緩衝區。 如圖所示，包含幾何的頂點緩衝區包含幾何資料的 n 個複本。 針對每個繪製的實例，會從第一個頂點緩衝區讀取幾何資料，並從第二個頂點緩衝區讀取實例資料。

以下是對應的頂點緩衝區宣告：


```
const D3DVERTEXELEMENT9 g_VBDecl_Geometry[] =
{
{0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
{0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL,   0},
{0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TANGENT,  0},
{0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BINORMAL, 0},
{0, 48, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0},
D3DDECL_END()
};

const D3DVERTEXELEMENT9 g_VBDecl_InstanceData[] =
{
{1, 0,  D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1},
{1, 16, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 2},
{1, 32, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 3},
{1, 48, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 4},
{1, 64, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_COLOR,    0},
D3DDECL_END()
};
```



這些宣告與索引幾何範例中所做的宣告相同。 同樣地，資料流程0的第一個宣告 () 會定義幾何資料，而針對資料流程) 1 的第二個宣告 (會定義每個物件的實例資料。 當您建立第一個頂點緩衝區時，請務必使用您將繪製之幾何資料的實例數目來載入它。

在轉譯之前，您必須設定分隔線，以告訴執行時間如何將第一個頂點緩衝區分割成 n 個實例。 然後使用 [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) 來設定分割，如下所示：


```
// Set the divider
pd3dDevice->SetStreamSourceFreq(0, 1);
// Bind the stream to the vertex buffer
pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
        D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

// Set up the instance data stream
pd3dDevice->SetStreamSourceFreq(1, verticesPerInstance);
pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
        D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));
```



第一次呼叫 [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) 時，會指出資料流程0包含 m 個頂點的 n 個實例。 然後， [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource)會將資料流程0系結至 geometry 頂點緩衝區。

在第二個呼叫中， [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) 會將資料流程1識別為實例資料的來源。 第二個參數是每個物件中的頂點數目 (m) 。 請記住，實例資料流程必須一律宣告為第二個數據流。 然後， [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource)會將資料流程1系結至包含實例資料的頂點緩衝區。

當您完成轉譯實例資料時，請務必將頂點資料流程頻率重設回其預設狀態。 因為此範例使用兩個數據流，所以請設定這兩個數據流，如下所示：


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="non-indexed-geometry-performance-comparison"></a>非索引幾何效能比較

此實例樣式的主要優點是它可以用於非索引的幾何。 雖然這項技術可能會降低每個應用程式中轉譯時間的結果，但請考慮串流處理到執行時間的資料量差異，以及將針對下列轉譯順序減少的狀態變更數目：


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    // Set the divider
    pd3dDevice->SetStreamSourceFreq(0, 1);
    pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

    // Set up the instance data stream
    pd3dDevice->SetStreamSourceFreq(1, verticesPerInstance));
    pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
                D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));

    pd3dDevice->SetVertexDeclaration( ... );
    pd3dDevice->SetVertexShader( ... );
    pd3dDevice->SetIndices( ... );

    pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    
    pd3dDevice->EndScene();
}
```



請注意，轉譯迴圈會呼叫一次。 雖然資料流程的幾何有 n 個實例，但幾何資料會經過資料流程處理。 來自實例頂點緩衝區的資料會經過資料流程處理。 下一個轉譯順序與功能相同，但不會利用實例：


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    for(int i=0; i < g_numObjects; i++)
    {
        pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

        pd3dDevice->SetVertexDeclaration( ... );
        pd3dDevice->SetVertexShader( ... );
        pd3dDevice->SetIndices( ... );

        pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    }
    
    pd3dDevice->EndScene();
}
```



如果沒有實例，則必須以第二個迴圈來包裝轉譯迴圈，以繪製每個物件。 藉由消除第二個轉譯迴圈，您應該會因為在迴圈內呼叫的轉譯狀態變更較少，而預期會有較佳的效能。

整體來說，預期索引的技巧 ([繪製索引的幾何](#drawing-indexed-geometry)) 比非索引的技巧更好， ([繪製非索引的幾何](#drawing-non-indexed-geometry)) ，因為索引技巧只會串流處理一個幾何資料複本。 請注意，任何轉譯序列的 [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) 參數都未變更。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Advanced 主題](advanced-topics.md)
</dt> <dt>

[實例範例](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)
</dt> </dl>

 

 
