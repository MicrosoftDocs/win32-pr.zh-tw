---
title: 'INapSystemHealthAgentRequest GetCacheSoHFlag 方法 (NapSystemHealthAgent .h) '
description: 僅供 NapAgent 使用。
ms.assetid: 97dd4e95-30c2-48e2-9359-b1019299581d
keywords:
- GetCacheSoHFlag 方法 NAP
- GetCacheSoHFlag 方法 NAP，INapSystemHealthAgentRequest 介面
- INapSystemHealthAgentRequest 介面 NAP，GetCacheSoHFlag 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetCacheSoHFlag
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9268e620f38ef314c0699612436518315e44cf7f554bb393d2259ae4664519cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133673"
---
# <a name="inapsystemhealthagentrequestgetcachesohflag-method"></a>INapSystemHealthAgentRequest：： GetCacheSoHFlag 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSystemHealthAgentRequest：： GetCacheSoHFlag** 方法僅供 NapAgent 使用。

## <a name="syntax"></a>語法


```C++
HRESULT GetCacheSoHFlag(
   BOOL *cacheSohForLaterUse
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*cacheSohForLaterUse* 
</dt> <dd>

如果 NapAgent 應該快取 [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) ，則 **布林****值為 TRUE** ，否則為 **FALSE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                     | 描述                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                                    |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>NapSystemHealthAgent。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagentrt.dll</dt> </dl>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





