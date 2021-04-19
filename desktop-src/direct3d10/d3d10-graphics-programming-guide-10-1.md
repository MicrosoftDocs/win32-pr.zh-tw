---
description: Direct3D 10.1 功能
ms.assetid: e60c6116-e2f9-46b7-aed8-13e3e5ae2b90
title: Direct3D 10.1 功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99935941f60a984407c688e4ae67f0a125b0130d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973774"
---
# <a name="direct3d-101-features"></a>Direct3D 10.1 功能

Direct3D 10.1 以下列新功能擴充 Direct3D 10.0 的功能集：

-   Blend 模式-每個轉譯目標的 blend 模式，使用新的 blend 狀態介面 (查看 [**ID3D10BlendState1 介面**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10blendstate1)) 。 雙來源混合作業僅限用來轉譯目標插槽 0;您不得寫入其他輸出，或將任何轉譯目標系結至插槽0以外的位置。
-   剔除行為-自動挑選零區域臉部;這只會影響線框轉譯。
-   浮點數規則-針對浮點數使用相同的 IEEE-754 規則，但是32位浮點數作業已經過加強，以產生0.5 單位-最後 (0.5 ULP) 的結果，這是無限精確的結果。 這適用于加法、減法和乘法。  (精確度為 0.5 ULP，適用于反向) 的 1.0 ULP。
-   格式： float16 混合的精確度已增加到 0.5 ULP。 UNORM16/SNORM16/SNORM8 格式也需要混色。
-   多階段式消除鋸齒功能已增強，可讓您以一般化的透明度為基礎，讓您更有效率地進行多重傳遞轉譯。 為了達成此目的，所有的多型語義都定義為每個樣本 (取樣頻率) 的每個樣本都一律執行一次，並針對每個樣本計算個別的色彩。 如果圖元著色器未使用任何每個樣本屬性，則會針對圖元中的每個涵蓋樣本計算相同的值。 在此情況下，它相當於每圖元執行著色器一次的硬體 (圖元頻率) ，將結果複寫至所有涵蓋的範例。 自然地，以圖元頻率執行的結果一律會產生相同的結果，如同在取樣頻率執行相同的著色器，並以圖元頻率來取樣屬性。 PSInvocations 管線統計資料會以取樣頻率遞增，除非著色器是以圖元頻率執行。
-   管線階段頻寬：增加可在著色器階段之間傳遞的資料量： 

    | 資源                        | 限制                    |
    |---------------------------------|---------------------------|
    | 在著色器階段之間註冊 | 32 (32 位 x 4-元件)  |
    | 頂點著色器輸入暫存器   | 32                        |
    | 輸入組合語言輸入位置     | 32                        |

    

     

-   柵格化規則-光柵的規則已針對線條進行了變更，此外也加入了新功能。
    -   MultisampleEnable 只會影響線條點陣 (點和三角形不受) 影響，並可用來選擇線條繪製演算法。 這表示已不再支援從 Direct3D 10 進行的一些多級程式化。
    -   新的範例-頻率圖元著色器執行與基本的點陣化。
-   資源-CopyResource 會在兩個新的案例中啟用：
    -   色彩和深度/樣板 MSAA 介面現在都可以搭配 CopyResource 使用，作為來源或目的地
    -   在特定32/64/128 位 prestructured、具類型的資源和相同位寬度的壓縮表示之間進行複製時的格式轉換。
-   紋理取樣-範例 \_ c 和範例 \_ c \_ lz 指示的定義是要同時搭配 Texture2DArrays 和 TextureCubeArrays 使用， (Alpha 元件的 Location 成員) 指定陣列索引。
-   TextureCube 和新的 TextureCubeArray (請參閱 [**D3D10 \_ TEXCUBE \_ ARRAY \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1)) 不是實際的資源，而是 Texture2DArray 資源上的新觀點。 使用新的使用方式旗標，從 Texture2DArray 資源建立資源檢視， (D3D10 \_ 資源的 \_ 其他 \_ TEXTURECUBE) ，請使用新的 [**ID3D10ShaderResourceView1 介面**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1) 介面，將 cube 材質視圖系結至管線。

新功能需要10.1 裝置類型 (查看 [**ID3D10Device1 介面**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)) 可透過呼叫 [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1)來建立，也可以藉由呼叫 [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1)同時建立裝置和交換鏈。

在 Windows Vista Service Pack 1 中，Direct3D 10.0 和 Direct3D 10.1 Dll 會並存于系統上。 若要存取10.1 功能，請執行下列其中一項：

## <a name="accessing-101-features-on-vista-gold-and-vista-service-pack-1"></a>存取 Vista 黃金和 Vista Service Pack 1 上的10.1 功能

想要支援 Vista 黃金和 SP1 的開發人員，必須考慮在 Vista 金上缺少新的 10.1 API 擴充功能。 DXUT 和 D3DX10 都將提供便利的功能，以根據系統上的可用 Dll 和可用硬體 (10.0 或 10.1) 來建立適當的裝置。 10.1 裝置繼承自10.0 裝置，而且可以使用 QueryInterface () 進行取出。 建議每個應用程式追蹤裝置類型，並維護10.1 裝置的指標 (如果有的話) 可避免在需要10.1 功能時經常進行 QueryInterface 呼叫。 同樣地，如果10.1 資源檢視和狀態物件是由應用程式的自訂類別所關聯，建議應用程式追蹤物件是否為10.0 或10.1 型別，以避免重複的 QueryInterface () 呼叫。 D3DX10 包含一組公用程式函式，可簡化此程式 (參閱 [**D3DX10CreateDevice**](d3dx10createdevice.md) 和 [**D3DX10CreateDeviceAndSwapChain**](d3dx10createdeviceandswapchain.md)) 。

## <a name="accessing-101-features-on-vista-service-pack-1-exclusively"></a>以獨佔方式存取 Vista Service Pack 1 上的10.1 功能

有些開發人員可能會選擇需要 Vista Service Pack 1，以廣泛地散發給使用者，並在 Direct3D 10.1 之外提供一系列的增強功能。 這些開發人員可以單獨使用 Direct3D 10.1 標頭和程式庫，相依于支援10.0 和10.1 硬體的 Direct3D 10.1 Dll (某些呼叫可能會失敗，但在不支援新功能) 的10.0 裝置上。

其他注意事項：

-   D3DX10.dll 中公開的 Api 將會接受10.0 和10.1 裝置，並會在可用時利用10.1 功能。
-   D3D10SDKLayers.dll 支援10.1 裝置，而且可以輸出適用于10.1 功能的 go-spew 偵錯工具。
-   D3D10Ref.dll 會實行10.0 和10.1 軟體裝置。
-   D3DX10 和 FXC.EXE 支援已更新的10.1 著色器模型，其目標如下： vs \_ 4 \_ 1、gs \_ 4 \_ 1、ps \_ 4 \_ 1 和 fx \_ 4 1，可系結 \_ 至10.1 裝置。 10.1 裝置支援著色器模型4.0 與4.1 著色器。
-   Direct3D 10.0 效果架構支援10.0 與10.1 裝置，但是任何包含著色器模型4.1 著色器或新的10.1 功能的技術都必須使用10.1 裝置。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 10 程式設計手冊](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 



