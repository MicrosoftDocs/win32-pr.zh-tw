---
title: 'INapEnforcementClientConnection SetMaxSize 方法 (NapEnforcementClient .h) '
description: 設定此用戶端的 SoH 封包大小上限。
ms.assetid: 30d3747d-bcf8-41b3-b0af-29f20d48417b
keywords:
- SetMaxSize 方法 NAP
- SetMaxSize 方法 NAP，INapEnforcementClientConnection 介面
- INapEnforcementClientConnection 介面 NAP，SetMaxSize 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetMaxSize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c487e26b89fbc53376837e59fdcc7c298b71ebb10ffc3e2490036b536f28264
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781018"
---
# <a name="inapenforcementclientconnectionsetmaxsize-method"></a>INapEnforcementClientConnection：： SetMaxSize 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapEnforcementClientConnection：： SetMaxSize** 方法會設定此用戶端的 SoH 封包大小上限。

## <a name="syntax"></a>語法


```C++
HRESULT SetMaxSize(
  [in] ProtocolMaxSize maxSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*maxSize* \[在\]
</dt> <dd>

[**ProtocolMaxSize**](nap-datatypes.md)結構，指出 SoH 封包的最大大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                     | 描述                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                                    |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

此值是由強制用戶端設定。

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

 

 





