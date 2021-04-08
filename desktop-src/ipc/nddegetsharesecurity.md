---
description: 抓取與 DDE 共用相關聯的安全描述項。 這通常是用來進行編輯。
ms.assetid: 7d3cc965-45ee-40ce-a462-568200592345
title: 'NDdeGetShareSecurity 函式 (Nddeapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetShareSecurity
- NDdeGetShareSecurityA
- NDdeGetShareSecurityW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: dae1352d9e7c45f9ce301dd30d4e7f73d508498c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852236"
---
# <a name="nddegetsharesecurity-function"></a>NDdeGetShareSecurity 函式

\[不再支援網路 DDE。 Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]

抓取與 DDE 共用相關聯的安全描述項。 這通常是用來進行編輯。

## <a name="syntax"></a>語法


```C++
UINT NDdeGetShareSecurity(
  _In_  LPTSTR               lpszServer,
  _In_  LPTSTR               lpszShareName,
  _In_  SECURITY_INFORMATION si,
  _Out_ PSECURITY_DESCRIPTOR pSD,
  _In_  DWORD                cbSD,
  _Out_ LPDWORD              lpcbsdRequired
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

要從 DSDM 中取出其安全描述項的共用名稱。 此參數不可以是 **Null**。

</dd> <dt>

*si* \[在\]
</dt> <dd>

[**安全性 \_ 資訊**](/windows/desktop/SecAuthZ/security-information)值，指定要從與共享相關聯的安全描述項中取出的安全性資訊。

</dd> <dt>

*pSD* \[擴展\]
</dt> <dd>

[**安全性 \_ 描述**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)元結構的指標，該結構會接收自我相關的安全描述項。 此參數可以是 **Null**。 如果此參數為 **Null**，則 DSDM 會判斷要求的安全性資訊大小，並傳回 *lpcbsdRequired* 參數中所需的位元組數目，以及 NDDE \_ BUF \_ 太小的 \_ 錯誤碼。

</dd> <dt>

*cbSD* \[在\]
</dt> <dd>

*PSD* 緩衝區的大小。 如果 *pSD* 為 **Null**，則此參數必須為零。

</dd> <dt>

*lpcbsdRequired* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收所抓取之安全描述項的實際大小。 此參數不可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NDDE \_ NO \_ ERROR。

如果函式失敗，則傳回值會是錯誤碼，您可以藉由呼叫 [**NDdeGetErrorString**](nddegeterrorstring.md)將其轉譯為文字錯誤訊息。 如果 *pSD* 參數為 **Null**，則會傳回 NDDE \_ BUF \_ 太 \_ 小。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Nddeapi。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Nddeapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **NDdeGetShareSecurityW** (Unicode) 和 **NDdeGetShareSecurityA** (ANSI) <br/>    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網路動態資料交換總覽](network-dynamic-data-exchange.md)
</dt> <dt>

[網路 DDE 函數](network-dde-functions.md)
</dt> <dt>

[**安全性 \_ 資訊**](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[**NDdeSetShareSecurity**](nddesetsharesecurity.md)
</dt> </dl>

 

