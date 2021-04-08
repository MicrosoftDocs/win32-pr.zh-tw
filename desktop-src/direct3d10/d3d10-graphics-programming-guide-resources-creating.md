---
description: 建立緩衝區需要定義緩衝區將儲存的資料、提供初始化資料，以及設定適當的使用方式和系結旗標。 若要建立紋理，請參閱建立 (Direct3D 10) 的材質資源。
ms.assetid: 9787b153-9301-4a0f-bd6f-21cc6f7fc650
title: " (Direct3D 10) 建立緩衝區資源"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d711265775c430728fbcffecd364f746580a566
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688935"
---
# <a name="creating-buffer-resources-direct3d-10"></a> (Direct3D 10) 建立緩衝區資源

建立緩衝區需要定義緩衝區將儲存的資料、提供初始化資料，以及設定適當的使用方式和系結旗標。 若要建立紋理，請參閱 [建立 (Direct3D 10) 的材質資源 ](d3d10-graphics-programming-guide-resources-creating-textures.md)。

-   [建立頂點緩衝區](#create-a-vertex-buffer)
    -   [建立緩衝區描述](#create-a-buffer-description)
    -   [建立緩衝區的初始化資料](#create-the-initialization-data-for-the-buffer)
    -   [建立緩衝區](#create-the-buffer)
-   [建立索引緩衝區](#create-an-index-buffer)
-   [建立常數緩衝區](#create-a-constant-buffer)
-   [相關主題](#related-topics)

## <a name="create-a-vertex-buffer"></a>建立頂點緩衝區

建立 [頂點緩衝區](d3d10-graphics-programming-guide-resources-types.md) 的步驟如下所示。

-   [建立緩衝區描述](#create-a-buffer-description)
-   [建立緩衝區的初始化資料](#create-the-initialization-data-for-the-buffer)
-   [建立緩衝區](#create-the-buffer)

### <a name="create-a-buffer-description"></a>建立緩衝區描述

建立頂點緩衝區時，緩衝區描述 (查看 [**D3D10 \_ 緩衝區 \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)) 用來定義資料在緩衝區內的組織方式、管線如何存取緩衝區，以及將如何使用緩衝區。

下列範例示範如何針對包含位置和色彩值的頂點，建立單一三角形的緩衝區描述。


```
struct SimpleVertex
{
    D3DXVECTOR3 Position;  
    D3DXVECTOR3 Color;  
};

    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage            = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth        = sizeof( SimpleVertex ) * 3;
    bufferDesc.BindFlags        = D3D10_BIND_VERTEX_BUFFER;
    bufferDesc.CPUAccessFlags   = 0;
    bufferDesc.MiscFlags        = 0;
```



在此範例中，會使用幾乎所有預設設定來初始化緩衝區描述，以 [**使用**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)、 [**CPU 存取**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag) 和 [**其他旗標**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)。 其他設定適用于系結 [**旗**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) 標，將資源識別為僅限頂點緩衝區，以及緩衝區的大小。

使用方式和 CPU 存取旗標對於效能而言很重要。 這兩個旗標一起決定了資源的存取頻率、資源可以載入哪些記憶體類型，以及哪些處理器需要存取資源。 預設使用此資源將不會經常更新。 將 CPU 存取設定為0表示 CPU 將不需要讀取或寫入資源。 這表示由於資源不需要 CPU 存取，因此執行時間可以將資源載入至 GPU 最高效能的記憶體。

如同預期，這兩個處理器之間的最佳效能與任何時間可存取性之間有取捨。 例如，沒有 CPU 存取的預設使用方式表示可將資源提供給 GPU 專用。 這可能包括將資源載入至記憶體中，但 CPU 無法直接存取。 資源只能使用 [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource)來修改。

### <a name="create-the-initialization-data-for-the-buffer"></a>建立緩衝區的初始化資料

緩衝區只是專案的集合，而且會配置為一維陣列。 如此一來，系統記憶體的間距和系統記憶體配量的兩端都相同;頂點資料宣告的大小。 當使用 [**subresource 描述**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data)建立緩衝區時，應用程式可以提供初始化資料，其中包含實際資源資料的指標，以及包含該資料之大小和配置的相關資訊。

以不可變的使用方式建立的任何緩衝區 (查看 [**D3D10 \_ 用法 \_ 不可變**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) 的) 必須在建立時初始化。 使用 [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource)、 [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)和 [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource)進行初始化之後，或使用 [**Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10buffer-map) 方法存取其基礎記憶體之後，可以更新使用任何其他使用旗標的緩衝區。

### <a name="create-the-buffer"></a>建立緩衝區

使用緩衝區描述和初始化資料 (這是選擇性的) 呼叫 [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) 來建立頂點緩衝區。 下列程式碼片段示範如何從應用程式所宣告的頂點資料陣列建立頂點緩衝區。


```
struct SimpleVertexCombined
{
    D3DXVECTOR3 Pos;  
    D3DXVECTOR3 Col;  
};


ID3D10InputLayout* g_pVertexLayout = NULL;
ID3D10Buffer*      g_pVertexBuffer[2] = { NULL, NULL };
ID3D10Buffer*      g_pIndexBuffer = NULL;


SimpleVertexCombined verticesCombo[] =
{
    D3DXVECTOR3( 0.0f, 0.5f, 0.5f ),
    D3DXVECTOR3( 0.0f, 0.0f, 0.5f ),
    D3DXVECTOR3( 0.5f, -0.5f, 0.5f ),
    D3DXVECTOR3( 0.5f, 0.0f, 0.0f ),
    D3DXVECTOR3( -0.5f, -0.5f, 0.5f ),
    D3DXVECTOR3( 0.0f, 0.5f, 0.0f ),
};


    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage            = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth        = sizeof( SimpleVertexCombined ) * 3;
    bufferDesc.BindFlags        = D3D10_BIND_VERTEX_BUFFER;
    bufferDesc.CPUAccessFlags   = 0;
    bufferDesc.MiscFlags        = 0;
    
    D3D10_SUBRESOURCE_DATA InitData;
    InitData.pSysMem = verticesCombo;
    InitData.SysMemPitch = 0;
    InitData.SysMemSlicePitch = 0;
    hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pVertexBuffer[0] );
```



## <a name="create-an-index-buffer"></a>建立索引緩衝區

建立索引緩衝區與建立頂點緩衝區非常類似;有兩個差異。 索引緩衝區只包含16位或32位的資料 (，而不是頂點緩衝區可用的各種格式。 索引緩衝區也需要索引緩衝區系結旗標。

下列範例示範如何從索引資料的陣列建立索引緩衝區。


```
ID3D10Buffer *g_pIndexBuffer = NULL;

    // Create indices
    unsigned int indices[] = { 0, 1, 2 };

    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage           = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth       = sizeof( unsigned int ) * 3;
    bufferDesc.BindFlags       = D3D10_BIND_INDEX_BUFFER;
    bufferDesc.CPUAccessFlags  = 0;
    bufferDesc.MiscFlags       = 0;

    D3D10_SUBRESOURCE_DATA InitData;
    InitData.pSysMem = indices;
    InitData.SysMemPitch = 0;
    InitData.SysMemSlicePitch = 0;
    hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pIndexBuffer );
    if( FAILED( hr ) )
        return hr;
  
    g_pd3dDevice->IASetIndexBuffer( g_pIndexBuffer, DXGI_FORMAT_R32_UINT, 0 );
```



## <a name="create-a-constant-buffer"></a>建立常數緩衝區

Direct3D 10 引進常數緩衝區。 常數緩衝區（或著色器常數緩衝區）是包含著色器常數的緩衝區。 以下是建立常數緩衝區（取自 [HLSLWithoutFX10 範例](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)）的範例。


```
ID3D10Buffer*   g_pConstantBuffer10 = NULL;

struct VS_CONSTANT_BUFFER
{
    D3DXMATRIX mWorldViewProj;      //mWorldViewProj will probably be global to all shaders in a project.
                                    //It's a good idea not to move it around between shaders.
    D3DXVECTOR4 vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;                    //fTime may also be global to all shaders in a project.
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
};

    D3D10_BUFFER_DESC cbDesc;
    cbDesc.ByteWidth = sizeof( VS_CONSTANT_BUFFER );
    cbDesc.Usage = D3D10_USAGE_DYNAMIC;
    cbDesc.BindFlags = D3D10_BIND_CONSTANT_BUFFER;
    cbDesc.CPUAccessFlags = D3D10_CPU_ACCESS_WRITE;
    cbDesc.MiscFlags = 0;
    hr = g_pd3dDevice->CreateBuffer( &cbDesc, NULL, &g_pConstantBuffer10 );
    if( FAILED( hr ) )
       return hr;

    g_pd3dDevice->VSSetConstantBuffers( 0, 1, g_pConstantBuffer10 );
```



請注意，使用 [**ID3D10Effect 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) 介面時， **ID3D10Effect 介面** 實例會處理建立、系結和 comitting 常數緩衝區的進程。 在這種情況下，只會 nescesary 使用其中一個 GetVariable 方法（例如 [**GetVariableByName**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) ）來從效果中取得變數，並使用其中一個 SetVariable 方法（例如 [**SetMatrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix)）來更新變數。 如需使用 **ID3D10Effect 介面** 管理常數緩衝區的範例，請參閱 [教學課程7：材質對應和常數緩衝區](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (Direct3D 10) 的資源 ](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



