---
title: 'INapEnforcementClientConnection GetStringCorrelationId 方法 (NapEnforcementClient .h) '
description: 取得用來讓要求和回應相互關聯的識別碼字串版本。
ms.assetid: d744fa4e-5e30-429e-810d-7326047bb3f8
keywords:
- GetStringCorrelationId 方法 NAP
- GetStringCorrelationId 方法 NAP，INapEnforcementClientConnection 介面
- INapEnforcementClientConnection 介面 NAP，GetStringCorrelationId 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetStringCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6a01ca16bffb627f4ca5be38ef547980951c0ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508443"
---
# <a name="inapenforcementclientconnectiongetstringcorrelationid-method"></a>INapEnforcementClientConnection：： GetStringCorrelationId 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapEnforcementClientConnection：： GetStringCorrelationId** 方法會取得用來讓要求和回應相互關聯的識別碼字串版本。

## <a name="syntax"></a>語法


```C++
HRESULT GetStringCorrelationId(
  [out] CountedString **correlationId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*correlationId* \[擴展\]
</dt> <dd>

[**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)結構的指標，其中包含連接 [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid)的字串版本。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                                    |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

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

 

 





