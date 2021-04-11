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
# <a name="checking-a-control-access-right-in-an-objects-acl"></a><span data-ttu-id="06426-104">在物件的 ACL 中檢查控制項存取權</span><span class="sxs-lookup"><span data-stu-id="06426-104">Checking a Control Access Right in an Object's ACL</span></span>

<span data-ttu-id="06426-105">若要在物件的 ACL 上檢查控制項存取權，請使用 [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) 函數。</span><span class="sxs-lookup"><span data-stu-id="06426-105">To check a control access right on an object's ACL, use the [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) function.</span></span> <span data-ttu-id="06426-106">若要使用這個函數，應用程式需要物件的 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) 指標，而不是 ADSI 安全描述項 COM 物件的 [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) 介面。</span><span class="sxs-lookup"><span data-stu-id="06426-106">To use this function, an application requires a pointer to the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) for the object instead of an [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) interface to an ADSI security descriptor COM object.</span></span>

<span data-ttu-id="06426-107">使用下列步驟來檢查物件上受控制存取權限的存取權：</span><span class="sxs-lookup"><span data-stu-id="06426-107">Use the following steps to check access for an controlled access right on an object:</span></span>

1.  <span data-ttu-id="06426-108">取得物件的 [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="06426-108">Get an [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) interface pointer to the object.</span></span>
2.  <span data-ttu-id="06426-109">您可以使用 [**IDirectoryObject：： GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) 方法取得物件的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="06426-109">Use the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) method to get the security descriptor of the object.</span></span> <span data-ttu-id="06426-110">包含安全描述項的屬性名稱是 [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor)。</span><span class="sxs-lookup"><span data-stu-id="06426-110">The name of the property containing the security descriptor is [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor).</span></span> <span data-ttu-id="06426-111">屬性會以指標的形式傳回至 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) 結構。</span><span class="sxs-lookup"><span data-stu-id="06426-111">The property is returned as a pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure.</span></span>
3.  <span data-ttu-id="06426-112">使用 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) 結構搭配 [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) 函式來檢查指定之用戶端的指定控制項存取權限許可權。</span><span class="sxs-lookup"><span data-stu-id="06426-112">Use the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure with the [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) function to check the permissions for the specified control access right for the specified client.</span></span>

<span data-ttu-id="06426-113">在 [物件 ACL 中檢查控制項存取權的範例程式](example-code-for-checking-a-control-access-right-in-an-objectampaposs-acl.md) 代碼範例中，會詳細說明如何進行這項作業。</span><span class="sxs-lookup"><span data-stu-id="06426-113">The example code in [Example Code for Checking a Control Access Right in an Object's ACL](example-code-for-checking-a-control-access-right-in-an-objectampaposs-acl.md) shows, in detail, how to do this.</span></span>

 

 