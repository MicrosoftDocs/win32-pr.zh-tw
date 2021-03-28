---
title: 如何建立頂點緩衝區
description: 本主題說明如何初始化靜態頂點緩衝區，也就是不會變更的頂點緩衝區。
ms.assetid: 584a39d1-7629-429a-b451-64b1432cb48f
keywords:
- 頂點緩衝區，建立
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e0b3d9d8f731b01e7c919105c21c8d150f864a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301275"
---
# <a name="how-to-create-a-vertex-buffer"></a>如何：建立頂點緩衝區

[頂點緩衝區](overviews-direct3d-11-resources-buffers-intro.md) 包含每個頂點資料。 本主題說明如何初始化靜態 [頂點緩衝區](overviews-direct3d-11-resources-buffers-intro.md)，也就是不會變更的頂點緩衝區。 如需初始化非靜態緩衝區的說明，請參閱「 [備註](#remarks) 」一節。

**若要初始化靜態頂點緩衝區**

1.  定義描述頂點的結構。 例如，如果您的頂點資料包含位置資料和色彩資料，您的結構會有一個描述位置的向量，另一個則會描述色彩。
2.  針對您在步驟1中定義的結構，使用 malloc 或新的) 配置記憶體 (。 使用描述您幾何的實際頂點資料來填滿此緩衝區。
3.  填入 [**D3D11 \_ 緩衝區 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) 結構來建立緩衝區描述。 將 D3D11 系 \_ 結 \_ 頂點 \_ 緩衝區旗標傳遞給 **BindFlags** 成員，然後將步驟1的結構大小傳遞給 **ByteWidth** 成員。
4.  填入 [**D3D11 \_ subresource \_ 資料**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) 結構，以建立 subresource 資料描述。 [**D3D11 \_ SUBRESOURCE \_ 資料**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data)結構的 **pSysMem** 成員應該直接指向步驟2中建立的資源資料。
5.  傳遞 [**D3D11 \_ 緩衝區 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)結構、 [**D3D11 \_ SUBRESOURCE \_ 資料**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data)結構，以及要初始化之 [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)介面指標的位址時，呼叫 [**ID3D11Device：： CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) 。

下列程式碼範例示範如何建立頂點緩衝區。 此範例假設 **g \_ pd3dDevice** 是有效的 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 物件。


```
ID3D11Buffer*      g_pVertexBuffer;

// Define the data-type that
// describes a vertex.
struct SimpleVertexCombined
{
    XMFLOAT3 Pos;  
    XMFLOAT3 Col;  
};

// Supply the actual vertex data.
SimpleVertexCombined verticesCombo[] =
{
    XMFLOAT3( 0.0f, 0.5f, 0.5f ),
    XMFLOAT3( 0.0f, 0.0f, 0.5f ),
    XMFLOAT3( 0.5f, -0.5f, 0.5f ),
    XMFLOAT3( 0.5f, 0.0f, 0.0f ),
    XMFLOAT3( -0.5f, -0.5f, 0.5f ),
    XMFLOAT3( 0.0f, 0.5f, 0.0f ),
};

// Fill in a buffer description.
D3D11_BUFFER_DESC bufferDesc;
bufferDesc.Usage            = D3D11_USAGE_DEFAULT;
bufferDesc.ByteWidth        = sizeof( SimpleVertexCombined ) * 3;
bufferDesc.BindFlags        = D3D11_BIND_VERTEX_BUFFER;
bufferDesc.CPUAccessFlags   = 0;
bufferDesc.MiscFlags        = 0;

// Fill in the subresource data.
D3D11_SUBRESOURCE_DATA InitData;
InitData.pSysMem = verticesCombo;
InitData.SysMemPitch = 0;
InitData.SysMemSlicePitch = 0;

// Create the vertex buffer.
hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pVertexBuffer );
    
```



## <a name="remarks"></a>備註

以下是一些初始化隨著時間變更之頂點緩衝區的方式。

1.  使用 [**D3D11 \_ 使用方式 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)建立第2個緩衝區; 使用 [**>id3d11devicecoNtext：： Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)、 [**>id3d11devicecoNtext：：**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)Map 來填滿第二個緩衝區; 使用 [**>id3d11devicecoNtext：： CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) 從暫存緩衝區複製到預設緩衝區。
2.  使用 [**>id3d11devicecoNtext：： UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) 從記憶體複製資料。
3.  使用 [**D3D11 使用 \_ \_ 動態**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)來建立緩衝區，並將 [**>id3d11devicecoNtext：： Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)、 [**>id3d11devicecoNtext：：**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) 取消對應 (適當地使用捨棄和 NoOverwrite 旗標) 來填滿。

\#1和 \# 2 適用于每個畫面格不到一次變更的內容。 一般而言，GPU 讀取速度很快，CPU 更新將會變慢。

\#3對每個畫面格變更一次以上的內容很有用。 一般而言，GPU 讀取速度會變慢，但是 CPU 更新會更快。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[緩衝區](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[如何使用 Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




