---
title: 位址註冊
description: A0 註冊是位址暫存器。
ms.assetid: ad86013c-3358-4770-a01c-544c868691f4
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e58f42848034d12063611e14b82cb2f2d132cb43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840467"
---
# <a name="address-register"></a>位址註冊

A0 註冊是位址暫存器。 版本與 1 1 之間有提供單一 \_ 登錄 \_ 。 在 vs 1 1 中指定為 a0. x 的位址暫存器， \_ \_ 可用來做為相對定址的帶正負號整數位移，以取得常數暫存器檔案的相對定址。 針對版本與 \_ 2 \_ 0 （含）以上版本，所有四個元件 (. x、. y、. z、w) 都可用於相對定址。


```
c[a0.x + n]
```



端點著色器無法讀取位址暫存器，它只能用於常數暫存器的相對定址。 若讀取合法範圍以外的值，將會傳回 (0.0、0.0、0.0、0.0) 。 位址暫存器只能是 [mov-vs](mov---vs.md) 指令的目的地。 如果將浮點數移至整數暫存器中，就會發生四捨五入到最接近的轉換。

所有著色器都必須先初始化位址暫存器，才能使用它。 針對版本 vs \_ 2 \_ 0 和更新版本， [mova vs](mova---vs.md) 指令可以將浮點值移至位址暫存器。



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2個 \_ sw | 2 \_ x | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| 位址註冊       | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器暫存器](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




