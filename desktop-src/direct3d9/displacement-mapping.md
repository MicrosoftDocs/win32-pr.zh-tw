---
description: 置換地圖類似于材質地圖，但由頂點引擎存取。
ms.assetid: d6f16ff2-5a66-48a3-82c4-523faaafa6ae
title: " (Direct3D 9) 的置換對應"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87b559c2c4758b773c48c0b556b6d61af54549f1b30e5c2693a24c4c27856c13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523760"
---
# <a name="displacement-mapping-direct3d-9"></a> (Direct3D 9) 的置換對應

置換地圖類似于材質地圖，但由頂點引擎存取。

## <a name="block-diagram"></a>框圖

頂點管道的早期部分會出現額外的取樣器階段，如下圖所示，它可以取樣置換圖來提供頂點置換資料。

![頂點管線中取樣器階段的圖表](images/tessellatordx9.png)

您可以使用階段編號256（這是新的階段號）， [**SetSamplerState**](/windows/desktop/api) 設定置換地圖取樣器狀態。 置換地圖材質是由 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)所設定。

地圖可以是 presampled 的，這表示可以用可在不進行篩選的情況下查閱置換值的方式來排序。

-   置換地圖類似于材質地圖，但由頂點引擎存取。
-   在可取樣置換圖的頂點管道早期部分中，會出現額外的取樣器階段。 這個階段是由一般 SetSamplerState API 存取，但階段號碼是 D3DDMAPSAMPLER = 256。
-   SetSamplerState (D3DDMAPSAMPLER，... ) API 可設定置換地圖取樣器狀態。
-   置換地圖材質是由 SetTexture (D3DDMAPSAMPLER、材質) API 所設定。
-   地圖可以預先取樣。 這表示可以用特定的方式來排序，而不需要篩選即可查閱置換值。
-   宣告結構中的變更允許用來查閱材質地圖的材質座標規格。 例如，Stream0、Offset、FLOAT2、LOOKUP、位移 \_ 值。 這會告訴鑲嵌在特定位移的 stream0 中，使用2D 浮點數向量作為材質座標，以查詢置換圖，並將置換 \_ 值使用方式的語法與它產生關聯。 頂點著色器宣告會包含類似于 {dcl \_ texture0，v0} 的行，指出 texture0 語義與 v0 輸入暫存器相關聯。 查閱的置換值會複製到輸入暫存器 v0 中。
-   預先取樣紋理對應時，會有一種特殊的置換對應。 產生之頂點的連續索引會當做材質圖的材質座標使用。 例如，0、0、 (D3DDECLTYPE) 0、D3DDECLMETHOD \_ LOOKUPPRESAMPLED、Usage、UsageIndex。
-   查閱的輸出為4個浮點數。
-   只有 N 個修補程式才支援置換對應。
-   如果驅動程式不處理置換對應，則必須忽略 SetTextureStageState 中的 D3DDMAPSAMPLER。
-   \_不支援 D3DTEXF 的非等向篩選模式。
-   當 \_ 置換地圖取樣器中的 D3DSAMP MIPFILTER 不是 D3DTEXF \_ NONE 時，會計算詳細資料層級，如下所示 (請注意，即使 D3DRS ENABLEADAPTIVETESSELLATION 為 FALSE) ，也會使用自動調整鑲嵌狀態 \_ ： Tmax = render state D3DRS  \_ MAXTESSELLATIONLEVEL
-   適用于頂點 Vi 的計算鑲嵌層級 Te： (Xi、Yi、Zi) 和「彈性鑲嵌」一節中所述的方式相同。 詳細資料層級 L = log2 (Tmax) log2 (Te) 。
-   材質篩選和取樣作業會遵循與圖元管線相同的規則， (詳細資料的層級 (」 LOD 套用) 偏差等 ) 。
-   並非所有格式都可用來做為置換圖，但僅可支援 D3DUSAGE \_ DMAP。 應用程式可以使用 CheckDeviceFormat [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)來查詢。
-   您 \_ 必須在 [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) 中指定 D3DUSAGE DMAP，以通知驅動程式此材質將用作置換地圖。
-   D3DUSAGE \_ DMAP 只能搭配紋理使用。 它不能與 cube 對應或磁片區一起使用。
-   使用 D3DUSAGE DMAP 建立的材質和轉譯目標 \_ 可以設定為一般取樣器階段和轉譯目標。
-   用來設定材質座標換行模式的轉譯狀態，會在位移對應中忽略。 一般而言，鑲嵌引擎沒有換行模式。
-   置換圖取樣器的行為與圖元材質取樣器的行為相同。 如果查閱的材質小於四個通道 (例如 R32f) ，則查閱的值會移至目的地註冊的適當通道 (以範例語義) 標記的頂點著色器輸入暫存器 \_ ，而其他通道預設為 (1，1，1) 。 當查閱時，D3DFMT \_ 的 L8 會廣播到 R、G、B 通道，並將預設值設定為1。 參考轉譯器具有完整的執行詳細資料。

## <a name="pre-sampled-displacement-mapping"></a>預先取樣的置換對應

-   引進新的取樣器狀態： D3DSAMP \_ DMAPOFFSET (DWORD) -位移 (在預取樣的置換地圖中的頂點) 。
-   引進新的宣告方法： D3DDECLMETHOD \_ LOOKUPPRESAMPLED。
-   應停用調適型鑲嵌。
-   材質篩選設定會被忽略。 點取樣完成。 Mip 材質篩選準則假設為 D3DTEXF \_ NONE。 所有其他材質篩選模式都假設為 D3DTEXF \_ 點。
-   紋理座標的計算方式為： U = (Index% TextureWidthInPixeles) / (float)  (TextureWidthInPixeles) V = (Index/TextureWidthInPixeles) / (float)  (TextureHeightInPixeles) 其中 Index 是產生的頂點加上 TSS D3DSAMP DMAPOFFSET 的連續索引 \[ \_ \] 。 在每個基本的開頭，順序索引會設定為零，並在產生頂點之後增加。

這些是支援置換對應的 API 變更。

-   已新增單一通道格式，D3DFMT \_ l16 也。
-   新的使用旗標，D3DUSAGE \_ DMAP。
-   用來設定置換地圖材質（D3DDMAPSAMPLER）的特殊材質階段。
-   已新增硬體 cap，D3DDEVCAPS2 \_ DMAPNPATCH 和 D3DDEVCAPS2 \_ PRESAMPLEDDMAPNPATCH。 請參閱 [D3DDEVCAPS2](d3ddevcaps2.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點管線](vertex-pipeline.md)
</dt> </dl>

 

 
