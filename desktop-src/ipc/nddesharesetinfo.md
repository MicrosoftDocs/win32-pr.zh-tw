---
description: 設定 DDE 共用資訊。 這通常是在編輯之後完成。
ms.assetid: 002c73ce-7b35-4e8e-bb7e-0e1393b97ccc
title: 'NDdeShareSetInfo 函式 (Nddeapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareSetInfo
- NDdeShareSetInfoA
- NDdeShareSetInfoW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: ccfa8cc80f60477e8512ac43f0e93825642dd0603ee398e232bbb67d6979a4c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481698"
---
# <a name="nddesharesetinfo-function"></a>NDdeShareSetInfo 函式

\[不再支援網路 DDE。 Nddeapi.dll 存在於 Windows Vista 中，但所有的函式呼叫會傳回 NDDE \_ 未 \_ 執行。\]

設定 DDE 共用資訊。 這通常是在編輯之後完成。

## <a name="syntax"></a>語法


```C++
UINT NDdeShareSetInfo(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ UINT   nLevel,
  _In_ LPBYTE lpBuffer,
  _In_ DWORD  cBufSize,
  _In_ WORD   sParmNum
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpszServer* \[在\]
</dt> <dd>

要修改其 DSDM 的伺服器名稱。

</dd> <dt>

*lpszShareName* \[在\]
</dt> <dd>

要修改其資訊的共用名稱名稱。 此參數不可以是 **Null**。

</dd> <dt>

*nLevel* \[在\]
</dt> <dd>

資訊層級。 此參數必須是2。

</dd> <dt>

*lpBuffer* \[in\]
</dt> <dd>

[**NDDESHAREINFO**](nddeshareinfo-str.md)結構的指標，指定要儲存在 DSDM 中的 DDE 共用資訊。 目前會修改整個 DDE 共用資訊，也就是說，不會進行部分編輯。 此參數不可以是 **Null**。

</dd> <dt>

*cBufSize* \[在\]
</dt> <dd>

*LpBuffer* 緩衝區的大小（以位元組為單位）。

</dd> <dt>

*sParmNum* \[在\]
</dt> <dd>

要修改的參數索引。 目前的執行不支援部分修改;因此，此參數必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NDDE \_ NO \_ ERROR。

如果函式失敗，則傳回值會是錯誤碼，您可以藉由呼叫 [**NDdeGetErrorString**](nddegeterrorstring.md)將其轉譯為文字錯誤訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Nddeapi。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Nddeapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **NDdeShareSetInfoW** (Unicode) 和 **NDdeShareSetInfoA** (ANSI) <br/>            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網路動態資料交換總覽](network-dynamic-data-exchange.md)
</dt> <dt>

[網路 DDE 函數](network-dde-functions.md)
</dt> <dt>

[**NDDESHAREINFO**](nddeshareinfo-str.md)
</dt> <dt>

[**NDdeShareGetInfo**](nddesharegetinfo.md)
</dt> </dl>

 

 




