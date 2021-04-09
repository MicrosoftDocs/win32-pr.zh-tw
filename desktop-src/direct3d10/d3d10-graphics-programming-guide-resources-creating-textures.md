---
description: 材質資源是一種結構化的資料集合。
ms.assetid: 4c716be8-044e-4ed4-aeca-4379440826bd
title: 建立 (Direct3D 10) 的材質資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81f2ca200b566d17b02af56c48cb1227c41106ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936326"
---
# <a name="creating-texture-resources-direct3d-10"></a>建立 (Direct3D 10) 的材質資源

[材質](d3d10-graphics-programming-guide-resources-types.md)資源是一種結構化的資料集合。 一般而言，色彩值會儲存在材質中，並在 [管線](d3d10-graphics-programming-guide-pipeline-stages.md) 于輸入和輸出的不同階段呈現時存取。 建立材質和定義其使用方式，是在 Direct3D 10 中呈現有趣外觀的重要部分。

雖然材質通常包含色彩資訊，但使用不同的 [**DXGI \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 建立紋理可讓它們儲存不同類型的資料。 如此一來，Direct3D 10 管線便可利用非傳統的方式來利用這項資料。

所有紋理都有其所耗用的記憶體數量，以及它們所包含的材質數目的限制。 這些限制是由 [資源常數](d3d10-graphics-reference-resource-constants.md)指定。

-   [從檔案建立材質](#create-a-texture-from-a-file)
    -   [另外建立材質和視野](#create-texture-and-view-separately)
    -   [同時建立材質和視野](#create-texture-and-view-simultaneously)
-   [建立空白紋理](#creating-empty-textures)
    -   [轉譯成材質](#rendering-to-a-texture)
    -   [手動填入紋理](#filling-textures-manually)
-   [多個 Rendertargets](#multiple-rendertargets)
-   [相關主題](#related-topics)

## <a name="create-a-texture-from-a-file"></a>從檔案建立材質

> [!Note]  
> [D3DX 公用程式程式庫](d3d10-graphics-reference-d3dx10.md)已針對 Windows 8 淘汰，不支援 Windows Store 應用程式。

 

當您在 Direct3D 10 中建立材質時，您也需要建立一個 [view](d3d10-graphics-programming-guide-resources-access-views.md)。 View 是一個物件，會告知裝置在轉譯期間應如何存取材質。 存取材質最常見的方式是使用 [著色器](../direct3dhlsl/dx-graphics-hlsl.md)來讀取它。 著色器資源檢視會告知著色器如何在轉譯期間讀取紋理。 當您建立材質時，必須指定材質的檢視類型。

您可以透過兩種不同的方式來建立材質和載入其初始資料：個別建立材質和視圖，或是同時建立材質和視圖。 API 提供這兩種技術，讓您可以選擇更適合您的需求。

### <a name="create-texture-and-view-separately"></a>另外建立材質和視野

建立材質最簡單的方式，就是從影像檔載入它。 若要建立紋理，請只填妥一個結構，並將材質的名稱提供給 [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md)。


```
ID3D10Device *pDevice = NULL;
// Initialize D3D10 device...

D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;

ID3D10Resource *pTexture = NULL;
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pTexture, NULL );
```



D3DX 函式 [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) 會執行三件事：首先，它會建立 Direct3D 10 紋理物件;其次，它會讀取輸入影像檔案;第三，它會將影像資料儲存在材質物件中。 在上述範例中，會載入 BMP 檔案，但函數可以載入各種檔案類型。

系結旗標表示紋理將建立為著色器資源，可讓著色器階段在轉譯期間讀取紋理。

上述範例未指定所有載入參數。 事實上，直接將載入參數輸出為零很有説明，因為這可讓 D3DX 根據輸入影像選擇適當的值。 如果您希望輸入影像判斷材質建立時所使用的所有參數，只要針對 **loadInfo** 參數指定 **Null** 即可，如下所示：


```
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", NULL, NULL, &pTexture, NULL );
```



針對載入資訊指定 **Null** 是一個簡單但功能強大的快捷方式。

現在已建立紋理，您需要建立著色器資源的視圖，讓材質可以系結為著色器的輸入。 由於 [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) 會傳回資源的指標，而不是紋理的指標，因此您必須判斷所載入的確切資源類型，然後您可以使用 [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview)來建立著色器資源檢視。


```
D3D10_SHADER_RESOURCE_VIEW_DESC srvDesc;
D3D10_RESOURCE_DIMENSION type;
pTexture->GetType( &type );
switch( type )
{
    case D3D10_RESOURCE_DIMENSION_BUFFER:
    //...
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE1D:
    //...
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE2D:
    {
        D3D10_TEXTURE2D_DESC desc;
        ID3D10Texture2D *pTexture2D = (ID3D10Texture2D*)pTexture;
        pTexture2D->GetDesc( &desc );
        
        srvDesc.Format = desc.Format;
        srvDesc.ViewDimension = D3D10_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Texture2D.MipLevels = desc.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = desc.MipLevels -1;

    }
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE3D:
    //...
    break;
    default:
    //...
    break;
}

ID3D10ShaderResourceView *pSRView = NULL;
pDevice->CreateShaderResourceView( pTexture, &srvDesc, &pSRView );
```



雖然上述範例會建立2D 著色器資源檢視，但建立其他著色器資源檢視類型的程式碼非常相似。 任何著色器階段現在都可以使用此材質做為輸入。

使用 [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) 和 [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview) 建立材質和其相關聯的視圖是準備材質系結至著色器階段的一種方式。 另一種方式是同時建立材質和其觀點，在下一節中將會討論。

### <a name="create-texture-and-view-simultaneously"></a>同時建立材質和視野

Direct3D 10 同時需要材質和著色器資源檢視，才能在執行時間期間讀取材質。 由於建立材質和著色器資源檢視是很常見的工作，D3DX 會提供 [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) 來為您完成此作業。


```
D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;

ID3D10ShaderResourceView *pSRView = NULL;
D3DX10CreateShaderResourceViewFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pSRView, NULL );
```



使用單一 D3DX 呼叫時，會建立材質和著色器資源檢視。 **LoadInfo** 參數的功能未變更;您可以使用它來自訂材質的建立方式，或針對 **loadInfo** 參數指定 **Null** ，以從輸入檔衍生必要的參數。

[**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md)函數所傳回的 [**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)物件稍後可以用來取得原始 [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)介面（如有需要）。 這可以藉由呼叫 [**GetResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10view-getresource) 方法來完成。

D3DX 提供單一函式，可將材質和著色器資源檢視建立為 convienience;您決定哪一種方法來建立材質和視野最適合您的應用程式需求。

現在您已瞭解如何建立材質和其著色器資源檢視，下一節將示範如何使用著色器 (從該材質讀取) 。

## <a name="creating-empty-textures"></a>建立空白紋理

有時候，應用程式會想要建立材質並計算要儲存在材質中的資料，或使用圖形 [管線](d3d10-graphics-programming-guide-pipeline-stages.md) 來轉譯成此材質，稍後再使用其他處理的結果。 圖形管線或應用程式本身可以更新這些紋理，這取決於建立時所指定的材質 [**使用**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) 類型。

### <a name="rendering-to-a-texture"></a>轉譯成材質

在執行時間中建立空白紋理以填滿資料的最常見案例，就是應用程式想要轉譯成材質，然後在後續階段中使用轉譯作業的結果。 以此目的建立的材質應指定預設 [**使用**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)方式。

下列程式碼範例會建立空的材質，讓管線可轉譯為，然後再作為 [著色器](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md)的輸入使用。


```
// Create the render target texture
D3D10_TEXTURE2D_DESC desc;
ZeroMemory( &desc, sizeof(desc) );
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = 1;
desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R32G32B32A32_FLOAT;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DEFAULT;
desc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;

ID3D10Texture2D *pRenderTarget = NULL;
pDevice->CreateTexture2D( &desc, NULL, &pRenderTarget );
```



建立材質需要應用程式指定材質將擁有之屬性的一些相關資訊。 材質中材質的寬度和高度設定為256。 針對此轉譯目標，我們只需要一個 mipmap 層級。 只有一個轉譯目標是必要的，因此陣列大小設定為1。 每個材質都包含 4 32 位浮點值，可用來儲存非常精確的資訊 (查看 [**DXGI \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)) 。 每個圖元都需要一個樣本。 使用方式會設定為 [預設]，因為這樣可讓轉譯目標在記憶體中最有效率的放置位置。 最後，紋理會系結為轉譯目標，並指定不同時間點的著色器資源。

紋理無法系結以直接轉譯為管線;使用呈現目標視圖，如下列程式碼範例所示。


```
D3D10_RENDER_TARGET_VIEW_DESC rtDesc;
rtDesc.Format = desc.Format;
rtDesc.ViewDimension = D3D10_RTV_DIMENSION_TEXTURE2D;
rtDesc.Texture2D.MipSlice = 0;

ID3D10RenderTargetView *pRenderTargetView = NULL;
pDevice->CreateRenderTargetView( pRenderTarget, &rtDesc, &pRenderTargetView );
```



轉譯目標視圖的格式只是設定為原始紋理的格式。 資源中的資訊應該被視為2D 材質，而我們只想要使用轉譯目標的第一個 mipmap 層級。

同樣地，您必須建立轉譯目標視圖，才能系結轉譯目標以輸出至管線，必須建立著色器資源檢視，才能將轉譯目標系結至管線做為輸入。 下列程式碼範例將示範這一點。


```
// Create the shader-resource view
D3D10_SHADER_RESOURCE_VIEW_DESC srDesc;
srDesc.Format = desc.Format;
srDesc.ViewDimension = D3D10_SRV_DIMENSION_TEXTURE2D;
srDesc.Texture2D.MostDetailedMip = 0;
srDesc.Texture2D.MipLevels = 1;

ID3D10ShaderResourceView *pShaderResView = NULL;
pDevice->CreateShaderResourceView( pRenderTarget, &srDesc, &pShaderResView );
```



著色器-資源檢視描述的參數與轉譯目標視圖描述的參數非常類似，而且基於相同的原因而被選擇。

### <a name="filling-textures-manually"></a>手動填入紋理

有時候應用程式會想要在執行時間計算值、手動將它們放入材質，然後讓圖形 [管線](d3d10-graphics-programming-guide-pipeline-stages.md) 在後續轉譯作業中使用此材質。 若要這樣做，應用程式必須以允許 CPU 存取基礎記憶體的方式，建立空的材質。 這是藉由建立動態材質來完成，並藉由呼叫特定方法來取得基礎記憶體的存取權。 下列程式碼範例示範如何執行這項操作。


```
D3D10_TEXTURE2D_DESC desc;
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DYNAMIC;
desc.BindFlags = D3D10_BIND_SHADER_RESOURCE;
desc.CPUAccessFlags = D3D10_CPU_ACCESS_WRITE;
ID3D10Texture2D *pTexture = NULL;
pd3dDevice->CreateTexture2D( &desc, NULL, &pTexture );
```



請注意，格式設定為每圖元32位，其中每個元件都是由8個位定義。 使用方式參數設定為動態，而系結旗標設定為指定材質將由著色器存取。 材質描述的其餘部分類似于建立轉譯目標。

呼叫 [**對應**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) 可讓應用程式存取材質的基礎記憶體。 然後，會使用已取出的指標來填滿具有資料的材質。 這可以在下列程式碼範例中看到。


```
D3D10_MAPPED_TEXTURE2D mappedTex;
pTexture->Map( D3D10CalcSubresource(0, 0, 1), D3D10_MAP_WRITE_DISCARD, 0, &mappedTex );

UCHAR* pTexels = (UCHAR*)mappedTex.pData;
for( UINT row = 0; row < desc.Height; row++ )
{
    UINT rowStart = row * mappedTex.RowPitch;
    for( UINT col = 0; col < desc.Width; col++ )
    {
        UINT colStart = col * 4;
        pTexels[rowStart + colStart + 0] = 255; // Red
        pTexels[rowStart + colStart + 1] = 128; // Green
        pTexels[rowStart + colStart + 2] = 64;  // Blue
        pTexels[rowStart + colStart + 3] = 32;  // Alpha
    }
}

pTexture->Unmap( D3D10CalcSubresource(0, 0, 1) );
```



## <a name="multiple-rendertargets"></a>多個 Rendertargets

使用 [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets))  (時，最多可以將8個轉譯目標視圖系結至管線。 針對每個圖元 (或每個範例，如果已啟用 [取樣]) ，則會針對每個轉譯目標視圖獨立進行混合。 其中兩個 blend 狀態變數（BlendEnable 和 RenderTargetWriteMask）是八陣列，每個陣列成員都對應到轉譯目標視圖。 使用多個呈現目標時，每個轉譯目標都必須是相同的 [資源類型](d3d10-graphics-programming-guide-resources-types.md) (緩衝區、1d 材質、2d 材質陣列等 ) ，而且必須具有相同的維度 (寬度、高度、3d 紋理的深度，以及紋理陣列的陣列大小) 。 如果呈現目標是多重取樣，則它們的每個圖元都必須有相同的樣本數目。

不論使用中的轉譯目標數目為何，都只能有一個作用中的深度樣板緩衝區為啟用狀態。 使用紋理陣列做為轉譯目標時，所有視圖維度都必須相符。 轉譯目標不需要具有相同的材質格式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (Direct3D 10) 的資源 ](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
