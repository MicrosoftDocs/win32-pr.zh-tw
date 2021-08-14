---
description: 顯示允許使用者選取憑證的對話方塊。
ms.assetid: 242c19a7-179b-4fc0-a050-a1b598566a6b
title: CryptUIDlgSelectCertificate 函式
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: fb37eb664841331ce3f37e9ce37ca3ab9e5c0f92c254cff0896c6c682a9f2872
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768161"
---
# <a name="cryptuidlgselectcertificate-function"></a>CryptUIDlgSelectCertificate 函式

**CryptUIDlgSelectCertificate** 函式會顯示可讓使用者選取憑證的對話方塊。

## <a name="syntax"></a>語法


```C++
PCCERT_CONTEXT WINAPI CryptUIDlgSelectCertificate(
  _In_  PCCRYPTUI_SELECTCERTIFICATE_STRUCT pcsc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pcsc* \[在\]
</dt> <dd>

[**CRYPTUI \_ SELECTCERTIFICATE \_ 結構**](cryptui-selectcertificate-struct.md)結構的指標，其中包含要顯示之對話方塊的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

憑證 [**\_ 內容**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) 結構的指標，表示使用者選取的憑證。 當您完成使用此憑證時，您必須將此指標傳遞至 [**CertFreeCertificateCoNtext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) 函式，以遞減憑證內容的參考計數。

如果 *pcsc* 結構的 **dwFlags** 成員未包含 **CRYPTUI \_ SELECTCERT \_ 多重** 選取旗標，則傳回值為 **Null** 表示使用者已關閉對話方塊，而不選取憑證。

如果 *pcsc* 結構的 **DwFlags** 成員包含 **CRYPTUI \_ SELECTCERT \_ 多重** 複選旗標，此函數一律會傳回 **Null**。 選取的憑證將包含在 *pcsc* 的 **hSelectedCertStore** 成員所代表的憑證存放區中。 如果存放區中的憑證數目在呼叫 **CryptUIDlgSelectCertificate** 之前和之後是相同的，使用者會關閉對話方塊，而不選取任何憑證。

## <a name="remarks"></a>備註

如果 [**CRYPTUI \_ SELECTCERTIFICATE \_ 結構**](cryptui-selectcertificate-struct.md)結構的 **dwFlags** 成員設定為 **CRYPTUI \_ SELECTCERT \_ 舊版**，則會顯示舊版對話方塊。 否則，就會顯示目前的憑證選擇對話方塊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows XP \[ desktop 應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                              |
| 結束支援<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                       |
| 程式庫<br/>                  | <dl> <dt>Cryptui .lib</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>Cryptui.dll</dt> </dl>            |
| Unicode 與 ANSI 名稱<br/>   | **CryptUIDlgSelectCertificateW** (Unicode) 和 **CryptUIDlgSelectCertificateA** (ANSI) <br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CRYPTUI \_ SELECTCERTIFICATE \_ 結構**](cryptui-selectcertificate-struct.md)
</dt> </dl>






