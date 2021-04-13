---
title: 'INapClientManagement GetRegisteredEnforcementClients 方法 (NapManagement .h) '
description: 抓取已註冊的強制用戶端的相關資訊。
ms.assetid: aae7c57c-a7fe-4cb2-94f6-53e501e38054
keywords:
- GetRegisteredEnforcementClients 方法 NAP
- GetRegisteredEnforcementClients 方法 NAP，INapClientManagement 介面
- INapClientManagement 介面 NAP，GetRegisteredEnforcementClients 方法
topic_type:
- apiref
api_name:
- INapClientManagement.GetRegisteredEnforcementClients
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7767f96c9b5410b3de9cfef3695193c0d5572b2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466044"
---
# <a name="inapclientmanagementgetregisteredenforcementclients-method"></a>INapClientManagement：： GetRegisteredEnforcementClients 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**GetRegisteredEnforcementClients** 方法會抓取已註冊的強制用戶端的相關資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetRegisteredEnforcementClients(
  [out] EnforcementEntityCount       *count,
  [out] NapComponentRegistrationInfo **enforcers
) const;
```



## <a name="parameters"></a>參數

<dl> <dt>

*計數* \[擴展\]
</dt> <dd>

[**EnforcementEntityCount**](nap-datatypes.md)的指標，其中包含已註冊的強制用戶端數目。

</dd> <dt>

*enforcers* \[擴展\]
</dt> <dd>

[**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo)結構陣列的指標，這些結構描述已註冊的強制用戶端。

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

 

 





