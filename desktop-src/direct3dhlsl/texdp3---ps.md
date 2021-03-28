---
title: texdp3-ps
description: 在材質暫存器編號中的資料和對應至目的地暫存器編號的材質座標集合之間，執行三個元件的點乘積。
ms.assetid: 82e02f3f-4b88-4007-b4be-0c66223d9c66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 64cc14ee66123ea3e25941579b9838977a753174
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313617"
---
# <a name="texdp3---ps"></a>texdp3-ps

在材質暫存器編號中的資料和對應至目的地暫存器編號的材質座標集合之間，執行三個元件的點乘積。

## <a name="syntax"></a>Syntax



| texdp3 dst、src |
|-----------------|



 

其中

-   dst 是目的地註冊。
-   src 是來源暫存器。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texdp3                |      | x    | x    |      |      |      |       |      |       |



 

材質暫存器必須使用下列順序。


```
 
tex    t(n)        // Define tn as a standard 3-vector (tn must be 
                   //   defined in some way before texdp3 uses it)
texdp3 t(m), t(n)  // where m > n
                   // Perform a three-component dot product between tn and 
                   //   the texture coordinate set m. The scalar result is
                   //   replicated to all components of t(m)
```



以下是如何完成點乘積的詳細資料。

Texdp3 指令會執行三個元件的點乘積，並將其複製到所有四個色頻。

t (m) <sub>RGBA</sub> = TextureCoordinates (階段 m) <sub>UVW</sub> \* t (x) <sub>RGB</sub>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




