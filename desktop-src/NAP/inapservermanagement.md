---
title: 'INapServerManagement 介面 (NapServerManagement .h) '
description: 用來管理 NAP 伺服器。
ms.assetid: 5c4f9bf1-fe82-48f5-8aa4-5c73ab01a78a
keywords:
- INapServerManagement 介面 NAP
- INapServerManagement 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapServerManagement
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5eed03f535653a3b9244ff1aa74fe499c1bf2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104147"
---
# <a name="inapservermanagement-interface"></a>INapServerManagement 介面

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapServerManagement** 提供用來管理 NAP 伺服器的方法。

## <a name="members"></a>成員

**INapServerManagement** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **INapServerManagement** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**INapServerManagement** 介面具有這些方法。



| 方法                                                                                                                       | 描述                                          |
|:-----------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------|
| [**INapServerManagement::RegisterSystemHealthValidator**](inapservermanagement-registersystemhealthvalidator-method.md)     | 註冊 SHV。<br/>                         |
| [**INapServerManagement::SetFailureCategoryMappings**](inapservermanagement-setfailurecategorymappings-method.md)           | 設定 SHV 的失敗類別對應。<br/> |
| [**INapServerManagement::UnregisterSystemHealthValidator**](inapservermanagement-unregistersystemhealthvalidator-method.md) | 從 NAP 伺服器取消註冊 SHV。<br/>   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                               |
| 標頭<br/>                   | <dl> <dt>NapServerManagement。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapServerManagement .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[NAP 介面](nap-interfaces.md)
</dt> <dt>

[NAP 參考](nap-reference.md)
</dt> </dl>

 

