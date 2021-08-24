---
title: IDWriteFontFace GetGdiCompatibleMetrics 方法
description: 取得字型字型的設計單位和一般度量。 這些計量適用于 fontface 內的所有字元，而且應用程式會使用這些計量來進行版面配置計算。
ms.assetid: 9e132ec0-64cb-4681-b079-02a0047badd5
keywords:
- GetGdiCompatibleMetrics 方法直接寫入
- GetGdiCompatibleMetrics 方法 Direct Write，IDWriteFontFace 介面
- IDWriteFontFace 介面 Direct Write，GetGdiCompatibleMetrics 方法
topic_type:
- apiref
api_name:
- IDWriteFontFace.GetGdiCompatibleMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fce5080edc44501290672bf0db0ebac69ef4856ec0b7163821cf60ac63d384ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290708"
---
# <a name="idwritefontfacegetgdicompatiblemetrics-method"></a>IDWriteFontFace：： GetGdiCompatibleMetrics 方法

取得字型字型的設計單位和一般度量。 這些計量適用于 fontface 內的所有字元，而且應用程式會使用這些計量來進行版面配置計算。

## <a name="syntax"></a>語法


```C++
virtual HRESULT GetGdiCompatibleMetrics(
                       FLOAT               emSize,
                       FLOAT               pixelsPerDip,
  [in, optional] const DWRITE_MATRIX       *transform,
  [out]                DWRITE_FONT_METRICS *fontFaceMetrics
) = 0;
```



## <a name="parameters"></a>參數

<dl> <dt>

*emSize* 
</dt> <dd>

類型： **FLOAT**

以 DIP 單位表示之字型的邏輯大小。

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

*fontFaceMetrics* \[擴展\]
</dt> <dd>

類型： **[ **DWRITE \_ 字型 \_ 計量**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)\***

要填入之 [**DWRITE \_ 字型 \_ 度量**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)S 結構的指標。 此函式所傳回的度量是在字型設計單位中。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

標準 HRESULT 錯誤碼。

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

 

