---
description: 抓取可用的 DDE 共用清單。
ms.assetid: ce5aeddd-d9d1-40a2-a807-1a9c9f98f171
title: 'NDdeShareEnum 函式 (Nddeapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareEnum
- NDdeShareEnumA
- NDdeShareEnumW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 8bfa4884b88e72cb9a3b64bebf58af53cdc1047e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997855"
---
# <a name="nddeshareenum-function"></a>NDdeShareEnum 函式

\[不再支援網路 DDE。 Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]

抓取可用的 DDE 共用清單。

## <a name="syntax"></a>語法


```C++
UINT NDdeShareEnum(
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

接收 DDE 共用清單的緩衝區指標。 DDE 共用清單會儲存為以 null 分隔的字串序列，結尾為雙 null 字元。 此參數可以是 **Null**。 如果 *lpBuffer* 為 **Null**，則 DSDM 會傳回在 *lpcbTotalAvailable* 參數中保存共用清單所需的緩衝區大小。

</dd> <dt>

*cBufSize* \[在\]
</dt> <dd>

*LpBuffer* 緩衝區的大小（以位元組為單位）。 如果 *lpBuffer* 為 **Null**，則此參數必須為零。

</dd> <dt>

*lpnEntriesRead* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收正在列舉的共用總數。 此參數不可以是 **Null**。

</dd> <dt>

*lpcbTotalAvailable* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收緩衝區中用來儲存 DDE 共用清單的總位元組數。 此參數不可以是 **Null**。

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
| Unicode 與 ANSI 名稱<br/>   | **NDdeShareEnumW** (Unicode) 和 **NDdeShareEnumA** (ANSI) <br/>                  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網路動態資料交換總覽](network-dynamic-data-exchange.md)
</dt> <dt>

[網路 DDE 函數](network-dde-functions.md)
</dt> </dl>

 

 




