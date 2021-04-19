---
title: IDWriteInlineObject GetOverhangMetrics 方法
description: IDWriteTextLayout 會呼叫這個回呼函式，以取得内嵌物件的 Dip)  (可見的範圍。 如果是簡單點陣圖，沒有填補且沒有任何懸垂，則所有 overhangs 只會是零。
ms.assetid: b3b3e9f0-ee35-4117-9a62-a975c03b5ca9
keywords:
- GetOverhangMetrics 方法直接寫入
- GetOverhangMetrics 方法 Direct Write，IDWriteInlineObject 介面
- IDWriteInlineObject 介面 Direct Write，GetOverhangMetrics 方法
topic_type:
- apiref
api_name:
- IDWriteInlineObject.GetOverhangMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0960f28394c5b55c3377136451a5c13748edc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990697"
---
# <a name="idwriteinlineobjectgetoverhangmetrics-method"></a>IDWriteInlineObject：： GetOverhangMetrics 方法

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 會呼叫這個回呼函式，以取得内嵌物件的 dip)  (可見的範圍。 如果是簡單點陣圖，沒有填補且沒有任何懸垂，則所有 overhangs 只會是零。

Overhangs 應該會傳回相對於所報告的物件大小 (請參閱 [**DWRITE \_ 內嵌 \_ 物件 \_ 度量**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics)) ，而且不應該調整基準。

## <a name="syntax"></a>語法


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a>參數

<dl> <dt>

*overhangs* \[擴展\]
</dt> <dd>

類型： **[ **DWRITE \_ 懸垂 \_ 計量**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***

超過可見範圍 (在物件外部的 Dip) 中。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 程式庫<br/> | <dl> <dt>Dwrite .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> <dt>

[**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> </dl>

 

