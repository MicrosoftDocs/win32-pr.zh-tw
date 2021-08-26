---
description: 從使用者認證取得憑證。
ms.assetid: 3C79D049-89DC-4AF5-8C0A-5B7EBBBD69D3
title: 'GetCertificateFromCred 函式 (Lsaidprov) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificateFromCred
api_type:
- HeaderDef
api_location:
- Lsaidprov.h
ms.openlocfilehash: 3660fd4cfb8baa3e025789a2cde9dc04dd7e1e1678b0516a56562f1ea5be43dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994479"
---
# <a name="getcertificatefromcred-function"></a>GetCertificateFromCred 函式

從使用者認證取得憑證。

## <a name="syntax"></a>語法


```C++
NTSTATUS GetCertificateFromCred(
  _In_  PVOID  ProviderHandle,
  _In_  HANDLE ClientToken,
  _In_  PVOID  SuppliedCred,
  _In_  ULONG  SuppliedCredSize,
  _Out_ PVOID  *CertContext
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ProviderHandle* \[在\]
</dt> <dd>

身分識別提供者控制碼。

</dd> <dt>

*ClientToken* \[在\]
</dt> <dd>

正在抓取憑證之呼叫者的 Token。

</dd> <dt>

*SuppliedCred* \[在\]
</dt> <dd>

SECPKG 所提供之 [**\_ \_ 認證**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) 結構的指標，其中包含要求其憑證的線上識別碼認證。 身分識別提供者必須驗證輸入資料，就像是來自不受信任的來源一樣。

</dd> <dt>

*SuppliedCredSize* \[在\]
</dt> <dd>

*SuppliedCred* 緩衝區的大小（以位元組為單位）。

</dd> <dt>

*CertCoNtext* \[擴展\]
</dt> <dd>

如果函式成功，這個參數會是所傳回 CCERT \_ 內容指標的指標。 當您完成使用憑證內容之後，請呼叫 [**CertFreeCertificateCoNtext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) 函式來釋放它。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，函數會傳回狀態 \_ SUCCESS。

如果函式失敗，函式可能會傳回下列其中一個 NTSTATUS 錯誤碼。



| 傳回值                                                                                            | 描述                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>\_不 \_ 支援的狀態</dt> </dl>       | 身分識別提供者無法辨識所提供認證的認證類型。 LSA 將會嘗試下一個身分識別提供者。<br/>                                           |
| <dl> <dt>狀態 \_ 登入 \_ 失敗</dt> </dl>       | 認證不正確。<br/>                                                                                                                                                |
| <dl> <dt>狀態 \_ 不正確 \_ 參數</dt> </dl>   | 參數無效。 認證的格式不正確，而不是定義的 [**SECPKG 提供的 \_ \_ 認證**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) 結構。<br/> |
| <dl> <dt>無法連線到狀態 \_ 網路 \_</dt> </dl> | 身分識別提供者無法連絡雲端以取得憑證。<br/>                                                                                                   |
| <dl> <dt>狀態 \_ 密碼已 \_ 過期</dt> </dl>    | 帳戶密碼已過期。<br/>                                                                                                                                           |
| <dl> <dt>狀態 \_ 帳戶已 \_ 鎖定 \_</dt> </dl> | 帳戶已被鎖定。 <br/>                                                                                                                                           |
| <dl> <dt>其他</dt> </dl>                       | 其他提供者特定的錯誤碼。 <br/>                                                                                                                                       |



 

## <a name="remarks"></a>備註

從雲端提取憑證之前，身分識別提供者應該在使用者的「我的」憑證存放區中檢查此使用者是否有有效的憑證。 如果有有效的憑證，則提供者應該傳回此憑證，以避免不必要的網路流量。

身分識別提供者也可以在本機快取憑證，只要該憑證受到目前使用者的保護。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Lsaidprov。h</dt> </dl> |



 

