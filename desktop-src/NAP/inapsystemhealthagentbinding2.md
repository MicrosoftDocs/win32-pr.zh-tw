---
title: 'INapSystemHealthAgentBinding2 介面 (NapSystemHealthAgent .h) '
description: 'Sha 用來與 NapAgent 通訊。 |INapSystemHealthAgentBinding2 介面 (NapSystemHealthAgent .h) '
ms.assetid: 2b087d79-a738-42d6-a8f2-4698ab844446
keywords:
- INapSystemHealthAgentBinding2 介面 NAP
- INapSystemHealthAgentBinding2 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c42db59c23826855ca6cda7529eb9dcbbadfb2a1ee2a5aa93d9bd45587c45a87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780928"
---
# <a name="inapsystemhealthagentbinding2-interface"></a>INapSystemHealthAgentBinding2 介面

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSystemHealthAgentBinding2** 會提供 sha 用來與 NapAgent 進行通訊的方法。

> [!Note]  
> 此介面會繼承 [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md) 的所有方法，因此應該改用。

 

## <a name="members"></a>成員

**INapSystemHealthAgentBinding2** 介面繼承自 [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)。 **INapSystemHealthAgentBinding2** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**INapSystemHealthAgentBinding2** 介面具有這些方法。



| 方法                                                                                                                    | 描述                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) | 由 Sha 呼叫以判斷系統隔離狀態和擴充的隔離狀態。<br/> |



 

## <a name="remarks"></a>備註

如果 NapAgent 已停止，此介面中的所有 Api 都會傳回 **RPC \_ E \_ 中斷** 連線。 這個物件會在重新開機後自動復原並重新系結至 NapAgent。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>NapSystemHealthAgent。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> <dt>

[NAP 介面](nap-interfaces.md)
</dt> <dt>

[NAP 參考](nap-reference.md)
</dt> </dl>

 

 





