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
ms.openlocfilehash: befc031c1be441ad23c7a50563030775b625b81b66a9e1f92df4fb7c641fe73c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993088"
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
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |



 

 
