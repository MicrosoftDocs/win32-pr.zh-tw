---
description: 已取代。 提供對系統上使用者身分識別的修改通知，以及切換目前使用者身分識別的使用者要求。
ms.assetid: 09903aa6-62bf-4820-9a09-79956d775441
title: 'IIdentityChangeNotify 介面 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 4a217b2cfb046bfb9ae5546e015264f74d00b1d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192675"
---
# <a name="iidentitychangenotify-interface"></a>IIdentityChangeNotify 介面

\[**IIdentityChangeNotify** 介面可用於 Windows 2000。 在 Windows XP 中，這項功能已由 [使用者帳戶取代為快速使用者切換和遠端桌面](fastuserswitching.md)，而且可能會在後續版本中變更或無法使用。\]

已取代。 提供對系統上使用者身分識別的修改通知，以及切換目前使用者身分識別的使用者要求。

## <a name="members"></a>成員

**IIdentityChangeNotify** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IIdentityChangeNotify** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IIdentityChangeNotify** 介面具有這些方法。



| 方法                                                                                 | 描述                                                                                                                           |
|:---------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [**IdentityInformationChanged**](iidentitychangenotify-identityinformationchanged.md) | 已取代。 當使用者身分識別的相關資訊變更，或新增或刪除使用者身分識別時呼叫。<br/>  |
| [**QuerySwitchIdentities**](iidentitychangenotify-queryswitchidentities.md)           | 已取代。 當目前使用者要求切換其使用者身分識別，但在切換之前發生時呼叫。<br/> |
| [**SwitchIdentities**](iidentitychangenotify-switchidentities.md)                     | 已取代。 當使用者身分識別切換時呼叫。<br/>                                                                      |



 

## <a name="remarks"></a>備註

若要執行通知，衍生介面必須藉由呼叫 [**IConnectionPoint：： Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise)和將指標傳遞至介面，來連接到 [**IUserIdentityManager**](iuseridentitymanager.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Msident。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msoe.dll</dt> </dl>    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint)
</dt> </dl>

 

 
