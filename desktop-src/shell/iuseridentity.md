---
description: IUserIdentity 不受支援，未來可能會變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: c2f11f8b-f944-445b-b4fc-ac57b0fe3a74
title: 'IUserIdentity 介面 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 068d806086aff44db172a4a7b09f55b600204478
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973113"
---
# <a name="iuseridentity-interface"></a>IUserIdentity 介面

\[**IUserIdentity** 不受支援，未來可能會變更或無法使用。 相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]

公開方法，以提供特定使用者身分識別的識別、登錄和資料夾資料。

## <a name="members"></a>成員

**IUserIdentity** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IUserIdentity** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IUserIdentity** 介面具有這些方法。



| 方法                                                         | 描述                                                                                      |
|:---------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**System.windows.application.getcookie**](iuseridentity-getcookie.md)                   | 已取代。 取得用來唯一識別此使用者識別的 cookie。<br/>             |
| [**GetIdentityFolder**](iuseridentity-getidentityfolder.md)   | 已取代。 取得與此身分識別相關聯的檔案資料夾。<br/>                       |
| [**GetName**](iuseridentity-getname.md)                       | 已取代。 取得與此使用者識別相關聯的名稱。<br/>                         |
| [**OpenIdentityRegKey**](iuseridentity-openidentityregkey.md) | 已取代。 抓取登錄中對應此使用者識別的索引鍵。<br/> |



 

## <a name="remarks"></a>備註

這個介面所提供的資訊，會對應至系統上存在的特定使用者識別。 您可以存取這個使用者身分識別的身分識別資料夾、其登錄機碼及其識別碼，以及取得與使用者身分識別相關聯的名稱。

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

[**IUserIdentity2**](iuseridentity2.md)
</dt> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> </dl>

 

 
