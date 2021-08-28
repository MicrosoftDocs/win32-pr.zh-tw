---
title: if_comp-vs
description: 啟動 if bool-vs .。。else-vs .。。endif-vs block，具有以可在著色器中計算之值為基礎的條件。 此指令是用來根據條件略過程式碼區塊。
ms.assetid: a3fe93c6-be26-4216-a601-3be52a74be06
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 11c7abceb9b484c4cd104e136c47edeb55b93b5273f953cb6d98052e247513d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743578"
---
# <a name="if_comp---vs"></a>如果是 \_ 複合-vs

啟動 [if bool-vs](if-bool---vs.md).。。[else-vs](else---vs.md).。。[endif-vs](endif---vs.md) block，具有以可在著色器中計算之值為基礎的條件。 此指令是用來根據條件略過程式碼區塊。

## <a name="syntax"></a>Syntax



| if \_ comp src0、src1 |
|---------------------|



 

其中：

-   \_comp 是兩個來源暫存器之間的比較。 可以是下列其中一項： 

    | Syntax | 比較            |
    |--------|-----------------------|
    | \_燃氣輪機   | 大於          |
    | \_淺色   | 小於             |
    | \_通用 電氣   | 大於或等於 |
    | \_樂   | 小於或等於    |
    | \_情 商   | 等於              |
    | \_ne   | 不等於          |

    

     

-   src0 是來源註冊。 需要複寫 swizzle 才能選取元件。
-   src1 是來源註冊。 需要複寫 swizzle 才能選取元件。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| 若為 \_ comp               |      |      | x    | x     | x    | x     |



 

此指令是用來根據條件略過程式碼區塊。


```
if_lt src0, src1
   jump to the corresponding else or endif instruction;
```



請小心使用浮點數的 equals 和 not equals 比較模式。 因為四捨五入是在浮點計算期間進行，所以可以針對 epsilon 值進行比較， (不) 的非零值，以避免發生錯誤。

限制包含：

-   如果 \_ 為 .。。[else-vs](else---vs.md).。。[endif-vs](endif---vs.md) 區塊 (以及區塊) 可以嵌套最多24層級的前提。
-   src0 和 src1 暫存器需要複製 swizzle。
-   如果 \_ 複合區塊必須以 [else-vs](else---vs.md) 或 [endif-vs](endif---vs.md) 指令結尾。
-   如果 \_ 為 .。。[else-vs](else---vs.md).。。[endif-vs](endif---vs.md) 區塊無法跨迴圈區塊。 If \_ 複合區塊必須完全在迴圈內，或在 [迴圈和迴圈](loop---vs.md) 中。

## <a name="example"></a>範例

此指令提供條件式動態流量控制。


```
if_lt r3.x, r4.y
// Instructions to run if r3.x < r4.y

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




