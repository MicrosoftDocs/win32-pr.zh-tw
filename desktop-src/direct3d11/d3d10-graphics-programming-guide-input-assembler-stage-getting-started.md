---
title: 使用 Input-Assembler 階段開始使用
description: 有幾個步驟需要初始化輸入組合語言 (IA) 階段。
ms.assetid: 84c0ca29-2356-4b7f-98ee-ff1758edc540
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901b3facfef781e3f44acf75bee737f280dece55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375800"
---
# <a name="getting-started-with-the-input-assembler-stage"></a>使用 Input-Assembler 階段開始使用

有幾個步驟需要初始化輸入組合語言 (IA) 階段。 例如，您需要使用管線所需的頂點資料來建立緩衝區資源、告知 IA 階段，其中緩衝區是和它們所包含的資料類型，並指定要從資料組合的基本類型。

本主題將涵蓋設定 IA 階段所需的基本步驟（如下表所示）。



| 步驟                                                                                    | 描述                                                                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [建立輸入緩衝區](#create-input-buffers)                                           | 使用輸入頂點資料來建立和初始化輸入緩衝區。                                           |
| [建立 Input-Layout 物件](#create-the-input-layout-object)                       | 定義如何使用輸入設定物件，將頂點緩衝區資料串流至 IA 階段。 |
| [將物件系結至 Input-Assembler 階段](#bind-objects-to-the-input-assembler-stage) | 將建立的物件 (輸入緩衝區和輸入設定物件) 系結至 IA 階段。                 |
| [指定基本類型](#specify-the-primitive-type)                               | 識別如何將頂點組合成基本專案。                                          |
| [呼叫 Draw 方法](#call-draw-methods)                                                 | 透過管線傳送系結至 IA 階段的資料。                                             |



 

在您瞭解這些步驟之後，請繼續 [使用 System-Generated 的值](d3d10-graphics-programming-guide-input-assembler-stage-using.md)。

## <a name="create-input-buffers"></a>建立輸入緩衝區

輸入緩衝區有兩種類型： [頂點緩衝區](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) 和索引緩衝區。 頂點緩衝區可提供頂點資料給 IA 階段。 索引緩衝區是選擇性的;它們會從頂點緩衝區提供頂點的索引。 您可以建立一或多個頂點緩衝區，並選擇性地建立索引緩衝區。

建立緩衝區資源之後，您必須建立輸入設定物件來描述 IA 階段的資料版面配置，然後您必須將緩衝區資源系結至 IA 階段。 如果您的著色器未使用緩衝區，則不需要建立和系結緩衝區。 如需繪製單一三角形的簡單頂點和圖元著色器範例，請參閱 [使用不含緩衝區的 Input-Assembler 階段](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md)。

如需建立頂點緩衝區的協助，請參閱 [建立頂點緩衝區](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating)。 如需建立索引緩衝區的協助，請參閱建立索引緩衝區。

## <a name="create-the-input-layout-object"></a>建立 Input-Layout 物件

輸入設定物件會封裝 IA 階段的輸入狀態。 這包括系結至 IA 階段之輸入資料的描述。 從一或多個頂點緩衝區，將資料從記憶體串流至 IA 階段。 描述會識別從一個或多個頂點緩衝區系結的輸入資料，並讓執行時間能夠根據著色器輸入參數類型來檢查輸入資料類型。 這種類型檢查不只會驗證類型是否相容，而且每個著色器所需的元素都可在緩衝區資源中使用。

輸入設定物件是從輸入-元素描述的陣列和已編譯著色器的指標所建立 (請參閱 [**ID3D11Device：： CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout)) 。 陣列包含一或多個輸入元素;每個輸入元素都會從單一頂點緩衝區描述單一頂點資料元素。 整組輸入元素描述會描述所有將繫結至 IA 階段的端點緩衝區中的所有頂點資料元素。

下列版面配置描述描述包含三個頂點資料元素的單一頂點緩衝區：


```
D3D11_INPUT_ELEMENT_DESC layout[] =
{
    { L"POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
    { L"TEXCOORD", 0, DXGI_FORMAT_R32G32_FLOAT, 0, 12, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
    { L"NORMAL", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 20, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
};
```



輸入專案描述會描述頂點緩衝區中單一頂點所包含的每個專案，包括大小、類型、位置和用途。 每個資料列都會使用語義、語義索引和資料格式來識別資料的類型。 [語義](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)是識別資料使用方式的文字字串。 在此範例中，第一個資料列會識別3個元件的位置資料 (*xyz*，例如) ;第二個數據列會識別兩個元件的材質資料 (*UV*，例如) ;第三個數據列會識別一般資料。

在此輸入專案描述的範例中，語義索引 (這三個數據列的第二個參數) 設定為零。 語義索引可協助您區分兩個使用相同語義的資料列。 因為此範例中沒有類似的語法，所以可以將語義索引設定為其預設值零。

第三個參數是 *格式*。 格式 (請參閱 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) 指定每個元素的元件數目，以及資料類型，該資料類型會定義每個元素的資料大小。 在建立資源時可以完全輸入格式，或您可以使用 **DXGI \_ 格式** 來建立資源，以識別元素中的元件數目，但不定義資料類型。

### <a name="input-slots"></a>輸入位置

資料會透過稱為 *輸入* 位置的輸入進入 IA 階段，如下圖所示。 IA 階段有 *n* 個輸入位置，其設計目的是要容納最多可提供輸入資料的 *n* 個頂點緩衝區。 每個頂點緩衝區都必須指派給不同的位置;當輸入設定物件建立時，這項資訊會儲存在輸入配置宣告中。 您也可以指定從每個緩衝區開頭到要讀取之緩衝區中第一個元素的位移。

![ia 階段輸入位置的圖例](images/d3d10-ia-slots.png)

接下來的兩個參數是 *輸入* 位置和 *輸入位移*。 當您使用多個緩衝區時，可以將它們系結至一或多個輸入位置。 輸入位移是緩衝區開頭與資料開頭之間的位元組數目。

### <a name="reusing-input-layout-objects"></a>重複使用 Input-Layout 物件

每個輸入設定物件都會根據著色器簽章建立;這可讓 API 針對著色器輸入簽章來驗證輸入設定物件元素，以確保與類型和語義完全相符。 只要所有著色器輸入簽章完全相符，您就可以為許多著色器建立單一的輸入版面設定物件。

## <a name="bind-objects-to-the-input-assembler-stage"></a>將物件系結至 Input-Assembler 階段

建立頂點緩衝區資源和輸入設定物件之後，您可以藉由呼叫 [**>id3d11devicecoNtext：： IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) 和 [**>id3d11devicecoNtext：： IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout)，將這些資源系結至 IA 階段。 下列範例顯示將單一頂點緩衝區和輸入設定物件系結至 IA 階段：


```
UINT stride = sizeof( SimpleVertex );
UINT offset = 0;
g_pd3dDevice->IASetVertexBuffers( 
    0,                // the first input slot for binding
    1,                // the number of buffers in the array
    &g_pVertexBuffer, // the array of vertex buffers
    &stride,          // array of stride values, one for each buffer
    &offset );        // array of offset values, one for each buffer

// Set the input layout
g_pd3dDevice->IASetInputLayout( g_pVertexLayout );
```



系結輸入版面設定物件只需要物件的指標。

在上述範例中，會系結單一頂點緩衝區;不過，多個頂點緩衝區可透過單一呼叫 [**>id3d11devicecoNtext：： IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers)來系結，而下列程式碼會顯示系結三個頂點緩衝區的呼叫：


```
UINT strides[3];
strides[0] = sizeof(SimpleVertex1);
strides[1] = sizeof(SimpleVertex2);
strides[2] = sizeof(SimpleVertex3);
UINT offsets[3] = { 0, 0, 0 };
g_pd3dDevice->IASetVertexBuffers( 
    0,                 //first input slot for binding
    3,                 //number of buffers in the array
    &g_pVertexBuffers, //array of three vertex buffers
    &strides,          //array of stride values, one for each buffer
    &offsets );        //array of offset values, one for each buffer
```



索引緩衝區會藉由呼叫 [**>id3d11devicecoNtext：： IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer)來系結至 IA 階段。

## <a name="specify-the-primitive-type"></a>指定基本類型

系結輸入緩衝區之後，必須告知 IA 階段如何將頂點組合成基本專案。 這是藉由呼叫 [**>id3d11devicecoNtext：： IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology); 指定 [基本類型](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-primitive-topologies)來完成下列程式碼會呼叫這個函式，將資料定義為不連續的三角形清單：


```
g_pd3dDevice->IASetPrimitiveTopology( D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST );
```



其餘的基本類型會列在 D3D 基本型 [**\_ \_ 拓撲**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology)中。

## <a name="call-draw-methods"></a>呼叫 Draw 方法

當輸入資源系結至管線之後，應用程式會呼叫 draw 方法來呈現基本專案。 有幾個 draw 方法，如下表所示：有些用途是使用索引緩衝區、某些使用實例資料，以及一些從資料流程輸出階段重複使用資料作為輸入組合語言階段輸入的資料。



| Draw 方法                                                                                  | Description                                                                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**ID3D11DeviceContext::Draw**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)                                 | 繪製非索引、非實例的基本類型。                                                            |
| [**ID3D11DeviceContext::DrawInstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawinstanced)               | 繪製非索引的實例基本專案。                                                                |
| [**ID3D11DeviceContext::DrawIndexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed)                   | 繪製索引、非實例的基本類型。                                                                |
| [**ID3D11DeviceContext::DrawIndexedInstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced) | 繪製已編制索引的實例基本專案。                                                                    |
| [**ID3D11DeviceContext::DrawAuto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto)                         | 從來自資料流程輸出階段的輸入資料，繪製非索引、非實例的基本類型。 |



 

每個 draw 方法都會呈現單一拓撲類型。 在轉譯期間，不完整的基本 (沒有足夠頂點的專案、缺少索引、部分基本專案，等等) 會以無訊息方式捨棄。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[輸入組合階段](d3d10-graphics-programming-guide-input-assembler-stage.md)
</dt> </dl>

 

 