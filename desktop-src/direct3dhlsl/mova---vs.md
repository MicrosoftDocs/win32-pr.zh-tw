---
title: mova-vs
description: 將資料從浮點暫存器移至位址暫存器（a0）。
ms.assetid: 929a0670-f337-4d6d-a7e7-d285e7dc8ae1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dec849009ee47b4aaef1bc3766e2b141a8a6ccf5e17b16a370c6ea8284eaf957
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986328"
---
# <a name="mova---vs"></a>mova-vs

將資料從浮點暫存器移至 [位址](dx9-graphics-reference-asm-vs-registers-address.md)暫存器（a0）。

## <a name="syntax"></a>Syntax



| mova dst、src |
|---------------|



 

其中

-   dst 必須是 [位址](dx9-graphics-reference-asm-vs-registers-address.md)暫存器（a0）。
-   src 是來源暫存器。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| mova                   |      | x    | x    | x     | x    | x     |



 

將浮點數據移至整數暫存器。 這些值會使用四捨五入到最接近的位置從浮點轉換。

Address register 是唯一允許的目的地註冊。

下列程式碼片段會顯示已執行的作業。


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src);
    dest = intSrc;
}
else
{
    dest = src;
}
```



如果是 2 \_ x 以上的版本，位址暫存器是元件向量。 因此，允許任何寫入遮罩。


```
mova a0.xz, r0
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




