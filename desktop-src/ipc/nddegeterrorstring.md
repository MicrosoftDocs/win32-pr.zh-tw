---
description: 將網路 DDE 函數所傳回的錯誤碼轉換成錯誤字串，以說明傳回的錯誤碼。
ms.assetid: 7077e3bc-df6e-401b-9ac7-15144b79af96
title: 'NDdeGetErrorString 函式 (Nddeapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetErrorString
- NDdeGetErrorStringA
- NDdeGetErrorStringW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 8e043c8281d3ad049346ac7ce68991eb6bd08af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026079"
---
# <a name="nddegeterrorstring-function"></a>NDdeGetErrorString 函式

\[不再支援網路 DDE。 Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]

將網路 DDE 函數所傳回的錯誤碼轉換成錯誤字串，以說明傳回的錯誤碼。

## <a name="syntax"></a>語法


```C++
UINT NDdeGetErrorString(
  _In_  UINT   uErrorCode,
  _Out_ LPTSTR lpszErrorString,
  _In_  DWORD  cBufSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*uErrorCode* \[在\]
</dt> <dd>

要轉換成錯誤字串的錯誤碼。

</dd> <dt>

*lpszErrorString* \[擴展\]
</dt> <dd>

接收轉譯的錯誤字串之緩衝區的指標。 此參數不可以是 **Null**。 如果緩衝區不夠大，無法儲存完整的錯誤字串，則會截斷字串。

</dd> <dt>

*cBufSize* \[在\]
</dt> <dd>

接收錯誤字串的緩衝區大小（以 **TCHARs**）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此函式成功，則傳回值為零。

如果函式失敗，則傳回值為非零的錯誤碼。 如果 *lpszErrorString* 緩衝區不夠大，無法接受完整的錯誤字串，而且字串遭到截斷，則函式會傳回值 NDDE \_ 內部 \_ 錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Nddeapi。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Nddeapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **NDdeGetErrorStringW** (Unicode) 和 **NDdeGetErrorStringA** (ANSI) <br/>        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網路動態資料交換總覽](network-dynamic-data-exchange.md)
</dt> <dt>

[網路 DDE 函數](network-dde-functions.md)
</dt> </dl>

 

 




