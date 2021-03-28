---
title: 'dcl_interface_dynamicindexed (sm5-asm) '
description: ')  (介面宣告函數資料表指標。 |dcl_interface_dynamicindexed (sm5-asm) '
ms.assetid: 5C77EBB6-7AEC-4471-AA6E-0F6D3E215156
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f78bb0152b44f7e29b9e76221db13da0c465a434
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992070"
---
# <a name="dcl_interface_dynamicindexed-sm5---asm"></a>dcl \_ 介面 \_ dynamicindexed (sm5-asm) 

)  (介面宣告函數資料表指標。



| dcl \_ 介面 \_ dynamicindexed fp \# \[ arraySize \] \[ numCallSites \] = {ft \# ，ft \# ，...} |
|--------------------------------------------------------------------------------------|



 



| 項目                                                          | 描述                                    |
|---------------------------------------------------------------|------------------------------------------------|
| <span id="fp_"></span><span id="FP_"></span>*Fp\#*<br/> | \[在 \] 函數資料表指標中。<br/> |



 

## <a name="remarks"></a>備註

每個介面都必須先從 API 系結，才能使用著色器。 系結會提供其中一個函式資料表的參考，以便填入方法位置。 編譯器不會產生未參考物件的指標。

函式資料表指標有一組完整的方法位置，可避免 c + + 指標點對點標記法需要的額外間接取值層級。 這也需要此指標為5元組。 在 HLSL 虛擬內嵌模型中，一律會知道用於呼叫的全域變數/輸入，因此我們可以為每個根物件設定資料表。

函式指標宣告指出哪些函數資料表可搭配使用。 這也允許衍生方法相互關聯資訊。

介面宣告的第一個 \[ \] 是陣列大小。 如果使用動態索引，宣告將會指出，如下所示。 介面指標的陣列也可以靜態地編制索引，而介面指標的陣列則不需要表示動態索引。

介面指標的編號是從0開始，第一個宣告，接著將陣列大小變成帳戶，因此第一個指標在四個專案陣列 fp0 4 個專案之後， \[ \] \[ \] 就會 fp4 \[ \] \[ \] 。

介面宣告的第二個 \[ \] 是呼叫位置的數目，必須符合宣告中所參考之每個資料表內的主體數目。

介面宣告中可能會列出多個函式資料表 (ft \#) 選項的界限。

給定的函式資料表 (ft \#) 可以在一個或多個介面宣告中出現一次以上。

### <a name="restrictions"></a>限制

-   著色器中的物件網站數目是其 arraySize 宣告之所有 *fp \#* 宣告的總和 \[ \] ，必須不超過253。 此數位對應到可出現 **的指標數目** 。 執行時間會強制執行這項253限制，以保持與 DDI 的大小系結，以傳達此指標資料。
-   著色器中的呼叫位置數，也就是可能分支目標數目之所有 fcall 語句的總和，不得超過4096。

    例如，針對第一個 *fp \[ \] \[ \]* 維度使用靜態索引的 [fcall](fcall--sm5---asm-.md)會計算為一個：

    `                       fcall fp0[0][0]         // +1`

    使用動態索引的 **fcall** 會計算為數組中的元素數目， (第一個 \[ \]) 的 **dcl \_ 介面**：

    `                    dcl_interface_dynamicindexed fp1[2][1] = {ft2, ft3, ft4}                      ...                     `

    `fcall fp1[r0.z + 0][1]  // +2`

    這項限制可協助某些實作為在常數類似緩衝區的儲存體中，輕鬆地容納函式主體選取的資料表。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此指令：



| 著色器模型                                              | 支援 |
|-----------------------------------------------------------|-----------|
| [著色器模型5](d3d11-graphics-reference-sm5.md)        | 是       |
| [著色器模型4。1](dx-graphics-hlsl-sm4.md)              | 不可以        |
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 不可以        |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 不可以        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 不可以        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 不可以        |



 

cs \_ 4 \_ 0 和 cs \_ 4 \_ 1 支援此 UAV 和 SRV 指令。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5元件 (DirectX HLSL) ](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





