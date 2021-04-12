---
description: 抓取呼叫進程內容中受信任之所有網路 DDE 共用的名稱。
ms.assetid: 8e2323a4-0c27-44e6-9598-08a3c1a88bd3
title: 'NDdeTrustedShareEnum 函式 (Nddeapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeTrustedShareEnum
- NDdeTrustedShareEnumA
- NDdeTrustedShareEnumW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: caa3f7c20b95243e03c0c6025d1ff32d60443ab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320275"
---
# <a name="nddetrustedshareenum-function"></a>NDdeTrustedShareEnum 函式

\[不再支援網路 DDE。 Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]

抓取呼叫進程內容中受信任之所有網路 DDE 共用的名稱。

## <a name="syntax"></a>語法


```C++
UINT NDdeTrustedShareEnum(
  _In_  LPTSTR  lpszServer,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnEntriesRead,
  _Out_ LPDWORD lpcbTotalAvailable
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpszServer* \[在\]
</dt> <dd>

DSDM 所在的伺服器名稱。

</dd> <dt>

*nLevel* \[在\]
</dt> <dd>

保留的。 此參數必須為零。

</dd> <dt>

*lpBuffer* \[擴展\]
</dt> <dd>

接收受信任的 DDE 共用清單的緩衝區指標。 受信任的 DDE 共用清單會以一系列以 null 分隔的字串，以結尾是雙 null 字元結束的順序傳回。 此參數可以是 **Null**。 如果 *lpBuffer* 為 **Null**，則 DSDM 會傳回在 *lpcbTotalAvailable* 欄位中保存共用清單所需的緩衝區大小。

</dd> <dt>

*cBufSize* \[在\]
</dt> <dd>

*LpBuffer* 緩衝區的大小（以位元組為單位）。 如果 *lpBuffer* 為 **Null**，則此參數必須為零。

</dd> <dt>

*lpnEntriesRead* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收所列舉之受信任共用的總計數。 此參數不可以是 **Null**。

</dd> <dt>

*lpcbTotalAvailable* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收儲存受信任的 DDE 共用清單所需的總位元組數。 此參數不可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NDDE \_ NO \_ ERROR。

如果函式失敗，則傳回值會是錯誤碼，您可以藉由呼叫 [**NDdeGetErrorString**](nddegeterrorstring.md)將其轉譯為文字錯誤訊息。 如果 *lpBuffer* 參數為 **Null**，則會傳回 NDDE \_ BUF \_ 太 \_ 小。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Nddeapi。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Nddeapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **NDdeTrustedShareEnumW** (Unicode) 和 **NDdeTrustedShareEnumA** (ANSI) <br/>    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網路動態資料交換總覽](network-dynamic-data-exchange.md)
</dt> <dt>

[網路 DDE 函數](network-dde-functions.md)
</dt> </dl>

 

 




