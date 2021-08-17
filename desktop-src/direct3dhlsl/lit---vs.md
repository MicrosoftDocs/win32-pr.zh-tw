---
title: 亮-vs
description: 藉由計算兩個點乘積的光源係數和指數來提供光源的部分支援。
ms.assetid: e0ed1a75-6682-4d05-b0e5-dc65e201de98
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3e5b5ff3451424251d778886af3841c673ce5a85d91022db9144c62574c16640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118089321"
---
# <a name="lit---vs"></a>亮-vs

藉由計算兩個點乘積的光源係數和指數來提供光源的部分支援。

## <a name="syntax"></a>Syntax



| 亮 dst、src |
|--------------|



 

其中

-   dst 是目的地註冊。
-   src 是來源暫存器。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| 點燃                    | x    | x    | x    | x     | x    | x     |



 

假設來源向量包含下列虛擬程式碼中所示的值。


```
src.x = N*L        ; The dot product between normal and direction to light
src.y = N*H        ; The dot product between normal and half vector
src.z = ignored    ; This value is ignored
src.w = exponent   ; The value must be between -128.0 and 128.0
```



下列程式碼片段會顯示已執行的作業。


```
dest.x = 1;
dest.y = 0;
dest.z = 0;
dest.w = 1;

float power = src.w;
const float MAXPOWER = 127.9961f;
if (power < -MAXPOWER)
    power = -MAXPOWER;          // Fits into 8.8 fixed point format
else if (power > MAXPOWER)
    power = MAXPOWER;          // Fits into 8.8 fixed point format

if (src.x > 0)
{
    dest.y = src.x;
    if (src.y > 0)
    {
        // Allowed approximation is EXP(power * LOG(src.y))
        dest.z = (float)(pow(src.y, power));
    }
}
```



評估目的地 y 元件 (destination. y) 可接受降低精確度算術。 執行必須在 power 引數中至少支援8個小數位。 點乘積以正規化向量計算，而夾具限制為-128 到128。

錯誤應該對應至 [logp-vs](logp---vs.md) 和 [exp-vs](exp---vs.md) 組合，或8位色彩元件的最多一個有效位。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




