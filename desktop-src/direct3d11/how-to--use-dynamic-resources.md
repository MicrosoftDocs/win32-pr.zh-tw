---
title: 如何使用動態資源
description: 當您的應用程式需要變更這些資源中的資料時，您會建立和使用動態資源。 您可以建立動態使用方式的材質和緩衝區。
ms.assetid: E73EA4B0-BD14-430C-89CA-4CFCF92C7548
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41e00cda7236040679c7863454e4cc18d81106b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183113"
---
# <a name="how-to-use-dynamic-resources"></a>如何：使用動態資源

**重要 API**

-   [**>id3d11devicecoNtext：： Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)
-   [**>id3d11devicecoNtext：：取消對應**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)
-   [**D3D11 \_ 使用方式**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)

當您的應用程式需要變更這些資源中的資料時，您會建立和使用動態資源。 您可以建立動態使用方式的材質和緩衝區。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [如何：建立材質](overviews-direct3d-11-resources-textures-create.md)
-   [如何：以程式設計方式初始化材質](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
-   [如何：建立常數緩衝區](overviews-direct3d-11-resources-buffers-constant-how-to.md)

### <a name="prerequisites"></a>必要條件

我們假設您熟悉 C++。 您還需要圖形程式設計概念的基本經驗。

## <a name="instructions"></a>指示

### <a name="step-1-specify-dynamic-usage"></a>步驟1：指定動態使用方式

如果您想要讓應用程式能夠變更資源，您必須在建立資源時將這些資源指定為動態和可寫入。

**若要指定動態使用方式**

1.  將資源使用方式指定為動態。 例如，在頂點或常數緩衝區之 [**D3D11 \_ 緩衝區 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)的 **usage** 成員中指定 [**D3D11 \_ 使用 \_ 動態**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)值，並在 [**D3D11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc)的 **usage** 成員中，為2d 材質指定 **D3D11 \_ 使用 \_ 動態** 值。
2.  將資源指定為可寫入。 例如，在 [**D3D11 \_ BUFFER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)或 [**D3D11 \_ TEXTURE2D \_ Desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc)的 **CPUAccessFlags** 成員中，指定 [**D3D11 \_ CPU \_ 存取 \_ 寫入**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag)值。
3.  將資源描述傳遞給建立函數。 例如，將 [**D3D11 \_ 緩衝區 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) 的位址傳遞至 [**ID3D11Device：： CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) ，並將 [**D3D11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) 的位址傳遞至 [**ID3D11Device：： CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d)。

以下是建立動態頂點緩衝區的範例：


```C++
    // Create a vertex buffer for a triangle.

    float2 triangleVertices[] =
    {
        float2(-0.5f, -0.5f),
        float2(0.0f, 0.5f),
        float2(0.5f, -0.5f),
    };

    D3D11_BUFFER_DESC vertexBufferDesc = { 0 };
    vertexBufferDesc.ByteWidth = sizeof(float2)* ARRAYSIZE(triangleVertices);
    vertexBufferDesc.Usage = D3D11_USAGE_DYNAMIC;
    vertexBufferDesc.BindFlags = D3D11_BIND_VERTEX_BUFFER;
    vertexBufferDesc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;
    vertexBufferDesc.MiscFlags = 0;
    vertexBufferDesc.StructureByteStride = 0;

    D3D11_SUBRESOURCE_DATA vertexBufferData;
    vertexBufferData.pSysMem = triangleVertices;
    vertexBufferData.SysMemPitch = 0;
    vertexBufferData.SysMemSlicePitch = 0;

    DX::ThrowIfFailed(
        m_d3dDevice->CreateBuffer(
        &vertexBufferDesc,
        &vertexBufferData,
        &vertexBuffer2
        )
        );

```



### <a name="step-2-change-a-dynamic-resource"></a>步驟2：變更動態資源

如果您在建立資源時將其指定為動態，您稍後可以對該資源進行變更。

**變更動態資源中的資料**

1.  設定資源的新資料。 宣告 [**D3D11 \_ 對應的 \_ SUBRESOURCE**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) 類型變數，並將它初始化為零。 您將使用此變數來變更資源。
2.  停用圖形處理單元 (GPU) 您要變更的資料存取，並取得包含資料之記憶體的指標。 若要取得這個指標，請在呼叫 [**>id3d11devicecoNtext：： MAP**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)時，將 [**D3D11 \_ MAP \_ WRITE \_ 捨棄**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)傳遞給 *MapType* 參數。 將此指標設定為上一個步驟中 [**D3D11 \_ 對應 \_ SUBRESOURCE**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) 變數的位址。
3.  將新資料寫入至記憶體。
4.  當您完成寫入新資料時，請呼叫 [**>id3d11devicecoNtext：：**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) 取消對應來重新啟用資料的 GPU 存取。

以下是變更動態頂點緩衝區的範例：


```C++
// This might get called as the result of a click event to double the size of the triangle.
void TriangleRenderer::MapDoubleVertices()
{
    D3D11_MAPPED_SUBRESOURCE mappedResource;
    ZeroMemory(&mappedResource, sizeof(D3D11_MAPPED_SUBRESOURCE));
    float2 vertices[] =
    {
        float2(-1.0f, -1.0f),
        float2(0.0f, 1.0f),
        float2(1.0f, -1.0f),
    };
    //  Disable GPU access to the vertex buffer data.
    auto m_d3dContext = m_deviceResources->GetD3DDeviceContext();
    m_d3dContext->Map(vertexBuffer2.Get(), 0, D3D11_MAP_WRITE_DISCARD, 0, &mappedResource);
    //  Update the vertex buffer here.
    memcpy(mappedResource.pData, vertices, sizeof(vertices));
    //  Reenable GPU access to the vertex buffer data.
    m_d3dContext->Unmap(vertexBuffer2.Get(), 0);
}
```



## <a name="remarks"></a>備註

### <a name="using-dynamic-textures"></a>使用動態紋理

建議您只針對每個格式建立一個動態材質，而且可能每個大小。 由於對應每個層級的額外負荷，因此不建議您建立動態 mipmap、cube 和磁片區。 針對 mipmap，您可以在最上層指定 [**D3D11 \_ 對應 \_ 寫入 \_ 捨棄**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) 。 所有層級都是藉由只對應最上層來捨棄。 此行為對於磁片區和 cube 而言是相同的。 針對 cube，會對應最上層和臉部0。

### <a name="using-dynamic-buffers"></a>使用動態緩衝區

當您在 GPU 使用緩衝區時，于靜態頂點緩衝區上呼叫 [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) 時，會產生顯著的效能影響。 在這種情況下， **map** 必須等到 GPU 完成從緩衝區讀取頂點或索引資料之後， **對應** 才能返回呼叫的應用程式，這會導致明顯的延遲。 呼叫 **map** ，然後針對每個框架從靜態緩衝區轉譯數次，也可防止 GPU 緩衝轉譯命令，因為它必須在傳回 Map 指標之前完成命令。 如果沒有緩衝的命令，GPU 會保持閒置，直到應用程式完成填滿頂點緩衝區或索引緩衝區，併發出轉譯命令為止。

在理想的情況下，頂點或索引資料永遠不會變更，但這並不一定可行。 在許多情況下，應用程式需要變更每個畫面格的頂點或索引資料，甚至是每個框架的次數。 在這些情況下，我們建議您建立具有 [**\_ \_ 動態 D3D11 使用**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)方式的頂點或索引緩衝區。 此使用旗標會讓執行時間針對頻繁的對應作業進行優化。 **D3D11 \_只有 \_** 當緩衝區經常對應時，使用動態才有用;如果資料仍維持不變，請將該資料放在靜態頂點或索引緩衝區中。

若要在使用動態頂點緩衝區時獲得效能改進，您的應用程式必須使用適當的 [**D3D11 \_ 對應**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)值來呼叫 [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) 。 [**D3D11 \_對應 \_ 寫入 \_ 捨棄**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) 表示應用程式不需要將舊的頂點或索引資料保留在緩衝區中。 當您使用 **D3D11 \_ 對應 \_ 寫入 \_ 捨棄** 來呼叫 **Map** 時，如果 GPU 仍在使用緩衝區，則執行時間會傳回新的記憶體區域的指標，而不是舊的緩衝區資料。 這可讓 GPU 在應用程式將資料放在新的緩衝區時，繼續使用舊的資料。 應用程式不需要額外的記憶體管理;當 GPU 完成時，會自動重複使用或終結舊的緩衝區。

> [!Note]  
> 當您對應具有 [**D3D11 \_ 對應 \_ 寫入 \_ 捨棄**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)的緩衝區時，執行時間一律會捨棄整個緩衝區。 您無法藉由指定非零位移或受限大小欄位，來保留緩衝區未對應區域中的資訊。

 

在某些情況下，應用程式在每個地圖上儲存的資料量很小，例如新增四個頂點以呈現 sprite。 [**D3D11 \_「對應 \_ 寫入 \_ 無 \_ 覆寫**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) 」表示應用程式不會覆寫動態緩衝區中已在使用中的資料。 [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)呼叫會傳回舊資料的指標，讓應用程式能夠在頂點或索引緩衝區未使用的區域中加入新的資料。 應用程式不能修改繪製作業中使用的頂點或索引，因為它們可能仍在 GPU 中使用。 我們建議應用程式在動態緩衝區填滿之後，使用 [**D3D11 \_ 對應 \_ 寫入 \_ 捨棄**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) ，以接收新的記憶體區域，這會在 GPU 完成之後捨棄舊的頂點或索引資料。

非同步查詢機制很適合用來判斷 GPU 是否仍在使用頂點。 在使用頂點的最後一個繪製呼叫之後，發出類型 [**D3D11 \_ query \_ 事件**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_query) 的查詢。 當 [**>id3d11devicecoNtext：：：：：：**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) 時，不會再使用頂點 \_ 。 當您對應具有 [**D3D11 \_ map \_ WRITE \_ 捨棄**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) 或無對應值的緩衝區時，一律保證頂點會與 GPU 正確地同步處理。 但是，當您對應但未對應值時，將會產生稍早所述的效能負面影響。

> [!Note]  
> 從 Windows 8 開始提供的 Direct3D 11.1 執行時間，可讓您將動態常數緩衝區和著色器資源流覽 (SRVs) 動態緩衝區，並將 [**D3D11 \_ 對應 \_ 寫入 [ \_ 不 \_ 覆寫**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)]。 Direct3D 11 和舊版執行時間限制對頂點或索引緩衝區的無覆寫部分更新對應。 若要判斷 Direct3D 裝置是否支援這些功能，請使用 [**D3D11 \_ 功能 \_ D3D11 \_ 選項**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature)來呼叫 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) 。 **CheckFeatureSupport** 會以裝置的功能填滿 [**D3D11 \_ 功能 \_ 資料 \_ D3D11 \_ 選項**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) 結構的成員。 這裡的相關成員是 **MapNoOverwriteOnDynamicConstantBuffer** 和 **MapNoOverwriteOnDynamicBufferSRV**。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何使用 Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




