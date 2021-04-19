---
title: 'INapSystemHealthAgentBinding 介面 (NapSystemHealthAgent .h) '
description: 'Sha 用來與 NapAgent 通訊。 |INapSystemHealthAgentBinding 介面 (NapSystemHealthAgent .h) '
ms.assetid: 9366f61f-086a-4f44-900e-9ec3165a35ba
keywords:
- INapSystemHealthAgentBinding 介面 NAP
- INapSystemHealthAgentBinding 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38d1331996e34c6879fc2e98ce566ce6802527a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106974822"
---
# <a name="inapsystemhealthagentbinding-interface"></a>INapSystemHealthAgentBinding 介面

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSystemHealthAgentBinding** 會提供 sha 用來與 NapAgent 進行通訊的方法。

> [!Note]  
> [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) 會繼承此介面的所有方法，因此應該改用。

 

## <a name="members"></a>成員

**INapSystemHealthAgentBinding** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **INapSystemHealthAgentBinding** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**INapSystemHealthAgentBinding** 介面具有這些方法。



| 方法                                                                                                                     | 描述                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**INapSystemHealthAgentBinding::FlushCache**](inapsystemhealthagentbinding-flushcache-method.md)                         | 由 SHA 呼叫以排清其 SoH 快取。<br/>                                                |
| [**INapSystemHealthAgentBinding::GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) | 由 Sha 呼叫以判斷系統隔離狀態。<br/>                                 |
| [**INapSystemHealthAgentBinding：： Initialize**](inapsystemhealthagentbinding-initialize-method.md)                         | 初始化 SHA，並將 SHA 系結至 NapAgent 服務。 <br/>                         |
| [**INapSystemHealthAgentBinding::NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md)               | 當其 SoH 變更時由 Sha 呼叫。<br/>                                                  |
| [**INapSystemHealthAgentBinding：：解除初始化**](inapsystemhealthagentbinding-uninitialize-method.md)                     | 由 Sha 呼叫，使 NapAgent 釋放所有對 SHA COM 指標的參考。<br/> |



 

## <a name="remarks"></a>備註

如果 NapAgent 已停止，此介面中的所有 Api 都會傳回 **RPC \_ E \_ 中斷** 連線。 這個物件會在重新開機後自動復原並重新系結至 NapAgent。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>NapSystemHealthAgent。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[NAP 介面](nap-interfaces.md)
</dt> <dt>

[NAP 參考](nap-reference.md)
</dt> </dl>

 

