---
title: 'INapClientManagement2 介面 (NapManagement .h) '
description: '提供 NAP 用戶端管理的方法。 |INapClientManagement2 介面 (NapManagement .h) '
ms.assetid: 3cf29bfe-471a-481a-903d-bf0479c57a08
keywords:
- INapClientManagement2 介面 NAP
- INapClientManagement2 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapClientManagement2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3441b52ddf776337765f39d23528bc223a17b1e4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104035304"
---
# <a name="inapclientmanagement2-interface"></a>INapClientManagement2 介面

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapClientManagement2** 介面提供 NAP 用戶端管理的方法。

> [!Note]  
> 此介面會繼承 [**INapClientManagement**](inapclientmanagement.md) 的所有方法，因此應該改用。

 

## <a name="members"></a>成員

**INapClientManagement2** 介面繼承自 [**INapClientManagement**](inapclientmanagement.md)。 **INapClientManagement2** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**INapClientManagement2** 介面具有這些方法。



| 方法                                                                                                    | 描述                                                                                                |
|:----------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**INapClientManagement2::GetSystemIsolationInfoEx**](inapclientmanagement2-getsystemisolationinfoex.md) | 抓取 Nap 用戶端的隔離狀態和擴充隔離狀態的相關資訊。<br/> |



 

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
</dt> <dt>

[NAP 介面](nap-interfaces.md)
</dt> <dt>

[NAP 參考](nap-reference.md)
</dt> </dl>

 

 





