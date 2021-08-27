---
title: IDWriteFactory2 CreateGlyphRunAnalysis 方法
description: 建立圖像執行分析物件，此物件會封裝用來呈現圖像執行的資訊。
ms.assetid: 13cecfbf-8bb6-88a2-c8b2-3243f6cb92fd
keywords:
- CreateGlyphRunAnalysis 方法直接寫入
- CreateGlyphRunAnalysis 方法 Direct Write，IDWriteFactory2 介面
- IDWriteFactory2 介面 Direct Write，CreateGlyphRunAnalysis 方法
topic_type:
- apiref
api_name:
- IDWriteFactory2.CreateGlyphRunAnalysis
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4ea5c2dc4cb97b1b9ba02e786efc20a4e2a44990b9a1d28b862aeab254079a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048828"
---
# <a name="idwritefactory2createglyphrunanalysis-method"></a>IDWriteFactory2：： CreateGlyphRunAnalysis 方法

建立圖像執行分析物件，此物件會封裝用來呈現圖像執行的資訊。

## <a name="syntax"></a>語法


```C++
virtual HRESULT CreateGlyphRunAnalysis(
  [in]           const DWRITE_GLYPH_RUN           *glyphRun,
  [in, optional] const DWRITE_MATRIX              *transform,
                       DWRITE_RENDERING_MODE      renderingMode,
                       DWRITE_MEASURING_MODE      measuringMode,
                       DWRITE_GRID_FIT_MODE       gridFitMode,
                       DWRITE_TEXT_ANTIALIAS_MODE antialiasMode,
                       FLOAT                      baselineOriginX,
                       FLOAT                      baselineOriginY,
  [out]                IDWriteGlyphRunAnalysis    **glyphRunAnalysis
) = 0;
```



## <a name="parameters"></a>參數

<dl> <dt>

*glyphRun* \[在\]
</dt> <dd>

Type： **Const [**DWRITE \_ 圖像 \_ 執行**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) \***

結構，指定圖像執行的屬性。

</dd> <dt>

*轉換* \[在中，選擇性\]
</dt> <dd>

Type： **Const [**DWRITE \_ 矩陣**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***

套用至字型及其位置的選擇性轉換。 這項轉換會在 emSize 和 pixelsPerDip 所指定的縮放比例之後套用。

</dd> <dt>

*renderingMode* 
</dt> <dd>

類型： **DWRITE \_ 轉譯 \_ 模式**

指定轉譯模式，它必須是其中一個光柵轉譯模式 (也就是，不是預設值，也不是外框) 。

</dd> <dt>

*measuringMode* 
</dt> <dd>

類型： **[ **DWRITE \_ 測量 \_ 模式**](/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode)**

指定量值的方法。

</dd> <dt>

*gridFitMode* 
</dt> <dd>

類型： **[ **DWRITE \_ 格線 \_ 擬合 \_ 模式**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**

如何將貼齊格線圖像大綱。 這必須為非預設值。

</dd> <dt>

*antialiasMode* 
</dt> <dd>

類型： **[ **DWRITE \_ 文字 \_ 消除鋸齒 \_ 模式**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode)**

指定消除鋸齒模式。

</dd> <dt>

*baselineOriginX* 
</dt> <dd>

類型： **FLOAT**

基準原點的水準位置（Dip）。

</dd> <dt>

*baselineOriginY* 
</dt> <dd>

類型： **FLOAT**

基準原點的垂直位置（Dip）。

</dd> <dt>

*glyphRunAnalysis* \[擴展\]
</dt> <dd>

類型： **[ **IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis)\*\***

接收新建立之物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[桌面應用程式 \| UWP 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows Server 2012R2 \[ desktop apps \| UWP 應用程式\]<br/>                          |
| 支援的最小電話<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]<br/> |
| 程式庫<br/>                  | <dl> <dt>Dwrite .lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDWriteFactory2**](idwritefactory2.md)
</dt> </dl>

 

