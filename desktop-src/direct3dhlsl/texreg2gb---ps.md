---
title: texreg2gb-ps
description: 將來源註冊的綠色和藍色色彩元件解讀為材質位址資料，以在對應至目的地暫存器編號的階段取樣材質。
ms.assetid: 81d3fb3e-ef53-4d25-b65d-c4c9fea0c74c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb18a2a79132a08e2659c6df426299ce996beba79566af277500ab9eb0a885f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118505746"
---
# <a name="texreg2gb---ps"></a>texreg2gb-ps

將來源註冊的綠色和藍色色彩元件解讀為材質位址資料，以在對應至目的地暫存器編號的階段取樣材質。

## <a name="syntax"></a>Syntax



| texreg2gb dst、src |
|--------------------|



 

其中

-   dst 是目的地註冊。
-   src 是來源暫存器。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texreg2gb             |      | x    | x    |      |      |      |       |      |       |



 

此指示適用于色彩空間重新對應作業。

以下是指示的順序範例。

<dl> tex t (n)   
texreg2gb t (m) ，t (n) ，其中 m > n  
第一個指令會將材質色彩載入 (RGBA)   
進入 register tn  
tex tn  
第二個指令會重新對應色彩  
t (m) <sub>rgba</sub> = TextureSample (階段 m) <sub>RGBA</sub> 使用 t (n) <sub>GB</sub> 作為座標
</dl>

\_bx2 不能用於 [texreg2ar ps](texreg2ar---ps.md) 或 texreg2gb 指令的 src 暫存器。

針對此指示，來源登錄必須使用未簽署的資料。 在來源註冊中使用已簽署或混合的資料將會產生未定義的結果。 如需詳細資訊，請參閱 [D3DFORMAT](/windows/desktop/direct3d9/d3dformat)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 