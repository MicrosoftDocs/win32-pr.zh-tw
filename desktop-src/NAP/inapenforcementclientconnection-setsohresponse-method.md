---
title: 'INapEnforcementClientConnection SetSoHResponse 方法 (NapEnforcementClient .h) '
description: 設定 SoH-Response，並在接收封包時由強制用戶端使用。
ms.assetid: 718669c7-73cf-44f4-8463-c59fdbe215cc
keywords:
- SetSoHResponse 方法 NAP
- SetSoHResponse 方法 NAP，INapEnforcementClientConnection 介面
- INapEnforcementClientConnection 介面 NAP，SetSoHResponse 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97a86c1a0fc86fcef9189f9d575063cee9abdf627e1cf3c58e68d669358142f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626228"
---
# <a name="inapenforcementclientconnectionsetsohresponse-method"></a>INapEnforcementClientConnection：： SetSoHResponse 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapEnforcementClientConnection：： SetSoHResponse** 方法會設定 SoH-Response，並在接收封包時由強制用戶端使用。

## <a name="syntax"></a>語法


```C++
HRESULT SetSoHResponse(
  [in] const NetworkSoHResponse *sohResponse
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*sohResponse* \[在\]
</dt> <dd>

唯一 [**NetworkSoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) 結構的指標，這是 enforcer 的不透明資料 blob。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                     | 描述                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | SoH 封包有效。<br/>                                |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

大小為零的封包有效。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>NapEnforcementClient。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





