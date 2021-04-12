---
title: 'INapEnforcementClientBinding NotifyConnectionStateDown 方法 (NapEnforcementClient .h) '
description: 用來通知 NapAgent，與強制用戶端的連接已關閉。
ms.assetid: 504c61c1-c8f9-46b8-87cd-c1f04846f0b3
keywords:
- NotifyConnectionStateDown 方法 NAP
- NotifyConnectionStateDown 方法 NAP，INapEnforcementClientBinding 介面
- INapEnforcementClientBinding 介面 NAP，NotifyConnectionStateDown 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.NotifyConnectionStateDown
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3129883342f493fd56a4cc81513910e8789ca4f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509482"
---
# <a name="inapenforcementclientbindingnotifyconnectionstatedown-method"></a>INapEnforcementClientBinding：： NotifyConnectionStateDown 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapEnforcementClientBinding：： NotifyConnectionStateDown** 方法是用來通知 NapAgent 與強制用戶端的連接已關閉。

## <a name="syntax"></a>語法


```C++
HRESULT NotifyConnectionStateDown(
  [in] INapEnforcementClientConnection *downCxn
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*downCxn* \[在\]
</dt> <dd>

向下連接之 [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) 介面的 COM 指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                             | Description                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>                   | 作業成功。<br/>                            |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl>         | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>          | 系統資源限制，無法執行操作。<br/> |
| <dl> <dt>**NAP \_ E \_ 未 \_ 初始化**</dt> </dl> | Enforcer 先前尚未初始化。<br/>       |



 

## <a name="remarks"></a>備註

當強制用戶端所建立的任何連線中斷時，強制用戶端應該從其使用中清單移除連線，並使用這個方法通知 NapAgent。 當這個呼叫傳回時，就可以釋出和釋放連線物件。 NapAgent 不會保留連線物件的參考。

由於此通知，NapAgent 會適當地更新其系統 NAP 狀態。

強制用戶端必須先呼叫 [**INapEnforcementClientBinding：： Initialize**](inapenforcementclientbinding-initialize-method.md) 方法，才能呼叫這個或 [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) 介面的任何其他方法。

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


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> </dl>

 

 





