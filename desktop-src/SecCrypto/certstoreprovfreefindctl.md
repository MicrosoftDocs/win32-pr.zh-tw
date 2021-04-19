---
description: 在 CertStoreProvFindCTL 的後續呼叫中，未使用 CertStoreProvFindCTL 回呼所傳回的憑證，因而加以釋放時呼叫。
ms.assetid: 04e62a4e-4542-4225-8750-fabbda5adf0d
title: CertStoreProvFreeFindCTL 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: ff0c9c3b7be6b8a4cafd759c3411f5096ee8640b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989358"
---
# <a name="certstoreprovfreefindctl-callback-function"></a>CertStoreProvFreeFindCTL 回呼函式

**CertStoreProvFreeFindCTL** 回呼函式會在 [**CertStoreProvFindCTL**](certstoreprovfindctl.md)回呼所傳回的憑證未使用時呼叫，因此會在後續的 **CertStoreProvFindCTL** 呼叫中釋放。 呼叫 CLOSE 回呼之前， [**CertStoreProvFindCTL**](certstoreprovfindctl.md) 回呼傳回的所有憑證都必須由提供者使用 **CertStoreProvFindCTL** 或 **CertStoreProvFreeFindCTL** 來釋放。

## <a name="syntax"></a>語法


```C++
BOOL CertStoreProvFreeFindCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
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

*pCtlCoNtext* \[在\]
</dt> <dd>

[**CTL \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)結構的指標。

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

[**CertStoreProvFindCTL**](certstoreprovfindctl.md)
</dt> <dt>

[**CTL \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
