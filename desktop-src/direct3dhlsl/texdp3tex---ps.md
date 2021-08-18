---
title: texdp3tex-ps
description: 執行三個元件的點乘積，並使用結果來執行1D 紋理查閱。
ms.assetid: vs|directx_sdk|~\texdp3tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91014b52b04417bbb23e76988beeb0bd4c473bd1e1d116433a8fd1dbf09a47ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118788034"
---
# <a name="texdp3tex---ps"></a>texdp3tex-ps

執行三個元件的點乘積，並使用結果來執行1D 紋理查閱。

## <a name="syntax"></a>Syntax



| texdp3tex dst、src |
|--------------------|



 

其中

-   dst 是目的地註冊。
-   src 是來源暫存器。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texdp3tex             |      | x    | x    |      |      |      |       |      |       |



 

材質暫存器必須使用下列順序。


```
 
tex       t(n)        // Define tn as a standard 3-vector (tn must be 
                      // defined in some way before texdp3tex uses it)
texdp3tex t(m), t(n)  // where m > n                 
                      // Perform a three-component dot product between t(n) and 
                      // the texture coordinate set m. Use the scalar result to
                      // do a 1D texture lookup at texturestage m and place
                      // the result in t(m)
```



以下是如何完成點乘積和紋理查閱的詳細資料。

Texdp3tex 指令會執行三個元件的點乘積。

u ' = TextureCoordinates (階段 m) <sub>UVW</sub> \* t (n) <sub>RGB</sub>

結果是用來執行1D 查閱，以在材質階段 m 進行紋理取樣。

t (m) <sub>rgba</sub> = TextureSample (階段 m) <sub>RGBA</sub> 使用 (u '，0，0) 作為座標

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




