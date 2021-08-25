---
title: Direct3D 11 中的緩衝區簡介
description: 緩衝區資源是一個完整輸入的資料集合，由元素所組成。
ms.assetid: e33ca01e-f13c-4f91-b0db-2b2bc6b4fd8f
keywords:
- 常數緩衝區，什麼是
- 頂點緩衝區，什麼是
- 索引緩衝區，什麼是
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d51f7b0dbd60264b77f9d9dc83f39cbb4325464079d537c3ee741a942d26a139
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752018"
---
# <a name="introduction-to-buffers-in-direct3d-11"></a>Direct3D 11 中的緩衝區簡介

緩衝區資源是一個完整輸入的資料集合，由元素所組成。 您可以使用緩衝區存放各式各樣的資料，包含位置向量、法向向量、頂點緩衝區中的紋理座標、索引緩衝區中的索引、或裝置狀態。 緩衝元素由 1 到 4 個元件組成。 緩衝元素可以包含封裝資料值 (像是 R8G8B8A8 面值)、單一 8 位整數，或四個 32 位元浮點數值。

建立緩衝區做為未結構化的資源。 因為未建立，緩衝不能包含任何 mipmap 層次，當讀取時無法篩選，而且無法多重採樣。

## <a name="buffer-types"></a>緩衝區類型

以下是 Direct3D 11 支援的緩衝區資源類型。 所有緩衝區類型都是由 [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) 介面所封裝。

-   [頂點緩衝區](#vertex-buffer)
-   [索引緩衝區](#index-buffer)
-   [常數緩衝區](#constant-buffer)

### <a name="vertex-buffer"></a>頂點緩衝區

頂點緩衝區包含用來定義您的幾何頂點資料。 頂點資料包括位置座標、色彩資料、紋理座標資料、一般資料等等。

最簡單的頂點緩衝區範例是僅包含位置資料者。 它可以像下圖一樣視覺化。

![包含位置資料的頂點緩衝區圖例](images/d3d10-resources-single-element-vb2.png)

頂點緩衝區經常包含可完整指定 3D 頂點所需的所有資料。 例如，可能會包含每個頂點位置、一般及紋理座標的頂點緩衝區。 此資料通常組織成每個頂點元素集，如下圖所示。

![頂點緩區的圖例，其包含位置、一般和紋理資料](images/d3d10-vertex-buffer-element.png)

這個頂點緩衝區包含每個頂點資料，而每個頂點儲存三個元素 (位置、一般和紋理座標)。 位置和一般都是使用 3 32 位浮點數 (DXGI \_ 格式 \_ R32G32B32 \_ FLOAT) 和材質座標（使用 2 32 位浮點數 (\_ \_ float 格式 R32G32 \_ FLOAT) ）來指定。

若要存取頂點緩衝區的資料，您需要知道所存取的頂點，再加上以下額外緩衝區參數︰

-   位移 - 從緩衝區的起始到第一個頂點資料的位元組數目。 您可以使用 [**>id3d11devicecoNtext：： IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) 方法來指定位移。
-   BaseVertexLocation - 從位移到適當繪製呼叫所使用的第一個頂點的位元組數目。

在建立頂點緩衝區之前，您必須先建立 [**ID3D11InputLayout**](/windows/win32/api/d3d11/nn-d3d11-id3d11inputlayout) 介面來定義其版面配置;這是藉由呼叫 [**ID3D11Device：： CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout) 方法來完成。 在建立輸入設定物件之後，您可以藉由呼叫 [**>id3d11devicecoNtext：： IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout)，將它系結至輸入組合語言階段。

若要建立頂點緩衝區，請呼叫 [**ID3D11Device：： CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer)。

### <a name="index-buffer"></a>索引緩衝區

索引緩衝包含整數位移至頂點緩衝區，可用於更有效率地呈現基本類型。 索引緩衝區包含連續的 16 位元或 32 位元索引集，而每個索引用來識別頂點緩衝區中的頂點。 索引緩衝區可以視覺化，如下圖所示。

![索引緩衝區的圖例](images/d3d10-index-buffer.png)

儲存在索引緩衝區中的循序索引，使用以下參數尋找︰

-   Offset - 索引緩衝的基底位址的位元組數目。 位移會提供給 [**>id3d11devicecoNtext：： IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer) 方法。
-   StartIndexLocation-指定基底位址中的第一個索引緩衝區元素，以及 [**IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer)中提供的位移。 開始位置會提供給 [**>id3d11devicecoNtext：:D rawindexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed) 或 [**>id3d11devicecoNtext：:D rawindexedinstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced) 方法，並代表要轉譯的第一個索引。
-   IndexCount - 要呈現的索引數目。 此數位會提供給 [**DrawIndexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed) 方法

索引緩衝區的開頭 = 索引緩衝區基底位址 + 位移 (位元組) + StartIndexLocation \* ElementSize (位元組) ;

在這個運算中，ElementSize 是各索引緩衝元素的大小，不是兩個就是四個位元組。

若要建立索引緩衝區，請呼叫 [**ID3D11Device：： CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer)。

### <a name="constant-buffer"></a>常數緩衝區

常數緩衝區可讓您有效率地提供著色器常數資料至管線。 您可以使用常數緩衝區來儲存資料流輸出階段的結果。 概念上，常數緩衝區看起來很像單一元素頂點緩衝區，如下圖所示。

![著色器常數緩衝區的圖例](images/d3d10-shader-resource-buffer.png)

每個元素會儲存 1 到 4 個元件常數，取決於儲存的資料格式。 若要建立著色器常數緩衝區，請呼叫 [**ID3D11Device：： CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) ，並指定 D3D11 系結 [**\_ \_ 旗**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)標列舉型別的 D3D11 系結 **\_ \_ 常數 \_ 緩衝區** 成員。

常數緩衝區只能使用單一系結旗標 (**D3D11 系 \_ 結 \_ 常數 \_ 緩衝區**) ，其無法與任何其他系結旗標合併。 若要將著色器常數緩衝區系結至管線，請呼叫下列其中一種方法： [**>id3d11devicecoNtext：： GSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetconstantbuffers)、 [**>id3d11devicecoNtext：:P ssetconstantbuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetconstantbuffers)或 [**>id3d11devicecoNtext：： VSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers)。

若要從著色器讀取著色器常數緩衝區，請使用 HLSL load 函數 (例如 [**load**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)) 。 每個著色器階段允許最多 15 個著色器常數緩衝區，而每個緩衝區可保留最多 4096 個常數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[緩衝區](overviews-direct3d-11-resources-buffers.md)
</dt> </dl>

 

 