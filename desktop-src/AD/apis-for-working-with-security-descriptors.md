---
title: 使用安全描述項的 Api
description: 使用安全描述項的 Api
ms.assetid: eb5ee183-949c-41f5-9f74-f9c418fdf0a2
ms.tgt_platform: multiple
keywords:
- 安全描述項廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfb798e036d5e30ba58a83499b92340bf30ee3cb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103933091"
---
# <a name="apis-for-working-with-security-descriptors"></a>使用安全描述項的 Api

Active Directory Domain Services 中的每個物件都有一個 **nTSecurityDescriptor** 屬性，其中包含物件安全描述項。 有兩種主要方式可以讀取和操作目錄物件安全描述項：

-   您可以使用 [**IADs：： Get**](/windows/desktop/api/iads/nf-iads-iads-get) 方法，將安全描述項取出為具有 [**IADSSECURITYDESCRIPTOR**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) 介面的 ADSI COM 物件。 **IADsSecurityDescriptor**、 [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)和 [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry)介面可以用來處理安全描述項及其元件 (acl、ace 等) 。 如需詳細資訊和程式碼範例，請參閱 [使用 IADs 取得安全描述項](using-iads-to-get-a-security-descriptor.md)。
-   您可以使用 [**IDirectoryObject：： GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) 方法，將物件安全描述項取出為 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) 結構的指標。 使用這個指標搭配 Win32 存取控制函數，例如 [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) 或 [**BuildSecurityDescriptor**](/windows/desktop/api/aclapi/nf-aclapi-buildsecuritydescriptora)。 如需詳細資訊和程式碼範例，請參閱 [使用 IDirectoryObject 取得安全描述項](using-idirectoryobject-to-get-a-security-descriptor.md)。

本指南的大部分程式碼範例所使用的建議技術，是使用 **IADs \*** 介面，因為它們簡化了處理安全描述項、acl 和 ace 的處理。 針對 Visual Basic 程式設計師， **IADs \*** 介面是處理安全描述項的最有效方式。

當需要 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)結構時， [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject)技術會很有用。 例如，在 [物件 ACL 中檢查控制項存取權](checking-a-control-access-right-in-an-objectampaposs-acl.md) 的程式碼範例會使用這個方法來取得要傳遞給 [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) 函數的安全描述項。

如需詳細資訊，請參閱

-   [使用 IADs 取得安全描述項](using-iads-to-get-a-security-descriptor.md)
-   [使用 IDirectoryObject 取得安全描述項](using-idirectoryobject-to-get-a-security-descriptor.md)
-   [安全描述項元件](security-descriptor-components.md)
-   [正在抓取物件的 DACL](retrieving-an-objectampaposs-dacl.md)
-   [正在抓取物件的 SACL](retrieving-an-objectampaposs-sacl.md)
-   [讀取物件的安全描述項](reading-an-objectampaposs-security-descriptor.md)
-   [建立安全描述項的範例程式碼](example-code-for-creating-a-security-descriptor.md)
-   [列舉 Active Directory Domain Services 中物件之 ACL 的範例程式碼](example-code-for-enumerating-the-acl-of-an-active-directory-object.md)

 

 