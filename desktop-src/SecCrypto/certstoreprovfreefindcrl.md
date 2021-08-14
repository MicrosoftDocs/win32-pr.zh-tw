---
description: 在 CertStoreProvFindCRL 的後續呼叫中，未使用 CertStoreProvFindCRL 回呼所傳回的憑證，因而加以釋放時呼叫。
ms.assetid: e90609f6-63cd-40eb-bd5a-289473daa5bb
title: CertStoreProvFreeFindCRL 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCRL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 1bf7e3b2518789bdf3755cefec0dcc27c88642c376cafca039ce5cc20533a068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769933"
---
# <a name="certstoreprovfreefindcrl-callback-function"></a>CertStoreProvFreeFindCRL 回呼函式

**CertStoreProvFreeFindCRL** 回呼函式會在 [**CertStoreProvFindCRL**](certstoreprovfindcrl.md)回呼所傳回的憑證未使用時呼叫，因此會在後續的 **CertStoreProvFindCRL** 呼叫中釋放。 呼叫 CLOSE 回呼之前， [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) 回呼傳回的所有憑證都必須由提供者使用 **CertStoreProvFindCRL** 或 **CertStoreProvFreeFindCRL** 來釋放。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI CertStoreProvFreeFindCRL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCRL_CONTEXT  pCrlContext,
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

*pCrlCoNtext* \[在\]
</dt> <dd>

[**CRL \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)的指標。

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
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CertStoreProvFindCRL**](certstoreprovfindcrl.md)
</dt> <dt>

[**CRL \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
