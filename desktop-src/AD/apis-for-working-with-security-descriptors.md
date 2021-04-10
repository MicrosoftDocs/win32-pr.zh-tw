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
# <a name="apis-for-working-with-security-descriptors"></a><span data-ttu-id="17c06-104">使用安全描述項的 Api</span><span class="sxs-lookup"><span data-stu-id="17c06-104">APIs for Working with Security Descriptors</span></span>

<span data-ttu-id="17c06-105">Active Directory Domain Services 中的每個物件都有一個 **nTSecurityDescriptor** 屬性，其中包含物件安全描述項。</span><span class="sxs-lookup"><span data-stu-id="17c06-105">Each object in Active Directory Domain Services has an **nTSecurityDescriptor** attribute that contains the object security descriptor.</span></span> <span data-ttu-id="17c06-106">有兩種主要方式可以讀取和操作目錄物件安全描述項：</span><span class="sxs-lookup"><span data-stu-id="17c06-106">There are two primary ways to read and manipulate a directory object security descriptor:</span></span>

-   <span data-ttu-id="17c06-107">您可以使用 [**IADs：： Get**](/windows/desktop/api/iads/nf-iads-iads-get) 方法，將安全描述項取出為具有 [**IADSSECURITYDESCRIPTOR**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) 介面的 ADSI COM 物件。</span><span class="sxs-lookup"><span data-stu-id="17c06-107">Use the [**IADs::Get**](/windows/desktop/api/iads/nf-iads-iads-get) method to retrieve the security descriptor as an ADSI COM object with an [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) interface.</span></span> <span data-ttu-id="17c06-108">**IADsSecurityDescriptor**、 [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)和 [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry)介面可以用來處理安全描述項及其元件 (acl、ace 等) 。</span><span class="sxs-lookup"><span data-stu-id="17c06-108">The **IADsSecurityDescriptor**, [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist), and [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) interfaces can be used to handle the security descriptor and its components (ACLs, ACEs, and so on).</span></span> <span data-ttu-id="17c06-109">如需詳細資訊和程式碼範例，請參閱 [使用 IADs 取得安全描述項](using-iads-to-get-a-security-descriptor.md)。</span><span class="sxs-lookup"><span data-stu-id="17c06-109">For more information and a code example, see [Using IADs to Get a Security Descriptor](using-iads-to-get-a-security-descriptor.md).</span></span>
-   <span data-ttu-id="17c06-110">您可以使用 [**IDirectoryObject：： GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) 方法，將物件安全描述項取出為 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="17c06-110">Use the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) method to retrieve an object security descriptor as a pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure.</span></span> <span data-ttu-id="17c06-111">使用這個指標搭配 Win32 存取控制函數，例如 [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) 或 [**BuildSecurityDescriptor**](/windows/desktop/api/aclapi/nf-aclapi-buildsecuritydescriptora)。</span><span class="sxs-lookup"><span data-stu-id="17c06-111">Use this pointer with a Win32 access-control function, such as [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) or [**BuildSecurityDescriptor**](/windows/desktop/api/aclapi/nf-aclapi-buildsecuritydescriptora).</span></span> <span data-ttu-id="17c06-112">如需詳細資訊和程式碼範例，請參閱 [使用 IDirectoryObject 取得安全描述項](using-idirectoryobject-to-get-a-security-descriptor.md)。</span><span class="sxs-lookup"><span data-stu-id="17c06-112">For more information and a code example, see [Using IDirectoryObject to Get a Security Descriptor](using-idirectoryobject-to-get-a-security-descriptor.md).</span></span>

<span data-ttu-id="17c06-113">本指南的大部分程式碼範例所使用的建議技術，是使用 **IADs \*** 介面，因為它們簡化了處理安全描述項、acl 和 ace 的處理。</span><span class="sxs-lookup"><span data-stu-id="17c06-113">The recommended technique, and the one used by most of the code examples in this guide, is to use the **IADs\*** interfaces because they simplify handling security descriptors, ACLs, and ACEs.</span></span> <span data-ttu-id="17c06-114">針對 Visual Basic 程式設計師， **IADs \*** 介面是處理安全描述項的最有效方式。</span><span class="sxs-lookup"><span data-stu-id="17c06-114">For Visual Basic programmers, the **IADs\*** interfaces are the most efficient way to handle security descriptors.</span></span>

<span data-ttu-id="17c06-115">當需要 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)結構時， [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject)技術會很有用。</span><span class="sxs-lookup"><span data-stu-id="17c06-115">The [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) technique is useful when a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure is required.</span></span> <span data-ttu-id="17c06-116">例如，在 [物件 ACL 中檢查控制項存取權](checking-a-control-access-right-in-an-objectampaposs-acl.md) 的程式碼範例會使用這個方法來取得要傳遞給 [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) 函數的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="17c06-116">For example, the code example in [Checking a Control Access Right in an Object's ACL](checking-a-control-access-right-in-an-objectampaposs-acl.md) uses this method to retrieve a security descriptor to pass to the [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) function.</span></span>

<span data-ttu-id="17c06-117">如需詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="17c06-117">For more information, see:</span></span>

-   [<span data-ttu-id="17c06-118">使用 IADs 取得安全描述項</span><span class="sxs-lookup"><span data-stu-id="17c06-118">Using IADs to Get a Security Descriptor</span></span>](using-iads-to-get-a-security-descriptor.md)
-   [<span data-ttu-id="17c06-119">使用 IDirectoryObject 取得安全描述項</span><span class="sxs-lookup"><span data-stu-id="17c06-119">Using IDirectoryObject to Get a Security Descriptor</span></span>](using-idirectoryobject-to-get-a-security-descriptor.md)
-   [<span data-ttu-id="17c06-120">安全描述項元件</span><span class="sxs-lookup"><span data-stu-id="17c06-120">Security Descriptor Components</span></span>](security-descriptor-components.md)
-   [<span data-ttu-id="17c06-121">正在抓取物件的 DACL</span><span class="sxs-lookup"><span data-stu-id="17c06-121">Retrieving an Object's DACL</span></span>](retrieving-an-objectampaposs-dacl.md)
-   [<span data-ttu-id="17c06-122">正在抓取物件的 SACL</span><span class="sxs-lookup"><span data-stu-id="17c06-122">Retrieving an Object's SACL</span></span>](retrieving-an-objectampaposs-sacl.md)
-   [<span data-ttu-id="17c06-123">讀取物件的安全描述項</span><span class="sxs-lookup"><span data-stu-id="17c06-123">Reading an Object's Security Descriptor</span></span>](reading-an-objectampaposs-security-descriptor.md)
-   [<span data-ttu-id="17c06-124">建立安全描述項的範例程式碼</span><span class="sxs-lookup"><span data-stu-id="17c06-124">Example Code for Creating a Security Descriptor</span></span>](example-code-for-creating-a-security-descriptor.md)
-   [<span data-ttu-id="17c06-125">列舉 Active Directory Domain Services 中物件之 ACL 的範例程式碼</span><span class="sxs-lookup"><span data-stu-id="17c06-125">Example Code for Enumerating the ACL of an Object in Active Directory Domain Services</span></span>](example-code-for-enumerating-the-acl-of-an-active-directory-object.md)

 

 