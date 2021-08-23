---
title: break_comp-ps
description: 根據每個元件的比較，中斷最近 endloop ps 或 endrep ps 的目前迴圈。
ms.assetid: d21e850f-05db-4a29-b15b-85bb1c1410d0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2fa79b7aa50bc734ddc1f9fb1fd54e4130c48518dd47ed429b4177b8fb867d95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118794455"
---
# <a name="break_comp---ps"></a>中斷 \_ 複合-ps

根據每個元件的比較，中斷最近 [endloop ps](endloop---ps.md) 或 [endrep ps](endrep---ps.md)的目前迴圈。

## <a name="syntax"></a>Syntax



| break \_ comp src0，src1 |
|------------------------|



 

其中：

-   \_comp 是兩個來源暫存器之間的純量 (或單一) 比較。 可以是下列其中一項： 

    | Syntax | 比較            |
    |--------|-----------------------|
    | \_燃氣輪機   | 大於          |
    | \_淺色   | 小於             |
    | \_通用 電氣   | 大於或等於 |
    | \_樂   | 小於或等於    |
    | \_情 商   | 等於              |
    | \_ne   | 不等於          |

    

     

-   src0 是來源註冊。 如果選取單一元件，則需要複寫 swizzle。
-   src1 是來源註冊。 如果選取單一元件，則需要複寫 swizzle。

## <a name="remarks"></a>備註

下列版本支援此指令。



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| 中斷 \_ 複合           |      |      |      |      |      | x    | x     | x    | x     |



 

當比較結果為 true 時，它會中斷目前的迴圈，如下所示。


```
if (!(src0 comparison src1))
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




