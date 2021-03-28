---
title: '暫存註冊 (HLSL 與參考) '
description: 頂點著色器暫存登錄用來保存中繼結果。
ms.assetid: 186adff6-0641-4507-9adc-e02cf1cc3ea9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c3dcaa5ac0c9c1531a1e1f0476d2ef13b4bac509
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "104313797"
---
# <a name="temporary-register-hlsl-vs-reference"></a>暫存註冊 (HLSL 與參考) 

頂點著色器暫存登錄用來保存中繼結果。

在使用暫存登錄之前，必須先將它初始化。 每個暫存登錄都具有單一寫入和三次讀取的存取權。 這表示單一著色器指令最多可使用三個暫存暫存器做為輸入。

無法使用在先前叫用端點著色器之前保持的臨時暫存器值。

暫存器包含的屬性會決定每個註冊的行為。



| 屬性        | 描述                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Name            | r \[ n \] 。 n 是選擇性的註冊編號。 預設值為0，如果未指定任何值，則為所使用的值。                                                                                 |
| Count           | 最多12個註冊程式。                                                                                                                                                                  |
| I/o 許可權 | 讀取/寫入 此暫存器可由 API 或著色器讀取或寫入。                                                                                                               |
| 讀取埠      | 在單一指令中可讀取的暫存器次數為3。 臨時暫存器是唯一可在單一指令中讀取和寫入一次以上的暫存器。 |



 

每個暫存登錄都具有單一寫入和三次讀取的存取權。 因此，指令在一組輸入來源運算元中最多可以有三個暫存暫存器。

臨時暫存器中的任何值都不能使用先前調用的端點著色器。 在寫入之前從暫時登錄讀取值的頂點著色器將會使 Direct3D API 呼叫無法建立頂點著色器。

## <a name="example"></a>範例

以下是使用暫存註冊的範例：


```
def c4, 0,0,0,1
...
// Decompress position
mov r0.x, v0.x
mov r0.y, c4.w       // 1
mov r0.z, v0.y
mov r0.w, c4.w       // 1

// Compute theta from distance and time
mov r4.xz, r0        // xz
```





| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2個 \_ sw | 2 \_ x | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| 暫時註冊     | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器暫存器](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




