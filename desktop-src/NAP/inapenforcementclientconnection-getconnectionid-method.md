---
title: 'INapEnforcementClientConnection GetConnectionId 方法 (NapEnforcementClient .h) '
description: 用來取得用戶端的唯一連接識別碼。
ms.assetid: bf744aa6-5786-473f-9508-db4ee0c75578
keywords:
- GetConnectionId 方法 NAP
- GetConnectionId 方法 NAP，INapEnforcementClientConnection 介面
- INapEnforcementClientConnection 介面 NAP，GetConnectionId 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetConnectionId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3ca16aea3c77ccf78359c3cdf5ab6461bc2219e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106427"
---
# <a name="inapenforcementclientconnectiongetconnectionid-method"></a>INapEnforcementClientConnection：： GetConnectionId 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapEnforcementClientConnection：： GetConnectionId** 方法是用來取得用戶端的唯一連接識別碼。

## <a name="syntax"></a>語法


```C++
HRESULT GetConnectionId(
  [out] ConnectionId **connectionId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*connectionId* \[擴展\]
</dt> <dd>

指標，指向可唯一識別此連接的 [**ConnectionId**](nap-datatypes.md) 指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                                    |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

連接識別碼主要用於記錄用途。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>NapEnforcementClient。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





