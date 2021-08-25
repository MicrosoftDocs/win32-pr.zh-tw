---
title: 磚資源 Api
description: 本節所述的 Api 適用于磚化的資源和磚集區。
ms.assetid: 02DCF9BA-F9EA-4176-AD6F-AA620CE968BA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f433b6c70d475d4da511b85fdcc2b1c273de1efa8e1186215b25ce6b9b95d0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894388"
---
# <a name="tiled-resource-apis"></a>磚資源 Api

本節所述的 Api 適用于磚化的資源和磚集區。

-   [將磚從磚集區指派給資源](#assigning-tiles-from-a-tile-pool-to-a-resource)
-   [查詢資源平鋪和支援](#querying-resource-tiling-and-support)
-   [複製磚資料](#copying-tiled-data)
-   [調整磚集區的大小](#resizing-tile-pool)
-   [磚資源關卡](#tiled-resource-barrier)
-   [相關主題](#related-topics)

## <a name="assigning-tiles-from-a-tile-pool-to-a-resource"></a>將磚從磚集區指派給資源

[**ID3D11DeviceCoNtext2：： UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings)和 [**ID3D11DeviceCoNtext2：： CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) api 會操作和查詢磚對應。 更新呼叫只會影響呼叫中所識別的圖格，而其他則會保留先前的定義。

磚集區中的任何指定磚都可以對應到資源中的多個位置，甚至是多個資源。 這項對應包含資源中的圖格，其具有所選的版面配置 ([Mipmap 封裝](mipmap-packing.md)) 其中多個 mipmap 會一起封裝成單一磚。 捕捉的原因是，如果資料透過一個對應寫入至磚，但透過不同設定的對應來讀取，則結果為未定義。 不過，若要謹慎使用這種彈性，您仍然可以對應用程式有所説明，像是在不會同時使用的資源之間共用磚，其中磚的內容一律會透過相同的資源對應來初始化，因為這些內容會後續讀取。 同樣地，對應來保存多個具有相同 surface 維度之不同資源之壓縮 mipmap 的圖格將會正常運作，這兩個對應中的資料會顯示相同。

您可以隨時在立即或延遲的內容中，對資源的圖格指派進行變更。

## <a name="querying-resource-tiling-and-support"></a>查詢資源平鋪和支援

若要查詢資源平鋪，請使用 [**ID3D11Device2：： GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling)。

如需其他資源平鋪支援，請使用 [**ID3D11Device2：： CheckMultisampleQualityLevels1**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-checkmultisamplequalitylevels1)。

## <a name="copying-tiled-data"></a>複製磚資料

Direct3D 中用來移動資料的任何方法，與並排顯示的資源相同，不同之處在于會捨棄未對應區域的寫入，而從未對應的區域讀取會產生0。 如果複製作業牽涉到多次寫入相同的記憶體位置，因為目的地資源中有多個位置對應到相同的磚記憶體，則對多對應磚所產生的寫入將不具決定性且不可重複。 也就是說，存取會依照硬體執行複製的任何順序進行。

Direct3D 11.2 引進了下列其他複製方式的方法：

-   在並排顯示的資源中的圖格之間進行複製 (以64KB 的圖格細微性) ，以及 (移入/移出圖形處理器中的緩衝區) 圖形處理單元中的緩衝區 (記憶體) 或預備資源 (- [ **ID3D11DeviceCoNtext2：： CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)
-   從應用程式提供的記憶體複製到磚資源中的磚- [ **ID3D11DeviceCoNtext2：： UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)

這些方法會視需要 swizzle/deswizzle，並在執行 \_ \_ \_ \_ 中的 GPU 工作未參考呼叫端保證目的地記憶體時，允許 D3D11 圖格複製沒有覆寫旗標。

複製中的圖格無法包含包含已封裝 mipmap 或具有未定義結果的磚。 若要將硬體套件的 mipmap 傳輸至/傳出，您必須針對整個 mip 鏈使用標準 (非磚專屬) 複製/更新 Api 或 [**>id3d11devicecoNtext：： GenerateMips**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-generatemips) 。

**注意：在 [**GenerateMips**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-generatemips)** 上，針對具有部分對應磚的資源使用 [**>id3d11devicecoNtext：： GenerateMips**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-generatemips) ，將會產生只遵循讀取 **和寫入結果** 的結果，而這些規則會套用至硬體和顯示器驅動程式用來 **GenerateMips** 的任何演算法。 因此，應用程式不會特別有用，除非有某些區域具有 **Null** 對應 (，且在產生階段期間其對其他 mips 的影響) 不會對應用程式所關注的介面部分產生影響。

例如，從暫存介面或應用程式記憶體複製磚資料，是上傳可能已從磁片串流處理之磚的方式。 串流處理磁片時的變化是將某種壓縮資料上傳至 GPU 記憶體，然後在 GPU 上進行解碼。 解碼目標可能是 GPU 記憶體中的緩衝區資源， [**CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) 接著會將它複製到實際的磚資源。 當 swizzle 模式未知時，此複製步驟可讓 GPU swizzle。 如果並排顯示的資源本身是緩衝區資源 (例如，而不是材質) ，則不需要 Swizzling。

複本之非並排緩衝資源端的磚記憶體配置，在64KB 的磚中，是在記憶體中的線性，而硬體和顯示驅動程式會在每個磚傳送至/從並排顯示的資源時適當地 swizzle/deswizzle。 若為多重取樣消除鋸齒 (MSAA) 介面，則會在移至下一個圖元之前，以樣本索引順序來遍歷每個圖元的樣本。 針對部分填滿于右邊的圖格，如果表面的寬度不是圖格寬度的倍數（以圖元) 為單位） (，則向下移動資料列的音調/stride 就是在磚填滿時，圖格可容納的圖元數（以位元組為單位）的完整大小（以位元組為單位）。 因此，記憶體中的每個圖元資料列之間可能會有間距。 為了簡化規格，mipmap 小於磚的大小不會一起封裝線上性版面配置中。 這似乎是浪費記憶體空間，但如前所述，將硬體套件複製到 mips 之後，不允許透過 [**CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) 或 [**UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)。 應用程式可以直接使用泛型 UpdateSubresource \* () 或 CopySubresource \* () api 來個別複製 small mips，但在 CopySubresource () 中， \* 這表示線性記憶體必須與並排顯示的資源 CopySubresource 相同的維度， \* () 無法從緩衝區資源複製到 Texture2D 實例。

如果已定義硬體標準 swizzle，則可以新增旗標，以表示緩衝區中的資料會以該格式來解讀 (傳送) 不需要任何 swizzle，不過在這種情況下上傳資料的替代方法可能也有意義，例如允許應用程式直接存取磚集區記憶體。

複製作業可以在立即或延遲的內容上完成。

## <a name="resizing-tile-pool"></a>調整磚集區的大小

若要調整磚集區的大小，請使用 [**ID3D11DeviceCoNtext2：： ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)。

## <a name="tiled-resource-barrier"></a>磚資源關卡

若要指定多個磚資源之間的資料存取順序條件約束，請使用 [**ID3D11DeviceCoNtext2：： TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[磚資源](tiled-resources.md)
</dt> </dl>

 

 




