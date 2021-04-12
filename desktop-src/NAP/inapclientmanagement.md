---
title: 'INapClientManagement 介面 (NapManagement .h) '
description: '提供 NAP 用戶端管理的方法。 |INapClientManagement 介面 (NapManagement .h) '
ms.assetid: 9c5724db-1e85-4da5-92b7-9ff6579f9cfb
keywords:
- INapClientManagement 介面 NAP
- INapClientManagement 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapClientManagement
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe90158d6f1e9a864f7d19448a412d70890133d2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103945942"
---
# <a name="inapclientmanagement-interface"></a>INapClientManagement 介面

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapClientManagement** 介面提供 NAP 用戶端管理的方法。

> [!Note]  
> [**INapClientManagement2**](inapclientmanagement2.md) 會繼承此介面的所有方法，因此應該改用。

 

## <a name="members"></a>成員

**INapClientManagement** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **INapClientManagement** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**INapClientManagement** 介面具有這些方法。



| 方法                                                                                                                | 描述                                                                   |
|:----------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**INapClientManagement::GetNapClientInfo**](inapclientmanagement-getnapclientinfo.md)                               | 抓取 NAP 用戶端的相關資訊。<br/>                          |
| [**INapClientManagement::GetRegisteredEnforcementClients**](inapclientmanagement-getregisteredenforcementclients.md) | 抓取已註冊的強制用戶端的相關資訊。<br/>    |
| [**INapClientManagement::GetRegisteredSystemHealthAgents**](inapclientmanagement-getregisteredsystemhealthagents.md) | 取得已註冊之 SHA 的相關資訊。<br/>                       |
| [**INapClientManagement::GetSystemIsolationInfo**](inapclientmanagement-getsystemisolationinfo.md)                   | 抓取 Nap 用戶端隔離狀態的相關資訊。<br/> |
| [**INapClientManagement::RegisterEnforcementClient**](inapclientmanagement-registerenforcementclient.md)             | 向 NAP 系統註冊強制用戶端。<br/>               |
| [**INapClientManagement::RegisterSystemHealthAgent**](inapclientmanagement-registersystemhealthagent.md)             | 向 NAP 系統註冊 SHA。<br/>                              |
| [**INapClientManagement::UnregisterEnforcementClient**](inapclientmanagement-unregisterenforcementclient.md)         | 使用 NAP 系統取消註冊強制用戶端。<br/>             |
| [**INapClientManagement::UnregisterSystemHealthAgent**](inapclientmanagement-unregistersystemhealthagent.md)         | 向 NAP 系統取消註冊 SHA。<br/>                            |



 

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

[NAP 介面](nap-interfaces.md)
</dt> <dt>

[NAP 參考](nap-reference.md)
</dt> </dl>

 

