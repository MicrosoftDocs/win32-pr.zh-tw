---
title: def-vs
description: 定義頂點著色器常數。
ms.assetid: 13274e16-990f-4de8-9c99-6c268c7c06ef
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3e5e3d5cbeb4d60f7beffd70c30ba0775863a9782cfb365a4d40bdf5552a186f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855348"
---
# <a name="def---vs"></a>def-vs

定義頂點著色器常數。

## <a name="syntax"></a>Syntax



| def dst、float1、float2、float3、float4 |
|-----------------------------------------|



 

其中

-   dst 是目的地註冊。
-   float1、float2、float3、float4 是四個浮點數。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| def                    | x    | x    | x    | x     | x    | x     |



 

Def 指令會定義著色器常數，其值會在著色器設定為裝置時載入。 這些都稱為立即常數。 立即的常數優先于 API 方法 SetVertexShaderConstantF 所設定的常數。

有兩種方式可以設定著色器中的常數。

1.  使用 def-vs，直接在著色器內定義常數。

    def-vs 只能定義浮點數常數。

2.  使用 API 方法來設定常數。
    -   使用 [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf) 設定浮點數常數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[defi-vs](defi---vs.md)
</dt> <dt>

[defb-vs](defb---vs.md)
</dt> </dl>

 

 