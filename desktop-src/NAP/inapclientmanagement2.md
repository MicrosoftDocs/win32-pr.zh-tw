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
ms.openlocfilehash: 4f459e6fa0d883203bf52ebbd0aaab06ee93cef00d1fb52af3d670f71cf7ab52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800098"
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
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                         |
| 標頭<br/>                   | <dl> <dt>NapManagement。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapManagement .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> <dt>

[NAP 介面](nap-interfaces.md)
</dt> <dt>

[NAP 參考](nap-reference.md)
</dt> </dl>

 

 





