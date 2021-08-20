---
title: Direct3D 11 中的資源簡介
description: 本主題介紹 Direct3D 資源，例如緩衝區和紋理。
ms.assetid: 9e991ab0-9648-484a-9a2c-5391ee5abf20
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1cc6f9ba62bdfedc59ff2a152588ccad3d81423d55f8c230ff3836c52e5251d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098243"
---
# <a name="introduction-to-a-resource-in-direct3d-11"></a>Direct3D 11 中的資源簡介

資源是您場景的組建區塊。 它們包含 Direct3D 用來解讀和轉譯場景的大部分資料。 資源是可由 Direct3D 管線存取的記憶體區域。 資源包含下列資料類型：幾何、材質、著色器資料。 本主題介紹 Direct3D 資源，例如緩衝區和紋理。

您可以建立強型別或不具類型的資源;您可以控制資源是否同時具有讀取和寫入存取權;您只能讓資源存取 CPU、GPU 或兩者。 每個管線階段可使用多達 128 種資源。

Direct3D 保證可針對任何超出範圍存取的資源傳回零。

Direct3D 資源的生命週期如下：

-   使用 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 介面的其中一個 create 方法來建立資源。
-   使用內容和 [**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) 介面的其中一個 set 方法，將資源系結至管線。
-   藉由呼叫資源介面的 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 方法來解除配置資源。

本節包含下列主題：

-   [強式與弱式類型](#strong-vs-weak-typing)
-   [資源檢視](#resource-views)
-   [緩衝區的原始視圖](#raw-views-of-buffers)
-   [相關主題](#related-topics)

## <a name="strong-vs-weak-typing"></a>強式與弱式類型

有兩種方式可以完整指定資源的配置 (或記憶體使用量)︰

-   輸入-在建立資源時完整指定類型。
-   無類型：當資源系結至管線時，完整指定類型。

建立完整具類型的資源會限制資源為其建立時使用的格式。 這可讓執行階段將存取最佳化，尤其是若資源的建立是使用指出應用程式無法對應的旗標。 除非使用 D3D10 的 DDI 系結 \_ \_ 存在旗標建立資源，否則無法使用 view 機制重新解譯以特定類型建立的資源 \_ 。 如果有 D3D10 的 DDI 系結， \_ \_ \_ 則可以使用適當系列的任何完整型別成員，在這些資源上建立設定轉譯-目標或著色器資源檢視器，即使原始資源已建立為完整類型。

在類型較少的資源中，第一次建立資源時，資料類型是未知的。 應用程式必須從可用的類型格式較少選擇 (查看 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) 。 您必須指定要配置的記憶體大小，以及執行階段是否需要在 Mipmap 中產生子紋理。 不過，確切的資料格式 (是否要將記憶體解釋為整數、浮點數、不帶正負號的整數等。在資源使用 [資源檢視](#resource-views)系結至管線之前，將不會決定 ) 。 因為直到紋理繫結到管線，紋理格式均維持彈性，所以資源稱為弱輸入的儲存空間。 弱型別的儲存體有其優點，只要元件的數目和每個元件的位元數目都相同，就可以使用另一種格式來重複使用或重新解譯。

單一資源可以繫結至多個管線階段，只要每一個都有唯一檢視，而這完全符合每個位置的格式。 例如，使用格式 DXGI 格式 R32G32B32A32 的資源， \_ \_ 可以當做 \_ dxgi \_ 格式 \_ R32G32B32A32 \_ FLOAT，也可以在 \_ \_ \_ 管線中的不同位置同時使用 dxgi 格式 R32G32B32A32 UINT。

## <a name="resource-views"></a>資源檢視

資源可以儲存為一般用途的記憶體格式，以供多個管線階段共用。 管線階段會使用 view 來解讀資源資料。 資源檢視在概念上類似于轉換資源資料，因此可用於特定的內容。

View 可以搭配無別別資源使用。 也就是說，您可以在編譯時期建立資源，並在資源系結至管線時宣告資料類型。 針對無值資源建立的視圖一律會有相同數目的每個元件的位數;資料的轉譯方式取決於指定的格式。 指定的格式必須與建立資源時所使用的無格式的系列相同。 例如，使用 R8G8B8A8 無型別格式建立的資源 \_ 無法視為 R32 \_ FLOAT 資源，即使這兩種格式在記憶體中的大小可能相同也一樣。

視圖也會公開其他功能，例如，在著色器中讀取深度/樣板表面、在單一行程中產生動態立方體貼圖，以及同時轉譯為磁片區的多個配量的能力。



| 資源介面                                             | 描述                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)       | 在深度樣板測試期間存取材質資源。                                       |
| [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)       | 存取用作轉譯目標的材質資源。                                    |
| [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)   | 存取著色器資源，例如常數緩衝區、材質緩衝區、材質或取樣器。 |
| [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) | 使用圖元著色器或計算著色器存取未排序的資源。                        |



 

## <a name="raw-views-of-buffers"></a>緩衝區的原始視圖

您可以將原始的緩衝區（也稱為 [位元組位址緩衝區](direct3d-11-advanced-stages-cs-resources.md)）視為您想要原始存取的一包，也就是您可以透過1到 4 32 位無型別位址值的區塊來輕鬆存取的緩衝區。 您會想要讓原始的緩衝區存取 (或（當您呼叫下列其中一種方法來建立緩衝區的視圖時，緩衝區) 的原始視圖）：

-   若要建立著色器資源檢視 (SRV) 至緩衝區，請呼叫 [**ID3D11Device：： CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview) ，並使用旗標 [**D3D11 \_ BUFFEREX \_ SRV \_ 旗標 \_ 原始旗**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bufferex_srv_flag)標。 您可以在 [**D3D11 \_ BUFFEREX \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_bufferex_srv)結構的 Flags 成員中指定這個旗 **標**。 您可以在 **pDesc：： ID3D11Device** 點的 *CreateShaderResourceView* 參數所屬 [**D3D11 \_ 著色器 \_ 資源 \_ 視圖 \_ DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc)結構的 **BUFFEREX** 成員中，設定 **D3D11 \_ BUFFEREX \_ SRV** 。 您也可以在 **D3D11 \_ 著色器 \_ 資源 \_ 視圖 \_ DESC** 的 **ViewDimension** 成員中設定 [**D3D11 \_ SRV \_ 維度 \_ BUFFEREX**](/previous-versions/windows/desktop/legacy/ff476217(v=vs.85))值，以指出 SRV 是原始的視圖。
-   若要建立未排序的存取權視圖 (UAV) 至緩衝區，請使用標記 [**D3D11 \_ 緩衝區 \_ UAV \_ 旗標 \_ RAW**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_buffer_uav_flag)來呼叫 [**ID3D11Device：： CreateUnorderedAccessView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createunorderedaccessview) 。 您可以在 [**D3D11 \_ 緩衝區 \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_uav)結構的 **旗標** 成員中指定這個旗標。 您可以在 [**D3D11 未 \_ 排序的 \_ 存取 \_ \_ 權**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_unordered_access_view_desc)（ *pDesc* ）參數 **ID3D11Device：： CreateUnorderedAccessView** 點的 **緩衝區** 成員中，設定 **D3D11 \_ buffer \_ UAV** 。 您也可以在 **D3D11 未 \_ 排序 \_ 存取 \_ 視圖 \_ DESC** 的 **ViewDimension** 成員中設定 [**D3D11 \_ UAV \_ 維度 \_ 緩衝區**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_uav_dimension)值，以表示 UAV 是原始的視圖。

當您使用原始緩衝區時，可以使用 HLSL [**ByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) 和 [**RWByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) 物件類型。

若要建立緩衝區的原始視圖，您必須先呼叫 [**ID3D11Device：： CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) ，並使用 [**D3D11 \_ 資源的「 \_ 其他緩衝區」 \_ \_ 允許 \_ 原始 \_ 視圖**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) 旗標來建立基礎緩衝區資源。 您可以在 [**D3D11 \_ 緩衝區 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)結構（ **ID3D11Device：： CreateBuffer** 點的 *pDesc* 參數）的 **MiscFlags** 成員中指定這個旗標。 您無法結合 **D3D11 \_ 資源的 \_ 其他 \_ 緩衝區 \_ 允許 \_ 原始的 \_ 視圖** 旗標與 [**D3D11 資源的 \_ \_ 其他 \_ 緩衝區 \_ 結構化**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)。 此外，如果您在 **D3D11 \_ 緩衝區 \_ DESC** 的 **BindFlags** 中指定 D3D11 系結 [**\_ \_ 常數 \_ 緩衝區**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)，您也不能在 **MiscFlags** 中指定 **D3D11 \_ 資源的 \_ 其他 \_ 緩衝區 \_ 允許原始的 \_ \_ 視圖**。 這並不是原始視圖的限制，因為常數緩衝區已經有條件約束，無法與任何其他視圖合併。

除了上述的無效案例之外，當您使用 D3D11 資源的其他緩衝區來建立緩衝區時，您也不會有 [**\_ 原始的 \_ \_ \_ \_ \_ 視圖**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)限制，而是不限於設定 **D3D11 \_ 資源 \_ 其他 \_ 緩衝區 \_ 允許原始的 \_ \_ 視圖**。 也就是說，您可以將這類緩衝區用於非原始存取，以任何可能使用 Direct3D 的方式進行。 如果您指定 **D3D11 \_ 資源的 \_ 其他 \_ 緩衝區 \_ 允許 \_ 原始的 \_ 視圖** 旗標，則只會增加可用的功能。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[資源](overviews-direct3d-11-resources.md)
</dt> <dt>

[新的資源類型](direct3d-11-advanced-stages-cs-resources.md)
</dt> </dl>

 

 