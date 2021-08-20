---
title: 'INapEnforcementClientConnection SetFlags 方法 (NapEnforcementClient .h) '
description: '是用來區分因為 enforcers 快取的 SoHRequests 而回應的第一次回應。 |INapEnforcementClientConnection SetFlags 方法 (NapEnforcementClient .h) '
ms.assetid: 2f35bcdf-662c-431f-a39e-a7c758f35603
keywords:
- SetFlags 方法 NAP
- SetFlags 方法 NAP，INapEnforcementClientConnection 介面
- INapEnforcementClientConnection 介面 NAP，SetFlags 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetFlags
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 306ab4312138136dc00aec701d322ed82e95a731c8c4f418fb2cfaddd921ed50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133990"
---
# <a name="inapenforcementclientconnectionsetflags-method"></a>INapEnforcementClientConnection：： SetFlags 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapEnforcementClientConnection：： SetFlags** 方法可用來區分因為 enforcers 快取的 SoHRequests 所產生之回應的第一次回應。

## <a name="syntax"></a>語法


```C++
HRESULT SetFlags(
  [in] UINT8 flags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*旗標* \[在\]
</dt> <dd>

判斷 [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) 是否因為快取 **SoHRequest** 所造成的旗標。 如果 *旗標* 的值為 [**freshSoHRequest**](nap-type-constants.md)，則為新的要求;否則，它會是快取的要求。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                     | 描述                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                                    |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

此值是由 NapAgent 所設定。

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

 

 





