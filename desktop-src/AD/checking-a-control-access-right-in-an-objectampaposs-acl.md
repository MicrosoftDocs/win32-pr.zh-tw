---
title: 在物件的 ACL 中檢查控制項存取權
description: 若要在物件的 ACL 上檢查控制項存取權，請使用 AccessCheckByTypeResultList 函數。
ms.assetid: 5a609622-6a1a-46ae-a336-afec504225c7
ms.tgt_platform: multiple
keywords:
- 在物件 ACL AD 中檢查控制項存取權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10170bd496da14657356a2334015975da1cc02ff
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023283"
---
# <a name="checking-a-control-access-right-in-an-objects-acl"></a>在物件的 ACL 中檢查控制項存取權

若要在物件的 ACL 上檢查控制項存取權，請使用 [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) 函數。 若要使用這個函數，應用程式需要物件的 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) 指標，而不是 ADSI 安全描述項 COM 物件的 [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) 介面。

使用下列步驟來檢查物件上受控制存取權限的存取權：

1.  取得物件的 [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) 介面指標。
2.  您可以使用 [**IDirectoryObject：： GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) 方法取得物件的安全描述項。 包含安全描述項的屬性名稱是 [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor)。 屬性會以指標的形式傳回至 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) 結構。
3.  使用 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) 結構搭配 [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) 函式來檢查指定之用戶端的指定控制項存取權限許可權。

在 [物件 ACL 中檢查控制項存取權的範例程式](example-code-for-checking-a-control-access-right-in-an-objectampaposs-acl.md) 代碼範例中，會詳細說明如何進行這項作業。

 

 