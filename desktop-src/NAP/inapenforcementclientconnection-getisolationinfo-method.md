---
title: 'INapEnforcementClientConnection GetIsolationInfo 方法 (NapEnforcementClient .h) '
description: 會使用取得用戶端的隔離資訊。
ms.assetid: 33040554-dcbe-4563-b047-fc7e28bac55c
keywords:
- GetIsolationInfo 方法 NAP
- GetIsolationInfo 方法 NAP，INapEnforcementClientConnection 介面
- INapEnforcementClientConnection 介面 NAP，GetIsolationInfo 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81f9fffc3f31b22e791b8f5dcff67bfc4b75c998f35158f99d5c558004a51f5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939956"
---
# <a name="inapenforcementclientconnectiongetisolationinfo-method"></a>INapEnforcementClientConnection：： GetIsolationInfo 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapEnforcementClientConnection：： GetIsolationInfo** 方法是用來取得用戶端的隔離資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetIsolationInfo(
  [out] IsolationInfo **isolationInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*isolationInfo* \[擴展\]
</dt> <dd>

[**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo)結構指標的指標，其中包含用戶端的連接狀態。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                                    |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

這項資訊是由 NapAgent 在處理 [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) 之後設定的，而且不得由 enforcer 設定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>NapEnforcementClient。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





