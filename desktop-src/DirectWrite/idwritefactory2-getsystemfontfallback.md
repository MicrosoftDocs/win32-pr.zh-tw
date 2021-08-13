---
title: IDWriteFactory2 GetSystemFontFallback 方法
description: 從系統字型 fallback 清單建立字型回溯物件。
ms.assetid: 7F2BDB39-2CB4-4DB7-BBBA-74B0C07E7420
keywords:
- GetSystemFontFallback 方法直接寫入
- GetSystemFontFallback 方法 Direct Write，IDWriteFactory2 介面
- IDWriteFactory2 介面 Direct Write，GetSystemFontFallback 方法
topic_type:
- apiref
api_name:
- IDWriteFactory2.GetSystemFontFallback
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4513c8ee7fb4e7a3796ec442d4d36bb663a0c8803bb6276a584edcfda306d588
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329441"
---
# <a name="idwritefactory2getsystemfontfallback-method"></a>IDWriteFactory2：： GetSystemFontFallback 方法

從系統字型 fallback 清單建立字型回溯物件。

## <a name="syntax"></a>語法


```C++
HRESULT GetSystemFontFallback(
  [out] IDWriteFontFallback **fontFallback
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*fontFallback* \[擴展\]
</dt> <dd>

類型： **[ **IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)\*\***

包含新建立之字型回寫物件之指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDWriteFactory2**](idwritefactory2.md)
</dt> </dl>

 

 