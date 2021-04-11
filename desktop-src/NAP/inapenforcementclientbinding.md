---
title: 'INapEnforcementClientBinding 介面 (NapEnforcementClient .h) '
description: 強制用戶端用來與 NapAgent 通訊。
ms.assetid: 73c5c9ad-f213-4d34-9262-996acb570a55
keywords:
- INapEnforcementClientBinding 介面 NAP
- INapEnforcementClientBinding 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23db912c08e68adb1411527c90580a5620601752
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844356"
---
# <a name="inapenforcementclientbinding-interface"></a>INapEnforcementClientBinding 介面

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapEnforcementClientBinding** 會提供強制用戶端用來與 NapAgent 進行通訊的方法。

## <a name="members"></a>成員

**INapEnforcementClientBinding** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **INapEnforcementClientBinding** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**INapEnforcementClientBinding** 介面具有這些方法。



| 方法                                                                                                                           | 描述                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapEnforcementClientBinding：： CreateConnection**](inapenforcementclientbinding-createconnection-method.md)                   | 供 enforcers 用來建立連線物件。<br/>                                                                                                                                                            |
| [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md)                         | 在強制用戶端需要特定連接的 SoH 要求時使用。<br/>                                                                                                                   |
| [**INapEnforcementClientBinding：： Initialize**](inapenforcementclientbinding-initialize-method.md)                               | 啟動 NapAgent 服務。 強制用戶端必須先呼叫這個方法，然後再呼叫這個介面的任何其他方法。<br/>                                                                            |
| [**INapEnforcementClientBinding::NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) | 用來通知 NapAgent，與強制用戶端的連接已關閉。<br/>                                                                                                                      |
| [**INapEnforcementClientBinding::NotifySoHChangeFailure**](inapenforcementclientbinding-notifysohchangefailure-method.md)       | 由強制用戶端用來通知 NapAgent，它無法處理先前的 [**INapEnforcementClientCallback：： NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md)。<br/> |
| [**INapEnforcementClientBinding：:P rocessSoHResponse**](inapenforcementclientbinding-processsohresponse-method.md)               | 在強制用戶端從強制服務器取得 SoH-Response 資料 blob 時使用。<br/>                                                                                                       |
| [**INapEnforcementClientBinding：：解除初始化**](inapenforcementclientbinding-uninitialize-method.md)                           | 結束此用戶端連接的 NapAgent 服務。<br/>                                                                                                                                                 |



 

## <a name="remarks"></a>備註

\_如果 NapAgent 已停止，此介面中的所有 api 都會傳回 RPC E \_ 中斷連線。 這個物件會在重新開機後自動復原並重新系結至 NapAgent。

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

[NAP 介面](nap-interfaces.md)
</dt> <dt>

[NAP 參考](nap-reference.md)
</dt> </dl>

 

