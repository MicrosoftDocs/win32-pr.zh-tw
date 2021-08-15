---
title: 'INapEnforcementClientConnection SetConnectionId 方法 (NapEnforcementClient .h) '
description: 是用來設定連接的唯一識別碼，而且必須在建立連接之後，強制用戶端設定此識別碼。
ms.assetid: 69d1a891-bc86-4c8a-b614-ebcdaa4a9057
keywords:
- SetConnectionId 方法 NAP
- SetConnectionId 方法 NAP，INapEnforcementClientConnection 介面
- INapEnforcementClientConnection 介面 NAP，SetConnectionId 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetConnectionId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fdde438be329627645c7615453ff198e9c4f01f540684c27e8e3a5699e48499
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939649"
---
# <a name="inapenforcementclientconnectionsetconnectionid-method"></a>INapEnforcementClientConnection：： SetConnectionId 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapEnforcementClientConnection：： SetConnectionId** 方法是用來設定連接的唯一識別碼，而且必須在建立連接之後，強制用戶端設定此識別碼。

## <a name="syntax"></a>語法


```C++
HRESULT SetConnectionId(
  [in] const ConnectionId *connectionId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*connectionId* \[在\]
</dt> <dd>

可唯一識別連接之 [**ConnectionId**](nap-datatypes.md) 的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                                    |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

此 ConnectionID 主要用於記錄用途。

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

 

 





