---
description: 在固定函式頂點管線中，處理頂點緩衝區中的頂點會套用裝置目前的轉換矩陣。
ms.assetid: a882a5c5-b05e-4659-9040-92d3e2ccd89c
title: 修正 (Direct3D 9) 的函式頂點處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 827a293a4fbd552327d93076de773aec90dbd895faf3c086f4794036978984fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988018"
---
# <a name="fixed-function-vertex-processing-direct3d-9"></a>修正 (Direct3D 9) 的函式頂點處理

在固定函式頂點管線中，處理頂點緩衝區中的頂點會套用裝置目前的轉換矩陣。 也可以選擇性地套用頂點作業，例如光源、產生剪輯旗標和更新範圍。 使用固定函式頂點處理時，修改目的頂點緩衝區中的元素是由 [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) 旗標所控制。 此旗標只適用于固定的函式頂點處理。 [**IDirect3DDevice9**](/windows/desktop/api)介面會公開 [**IDirect3DDevice9：:P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices)方法來處理頂點。 您可以從頂點著色器將頂點處理至輸入資料流程的集合，藉由呼叫 **IDirect3DDevice9：:P rocessvertices** 方法，將交錯頂點資料的單一資料流程產生至目的地頂點緩衝區。 方法會接受五個參數，這些參數會描述方法的目標位置和頂點數量、目的地頂點緩衝區和處理選項。 在呼叫之後，目的緩衝區就會包含已處理的頂點資料。

第一個、第二個和第三個參數（SrcStartIndex、DestIndex 和 VertexCount）會反映要載入之第一個頂點的索引、放置頂點的目的緩衝區內的索引，以及要在目的緩衝區中分別處理和放置的頂點總數。 第四個參數 pDestBuffer 應該設定為將接收來源頂點之頂點緩衝區物件的 [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) 介面位址。 SrcStartIndex 參數會指定方法應該開始處理頂點的索引。

最後一個參數旗標會決定方法的特殊處理選項。 您可以將此參數設定為0以進行預設頂點處理，或將 [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) 設定為在某些情況下將處理優化。 您也可以將 D3DPV \_ DONOTCOPYDATA 值與適用于目的緩衝區的一或多個 [D3DLOCK](d3dlock.md) 值結合。 當您將旗標設為0時，目的地頂點緩衝區頂點格式的頂點元件若未受到頂點作業影響，仍然會從頂點著色器複製或設定為0。 不過，使用 D3DPV \_ DONOTCOPYDATA 時， [**IDirect3DDevice9：:P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) 不會覆寫目的地緩衝區中的色彩和材質座標資訊，除非此資料是由 Direct3D 產生。 啟用光源時，會產生擴散色彩，也就是 D3DRS \_ 光源設定為 **TRUE**。 當啟用光源且已啟用反射時（也就是 D3DRS \_ SPECULARENABLE 和 D3DRS \_ 光源會設定為 **TRUE**），就會產生反射色彩。 啟用霧化時也會產生反射色彩。 啟用紋理轉換或材質產生時，就會產生材質座標。 **IDirect3DDevice9：:P rocessvertices** 會使用目前的轉譯狀態來判斷應完成的頂點處理。

## <a name="fvf-usage-settings-for-destination-vertex-buffers"></a>目的地頂點緩衝區的 FVF 使用量設定

[**IDirect3DDevice9：:P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices)方法需要目的地頂點緩衝區之 [D3DFVF](d3dfvf.md)的特定設定。 FVF 使用方式設定必須與頂點處理的目前設定相容。

針對固定函數頂點處理， [**IDirect3DDevice9：:P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) 需要下列 FVF 設定：

-   Position 類型一律為 [D3DFVF \_ XYZRHW](d3dfvf.md) ; 因此，D3DFVF \_ XYZ 和 D3DFVF \_ XYZB1 到 D3DFVF \_ XYZB5 是不正確。
-   不得設定 [D3DFVF \_ NORMAL](d3dfvf.md)、D3DFVF \_ RESERVED0 和 D3DFVF \_ RESERVED2 旗標。
-   如果下列條件的或運算傳回 true，則必須設定 [D3DFVF \_ 擴散](d3dfvf.md) 旗標：
    -   已啟用光源;也就是說，D3DRS \_ 光源是 **TRUE**。
    -   已停用光源、在輸入頂點資料流程中出現擴散色彩，且未設定 [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) 。
-   如果下列條件的或運算傳回 true，則必須設定 [D3DFVF \_ 反射](d3dfvf.md) 旗標：
    -   已啟用光源且已啟用反射色彩;也就是說，D3DRS \_ SPECULARENABLE 是 **TRUE**。
    -   光源已停用、反射色彩存在於輸入頂點資料流程中，且未設定 [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) 。
    -   已啟用頂點霧化;也就是說，D3DRS \_ FOGVERTEXMODE 不會設定為 D3DFOG \_ NONE。

此外，您必須以下列方式設定材質座標計數：

-   如果所有使用中的材質階段都停用材質轉換和材質產生，且未設定 [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) ，則需要輸出材質座標的數目和類型，以符合輸入頂點材質座標的數目和類型。 如果已 \_ 設定 D3DPV DONOTCOPYDATA，且紋理轉換和材質產生已停用，則會忽略輸出材質座標。
-   如果針對任何使用中的材質階段啟用紋理轉換或材質產生，輸出頂點可能需要包含比輸入頂點更多的材質座標集合。 這是因為材質座標產生的材質座標和材質轉換所產生或衍生的材質座標激增。 請注意，在 IDirect3DDevice9 期間會發生類似的材質座標激增 [**：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 呼叫，但應用程式程式設計人員看不到。 在此情況下，Direct3D 會產生一組新的材質座標。 新的材質座標集是藉由逐步執行材質階段並分析材質產生、材質轉換和材質座標索引的設定所衍生，以判斷該階段是否需要唯一的材質座標集合。 每次需要新的集合時，會以遞增順序配置。 請注意，最大和一般需求為每個階段一組設定，但因為透過 D3DTSS TEXCOORDINDEX 共用 nontransformed 材質座標可能較少 \_ 。

因此，如果材質系結至該階段且符合下列任一條件，則會針對每個材質階段產生一組新的材質座標：

-   該階段會啟用材質產生。
-   已針對該階段啟用紋理轉換。
-   第一次透過 D3DTSS TEXCOORDINDEX 參考 Nontransformed 輸入材質座標 \_ 。

當 Direct3D 產生材質座標時，需要應用程式執行下列動作：

1.  使用具有適當 FVF 用法的目的地頂點緩衝區。
2.  \_根據 postprocessed 材質座標的位置，Reprogram 材質階段的 D3DTSS TEXCOORDINDEX。 請注意，在 \_ 後續的 IDirect3DDevice9 中使用已處理的頂點緩衝區時，就會發生 D3DTSS TEXCOORDINDEX 設定 reprogramming [**：:D Rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 和 [**IDirect3DDevice9：:D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) 呼叫。

最後，您必須以下列方式設定材質座標維度 ([D3DFVF \_ TEX0](d3dfvf.md) 至 D3DFVF \_ TEX8 ) ：

-   針對每個材質座標集，如果材質轉換和材質產生已停用，則輸出材質座標維度必須符合輸入。 如果紋理轉換已啟用，則輸出維度必須符合 D3DTTFF \_ COUNT1、D3DTTFF \_ COUNT2、D3DTTFF \_ COUNT3 或 D3DTTFF \_ COUNT4 設定所定義的計數。 如果材質轉換已停用並啟用材質產生，則輸出維度必須符合紋理產生模式的設定;目前所有模式都會產生三個浮點值。

當 [**IDirect3DDevice9：:P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) 由於不相容的目的地頂點緩衝區 FVF 程式碼而失敗時，會將預期的程式碼列印到 debug 輸出， (debug 組建只) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點緩衝區](vertex-buffers.md)
</dt> </dl>

 

 
