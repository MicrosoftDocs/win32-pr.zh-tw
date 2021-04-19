---
title: IDWriteTextLayout GetOverhangMetrics 方法
description: 傳回配置的 Dip) 中的 overhangs (，以及其中包含的所有物件，包括文字字元和内嵌物件。
ms.assetid: 4b23f6c5-cacc-41e2-8934-6f95208b999a
keywords:
- GetOverhangMetrics 方法直接寫入
- GetOverhangMetrics 方法 Direct Write，IDWriteTextLayout 介面
- IDWriteTextLayout 介面 Direct Write，GetOverhangMetrics 方法
topic_type:
- apiref
api_name:
- IDWriteTextLayout.GetOverhangMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d8a015998f0a673a310319f93d8f4892dd4b1c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977719"
---
# <a name="idwritetextlayoutgetoverhangmetrics-method"></a>IDWriteTextLayout：： GetOverhangMetrics 方法

傳回配置的 Dip) 中的 overhangs (，以及其中包含的所有物件，包括文字字元和内嵌物件。

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

越過可見範圍 (在版面配置之外的 Dip) 中。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

底線和 strikethroughs 不會對黑色方塊的決定造成影響，因為轉譯器實際上會繪製這些轉譯器，而這些轉譯器實際上是以各種不同的樣式來繪製它們。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 程式庫<br/> | <dl> <dt>Dwrite .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

