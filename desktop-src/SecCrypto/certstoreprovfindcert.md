---
description: 列舉或尋找符合指定準則之外部存放區中的第一個或下一個憑證。
ms.assetid: 1129a372-4d7c-454e-969b-26a1d6037bc0
title: CertStoreProvFindCert 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCert
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: a50a53e819fcfd12ff490b4e6642536c01d9a49b4e9345e7713bf0eb08a0fac6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770017"
---
# <a name="certstoreprovfindcert-callback-function"></a>CertStoreProvFindCert 回呼函式

**CertStoreProvFindCert** 回呼函式會在 [*外部存放區*](../secgloss/e-gly.md)中列舉或尋找符合指定準則的第一個或下一個憑證。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI CertStoreProvFindCert(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCERT_CONTEXT              pPrevCertContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCERT_CONTEXT              *ppProvCertContext
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hStoreProv* \[在\]
</dt> <dd>

**HCERTSTOREPROV** [*憑證存放區*](../secgloss/c-gly.md)的控制碼。

</dd> <dt>

*pFindInfo* \[在\]
</dt> <dd>

[**證書 \_ 存儲 \_ >prov \_ 尋找 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)結構的指標，其中包含傳遞至 [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)函數的所有參數。

</dd> <dt>

*pPrevCertCoNtext* \[在\]
</dt> <dd>

找到之憑證的 [**憑證 \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) 指標。 第一次呼叫函式時，此參數應該設定為 **Null**。 在後續的呼叫中，它應該設定為最後一次呼叫時，在 *ppProvCertCoNtext* 參數中傳回的指標。 在這個參數中傳遞的非 **Null** 指標是由回呼函數釋放。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

任何需要的旗標值。

</dd> <dt>

*ppvStoreProvFindInfo* \[in、out\]
</dt> <dd>

指向緩衝區指標的指標，以傳回存放區提供者資訊。 （選擇性）回呼可以傳回這個參數中內部尋找資訊的指標。 在第一次呼叫之後，這個參數會設定為先前呼叫函數所傳回的指標。

</dd> <dt>

*ppProvCertCoNtext* \[擴展\]
</dt> <dd>

在成功尋找時，會在此參數中傳回找到之憑證的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回 **TRUE** ，否則會傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**憑證 \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**證書 \_ 存儲 \_ >PROV \_ 尋找 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)
</dt> </dl>

 

 
