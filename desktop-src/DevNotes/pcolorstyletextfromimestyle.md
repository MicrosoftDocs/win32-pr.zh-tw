---
description: 抓取指定樣式的文字色彩樣式。
ms.assetid: 242c37af-5b39-4b18-9c8f-4e692f41c497
title: PColorStyleTextFromIMEStyle 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PColorStyleTextFromIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 58fb2c2830f016080ac27c48b188bbd1948406a6cb7516b3279c411c87d9c155
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955717"
---
# <a name="pcolorstyletextfromimestyle-function"></a>PColorStyleTextFromIMEStyle 函式

抓取指定樣式的文字色彩樣式。

## <a name="syntax"></a>語法


```C++
const IMECOLORSTY* __cdecl PColorStyleTextFromIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pimestyle* \[在\]
</dt> <dd>

從 [**PIMEStyleFromAttr**](pimestylefromattr.md)函數傳回的 **IMESTYLE** 結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

**IMECOLORSTY** 結構的指標，代表文字色彩樣式。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

**IMECOLORSTY** 結構的定義如下：

``` syntax
typedef struct {
    UINT colorId;
    union {
        COLORREF    rgb;
        UINT        colorWin;
        UINT        colorSpec;
        UINT        colorFund;
    };
} IMECOLORSTY;
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PIMEStyleFromAttr**](pimestylefromattr.md)
</dt> </dl>

 

 
