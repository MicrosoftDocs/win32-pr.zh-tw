---
description: 將 IMECOLORSTY 結構轉換成 COLORREF 結構。
ms.assetid: f7a3eab0-16ca-4c4e-9eda-bead8d1a91b8
title: RGBFromIMEColorStyle 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RGBFromIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: d568cc33ab2ab19ae9bbe516386b8bb5f5cf909563883ebcc90ef4593cc2f14a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119385708"
---
# <a name="rgbfromimecolorstyle-function"></a>RGBFromIMEColorStyle 函式

將 **IMECOLORSTY** 結構轉換成 [**COLORREF**](../gdi/colorref.md) 結構。

## <a name="syntax"></a>語法


```C++
COLORREF RGBFromIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pcolorstyle* \[在\]
</dt> <dd>

從 [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md)或 [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md)函數傳回的 **IMECOLORSTY** 結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 [**COLORREF**](../gdi/colorref.md) 結構。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COLORREF**](../gdi/colorref.md)
</dt> <dt>

[**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md)
</dt> <dt>

[**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
