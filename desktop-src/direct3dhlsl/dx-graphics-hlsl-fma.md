---
title: 'fma (Corecrt \_ math .h) '
description: 傳回 \ b + c 的雙精確度融合乘積。
ms.assetid: C4EF2552-7388-4CA8-B78F-6B2D4C8FC5F6
keywords:
- fma HLSL
topic_type:
- apiref
api_name:
- fma
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2b9a6932a1b0f0f8f1f7bc674920162def49e556c8d5b757547d4837caa60b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120202"
---
# <a name="fma"></a>fma

傳回 b + c 的雙精確度融合乘積 \* 。



| *ret* fma (雙 *a*、 *b*、 *c*) ; |
|----------------------------------|



 

## <a name="parameters"></a>參數

<dl> <dt>

<span id="a"></span><span id="A"></span>*的*
</dt> <dd>

\[在 \] 融合的乘法-加法中的第一個值。

</dd> <dt>

<span id="b"></span><span id="B"></span>*B*
</dt> <dd>

\[在 \] 融合的乘法-加法中的第二個值。

</dd> <dt>

<span id="c"></span><span id="C"></span>*C*
</dt> <dd>

\[在 \] 融合乘積的第三個值中。

</dd> </dl>

## <a name="return-value"></a>傳回值

雙精確度融合的數位加上 \* *b*  +  *c* 的參數。 傳回的值必須精確為0.5 的精確度 (ULP) 的最小有效位數。

## <a name="remarks"></a>備註

**Fma** 內建函式必須支援 Nan、Inf 和 Denorms。

若要在您的著色器程式碼中使用 **fma** 內建，請使用 [**D3D11 \_ 功能 \_ D3D11 \_ 選項**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature)來呼叫 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport)方法，以確認 Direct3D 裝置支援 [**ExtendedDoublesShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)功能選項。 **Fma** 內建需要 WDDM 1.2 顯示驅動程式，而所有 WDDM 1.2 顯示器驅動程式都必須支援 **fma**。 如果您的應用程式使用 [功能層級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11.0 或11.1 建立轉譯裝置，而且編譯目標為著色器模型5或更新版本，則 HLSL 原始程式碼可以使用 **fma** 內建。

### <a name="type-description"></a>類型描述



| 名稱  | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md) | 大小                         |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| *的*   | 純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣** | [**雙**](/windows/desktop/WinProg/windows-data-types)                       | 任意                          |
| *b*   | 與輸入 *a* 相同                                                                                              | [**雙**](/windows/desktop/WinProg/windows-data-types)                       | 與輸入 a 相同 *的* 維度 |
| *c*   | 與輸入 *a* 相同                                                                                              | [**雙**](/windows/desktop/WinProg/windows-data-types)                       | 與輸入 a 相同 *的* 維度 |
| *Ret* | 與輸入 *a* 相同                                                                                              | [**雙**](/windows/desktop/WinProg/windows-data-types)                       | 與輸入 a 相同 *的* 維度 |



 

### <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                | 支援 |
|-------------------------------------------------------------|-----------|
| [著色器模型5或更新版本](d3d11-graphics-reference-sm5.md) | 是       |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[桌面應用程式 \| UWP 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows Server 2012 \[桌面應用程式 \| UWP 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Corecrt \_ math。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[內建函式](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

