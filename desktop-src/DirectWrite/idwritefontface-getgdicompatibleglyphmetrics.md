---
title: IDWriteFontFace GetGdiCompatibleGlyphMetrics 方法
description: 使用與 GDI 產生的值相容的傳回值，取得字型設計單位中的字元度量。
ms.assetid: 7bda3916-6db3-4f56-b18c-288506c0b646
keywords:
- GetGdiCompatibleGlyphMetrics 方法直接寫入
- GetGdiCompatibleGlyphMetrics 方法 Direct Write，IDWriteFontFace 介面
- IDWriteFontFace 介面 Direct Write，GetGdiCompatibleGlyphMetrics 方法
topic_type:
- apiref
api_name:
- IDWriteFontFace.GetGdiCompatibleGlyphMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a949edbdad2f25d748e5af64ebe408c79c7372b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999371"
---
# <a name="idwritefontfacegetgdicompatibleglyphmetrics-method"></a>IDWriteFontFace：： GetGdiCompatibleGlyphMetrics 方法

使用與 GDI 產生的值相容的傳回值，取得字型設計單位中的字元度量。

## <a name="syntax"></a>語法


```C++
virtual HRESULT GetGdiCompatibleGlyphMetrics(
                       FLOAT                emSize,
                       FLOAT                pixelsPerDip,
  [in, optional] const DWRITE_MATRIX        *transform,
                       BOOL                 useGdiNatural,
  [in]           const UINT16               *glyphIndices,
                       UINT32               glyphCount,
  [out]                DWRITE_GLYPH_METRICS *glyphMetrics,
                       BOOL                 isSideways = FALSE
) = 0;
```



## <a name="parameters"></a>參數

<dl> <dt>

*emSize* 
</dt> <dd>

類型： **FLOAT**

以 DIP 單位表示的字型邏輯大小。

</dd> <dt>

*pixelsPerDip* 
</dt> <dd>

類型： **FLOAT**

每個 DIP 的實體圖元數目。

</dd> <dt>

*轉換* \[在中，選擇性\]
</dt> <dd>

Type： **Const [**DWRITE \_ 矩陣**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***

套用至字型及其位置的選擇性轉換。 此轉換會在字型大小和 *pixelsPerDip* 所指定的縮放比例之後套用。

</dd> <dt>

*useGdiNatural* 
</dt> <dd>

類型： **BOOL**

當設定為 **FALSE** 時，計量與 GDI 別名文字的計量相同。 當設定為 **TRUE** 時，計量會與使用以 **CLEARTYPE \_ 自然 \_ 品質** 建立之字型所測量的文字計量相同。

</dd> <dt>

*glyphIndices* \[在\]
</dt> <dd>

類型： **CONST UINT16 \***

要計算度量的圖像索引陣列。

</dd> <dt>

*glyphCount* 
</dt> <dd>

類型： **UINT32**

*GlyphIndices* 陣列中的元素數目。

</dd> <dt>

*glyphMetrics* \[擴展\]
</dt> <dd>

類型： **[ **DWRITE \_ 圖像 \_ 度量**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics)\***

這個函式所填滿的 [**DWRITE 圖像 \_ \_ 度量**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) 結構陣列。 計量是以字型設計單位表示。

</dd> <dt>

*isSideways* 
</dt> <dd>

類型： **BOOL**

布林值，指出是否在側邊執行中使用字型。 如果字型有傾斜的模擬，這可能會影響圖像度量，因為側向傾斜模擬與非側面傾斜模擬不同。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

標準 **HRESULT** 錯誤碼。 如果任何輸入圖像索引是在目前字型臉部的有效圖像索引範圍之外，則會傳回 **E \_ INVALIDARG** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 程式庫<br/> | <dl> <dt>Dwrite .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 

