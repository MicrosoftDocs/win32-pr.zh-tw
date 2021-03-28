---
title: defi-vs
description: 定義整數常數值，此值應該會在著色器設定為裝置時，隨時載入。
ms.assetid: d6067a7d-58fb-4553-a42f-192c29bf78b7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 897a544cc9974b8ffa727f2d39219cfeab82d52a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508060"
---
# <a name="defi---vs"></a>defi-vs

定義整數常數值，此值應該會在著色器設定為裝置時，隨時載入。

## <a name="syntax"></a>Syntax



| defi dst、integerValue0、integerValue1、integerValue2、integerValue3 |
|----------------------------------------------------------------------|



 

-   dst 是目的地註冊。
-   integerValue \# 是常數整數值。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| defi                   |      | x    | x    | x     | x    | x     |



 

Defi 指令會定義整數著色器常數，其值會在著色器設定為裝置時載入。 這些都稱為立即常數。 立即的常數優先于 API 方法 SetVertexShaderConstantI 所設定的常數。

有兩種方式可以設定著色器中的整數常數。

1.  您可以使用 defi 直接定義著色器內的整數常數向量。
2.  使用 API 方法來設定常數。
    -   使用 [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti) 來設定整數常數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[def-vs](def---vs.md)
</dt> <dt>

[defb-vs](defb---vs.md)
</dt> </dl>

 

 