---
title: defb-vs
description: 定義布林值常數值，此值應該會在著色器設定為裝置時，隨時載入。
ms.assetid: 1db41115-14aa-462e-a7ee-c0a53fee97d8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e5ace74e275ae63a62306d47d50924e9c4e9a9771027e75659ef72345f69906d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792669"
---
# <a name="defb---vs"></a>defb-vs

定義布林值常數值，此值應該會在著色器設定為裝置時，隨時載入。

## <a name="syntax"></a>Syntax



| defb dest，booleanValue |
|-------------------------|



 

其中

-   dst 是目的地註冊。
-   booleanValue 是布林值，也就是 True 或 False。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| defb                   |      | x    | x    | x     | x    | x     |



 

Defb-vs 指令會定義布林著色器常數，其值會在著色器設定為裝置時載入。 這些都稱為立即常數。 立即的常數優先于 API 方法 SetVertexShaderConstantB 所設定的常數。

有兩種方式可以設定著色器中的布林值常數。

1.  使用 defb-vs，直接在著色器內定義常數。
2.  使用 API 方法來設定常數。
    -   使用 [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb) 設定布林值常數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[def-vs](def---vs.md)
</dt> <dt>

[defi-vs](defi---vs.md)
</dt> </dl>

 

 