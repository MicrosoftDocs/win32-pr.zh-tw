---
title: 正在抓取物件的 SACL
description: Active Directory Domain Services 中物件的安全描述項可能包含 (SACL) 的系統存取控制清單。
ms.assetid: b1da91a2-d9b0-48a3-9de5-1e588209032d
ms.tgt_platform: multiple
keywords:
- SACL AD
- SACL AD，正在抓取物件的 SACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2b259ba838dbd0245725990a0c849ec4c3543b2bcac0e3c1e90dd7abd873c91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184176"
---
# <a name="retrieving-an-objects-sacl"></a>正在抓取物件的 SACL

Active Directory Domain Services 中物件的安全描述項可能包含 (SACL) 的系統存取控制清單。 SACL 包含 (Ace) 的存取控制專案，指定在網域控制站的安全性事件記錄檔中產生審核記錄的存取嘗試類型。 請注意，SACL 只會在發生存取嘗試的網域控制站上產生記錄專案，而不是在包含物件複本的每個 DC 上產生記錄專案。

若要設定或取得物件安全描述項中的 SACL，必須在要求之執行緒的存取權杖中啟用 [ **SE \_ 安全性 \_ 名稱**] 許可權。 系統管理員群組預設具有此許可權，而且可以指派給其他使用者或群組。 如需詳細資訊，請參閱 [SACL 訪問](/windows/desktop/SecAuthZ/sacl-access-right)許可權。

若要取得並設定目錄物件的 SACL，請使用 [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) 介面。 使用 c + +， [**IADsSecurityDescriptor：： get \_ SystemAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) 方法會傳回 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 指標。 在該 **IDispatch** 指標上呼叫 **QueryInterface** 以取得 [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)介面，然後使用該介面上的方法來存取 SACL 中的個別 ace。 如需修改 SACL 的程式（類似于修改 DACL）的詳細資訊，請參閱 [設定物件的存取權限](setting-access-rights-on-an-object.md)。

若要列舉 SACL 中的 Ace，請使用 [**IADsAccessControlList：： get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-get__newenum)方法，它會傳回 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)指標。 呼叫該 **IUnknown** 指標上的 **QueryInterface** 來取得 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)介面。 使用 [**IEnumVARIANT：： Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) 方法來列舉 ACL 中的 ace。 每個 ACE 都會以包含 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)指標的 **VARIANT** 傳回：請注意， **vt** 成員是 **vt \_ 分派**。 在該 **IDispatch** 指標上呼叫 **QueryInterface** ，以取得 ACE 的 [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry)介面。 使用 **IADsAccessControlEntry** 介面方法來設定或取得 ACE 的元件。

如需 Sacl 的詳細資訊，請參閱：

-   [ (Acl 的存取控制清單) ](/windows/desktop/SecAuthZ/access-control-lists)
-   [稽核產生](/windows/desktop/SecAuthZ/audit-generation)

 

 