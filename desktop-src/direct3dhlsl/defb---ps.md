---
title: defb-ps
description: 定義布林值常數值，此值應該會在著色器設定為裝置時載入。
ms.assetid: bb0b87cb-08a4-4790-88da-e398cea62911
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1ad823cd9932e98f919764e57666549189623986eb173ba6b4ef74cdade21f33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855355"
---
# <a name="defb---ps"></a>defb-ps

定義布林值常數值，此值應該會在著色器設定為裝置時載入。

## <a name="syntax"></a>Syntax



| defb dest，booleanValue |
|-------------------------|



 

其中

-   dst 是目的地註冊。
-   booleanValue 是單一布林值，也就是 true 或 false。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| defb                  |      |      |      |      |      | x    | x     | x    | x     |



 

Defb 指令會定義布林著色器常數，其值會在著色器設定為裝置時載入。 這些都稱為立即常數。 立即的常數優先于 API 方法 SetPixelShaderConstantB 所設定的常數。

有兩種方式可以設定著色器中的 booleanconstant。

1.  您可以使用 defb，直接在著色器內定義常數。
2.  使用 API 方法來設定常數。
    -   使用 [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) 設定布林值常數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[def-ps](def---ps.md)
</dt> <dt>

[defi-ps](defi---ps.md)
</dt> </dl>

 

 