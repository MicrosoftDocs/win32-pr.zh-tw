---
title: 流程式控制制的嵌套限制
description: 頂點著色器流程式控制制指示有兩個特殊限制。
ms.assetid: c9f80a97-8245-4974-a284-7974e2d2e504
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4ebb5b491e074c2275081aa3fe629a2486a24c6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675860"
---
# <a name="flow-control-nesting-limits"></a>流程式控制制的嵌套限制

頂點著色器流程式控制制指示有兩個特殊限制。 嵌套深度會限制可在彼此內部呼叫的指令數目。 此外，每個指令都具有適用于著色器可支援之指令最大數目的指令位置計數。

> [!Note]  
> 當您使用 \* \_ 4 個 \_ \_ 層級 \_ 9 \_ x HLSL 著色器設定檔時，會隱含地使用[著色器模型](dx-graphics-hlsl-sm2.md)2.x 設定檔來支援具有 Direct3D 9 功能的硬體。 著色器模型2.x 設定檔支援的流程式控制制行為比 [著色器模型](dx-graphics-hlsl-sm4.md) 4.x 和更新版本設定檔更受限。

 

## <a name="depth-count-per-instruction-for-vs_2_0"></a>Vs \_ 2 0 每個指令的深度計數 \_

每個指令都會計入一或多個嵌套深度限制。 下表顯示每個指令從現有深度新增或減去的深度計數：



| 指令                              | 靜態嵌套 | 動態嵌套 | 迴圈/rep 的嵌套 | 呼叫嵌套 | 靜態流程計數                        |
|------------------------------------------|----------------|-----------------|------------------|--------------|------------------------------------------|
| [if bool-vs](if-bool---vs.md)         | 0              | 0               | 0                | 0            | 1                                        |
| [如果是 \_ 複合-vs](if-comp---vs.md)        | n/a            | n/a             | n/a              | n/a          | n/a                                      |
| [如果 pred-vs](if-pred---vs.md)         | n/a            | n/a             | n/a              | n/a          | n/a                                      |
| [else-vs](else---vs.md)               | 0              | 0               | 0                | 0            | 1 ([如果僅限 bool-vs](if-bool---vs.md))  |
| [endif-vs](endif---vs.md)             | -1             | 0               | 0                | 0            | 0                                        |
| [rep-vs](rep---vs.md)                 | 0              | 0               | 1                | 0            | 1                                        |
| [endrep-vs](endrep---vs.md)           | 0              | 0               | -1               | 0            | 0                                        |
| [迴圈-vs](loop---vs.md)               | 0              | 0               | 1                | 0            | 1                                        |
| [endloop-vs](endloop---vs.md)         | 0              | 0               | -1               | 0            | 0                                        |
| [中斷-vs](break---vs.md)             | n/a            | n/a             | n/a              | n/a          | n/a                                      |
| [中斷 \_ 複合-vs](break-comp---vs.md)  | n/a            | n/a             | n/a              | n/a          | n/a                                      |
| [breakp-vs](breakp---vs.md)           | n/a            | n/a             | n/a              | n/a          | n/a                                      |
| [呼叫-vs](call---vs.md)               | 0              | 0               | 0                | 1            | 1                                        |
| [callnz bool-vs](callnz-bool---vs.md) | 0              | 0               | 0                | 1            | 1                                        |
| [callnz pred-vs](callnz-pred---vs.md) | n/a            | n/a             | n/a              | n/a          | n/a                                      |
| [ret-vs](ret---vs.md)                 | 0              | 0               | 0                | -1           | 0                                        |
| [setp \_ 複合-vs](setp-comp---vs.md)    | n/a            | n/a             | n/a              | n/a          | n/a                                      |



 

### <a name="nesting-depth"></a>嵌套深度

「嵌套深度」定義可以在彼此內部呼叫的指令數目。 每種類型的指令都有一或多個嵌套限制：



| 指令類型  | 最大值                               |
|-------------------|---------------------------------------|
| 靜態嵌套    | 僅受限於靜態流程計數 |
| 動態嵌套   | n/a                                   |
| 迴圈/rep 的嵌套  | 1                                     |
| 呼叫嵌套      | 1                                     |
| 靜態流程計數 | 16                                    |



 

## <a name="depth-count-per-instruction-for-vs_2_x"></a>Vs \_ 2 x 的每個指令深度計數 \_

每個指令都會計入一或多個嵌套深度限制。 下表顯示每個指令從現有深度新增或減去的深度計數：



| 指令                              | 靜態嵌套                       | 動態嵌套                                                           | 迴圈/rep 的嵌套 | 呼叫嵌套 | 靜態流程計數                        |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|------------------------------------------|
| [if bool-vs](if-bool---vs.md)         | 1                                    | 0                                                                         | 0                | 0            | 1                                        |
| [如果是 \_ 複合-vs](if-comp---vs.md)        | 0                                    | 1                                                                         | 0                | 0            | 0                                        |
| [如果 pred-vs](if-pred---vs.md)         | 0                                    | 1                                                                         | 0                | 0            | 0                                        |
| [else-vs](else---vs.md)               | 0                                    | 0                                                                         | 0                | 0            | 1 ([如果僅限 bool-vs](if-bool---vs.md))  |
| [endif-vs](endif---vs.md)             | -1 ([if bool-vs](if-bool---vs.md))  | -1 ([if pred-vs](if-pred---vs.md) 或 [ \_ 複合-vs](if-comp---vs.md))  | 0                | 0            | 0                                        |
| [rep-vs](rep---vs.md)                 | 0                                    | 0                                                                         | 1                | 0            | 1                                        |
| [endrep-vs](endrep---vs.md)           | 0                                    | 0                                                                         | -1               | 0            | 0                                        |
| [迴圈-vs](loop---vs.md)               | 0                                    | 0                                                                         | 1                | 0            | 1                                        |
| [endloop-vs](endloop---vs.md)         | 0                                    | 0                                                                         | -1               | 0            | 0                                        |
| [中斷-vs](break---vs.md)             | 0                                    | 0                                                                         | 0                | 0            | 0                                        |
| [中斷 \_ 複合-vs](break-comp---vs.md)  | 0                                    | 1，-1                                                                     | 0                | 0            | 0                                        |
| [breakp-vs](breakp---vs.md)           | 0                                    | 0                                                                         | 0                | 0            | 0                                        |
| [呼叫-vs](call---vs.md)               | 0                                    | 0                                                                         | 0                | 1            | 1                                        |
| [callnz bool-vs](callnz-bool---vs.md) | 0                                    | 0                                                                         | 0                | 1            | 1                                        |
| [callnz pred-vs](callnz-pred---vs.md) | 0                                    | 1                                                                         | 0                | 1            | 0                                        |
| [ret-vs](ret---vs.md)                 | 0                                    | -1 ([callnz pred-vs](callnz-pred---vs.md))                              | 0                | -1           | 0                                        |
| [setp \_ 複合-vs](setp-comp---vs.md)    | 0                                    | 0                                                                         | 0                | 0            | 0                                        |



 

### <a name="nesting-depth"></a>嵌套深度

「嵌套深度」定義可以在彼此內部呼叫的指令數目。 每種類型的指令都有一或多個嵌套限制：



| 指令類型  | 最大值                                                                              |
|-------------------|--------------------------------------------------------------------------------------|
| 靜態嵌套    | 僅受限於靜態流程計數                                                |
| 動態嵌套   | 0或24，請參閱 D3DCAPS9。VS20Caps.DynamicFlowControlDepth                               |
| 迴圈/rep 的嵌套  | 1到4，請參閱 D3DCAPS9。VS20Caps.StaticFlowControlDepth                                 |
| 呼叫嵌套      | 1到4，請參閱 D3DCAPS9。VS20Caps. StaticFlowControlDepth (獨立于迴圈/rep 限制)  |
| 靜態流程計數 | 16                                                                                   |



 

## <a name="depth-count-per-instruction-for-vs_2_sw"></a>Vs \_ 2 sw 的每個指令深度計數 \_

每個指令都會計入一或多個嵌套深度限制。 下表顯示每個指令從現有深度新增或減去的深度計數：



| 指令                              | 靜態嵌套                       | 動態嵌套                                                           | 迴圈/rep 的嵌套 | 呼叫嵌套 | 靜態流程計數 |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|-------------------|
| [if bool-vs](if-bool---vs.md)         | 1                                    | 0                                                                         | 0                | 0            | n/a               |
| [如果是 \_ 複合-vs](if-comp---vs.md)        | 0                                    | 1                                                                         | 0                | 0            | n/a               |
| [如果 pred-vs](if-pred---vs.md)         | 0                                    | 1                                                                         | 0                | 0            | n/a               |
| [else-vs](else---vs.md)               | 0                                    | 0                                                                         | 0                | 0            | n/a               |
| [endif-vs](endif---vs.md)             | -1 ([if bool-vs](if-bool---vs.md))  | -1 ([if pred-vs](if-pred---vs.md) 或 [ \_ 複合-vs](if-comp---vs.md))  | 0                | 0            | n/a               |
| [rep-vs](rep---vs.md)                 | 0                                    | 0                                                                         | 1                | 0            | n/a               |
| [endrep-vs](endrep---vs.md)           | 0                                    | 0                                                                         | -1               | 0            | n/a               |
| [迴圈-vs](loop---vs.md)               | 0                                    | 0                                                                         | 1                | 0            | n/a               |
| [endloop-vs](endloop---vs.md)         | 0                                    | 0                                                                         | -1               | 0            | n/a               |
| [中斷-vs](break---vs.md)             | 0                                    | 0                                                                         | 0                | 0            | n/a               |
| [中斷 \_ 複合-vs](break-comp---vs.md)  | 0                                    | 1，-1                                                                     | 0                | 0            | n/a               |
| [breakp-vs](breakp---vs.md)           | 0                                    | 0                                                                         | 0                | 0            | n/a               |
| [呼叫-vs](call---vs.md)               | 0                                    | 0                                                                         | 0                | 1            | n/a               |
| [callnz bool-vs](callnz-bool---vs.md) | 0                                    | 0                                                                         | 0                | 1            | n/a               |
| [callnz pred-vs](callnz-pred---vs.md) | 0                                    | 1                                                                         | 0                | 1            | n/a               |
| [ret-vs](ret---vs.md)                 | 0                                    | -1 ([callnz pred-vs](callnz-pred---vs.md))                              | 0                | -1           | n/a               |
| [setp \_ 複合-vs](setp-comp---vs.md)    | 0                                    | 0                                                                         | 0                | 0            | n/a               |



 

### <a name="nesting-depth"></a>嵌套深度

「嵌套深度」定義可以在彼此內部呼叫的指令數目。 每種類型的指令都有一或多個嵌套限制：



| 指令類型  | 最大值  |
|-------------------|----------|
| 靜態嵌套    | 24       |
| 動態嵌套   | 24       |
| 迴圈/rep 的嵌套  | 4        |
| 呼叫嵌套      | 4        |
| 靜態流程計數 | 沒有限制 |



 

## <a name="depth-count-per-instruction-for-vs_3_0"></a>Vs \_ 3 0 每個指令的深度計數 \_

每個指令都會計入一或多個嵌套深度限制。 下表顯示每個指令從現有深度新增或減去的深度計數：



| 指令                              | 靜態嵌套                       | 動態嵌套                                                           | 迴圈/rep 的嵌套 | 呼叫嵌套 | 靜態流程計數 |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|-------------------|
| [if bool-vs](if-bool---vs.md)         | 1                                    | 0                                                                         | 0                | 0            | n/a               |
| [如果是 \_ 複合-vs](if-comp---vs.md)        | 0                                    | 1                                                                         | 0                | 0            | n/a               |
| [如果 pred-vs](if-pred---vs.md)         | 0                                    | 1                                                                         | 0                | 0            | n/a               |
| [else-vs](else---vs.md)               | 0                                    | 0                                                                         | 0                | 0            | n/a               |
| [endif-vs](endif---vs.md)             | -1 ([if bool-vs](if-bool---vs.md))  | -1 ([if pred-vs](if-pred---vs.md) 或 [ \_ 複合-vs](if-comp---vs.md))  | 0                | 0            | n/a               |
| [rep-vs](rep---vs.md)                 | 0                                    | 0                                                                         | 1                | 0            | n/a               |
| [endrep-vs](endrep---vs.md)           | 0                                    | 0                                                                         | -1               | 0            | n/a               |
| [迴圈-vs](loop---vs.md)               | 0                                    | 0                                                                         | 1                | 0            | n/a               |
| [endloop-vs](endloop---vs.md)         | 0                                    | 0                                                                         | -1               | 0            | n/a               |
| [中斷-vs](break---vs.md)             | 0                                    | 0                                                                         | 0                | 0            | n/a               |
| [中斷 \_ 複合-vs](break-comp---vs.md)  | 0                                    | 1，-1                                                                     | 0                | 0            | n/a               |
| [breakp-vs](breakp---vs.md)           | 0                                    | 0                                                                         | 0                | 0            | n/a               |
| [呼叫-vs](call---vs.md)               | 0                                    | 0                                                                         | 0                | 1            | n/a               |
| [callnz bool-vs](callnz-bool---vs.md) | 0                                    | 0                                                                         | 0                | 1            | n/a               |
| [callnz pred-vs](callnz-pred---vs.md) | 0                                    | 1                                                                         | 0                | 1            | n/a               |
| [ret-vs](ret---vs.md)                 | 0                                    | -1 ([callnz pred-vs](callnz-pred---vs.md))                              | 0                | -1           | n/a               |
| [setp \_ 複合-vs](setp-comp---vs.md)    | 0                                    | 0                                                                         | 0                | 0            | n/a               |



 

### <a name="nesting-depth"></a>嵌套深度

「嵌套深度」定義可以在彼此內部呼叫的指令數目。 每種類型的指令都有一或多個嵌套限制：



| 指令類型  | 最大值  |
|-------------------|----------|
| 靜態嵌套    | 24       |
| 動態嵌套   | 24       |
| 迴圈/rep 的嵌套  | 4        |
| 呼叫嵌套      | 4        |
| 靜態流程計數 | 沒有限制 |



 

## <a name="depth-count-per-instruction-for-vs_3_sw"></a>Vs \_ 3 sw 的每個指令深度計數 \_

每個指令都會計入一或多個嵌套深度限制。 下表顯示每個指令從現有深度新增或減去的深度計數：



| 指令                              | 靜態嵌套                       | 動態嵌套                                                           | 迴圈/rep 的嵌套 | 呼叫嵌套 | 靜態流程計數 |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|-------------------|
| [if bool-vs](if-bool---vs.md)         | 1                                    | 0                                                                         | 0                | 0            | n/a               |
| [如果是 \_ 複合-vs](if-comp---vs.md)        | 0                                    | 1                                                                         | 0                | 0            | n/a               |
| [如果 pred-vs](if-pred---vs.md)         | 0                                    | 1                                                                         | 0                | 0            | n/a               |
| [else-vs](else---vs.md)               | 0                                    | 0                                                                         | 0                | 0            | n/a               |
| [endif-vs](endif---vs.md)             | -1 ([if bool-vs](if-bool---vs.md))  | -1 ([if pred-vs](if-pred---vs.md) 或 [ \_ 複合-vs](if-comp---vs.md))  | 0                | 0            | n/a               |
| [rep-vs](rep---vs.md)                 | 0                                    | 0                                                                         | 1                | 0            | n/a               |
| [endrep-vs](endrep---vs.md)           | 0                                    | 0                                                                         | -1               | 0            | n/a               |
| [迴圈-vs](loop---vs.md)               | 0                                    | 0                                                                         | 1                | 0            | n/a               |
| [endloop-vs](endloop---vs.md)         | 0                                    | 0                                                                         | -1               | 0            | n/a               |
| [中斷-vs](break---vs.md)             | 0                                    | 0                                                                         | 0                | 0            | n/a               |
| [中斷 \_ 複合-vs](break-comp---vs.md)  | 0                                    | 1，-1                                                                     | 0                | 0            | n/a               |
| [breakp-vs](breakp---vs.md)           | 0                                    | 0                                                                         | 0                | 0            | n/a               |
| [呼叫-vs](call---vs.md)               | 0                                    | 0                                                                         | 0                | 1            | n/a               |
| [callnz bool-vs](callnz-bool---vs.md) | 0                                    | 0                                                                         | 0                | 1            | n/a               |
| [callnz pred-vs](callnz-pred---vs.md) | 0                                    | 1                                                                         | 0                | 1            | n/a               |
| [ret-vs](ret---vs.md)                 | 0                                    | -1 ([callnz pred-vs](callnz-pred---vs.md))                              | 0                | -1           | n/a               |
| [setp \_ 複合-vs](setp-comp---vs.md)    | 0                                    | 0                                                                         | 0                | 0            | n/a               |



 

### <a name="nesting-depth"></a>嵌套深度

「嵌套深度」定義可以在彼此內部呼叫的指令數目。 每種類型的指令都有一或多個嵌套限制：



| 指令類型  | 最大值  |
|-------------------|----------|
| 靜態嵌套    | 24       |
| 動態嵌套   | 24       |
| 迴圈/rep 的嵌套  | 4        |
| 呼叫嵌套      | 4        |
| 靜態流程計數 | 沒有限制 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




