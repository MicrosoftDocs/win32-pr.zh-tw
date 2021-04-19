---
description: 抓取憑證信任清單 (CTL) 的指定屬性。
ms.assetid: 65309715-65b4-4608-960d-3404e68800a2
title: CertStoreProvGetCTLProperty 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCTLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: e30a9e735d44fc5681d5cd3932baaf3cc90aa30d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106999921"
---
# <a name="certstoreprovgetctlproperty-callback-function"></a>CertStoreProvGetCTLProperty 回呼函式

**CertStoreProvGetCTLProperty** 回呼函式會抓取 [*憑證信任清單*](../secgloss/c-gly.md) (CTL) 的指定屬性。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI CertStoreProvGetCTLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCTL_CONTEXT  pCtlContext,
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

[*憑證存放區*](../secgloss/c-gly.md)的 **HCERTSTOREPROV** 控制碼。

</dd> <dt>

*pCtlCoNtext* \[在\]
</dt> <dd>

[**CTL \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)結構的指標。

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

緩衝區的指標，其中包含要由函式傳回之 [**CTL \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) 結構的指標。 若要在為緩衝區配置記憶體之前取得 *pcbData* 的值，在第一次呼叫函式時，此參數可以設定為 **Null** 。

</dd> <dt>

*pcbData* \[in、out\]
</dt> <dd>

**DWORD** 的指標，表示 *pvData* 緩衝區的長度。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，函數會傳回非零值。

如果函式失敗，則會傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTL \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
