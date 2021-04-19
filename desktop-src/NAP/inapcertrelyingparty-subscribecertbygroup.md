---
title: 'INapCertRelyingParty SubscribeCertByGroup 方法 (NapCertRelyingParty .h) '
description: 訂閱健康情況憑證伺服器 (HCS) 。
ms.assetid: 6fce113d-e183-45d7-8fb5-e04b6f4afcca
keywords:
- SubscribeCertByGroup 方法 NAP
- SubscribeCertByGroup 方法 NAP，INapCertRelyingParty 介面
- INapCertRelyingParty 介面 NAP，SubscribeCertByGroup 方法
topic_type:
- apiref
api_name:
- INapCertRelyingParty.SubscribeCertByGroup
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 053c3c2dbf00e706003988bd5769cb2aa9201c41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106999607"
---
# <a name="inapcertrelyingpartysubscribecertbygroup-method"></a>INapCertRelyingParty：： SubscribeCertByGroup 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**SubscribeCertByGroup** 方法會訂閱健康情況憑證伺服器 (HCS) 。 HCS 必須已在訂閱之前註冊。

## <a name="syntax"></a>語法


```C++
HRESULT SubscribeCertByGroup(
  [in]        EnforcementEntityId  id,
  [in]  const BSTR                subscriberName,
  [in]  const  VARIANT            *reserved,
  [out]       BOOL                *certExists
);
```



## <a name="parameters"></a>參數

<dl> <dt>

  \[ 中的識別碼\]
</dt> <dd>

[**EnforcementEntityId**](nap-datatypes.md) ，其中包含所訂閱之強制用戶端的識別碼。

</dd> <dt>

*microsoft.sqlserver.replication.subscription.subscribername* \[在\]
</dt> <dd>

訂閱者的名稱。

> [!Note]  
> 這目前僅供記錄之用。

 

</dd> <dt>

*保留* \[在\]
</dt> <dd>

必須是 **Null**。

</dd> <dt>

*certExists* \[擴展\]
</dt> <dd>

指出此 HCS 的健康情況憑證是否已由 NapAgent 維護，並存在於電腦存放區中。 若 **為 TRUE**，則表示健康狀態憑證已在維護中且存在。 如果 **為 FALSE**，則表示健康情況憑證目前未進行維護，而且不存在。

</dd> </dl>

## <a name="return-value"></a>傳回值

根據此操作的結果，傳回下列其中一個錯誤碼。



| 傳回碼                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                            |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                               |
| 標頭<br/>                   | <dl> <dt>NapCertRelyingParty。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCertRelyingParty .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapCertRelyingParty**](inapcertrelyingparty.md)
</dt> </dl>

 

 





