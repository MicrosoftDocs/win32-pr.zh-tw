---
title: 'INapEnforcementClientConnection SetCorrelationId 方法 (NapEnforcementClient .h) '
description: 設定用來相互關聯 SoH 要求和 SoH 回應的識別碼。
ms.assetid: 8f9d5bde-95b1-4566-84ee-31c6ed5e8986
keywords:
- SetCorrelationId 方法 NAP
- SetCorrelationId 方法 NAP，INapEnforcementClientConnection 介面
- INapEnforcementClientConnection 介面 NAP，SetCorrelationId 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c99576b8302f7fcf949f132cf110a5ac5f675ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508440"
---
# <a name="inapenforcementclientconnectionsetcorrelationid-method"></a>INapEnforcementClientConnection：： SetCorrelationId 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapEnforcementClientConnection：： SetCorrelationId** 方法會設定用來相互關聯 soh 要求和 soh 回應的識別碼。

## <a name="syntax"></a>語法


```C++
HRESULT SetCorrelationId(
  [in] CorrelationId correlationId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*correlationId* \[在\]
</dt> <dd>

識別特定 SoH 交換的唯一 [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) 結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                                    |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

相互關聯識別碼是由 NapAgent 所設定，並以連接識別碼為基礎。

此識別碼是用來讓要求和回應相互關聯，也就是它可唯一描述 SoH 交換，而且一律會包含連線物件上最新 SoH 集的識別碼。

收到 SoH-Response 時，NapAgent 會先確保識別碼相符;如果沒有，則會傳回錯誤，且 enforcer 必須卸載封包。 如需詳細資訊，請參閱 [**INapEnforcementClientBinding：:P rocesssohresponse**](inapenforcementclientbinding-processsohresponse-method.md) 。

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

 

 





