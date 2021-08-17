---
title: 'INapCertRelyingParty UnSubscribeCertByGroup 方法 (NapCertRelyingParty .h) '
description: 從健康情況憑證伺服器取消訂閱 (HCS) 。
ms.assetid: 2b26b110-8aba-487e-bd49-c6afc6af11f8
keywords:
- UnSubscribeCertByGroup 方法 NAP
- UnSubscribeCertByGroup 方法 NAP，INapCertRelyingParty 介面
- INapCertRelyingParty 介面 NAP，UnSubscribeCertByGroup 方法
topic_type:
- apiref
api_name:
- INapCertRelyingParty.UnSubscribeCertByGroup
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d8b9f5398ba63c0e6108adfefd51d0546180db4536dbd95615e5b15dddde523
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940216"
---
# <a name="inapcertrelyingpartyunsubscribecertbygroup-method"></a>INapCertRelyingParty：： UnSubscribeCertByGroup 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**UnSubscribeCertByGroup** 方法會從健康情況憑證伺服器取消訂閱 (HCS) 。

## <a name="syntax"></a>語法


```C++
HRESULT UnSubscribeCertByGroup(
  [in]        EnforcementEntityId   id,
  [in] const  VARIANT             * reserved
);
```



## <a name="parameters"></a>參數

<dl> <dt>

  \[ 中的識別碼\]
</dt> <dd>

[**EnforcementEntityId**](nap-datatypes.md) ，其中包含正在取消訂閱之強制用戶端的識別碼。

</dd> <dt>

 *保留* \[在\]
</dt> <dd>

必須是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

根據此操作的結果，傳回下列其中一個錯誤碼。



| 傳回碼                                                                                     | 描述                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                            |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

如果沒有其他 HCS 的訂閱者，NapAgent 將會從本機電腦存放區中刪除對應的健康情況憑證。

呼叫這個方法之前，請先呼叫 [**SubscribeCertByGroup**](inapcertrelyingparty-subscribecertbygroup.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                               |
| 標頭<br/>                   | <dl> <dt>NapCertRelyingParty。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCertRelyingParty .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapCertRelyingParty**](inapcertrelyingparty.md)
</dt> </dl>

 

 





