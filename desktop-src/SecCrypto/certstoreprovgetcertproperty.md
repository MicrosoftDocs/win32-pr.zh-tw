---
description: 抓取憑證的指定屬性。
ms.assetid: 827e0331-1f87-4891-8cc1-de1bcbad2963
title: CertStoreProvGetCertProperty 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCertProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 50de9a73438e2755e002570f921d15e6086a4b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978920"
---
# <a name="certstoreprovgetcertproperty-callback-function"></a>CertStoreProvGetCertProperty 回呼函式

**CertStoreProvGetCertProperty** 回呼函式會抓取憑證的指定屬性。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI CertStoreProvGetCertProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCERT_CONTEXT pCertContext,
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

*pCertCoNtext* \[在\]
</dt> <dd>

憑證 [**\_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) 結構的指標。

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

緩衝區的指標，其中包含要由函式傳回之憑證 [**\_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) 結構的指標。 在第一次呼叫函式時，可以設定為 **Null** ，以取得 *pcbData* 的值，然後再為緩衝區配置記憶體。

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
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**憑證 \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
