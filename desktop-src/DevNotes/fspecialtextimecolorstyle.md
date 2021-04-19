---
description: 指定指定的色彩是否為特殊的文字色彩。
ms.assetid: 527806f5-5046-48b0-a8db-86a5b8c0db08
title: FSpecialTextIMEColorStyle 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSpecialTextIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: cfaf83aeb2fcb03ab61c1280ec821174117026fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978655"
---
# <a name="fspecialtextimecolorstyle-function"></a>FSpecialTextIMEColorStyle 函式

指定指定的色彩是否為特殊的文字色彩。

## <a name="syntax"></a>語法


```C++
BOOL __cdecl FSpecialTextIMEColorStyle(
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

當色彩為特殊文字色彩時傳回 **TRUE** 。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md)
</dt> <dt>

[**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
