---
description: 從存放區刪除 CTL 之前，由 CertDeleteCTLFromStore 呼叫。
ms.assetid: 6cda772f-7e94-414d-99fc-a90451ac0ccf
title: CertStoreProvDeleteCTL 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvDeleteCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: abeea0fdc3b6d77974b2c057d0e2ea98fe11e63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848908"
---
# <a name="certstoreprovdeletectl-callback-function"></a>CertStoreProvDeleteCTL 回呼函式

從存放區刪除 CTL 之前， [**CertDeleteCTLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore)會呼叫 **CertStoreProvDeleteCTL** 回呼函數。 此函數會決定是否可刪除 CTL。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI CertStoreProvDeleteCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
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

[**CTL \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)結構的指標。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

任何需要的旗標值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果可以從存放區刪除 CTL， **則傳回 TRUE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |



 

 
