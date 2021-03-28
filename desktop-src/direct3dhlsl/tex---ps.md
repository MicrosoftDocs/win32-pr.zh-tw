---
title: tex-ps
description: 使用色彩資料載入目的地登錄 (RGBA) 從材質取樣。 材質必須系結至特定的材質階段 (n) 使用 SetTexture。 紋理取樣是由 SetSamplerState 控制。
ms.assetid: vs|directx_sdk|~\tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a3070883b167d26cf31f7d7f388f6bd3736a4bde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933394"
---
# <a name="tex---ps"></a>tex-ps

使用色彩資料載入目的地登錄 (RGBA) 從材質取樣。 材質必須系結至特定的材質階段 (n) 使用 [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)。 紋理取樣是由 [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate)控制。

## <a name="syntax"></a>Syntax



| tex dst |
|---------|



 

其中

-   dst 是目的地註冊。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| tex                   | x    | x    | x    |      |      |      |       |      |       |



 

目的地暫存器編號會指定紋理階段號碼。

紋理取樣使用材質座標來查閱（或取樣）位於指定之 (u、v、w、q) 座標的色彩值，同時將材質階段狀態屬性納入考慮。

材質座標資料是從頂點材質座標資料中插入，並且與特定的材質階段相關聯。 預設關聯是紋理階段編號和材質座標宣告順序之間的一對一對應。 這表示，以頂點格式定義的第一組材質座標預設會與材質階段0相關聯。

材質座標可以與使用兩個技術的任何階段相關聯。 使用固定的函式頂點著色器或固定函式管線時，紋理階段狀態旗標 TSS \_ TEXCOORDINDEX 可以在 [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) 中用來將座標關聯至階段。 否則，當使用可程式化頂點著色器時，頂點著色器 oTn 暫存器會輸出材質座標。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 