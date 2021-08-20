---
title: 'INapClientManagement UnregisterSystemHealthAgent 方法 (NapManagement .h) '
description: 向 NAP 系統取消註冊 SHA。
ms.assetid: c3ad6f2a-c39a-4590-8487-24c802433845
keywords:
- UnregisterSystemHealthAgent 方法 NAP
- UnregisterSystemHealthAgent 方法 NAP，INapClientManagement 介面
- INapClientManagement 介面 NAP，UnregisterSystemHealthAgent 方法
topic_type:
- apiref
api_name:
- INapClientManagement.UnregisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad43df1c7edeb2525ff5c8901278d082c4ba299ea78d56c67a4380f8a7bab019
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134506"
---
# <a name="inapclientmanagementunregistersystemhealthagent-method"></a>INapClientManagement：： UnregisterSystemHealthAgent 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**UnregisterSystemHealthAgent** 方法會向 NAP 系統取消註冊 SHA。

## <a name="syntax"></a>語法


```C++
HRESULT UnregisterSystemHealthAgent(
  [in] SystemHealthEntityId id
);
```



## <a name="parameters"></a>參數

<dl> <dt>

 \[ 中的識別碼\]
</dt> <dd>

識別要取消註冊之系統健康狀態代理程式的 [**SystemHealthEntityId**](nap-datatypes.md) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 HRESULT 狀態碼，包括但不限於下列其中一項。



| 傳回碼                                                                                         | 描述                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                | 作業成功。<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>      | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | 系統資源限制，無法執行操作。<br/> |
| <dl> <dt>**NAP \_ E \_ 仍系結 \_**</dt> </dl> | SHA 仍保持系結狀態，無法取消註冊。<br/>    |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                         |
| 標頭<br/>                   | <dl> <dt>NapManagement。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapManagement .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 





