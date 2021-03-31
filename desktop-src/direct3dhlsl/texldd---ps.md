---
title: texldd-ps
description: 使用額外的漸層輸入來取樣材質。
ms.assetid: 6d6b3180-d82e-4be4-929b-e5a6431bec38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 72f3c4aaf9ac7e6beaad1343c024aa28bd2a85ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375368"
---
# <a name="texldd---ps"></a>texldd-ps

使用額外的漸層輸入來取樣材質。

## <a name="syntax"></a>Syntax



| texldd、dst、src0、src1、src2 收取、src3 |
|-------------------------------------|



 

其中：

-   dst 是目的地註冊。
-   src0 是一種來源暫存器，可提供紋理範例的材質座標。 請參閱 [材質座標註冊](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)。
-   src1 會識別來源取樣器 (s \#) ，其中 \# 指定要取樣的材質取樣器數目。 取樣器已將材質與 [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) 列舉所定義的材質和控制項狀態相關聯 (例如。 D3DSAMP \_ MINFILTER) 。
-   src2 收取是指定 x 漸層的輸入來源暫存器。
-   src3 是指定 y 漸層的輸入來源暫存器。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldd                |      |      |      |      |      | X \* | x     | x    | x     |



 

\* 只有 ps 2 a 才支援此 \_ 指令 \_ 。 Ps 2 b 不支援此 \_ 功能 \_ 。 如需設定檔的詳細資訊，請參閱 [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)。

此指示會使用 src0、src1 所指定的取樣器和漸層 DSX 和 DSY 的材質座標來取樣材質。 X 和 y 漸層值是用來為取樣選取適當的紋理 mipmap 層級。

所有來源都支援任意 swizzles。

所有寫入遮罩在目的地都有效。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 