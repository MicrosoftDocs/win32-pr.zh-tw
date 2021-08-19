---
title: texreg2ar-ps
description: 將來源註冊的 Alpha 和紅色元件以材質位址資料的形式轉譯 (u，v) ，以在對應至目的地暫存器編號的階段取樣紋理。 結果會儲存在目的地註冊中。
ms.assetid: b31a2ee4-f9b9-4aee-b3be-7ccc5b8c6f3e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee9516c43f5e8d774ef496a0e66ae1a8ee839ff3df6f2f5436caaf887f95da54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118283999"
---
# <a name="texreg2ar---ps"></a>texreg2ar-ps

將來源註冊的 Alpha 和紅色元件以材質位址資料的形式轉譯 (u，v) ，以在對應至目的地暫存器編號的階段取樣紋理。 結果會儲存在目的地註冊中。

## <a name="syntax"></a>Syntax



| texreg2ar dst、src |
|--------------------|



 

其中

-   dst 是目的地註冊。
-   src 是來源暫存器。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texreg2ar             | x    | x    | x    |      |      |      |       |      |       |



 

此指示適用于色彩空間重新對應作業。

以下是指示所遵循的順序範例：

<dl> tex t (n)   
texreg2ar t (m) ，t (n) ，其中 m > n  
第一個指令會將材質色彩載入 (RGBA)   
進入 register tn  
tex tn  
第二個指令會重新對應色彩  
t (m) <sub>rgba</sub> = TextureSample (階段 m) <sub>RGBA</sub> 使用 t (n) <sub>AR</sub> 作為座標
</dl>

\_bx2 不能用在 src register for texreg2ar 或 [texreg2gb-ps](texreg2gb---ps.md) 指令。

針對此指示，來源登錄必須使用未簽署的資料。 在來源註冊中使用已簽署或混合的資料將會產生未定義的結果。 如需詳細資訊，請參閱 [D3DFORMAT](/windows/desktop/direct3d9/d3dformat)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 