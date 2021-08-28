---
title: Flow控制項限制
description: 圖元著色器流程式控制制指令有限制，會影響指令中可包含的嵌套層級數目。 此外，使用漸層指示來執行每個圖元的流量控制也有一些限制。
ms.assetid: 17a902cd-16a4-4065-9249-01f9b1f40506
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b261cff11a95236e9bc6653c59c16ca0ac221ca719ade7497dbfffa2198da207
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982938"
---
# <a name="flow-control-limitations"></a>Flow控制項限制

圖元著色器流程式控制制指令有限制，會影響指令中可包含的嵌套層級數目。 此外，使用漸層指示來執行每個圖元的流量控制也有一些限制。

> [!Note]  
> 當您使用 \* \_ 4 個 \_ \_ 層級 \_ 9 \_ x HLSL 著色器設定檔時，會隱含地使用[著色器模型](dx-graphics-hlsl-sm2.md)2.x 設定檔來支援具有 Direct3D 9 功能的硬體。 著色器模型2.x 設定檔支援的流程式控制制行為比 [著色器模型](dx-graphics-hlsl-sm4.md) 4.x 和更新版本設定檔更受限。

 

-   [圖元著色器指令深度計數](#pixel-shader-instruction-depth-counts)
-   [Per-Pixel Flow 控制項與螢幕漸層的互動](#interaction-of-per-pixel-flow-control-with-screen-gradients)

## <a name="pixel-shader-instruction-depth-counts"></a>圖元著色器指令深度計數

ps \_ 2 \_ 0 不支援流量控制。 其他圖元著色器版本的限制如下所示。

### <a name="instruction-depth-count-for-ps_2_x"></a>Ps \_ 2 x 的指令深度 \_ 計數

每個指令都會計入一或多個嵌套深度限制。 下表列出每個指令在現有深度中新增或減去的深度計數。



| 指令                              | 靜態嵌套                       | 動態嵌套                                                           | 迴圈/rep 的嵌套 | 呼叫嵌套 |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|
| [if bool-ps](if-bool---ps.md)         | 1                                    | 0                                                                         | 0                | 0            |
| [如果 \_ 是](if-comp---ps.md)        | 0                                    | 1                                                                         | 0                | 0            |
| [若為 pred-ps](if-pred---ps.md)         | 0                                    | 1                                                                         | 0                | 0            |
| [其他-ps](else---ps.md)               | 0                                    | 0                                                                         | 0                | 0            |
| [endif-ps](endif---ps.md)             | -1 ([if bool-ps](if-bool---ps.md))  | -1 ([if pred-ps](if-pred---ps.md)或[) \_ ](if-comp---ps.md) | 0                | 0            |
| [rep-ps](rep---ps.md)                 | 0                                    | 0                                                                         | 1                | 0            |
| [endrep-ps](endrep---ps.md)           | 0                                    | 0                                                                         | -1               | 0            |
| [中斷-ps](break---ps.md)             | 0                                    | 0                                                                         | 0                | 0            |
| [中斷 \_ 複合-ps](break-comp---ps.md)  | 0                                    | 1，-1                                                                     | 0                | 0            |
| [breakp-ps](break-p---ps.md)          | 0                                    | 0                                                                         | 0                | 0            |
| [呼叫-ps](call---ps.md)               | 0                                    | 0                                                                         | 0                | 1            |
| [callnz bool-ps](callnz-bool---ps.md) | 0                                    | 0                                                                         | 0                | 1            |
| [callnz pred-ps](callnz-pred---ps.md) | 0                                    | 1                                                                         | 0                | 1            |
| [ret-ps](ret---ps.md)                 | 0                                    | -1 ([callnz pred-ps](callnz-pred---ps.md))                               | 0                | -1           |
| [setp \_ comp-ps](setp-comp---ps.md)    | 0                                    | 0                                                                         | 0                | 0            |



 

### <a name="nesting-depth"></a>嵌套深度

「嵌套深度」定義可以從彼此內部呼叫的指令數目。 每種類型的指令都有一或多個嵌套限制，如下表所示。



| 指令類型 | 最大值                                                                                   |
|------------------|-------------------------------------------------------------------------------------------|
| 靜態嵌套   | 如果 (D3DCAPS9，則為24。D3DPSHADERCAPS2 \_ 0. StaticFlowControlDepth > 0) ; 否則為0            |
| 動態嵌套  | 0到24，請參閱 D3DCAPS9。D3DPSHADERCAPS2 \_ 0. DynamicFlowControlDepth                          |
| rep 的嵌套      | 0到4，請參閱 D3DCAPS9。D3DPSHADERCAPS2 \_ 0. StaticFlowControlDepth                            |
| 呼叫嵌套     | 0到4，請參閱 D3DCAPS9。D3DPSHADERCAPS2 \_ 0. StaticFlowControlDepth (獨立于 rep 限制)  |



 

### <a name="instruction-depth-count-for-ps_2_sw"></a>Ps \_ 2 sw 的指令深度 \_ 計數

每個指令都會計入一或多個嵌套深度限制。 下表顯示每個指令在現有深度中新增或減去的深度計數。



| 指令                              | 靜態嵌套                       | 動態嵌套                                                           | 迴圈/rep 的嵌套 | 呼叫嵌套 |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|
| [if bool-ps](if-bool---ps.md)         | 1                                    | 0                                                                         | 0                | 0            |
| [若為 pred-ps](if-pred---ps.md)         | 0                                    | 1                                                                         | 0                | 0            |
| [如果 \_ 是](if-comp---ps.md)        | 0                                    | 1                                                                         | 0                | 0            |
| [其他-ps](else---ps.md)               | 0                                    | 0                                                                         | 0                | 0            |
| [endif-ps](endif---ps.md)             | -1 ([if bool-ps](if-bool---ps.md))  | -1 ([if pred-ps](if-pred---ps.md)或[) \_ ](if-comp---ps.md) | 0                | 0            |
| [rep-ps](rep---ps.md)                 | 0                                    | 0                                                                         | 1                | 0            |
| [endrep-ps](endrep---ps.md)           | 0                                    | 0                                                                         | -1               | 0            |
| [迴圈-ps](loop---ps.md)               | n/a                                  | n/a                                                                       | n/a              | n/a          |
| [endloop-ps](endloop---ps.md)         | n/a                                  | n/a                                                                       | n/a              | n/a          |
| [中斷-ps](break---ps.md)             | 0                                    | 0                                                                         | 0                | 0            |
| [中斷 \_ 複合-ps](break-comp---ps.md)  | 0                                    | 1，-1                                                                     | 0                | 0            |
| [breakp-ps](break-p---ps.md)          | 0                                    | 0                                                                         | 0                | 0            |
| [呼叫-ps](call---ps.md)               | 0                                    | 0                                                                         | 0                | 1            |
| [callnz bool-ps](callnz-bool---ps.md) | 0                                    | 0                                                                         | 0                | 1            |
| [callnz pred-ps](callnz-pred---ps.md) | 0                                    | 1                                                                         | 0                | 1            |
| [ret-ps](ret---ps.md)                 | 0                                    | -1 ([callnz pred-ps](callnz-pred---ps.md))                               | 0                | -1           |
| [setp \_ comp-ps](setp-comp---ps.md)    | 0                                    | 0                                                                         | 0                | 0            |



 

### <a name="nesting-depth"></a>嵌套深度

[嵌套深度] 會定義可從彼此內部呼叫的指令數目。 每種類型的指令都有一或多個嵌套限制，如下表所示。



| 指令類型 | 最大值 |
|------------------|---------|
| 靜態嵌套   | 24      |
| 動態嵌套  | 24      |
| rep 的嵌套      | 4       |
| 呼叫嵌套     | 4       |



 

### <a name="instruction-depth-count-for-ps_3_0"></a>Ps \_ 3 0 的指令深度 \_ 計數

每個指令都會計入一或多個嵌套深度限制。 下表顯示每個指令在現有深度中新增或減去的深度計數。



| 指令                              | 靜態嵌套                       | 動態嵌套                                                           | 迴圈/rep 的嵌套 | 呼叫嵌套 |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|
| [if bool-ps](if-bool---ps.md)         | 1                                    | 0                                                                         | 0                | 0            |
| [若為 pred-ps](if-pred---ps.md)         | 0                                    | 1                                                                         | 0                | 0            |
| [如果 \_ 是](if-comp---ps.md)        | 0                                    | 1                                                                         | 0                | 0            |
| [其他-ps](else---ps.md)               | 0                                    | 0                                                                         | 0                | 0            |
| [endif-ps](endif---ps.md)             | -1 ([if bool-ps](if-bool---ps.md))  | -1 ([if pred-ps](if-pred---ps.md)或[) \_ ](if-comp---ps.md) | 0                | 0            |
| [rep-ps](rep---ps.md)                 | 0                                    | 0                                                                         | 1                | 0            |
| [endrep-ps](endrep---ps.md)           | 0                                    | 0                                                                         | -1               | 0            |
| [迴圈-ps](loop---ps.md)               | 0                                    | 0                                                                         | 1                | 0            |
| [endloop-ps](endloop---ps.md)         | 0                                    | 0                                                                         | -1               | 0            |
| [中斷-ps](break---ps.md)             | 0                                    | 0                                                                         | 0                | 0            |
| [中斷 \_ 複合-ps](break-comp---ps.md)  | 0                                    | 1，-1                                                                     | 0                | 0            |
| [breakp-ps](break-p---ps.md)          | 0                                    | 0                                                                         | 0                | 0            |
| [呼叫-ps](call---ps.md)               | 0                                    | 0                                                                         | 0                | 1            |
| [callnz bool-ps](callnz-bool---ps.md) | 0                                    | 0                                                                         | 0                | 1            |
| [callnz pred-ps](callnz-pred---ps.md) | 0                                    | 1                                                                         | 0                | 1            |
| [ret-ps](ret---ps.md)                 | 0                                    | -1 ([callnz pred-ps](callnz-pred---ps.md))                               | 0                | -1           |
| [setp \_ comp-ps](setp-comp---ps.md)    | 0                                    | 0                                                                         | 0                | 0            |



 

### <a name="nesting-depth"></a>嵌套深度

[嵌套深度] 會定義可從彼此內部呼叫的指令數目。 每種類型的指令都有一或多個嵌套限制，如下表所示。



| 指令類型 | 最大值 |
|------------------|---------|
| 靜態嵌套   | 24      |
| 動態嵌套  | 24      |
| 迴圈/rep 的嵌套 | 4       |
| 呼叫嵌套     | 4       |



 

### <a name="instruction-depth-count-for-ps_3_sw"></a>Ps \_ 3 sw 的指令深度 \_ 計數

每個指令都會計入一或多個嵌套深度限制。 下表顯示每個指令在現有深度中新增或減去的深度計數。



| 指令                              | 靜態嵌套                       | 動態嵌套                                                           | 迴圈/rep 的嵌套 | 呼叫嵌套 |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|
| [if bool-ps](if-bool---ps.md)         | 1                                    | 0                                                                         | 0                | 0            |
| [若為 pred-ps](if-pred---ps.md)         | 0                                    | 1                                                                         | 0                | 0            |
| [如果 \_ 是](if-comp---ps.md)        | 0                                    | 1                                                                         | 0                | 0            |
| [其他-ps](else---ps.md)               | 0                                    | 0                                                                         | 0                | 0            |
| [endif-ps](endif---ps.md)             | -1 ([if bool-ps](if-bool---ps.md))  | -1 ([if pred-ps](if-pred---ps.md)或[) \_ ](if-comp---ps.md) | 0                | 0            |
| [rep-ps](rep---ps.md)                 | 0                                    | 0                                                                         | 1                | 0            |
| [endrep-ps](endrep---ps.md)           | 0                                    | 0                                                                         | -1               | 0            |
| [迴圈-ps](loop---ps.md)               | 0                                    | 0                                                                         | 1                | 0            |
| [endloop-ps](endloop---ps.md)         | 0                                    | 0                                                                         | -1               | 0            |
| [中斷-ps](break---ps.md)             | 0                                    | 0                                                                         | 0                | 0            |
| [中斷 \_ 複合-ps](break-comp---ps.md)  | 0                                    | 1，-1                                                                     | 0                | 0            |
| [breakp-ps](break-p---ps.md)          | 0                                    | 0                                                                         | 0                | 0            |
| [呼叫-ps](call---ps.md)               | 0                                    | 0                                                                         | 0                | 1            |
| [callnz bool-ps](callnz-bool---ps.md) | 0                                    | 0                                                                         | 0                | 1            |
| [callnz pred-ps](callnz-pred---ps.md) | 0                                    | 1                                                                         | 0                | 1            |
| [ret-ps](ret---ps.md)                 | 0                                    | -1 ([callnz pred-ps](callnz-pred---ps.md))                               | 0                | -1           |
| [setp \_ comp-ps](setp-comp---ps.md)    | 0                                    | 0                                                                         | 0                | 0            |



 

### <a name="nesting-depth"></a>嵌套深度

[嵌套深度] 會定義可從彼此內部呼叫的指令數目。 每種類型的指令都有一或多個嵌套限制，如下表所示。



| 指令類型 | 最大值 |
|------------------|---------|
| 靜態嵌套   | 24      |
| 動態嵌套  | 24      |
| 迴圈/rep 的嵌套 | 4       |
| 呼叫嵌套     | 4       |



 

## <a name="interaction-of-per-pixel-flow-control-with-screen-gradients"></a>Per-Pixel Flow 控制項與螢幕漸層的互動

圖元著色器指令集包含數個指令，可產生或使用與螢幕空間 x 和 y 相關的數量漸層。 漸層最常見的用法是計算紋理取樣的詳細層級計算，而在非等向篩選的情況下，選取沿著 anisotropy 軸的範例。 通常，硬體執行會同時在多個圖元上執行圖元著色器 (例如2x2 格線) ，如此一來，在著色器中計算之數量的漸層可以合理地近似在相同的執行點上，以連續的圖元作為值的差異。

當流程式控制件存在於著色器中時，當連續的圖元可能執行不同的流程式控制制路徑時，在指定分支路徑內要求的漸層計算結果會是不明確的。 因此，使用任何圖元著色器作業時，可能會要求漸層計算發生在流程式控制制結構內的位置，而該位置可能會因圖元而異，而對指定的基本類型進行了點陣化。

所有圖元著色器的指令都已分割成這些作業，這些作業可被允許並併入流程式控制制內不允許的作業：

-   案例 A：不允許在流量控制內的作業，可能會在基本的圖元之間變化。 這些包括下表列出的作業。 

    | 指令                                                                                                      | 在下列情況中，Flow 控制允許：                       |
    |------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
    | [texld-ps \_ 2 \_ 0 和 up](texld---ps-2-0.md)、 [texldb-ps](texldb---ps.md) 和 [texldp-ps](texldp---ps.md) | 紋理座標會使用暫存登錄。 |
    | [dsx-ps](dsx---ps.md) 和 [dsy-ps](dsy---ps.md)                                                            | 用於運算元的臨時暫存器。            |

    

     

-   案例 B：可在任何地方使用的作業。 這些包括下表列出的作業。 

    | 指令                                                                                                      | 在下列任何位置都允許：                                                                                             |
    |------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
    | [texld-ps \_ 2 \_ 0 和 up](texld---ps-2-0.md)、 [texldb-ps](texldb---ps.md) 和 [texldp-ps](texldp---ps.md) | 「材質座標」（read only quantity）是用於材質座標 (可能會因每圖元而異，例如插補材質座標) 。 |
    | [dsx-ps](dsx---ps.md) 和 [dsy-ps](dsy---ps.md)                                                            | 唯讀數量會用於輸入運算元 (可能會因每圖元而異，例如插補材質座標) 。      |
    | [texldl-ps](texldl---ps.md)                                                                                   | 使用者提供詳細程度的引數，因此沒有任何漸層，因此不會有流量控制的問題。       |
    | [texldd-ps](texldd---ps.md)                                                                                   | 使用者提供漸層做為輸入引數，因此 flow 控制沒有任何問題。                                 |

    

     

這些限制會嚴格地在著色器驗證中強制執行。 如果條件運算式中的運算元是圖元著色器計算的數量，則具有像它這樣的分支條件的案例會在基本的情況下維持一致的狀態，但仍會落在案例 A 中，但不允許。 同樣地，在某些著色器計算數量 x 的情況下，從動態流量控制中要求漸層的情況，但在這種情況下，x 不會在任何分支上修改，但仍會進入案例 A，但不允許。

Predication 已包含在流量控制的這些限制中，因此，您可以使用前提指示將分支指示的執行保持為可自由完整交換。

使用者可以同時使用案例 A 和 B 的指示。 例如，假設使用者需要指定著色器計算紋理座標的非等向材質範例;不過，只有滿足某些每個圖元條件的圖元才需要材質載入。 為了符合這些需求，使用者可以計算所有圖元的材質座標（每圖元不同的流量控制），並使用 [dsx ps](dsx---ps.md) 和 [dsy ps](dsy---ps.md) 指令立即計算漸層。 然後，在每個圖元內的[布林-ps](if-bool---ps.md) / [endif-ps](endif---ps.md)區塊中，使用者可以使用[texldd-ps](texldd---ps.md) (材質載入與使用者提供的漸層) ，傳遞預先計算的漸層。 描述此使用模式的另一種方式是，雖然基本型別中的所有圖元都必須計算材質座標，而且牽涉到漸層計算，但是只有取樣紋理所需的圖元才會實際執行這項作業。

無論這些規則為何，在計算任何漸層 (或執行隱含計算漸層) 的材質範例之前，都必須先為所有執行路徑初始化包含來源資料的註冊。 臨時暫存器的初始化不會在一般情況中進行驗證或強制執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




