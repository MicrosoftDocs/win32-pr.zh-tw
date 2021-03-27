---
title: if_comp-ps
description: 啟動 if bool-ps .。。其他-ps .。。endif-ps 區塊，具有以可在著色器中計算之值為基礎的條件。 此指令是用來根據條件略過程式碼區塊。
ms.assetid: a641e347-df28-4a3f-a461-0b6aee758e59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: db30983c83bc7d66e06befd07f4eb1dcdc9b21ea
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679100"
---
# <a name="if_comp---ps"></a>如果 \_ 是

啟動 [if bool-ps](if-bool---ps.md).。。[其他-ps](else---ps.md).。。[endif-ps](endif---ps.md) 區塊，具有以可在著色器中計算之值為基礎的條件。 此指令是用來根據條件略過程式碼區塊。

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



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| 若為 \_ comp              |      |      |      |      |      | x    | x     | x    | x     |



 

此指令是用來根據條件略過程式碼區塊。


```
if (src0 comparison src1)
   jump to the corresponding else or endif instruction;
```



請小心使用浮點數的 equals 和 not equals 比較模式。 因為四捨五入是在浮點計算期間進行，所以可以針對 epsilon 值進行比較， (不) 的非零值，以避免發生錯誤。

限制包含：

-   如果 \_ 為 .。。[其他-ps](else---ps.md).。。[如果](if-bool---ps.md)[區塊) ](endif---ps.md)最多可嵌套至24層，則會將 (與前提搭配使用。
-   src0 和 src1 暫存器需要複製 swizzle。
-   如果 \_ 複合區塊必須以 [else-vs](else---vs.md) 或 [endif-vs](endif---vs.md) 指令結尾。
-   如果 \_ 為 .。。[其他-ps](else---ps.md).。。[endif-ps](endif---ps.md) 區塊無法跨迴圈區塊。 If \_ 複合區塊必須完全在迴圈區塊內部或外部。

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

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




