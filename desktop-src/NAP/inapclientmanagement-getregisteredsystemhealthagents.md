---
title: 'INapClientManagement GetRegisteredSystemHealthAgents 方法 (NapManagement .h) '
description: 抓取已註冊 Sha 的相關資訊。
ms.assetid: c38d2d23-62d4-49f0-81a3-52394866f0c4
keywords:
- GetRegisteredSystemHealthAgents 方法 NAP
- GetRegisteredSystemHealthAgents 方法 NAP，INapClientManagement 介面
- INapClientManagement 介面 NAP，GetRegisteredSystemHealthAgents 方法
topic_type:
- apiref
api_name:
- INapClientManagement.GetRegisteredSystemHealthAgents
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4852e2d4c1ffa08b1a7ea7b3d8395c1b116cca6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934678"
---
# <a name="inapclientmanagementgetregisteredsystemhealthagents-method"></a>INapClientManagement：： GetRegisteredSystemHealthAgents 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**GetRegisteredSystemHealthAgents** 方法會抓取已註冊 sha 的相關資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetRegisteredSystemHealthAgents(
  [out] SystemHealthEntityCount      *count,
  [out] NapComponentRegistrationInfo **agents
) const;
```



## <a name="parameters"></a>參數

<dl> <dt>

*計數* \[擴展\]
</dt> <dd>

描述已註冊 Sha 數目之 [**SystemHealthEntityCount**](nap-datatypes.md) 的指標。

</dd> <dt>

*代理* \[ 程式擴展\]
</dt> <dd>

描述已註冊 Sha 之 [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) 結構陣列的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 HRESULT 狀態碼，包括但不限於下列其中一項。



| 傳回碼                                                                                         | Description                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                | 作業成功。<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>      | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | 系統資源限制，無法執行操作。<br/> |
| <dl> <dt>**RPC \_ E \_ 中斷連接**</dt> </dl> | NapAgent 未執行。<br/>                            |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                         |
| 標頭<br/>                   | <dl> <dt>NapManagement。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapManagement .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 





