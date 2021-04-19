---
description: 在 CertStoreProvFindCert 的後續呼叫中，未使用 CertStoreProvFindCert 回呼所傳回的憑證，因而加以釋放時呼叫。
ms.assetid: be882b56-027c-4540-9426-27d3c2b262e9
title: CertStoreProvFreeFindCert 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCert
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 320145ebfe95d1e678193ea1b11e7cb0d5294c69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985015"
---
# <a name="certstoreprovfreefindcert-callback-function"></a>CertStoreProvFreeFindCert 回呼函式

**CertStoreProvFreeFindCert** 回呼函式會在 [**CertStoreProvFindCert**](certstoreprovfindcert.md)回呼所傳回的憑證未使用時呼叫，因此會在後續的 **CertStoreProvFindCert** 呼叫中釋放。 呼叫 CLOSE 回呼之前， [**CertStoreProvFindCert**](certstoreprovfindcert.md) 回呼傳回的所有憑證都必須由提供者使用 **CertStoreProvFindCert** 或 **CertStoreProvFreeFindCert** 來釋放。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI CertStoreProvFreeFindCert(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCERT_CONTEXT pCertContext,
  _In_ void           *pvStoreProvFindInfo,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hStoreProv* \[在\]
</dt> <dd>

**HCERTSTOREPROV** [*憑證存放區*](../secgloss/c-gly.md)的控制碼。

</dd> <dt>

*pCertCoNtext* \[在\]
</dt> <dd>

憑證 [**\_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)的指標。

</dd> <dt>

*pvStoreProvFindInfo* \[在\]
</dt> <dd>

包含尋找資訊之緩衝區的指標。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

任何需要的旗標值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回 **TRUE** ，否則會傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**憑證 \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**CertStoreProvFindCert**](certstoreprovfindcert.md)
</dt> </dl>

 

 
