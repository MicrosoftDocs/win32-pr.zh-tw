---
description: 抓取 CRL 的指定屬性。
ms.assetid: b02f4f92-952a-4625-a7d4-6e78e542774e
title: CertStoreProvGetCRLProperty 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCRLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 2662c29ede9feec90b10869a4dc21277a8c6bdc6243e60ce894819e4b27dce5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877048"
---
# <a name="certstoreprovgetcrlproperty-callback-function"></a>CertStoreProvGetCRLProperty 回呼函式

**CertStoreProvGetCRLProperty** 回呼函式會捕獲指定的 [*CRL*](../secgloss/c-gly.md)屬性。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI CertStoreProvGetCRLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCRL_CONTEXT  pCrlContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
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

[**CRL \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)結構的指標。

</dd> <dt>

*dwPropId* \[在\]
</dt> <dd>

表示屬性識別碼。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

任何需要的旗標值。

</dd> <dt>

*pvData* \[擴展\]
</dt> <dd>

緩衝區的指標，其中包含要由函式傳回的 [**CRL \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) 結構指標。 在第一次呼叫函式時，可以設定為 **Null** ，以取得 *pcbData* 的值，然後再為緩衝區配置記憶體。

</dd> <dt>

*pcbData* \[in、out\]
</dt> <dd>

**DWORD** 的指標，表示 *pvData* 緩衝區的長度。

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

[**CRL \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
