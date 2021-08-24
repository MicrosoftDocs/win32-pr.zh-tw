---
title: def-ps
description: 定義圖元著色器浮點數常數。
ms.assetid: 679b3074-73f3-48de-8c7a-f43bff76b25a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce5f842f44e915d3f3240618261b501f2240c3636227f930538e1bbcbe0d9367
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726558"
---
# <a name="def---ps"></a>def-ps

定義圖元著色器浮點數常數。

## <a name="syntax"></a>Syntax



| def dst、fVvalue1、fValue2、fValue3、fValue4 |
|----------------------------------------------|



 

其中：

-   dst 是目的地註冊。
-   fValue1 至 fValue4 是浮點值。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| def                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

有兩種方式可設定圖元著色器中的浮點數常數。

1.  您可以使用 def，直接在著色器內定義常數。
2.  使用 API 來設定具有 [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)的常數。

def 定義了著色器常數，其值會在著色器設定為裝置時載入。 這些都稱為立即常數。 立即的常數優先于 API 方法所設定的常數。

-   必須出現在著色器中的第一個算術或定址指令之前。
-   可以混合使用 [ (的 sm2、sm3 ps asm) ](dcl---ps.md) 指示 (這是位於著色器) 開頭的另一種指令類型。
-   dst 註冊必須是 [常數註冊](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)。
-   寫入遮罩必須是 full (預設) 。
-   如果在著色器中多次定義 [常數](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) 暫存器，則會保存最後一個暫存器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 