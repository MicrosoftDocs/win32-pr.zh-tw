---
title: rcp
description: 計算每個元件的快速、近似、每個元件。
ms.assetid: c8d451e4-717e-45b3-a0fe-da55feb8f443
keywords:
- rcp HLSL
topic_type:
- apiref
api_name:
- rcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a857c897def08f31e18ef19466daa2b4584740a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682581"
---
# <a name="rcp"></a>rcp

計算每個元件的快速、近似、每個元件。



| *ret* rcp (*x*)  |
|----------------|



 

## <a name="parameters"></a>參數

<dl> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

\[在 \] 輸入值中。

</dd> </dl>

## <a name="return-value"></a>傳回值

*X* 參數的倒數。

## <a name="type-description"></a>類型描述



| Name  | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md)                      | 大小                           |
|-------|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|--------------------------------|
| *x*   | 純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣** | [**浮點數**](/windows/desktop/WinProg/windows-data-types)或 [**雙精度** 浮點數](/windows/desktop/WinProg/windows-data-types) | 任意                            |
| *Ret* | 與輸入 *x* 相同                                                                                              | [**浮點數**](/windows/desktop/WinProg/windows-data-types)或 [**雙精度** 浮點數](/windows/desktop/WinProg/windows-data-types) | ) 為輸入 *x* 的相同維度 (s |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                | 支援 |
|-----------------------------------------------------------------------------|-----------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型 | 是       |



 

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[內建函式](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 