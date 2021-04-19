---
description: 捕獲 DDE 共用資訊。 這通常是為了編輯而完成。
ms.assetid: a2e48a4d-2b72-40a3-b827-474da1db0910
title: 'NDdeShareGetInfo 函式 (Nddeapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareGetInfo
- NDdeShareGetInfoA
- NDdeShareGetInfoW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 72dc9ae12b174555debfa21afac15e5bfbed993e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966663"
---
# <a name="nddesharegetinfo-function"></a>NDdeShareGetInfo 函式

\[不再支援網路 DDE。 Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]

捕獲 DDE 共用資訊。 這通常是為了編輯而完成。

## <a name="syntax"></a>語法


```C++
UINT NDdeShareGetInfo(
  _In_  LPTSTR  lpszServer,
  _In_  LPTSTR  lpszShareName,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnTotalAvailable,
  _In_  LPWORD  lpnItems
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpszServer* \[在\]
</dt> <dd>

DSDM 所在的伺服器名稱。

</dd> <dt>

*lpszShareName* \[在\]
</dt> <dd>

要從 DSDM 中取出其資訊的共用名稱。 此參數不得為 **Null**。

</dd> <dt>

*nLevel* \[在\]
</dt> <dd>

資訊層級。 此參數必須是2。

</dd> <dt>

*lpBuffer* \[擴展\]
</dt> <dd>

緩衝區的指標，此緩衝區會接收其成員所指向的 [**NDDESHAREINFO**](nddeshareinfo-str.md) 結構和相關聯的資料。 此參數可以是 **Null**。 如果 *lpBuffer* 為 **Null**，則 DSDM 會計算儲存所要求之共用資訊所需的位元組數目，並在 *lpnTotalAvailable* 欄位中傳回該值，並將該值與 NDDE \_ BUF \_ 太小的錯誤一起傳回 \_ 。

</dd> <dt>

*cBufSize* \[在\]
</dt> <dd>

*LpBuffer* 緩衝區的大小（以位元組為單位）。 如果 *lpBuffer* 為 **Null**，則 *cBufSize* 應為零。

</dd> <dt>

*lpnTotalAvailable* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收儲存所要求之共用資訊所需的位元組總數。 此參數不可以是 **Null**。

</dd> <dt>

*lpnItems* \[在\]
</dt> <dd>

部分共用資訊抓取的專案選取遮罩指標。

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
| Unicode 與 ANSI 名稱<br/>   | **NDdeShareGetInfoW** (Unicode) 和 **NDdeShareGetInfoA** (ANSI) <br/>            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網路動態資料交換總覽](network-dynamic-data-exchange.md)
</dt> <dt>

[網路 DDE 函數](network-dde-functions.md)
</dt> <dt>

[**NDDESHAREINFO**](nddeshareinfo-str.md)
</dt> <dt>

[**NDdeShareSetInfo**](nddesharesetinfo.md)
</dt> </dl>

 

 




