---
description: 運算式是在等號右邊使用的數學或邏輯語句。 有許多類型的運算式。
ms.assetid: 642aa188-5dd7-49fc-b6cc-845f8fc22530
title: " (Direct3D 9) 的運算式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa574069094853eb506f7a1b38cdb6cd4379d3b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106991584"
---
# <a name="expressions-direct3d-9"></a> (Direct3D 9) 的運算式

運算式是在等號右邊使用的數學或邏輯語句。 有許多類型的運算式。

## <a name="expressions"></a>運算式

1.  變數參考
    ```
    ( variable ) or<variable >
    ```

    

2.  數值純量
    ```
    scalar 
    ```

    

3.  數值運算式

    ```
    ( numeric expression )
    ```

    

    此處支援所有標準數值 HLL 運算式。

4.  建構函式
    ```
    type ( constructor arguments )
    ```

    

5.  初始化運算式清單

    ```
    { scalar value [, scalar value ...  ] }
    
    ```

    

    純量值必須是常值純量值。

    初始化運算式的數目必須與等號左邊的變數 (狀態) 相容。

6.  OR 運算式

    ```
    token [ | token ... ]
    ```

    

    標記必須與等號左邊的變數 (狀態) 相容。

    標記不區分大小寫。

7.  NULL

    ```
    NULL
    ```

    

    Null 只能指派給著色器、取樣器或紋理物件。

8.  元件區塊

    ```
    asm { code }
    ```

    

    必須將 PS 元件區塊指派給無效狀態。

    必須將 VS 元件區塊指派給 VERTEXSHADER 狀態。

9.  取樣器狀態欄塊

    ```
    sampler_state { [ state = expression ; [ state = ... ] ] }
    ```

    

    取樣器狀態欄塊是未索引的取樣器階段狀態或材質指派的順序。

    取樣器狀態欄塊必須指派給取樣器效果狀態。

10. 效果狀態狀態欄塊

    ```
    stateblock_state { [ state [ [index] ] = expression; 
        [ state [ [index] ] = ... ] ] }
    ```

    

    狀態欄塊是一般狀態的序列。 狀態欄塊可以進行嵌套，但不能包含迴圈參考。

    必須將狀態欄塊指派給 STATEBLOCK 效果狀態。

11. HLSL 編譯

    ```
    compile target entrypoint ( [ arguments ] )
    ```

    

    頂點著色器與 \_ m \_ n 目標表示 D3DVS \_ 版本 (m，n) 頂點著色器版本。 圖元著色器 ps \_ m \_ n 目標表示 D3DPS \_ 版 (m，n) 圖元著色器版本。

    頂點著色器高階語言編譯運算式只能指派給 VERTEXSHADER 效果狀態。 圖元著色器高階語言編譯運算式只能指派給無效效果狀態。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[效果格式](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



