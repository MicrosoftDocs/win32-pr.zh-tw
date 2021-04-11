---
title: 'INapEnforcementClientConnection GetSoHResponse 方法 (NapEnforcementClient .h) '
description: 取得強制用戶端接收的 SoH-Response。
ms.assetid: fc0084a3-a668-435e-8390-f322941c5cd4
keywords:
- GetSoHResponse 方法 NAP
- GetSoHResponse 方法 NAP，INapEnforcementClientConnection 介面
- INapEnforcementClientConnection 介面 NAP，GetSoHResponse 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67be4d65135d6e4ce606a83eb08fdeed036cc62a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843328"
---
# <a name="inapenforcementclientconnectiongetsohresponse-method"></a>INapEnforcementClientConnection：： GetSoHResponse 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapEnforcementClientConnection：： GetSoHResponse** 方法會取得強制用戶端所接收的 SoH-Response。

## <a name="syntax"></a>語法


```C++
HRESULT GetSoHResponse(
  [out] NetworkSoHResponse **sohResponse
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*sohResponse* \[擴展\]
</dt> <dd>

指向唯一 [**NetworkSoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) 結構指標的指標，這是 enforcer 的不透明資料 blob。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                                    |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

零位元組大小的封包有效。

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

 

 





