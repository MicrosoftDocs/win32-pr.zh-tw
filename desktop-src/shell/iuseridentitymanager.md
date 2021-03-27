---
description: IUserIdentityManager 不受支援，未來可能會變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: 3d24b858-bbaf-455c-83cd-3f6f93aba2a8
title: 'IUserIdentityManager 介面 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: d0d00399e0ba958ef63c5e6597eb4a34387f92f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847623"
---
# <a name="iuseridentitymanager-interface"></a>IUserIdentityManager 介面

\[**IUserIdentityManager** 不受支援，未來可能會變更或無法使用。 相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]

公開方法，以識別、列舉和管理系統上的使用者身分識別。

## <a name="members"></a>成員

**IUserIdentityManager** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IUserIdentityManager** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IUserIdentityManager** 介面具有這些方法。



| 方法                                                                  | 描述                                                                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumIdentities**](iuseridentitymanager-enumidentities.md)           | 已取代。 取得 [**IEnumUserIdentity**](ienumuseridentity.md) 物件，可用來列舉系統上存在的使用者身分識別。<br/> |
| [**GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md) | 已取代。 依據用來唯一識別它的 cookie 取得特定使用者身分識別。<br/>                                                                        |
| [**登出**](iuseridentitymanager-logoff.md)                           | 已取代。 登出目前的身分識別。<br/>                                                                                                                    |
| [**登入**](iuseridentitymanager-logon.md)                             | 已取代。 向使用者顯示 UI，讓使用者可以選擇使用者身分識別。 如果成功，將會登入並取出使用者身分識別。<br/>        |
| [**ManageIdentities**](iuseridentitymanager-manageidentities.md)       | 已取代。 向使用者顯示 UI，讓使用者可以管理使用者身分識別。<br/>                                                                          |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 用戶端支援結束<br/>    | Windows 2000 Professional<br/>                                                   |
| 伺服器支援結束<br/>    | Windows 2000 Server<br/>                                                         |
| 標頭<br/>                   | <dl> <dt>Msident。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IUserIdentity**](iuseridentity.md)
</dt> <dt>

[**IUserIdentity2**](iuseridentity2.md)
</dt> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> <dt>

[**IIdentityChangeNotify**](iidentitychangenotify.md)
</dt> </dl>

 

 
