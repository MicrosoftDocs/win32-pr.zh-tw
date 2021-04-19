---
description: 列舉或尋找符合指定準則之外部存放區中的第一個或下一個 CTL。
ms.assetid: 0b465e6e-fb5c-4621-a968-c2cdcab0ea15
title: CertStoreProvFindCTL 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 9454f918c9cbc5b6f90642d46fbb33573b70457f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980579"
---
# <a name="certstoreprovfindctl-callback-function"></a>CertStoreProvFindCTL 回呼函式

**CertStoreProvFindCTL** 回呼函式會在 [*外部存放區*](../secgloss/e-gly.md)中列舉或尋找符合指定準則的第一個或下一個 [*CTL*](../secgloss/c-gly.md) 。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI CertStoreProvFindCTL(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCTL_CONTEXT               pPrevCtlContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCTL_CONTEXT               *ppProvCtlContext
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

[**證書 \_ 存儲 \_ >prov \_ 尋找 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)結構的指標，其中包含傳遞至 [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)的所有參數。 。

</dd> <dt>

*pPrevCtlCoNtext* \[在\]
</dt> <dd>

找到最後一個 CTL 的 [**ctl \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) 結構指標。 第一次呼叫函式時，此參數應該設定為 **Null**。 在後續的呼叫中，它應該設定為最後一次呼叫時，在 *ppProvCTLCoNtext* 參數中傳回的指標。 在這個參數中傳遞的非 **Null** 指標是由回呼函數釋放。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

任何需要的旗標值。

</dd> <dt>

*ppvStoreProvFindInfo* \[in、out\]
</dt> <dd>

指向緩衝區指標的指標，以傳回存放區提供者資訊。 （選擇性）回呼可以傳回這個參數中內部尋找資訊的指標。 在第一次呼叫之後，這個參數會設定為先前呼叫函數所傳回的指標。

</dd> <dt>

*ppProvCtlCoNtext* \[擴展\]
</dt> <dd>

在成功尋找時，會在此參數中傳回所找到之 CTL 的指標。

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

[**證書 \_ 存儲 \_ >PROV \_ 尋找 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)
</dt> <dt>

[**CTL \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
