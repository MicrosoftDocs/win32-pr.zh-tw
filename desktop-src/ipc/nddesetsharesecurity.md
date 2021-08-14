---
description: 設定與 DDE 共用相關聯的安全描述項。
ms.assetid: 8bb8c466-3dd7-49a6-8ba5-632001b8a47f
title: 'NDdeSetShareSecurity 函式 (Nddeapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeSetShareSecurity
- NDdeSetShareSecurityA
- NDdeSetShareSecurityW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 00e6d8c4b235e8f7d02ba22e737fc4de9bf4a739864afb1464e6f84c620faa48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481822"
---
# <a name="nddesetsharesecurity-function"></a>NDdeSetShareSecurity 函式

\[不再支援網路 DDE。 Nddeapi.dll 存在於 Windows Vista 中，但所有的函式呼叫會傳回 NDDE \_ 未 \_ 執行。\]

設定與 DDE 共用相關聯的安全描述項。 這通常是在編輯指派給 DDE 共用的 DACL 之後完成。

## <a name="syntax"></a>語法


```C++
UINT NDdeSetShareSecurity(
  _In_ LPTSTR               lpszServer,
  _In_ LPTSTR               lpszShareName,
  _In_ SECURITY_INFORMATION si,
  _In_ PSECURITY_DESCRIPTOR pSD
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

要修改其安全描述項的共用名稱。 此參數不可以是 **Null**。

</dd> <dt>

*si* \[在\]
</dt> <dd>

[**安全性 \_ 資訊**](/windows/desktop/SecAuthZ/security-information)值，可識別要取出的安全性資訊。

</dd> <dt>

*pSD* \[在\]
</dt> <dd>

[**安全性 \_ 描述**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)元結構的指標，其中包含安全性資訊。 此參數不可以是 **Null** ，而且應指向有效的安全描述項。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NDDE \_ NO \_ ERROR。

如果函式失敗，則傳回值會是錯誤碼，您可以藉由呼叫 [**NDdeGetErrorString**](nddegeterrorstring.md)將其轉譯為文字錯誤訊息。

## <a name="remarks"></a>備註

若要修改與 DSDM 中的 DDE 共用相關聯的 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) ，使用者必須具有適當的許可權; 共用建立者具有此許可權。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Nddeapi。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Nddeapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **NDdeSetShareSecurityW** (Unicode) 和 **NDdeSetShareSecurityA** (ANSI) <br/>    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網路動態資料交換總覽](network-dynamic-data-exchange.md)
</dt> <dt>

[網路 DDE 函數](network-dde-functions.md)
</dt> <dt>

[**安全性 \_ 資訊**](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[**NDdeGetShareSecurity**](nddegetsharesecurity.md)
</dt> </dl>

 

