---
title: 正在抓取物件的 DACL
description: 物件的安全描述項可能包含 (DACL) 的任意存取控制清單。
ms.assetid: 93b16094-9923-4886-804f-4e989fbf6977
ms.tgt_platform: multiple
keywords:
- DACL 廣告
- DACL AD，正在抓取物件的 DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b515e6c5d28be7003734510300fc7f6d2de776b479b56e62ad521567c76dce4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025106"
---
# <a name="retrieving-an-objects-dacl"></a>正在抓取物件的 DACL

物件的安全描述項可能包含 (DACL) 的任意存取控制清單。 DACL 包含零或多個存取控制專案 (Ace) 可識別可存取物件的使用者和群組。 如果 DACL 是空的 (也就是說，它包含零個 Ace) ，沒有明確授與存取權，因此會隱含拒絕存取。 但是，如果物件的安全描述項沒有 DACL，則物件會受到保護，且每個人都有完整的存取權。

若要抓取物件的 DACL，您必須是物件的擁有者，或擁有物件的 **讀取 \_ 控制** 存取權。

若要取得並設定目錄物件的 DACL，請使用 [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) 介面。 使用 c + +， [**IADsSecurityDescriptor：： get \_ objdescriptor.discretionaryacl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) 方法會傳回 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 指標。 在該 **IDispatch** 指標上呼叫 **QueryInterface** 以取得 [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)介面，並在該介面上使用方法來存取 DACL 中的個別 ace。 修改 DACL 的程式描述于 [設定物件的存取權限](setting-access-rights-on-an-object.md)。

若要列舉 Ace，請使用 [**IADsAccessControlList：： get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-get__newenum)方法。 方法會傳回 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 指標。 呼叫該 **IUnknown** 指標上的 **QueryInterface** 來取得 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)介面。 使用 [**IEnumVARIANT：： Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) 方法來列舉 ACL 中的 ace。 每個 ACE 都會以包含 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)指標的 **VARIANT** 傳回， (**vt** 成員是 **vt \_ 分派**) 。 在該 **IDispatch** 指標上呼叫 **QueryInterface** ，以取得 ACE 的 [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry)介面。 您可以使用 **IADsAccessControlEntry** 介面的方法來設定或取得 ACE 的元件。

如需有關 Dacl 和 Ace 的詳細資訊，請參閱平臺軟體發展工具組中的下列主題 (SDK) 。

-   [ (Acl 的存取控制清單) ](/windows/desktop/SecAuthZ/access-control-lists)
-   [ (Ace 的存取控制專案) ](/windows/desktop/SecAuthZ/access-control-entries)

 

 