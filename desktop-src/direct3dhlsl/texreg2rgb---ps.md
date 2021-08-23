---
title: texreg2rgb-ps
description: 將來源暫存器的紅色、綠色和藍色 (RGB) 色彩元件，轉譯為紋理位址資料，以便在對應至目的地暫存器編號的階段取樣材質。 結果會儲存在目的地註冊中。
ms.assetid: 8ec44014-d796-407c-8fe0-036decaf2a3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5c32ee8e6b1560bfcebf6a914a45be2c74b19e94568c9d4e9b24084bf56c3f01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043046"
---
# <a name="texreg2rgb---ps"></a>texreg2rgb-ps

將來源暫存器的紅色、綠色和藍色 (RGB) 色彩元件，轉譯為紋理位址資料，以便在對應至目的地暫存器編號的階段取樣材質。 結果會儲存在目的地註冊中。

## <a name="syntax"></a>Syntax



| texreg2rgb dst、src |
|---------------------|



 

其中

-   dst 是目的地註冊。
-   src 是來源暫存器。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texreg2rgb            |      | x    | x    |      |      |      |       |      |       |



 

此指示適用于色彩空間重新對應作業。 它支援二維 (2D) 和三維 (3D) 座標。 它的使用方式就像是 [texreg2ar-ps](texreg2ar---ps.md) 或 [texreg2gb-ps](texreg2gb---ps.md) ，可重新對應2d 資料。 不過，此指示也支援3D 資料，因此可用於 cube 地圖和3D 音量材質。

以下是指示的順序範例。


```
 
tex t(n)
texreg2rgb t(m), t(n)     where m > n
```



以下是如何完成重新對應的詳細資料。

<dl> 第一個指令會將材質色彩 (RGBA) 載入至 register tn  
tex tn  
第二個指令會重新對應色彩  
t (m) <sub>rgba</sub> = TextureSample (階段 m) <sub>RGBA</sub> 使用 t (n) <sub>RGB</sub> 作為座標
</dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




