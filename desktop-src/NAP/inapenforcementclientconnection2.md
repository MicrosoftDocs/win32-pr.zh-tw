---
title: 'INapEnforcementClientConnection2 介面 (NapEnforcementClient .h) '
description: '允許用戶端連接管理。 |INapEnforcementClientConnection2 介面 (NapEnforcementClient .h) '
ms.assetid: f7b5d8cc-6a91-4e49-8957-cf67d1001089
keywords:
- INapEnforcementClientConnection2 介面 NAP
- INapEnforcementClientConnection2 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3503e1bf6db01920e814b96e3daf5fe04eabc6b9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853627"
---
# <a name="inapenforcementclientconnection2-interface"></a>INapEnforcementClientConnection2 介面

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapEnforcementClientConnection2** 提供允許用戶端連接管理的方法。

> [!Note]  
> 此介面會繼承 [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) 的所有方法，因此應該改用。

 

## <a name="members"></a>成員

**INapEnforcementClientConnection2** 介面繼承自 [**INapEnforcementClientConnection**](inapenforcementclientconnection.md)。 **INapEnforcementClientConnection2** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**INapEnforcementClientConnection2** 介面具有這些方法。



| 方法                                                                                                              | 描述                                                                      |
|:--------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**INapEnforcementClientConnection2::GetInstalledShvs**](inapenforcementclientconnection2-getinstalledshvs.md)     | 用來取得用戶端已安裝之 Shv 的識別碼。<br/>             |
| [**INapEnforcementClientConnection2::GetIsolationInfoEx**](inapenforcementclientconnection2-getisolationinfoex.md) | 用來取得用戶端的隔離資訊。<br/>                 |
| [**INapEnforcementClientConnection2::SetInstalledShvs**](inapenforcementclientconnection2-setinstalledshvs.md)     | 供 NapAgent 用來設定用戶端已安裝的 SHV 識別碼。<br/>     |
| [**INapEnforcementClientConnection2::SetIsolationInfoEx**](inapenforcementclientconnection2-setisolationinfoex.md) | 供 NapAgent 用來設定用戶端的隔離資訊。<br/> |



 

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

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> <dt>

[NAP 介面](nap-interfaces.md)
</dt> <dt>

[NAP 參考](nap-reference.md)
</dt> </dl>

 

 





