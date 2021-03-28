---
title: 階段-ps
description: 階段指令會標示第1階段和第2階段之間的轉換。 如果沒有任何階段指令，則整個著色器的執行方式就如同第2階段著色器。
ms.assetid: e0e89425-dc8e-489f-a0d1-3eefbfd09178
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e9a16b01e186de5645ffe65e003ebbe6defca2d5
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022847"
---
# <a name="phase---ps"></a>階段-ps

階段指令會標示第1階段和第2階段之間的轉換。 如果沒有任何階段指令，則整個著色器的執行方式就如同第2階段著色器。

此指令僅適用于第1版 \_ 。

## <a name="syntax"></a>語法


```
phase
```



## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| 階段                 |      |      |      | x    |      |      |       |      |       |



 

階段指令之前發生的著色器指示是階段1指示。 所有其他指示都是階段2指示。 有兩個指示的階段，每個著色器的指令數目上限就會增加。

階段轉換的副作用是， [暫存](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) 暫存器的 Alpha 元件不會跨轉換保存。 換句話說，Alpha 元件必須在階段指令之後重新初始化。

## <a name="example"></a>範例

此範例示範如何將指令群組為著色器內的第1階段或第2階段指令。

階段指令通常也稱為階段標記，因為它會標示第1階段和第2個指令之間的轉換。 在第1版的 \_ 圖元著色器中，如果階段標記不存在，就會以第2階段執行著色器。 這點很重要，因為階段1和2的指示之間有差異，並註冊可用性。 所有參考部分都會注明差異。


```
ps_1_4
  // Add phase 1 instructions here

phase
  // Add phase 2 instructions here
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




