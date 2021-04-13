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
ms.openlocfilehash: 3db74cb235b5cb322f0edf3dc4cfb32f50b4c00c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104314608"
---
# <a name="retrieving-an-objects-dacl"></a><span data-ttu-id="0cc32-105">正在抓取物件的 DACL</span><span class="sxs-lookup"><span data-stu-id="0cc32-105">Retrieving an Object's DACL</span></span>

<span data-ttu-id="0cc32-106">物件的安全描述項可能包含 (DACL) 的任意存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="0cc32-106">An object's security descriptor may contain a discretionary access-control list (DACL).</span></span> <span data-ttu-id="0cc32-107">DACL 包含零或多個存取控制專案 (Ace) 可識別可存取物件的使用者和群組。</span><span class="sxs-lookup"><span data-stu-id="0cc32-107">A DACL contains zero or more access-control entries (ACEs) that identify the users and groups who can access the object.</span></span> <span data-ttu-id="0cc32-108">如果 DACL 是空的 (也就是說，它包含零個 Ace) ，沒有明確授與存取權，因此會隱含拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="0cc32-108">If a DACL is empty (that is, it contains zero ACEs), no access is explicitly granted, so access is implicitly denied.</span></span> <span data-ttu-id="0cc32-109">但是，如果物件的安全描述項沒有 DACL，則物件會受到保護，且每個人都有完整的存取權。</span><span class="sxs-lookup"><span data-stu-id="0cc32-109">However, if an object's security descriptor does not have a DACL, the object is unprotected and everyone has complete access.</span></span>

<span data-ttu-id="0cc32-110">若要抓取物件的 DACL，您必須是物件的擁有者，或擁有物件的 **讀取 \_ 控制** 存取權。</span><span class="sxs-lookup"><span data-stu-id="0cc32-110">To retrieve an object's DACL, you must be the object's owner or have **READ\_CONTROL** access to the object.</span></span>

<span data-ttu-id="0cc32-111">若要取得並設定目錄物件的 DACL，請使用 [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) 介面。</span><span class="sxs-lookup"><span data-stu-id="0cc32-111">To get and set the DACL of a directory object, use the [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) interface.</span></span> <span data-ttu-id="0cc32-112">使用 c + +， [**IADsSecurityDescriptor：： get \_ objdescriptor.discretionaryacl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) 方法會傳回 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 指標。</span><span class="sxs-lookup"><span data-stu-id="0cc32-112">Using C++, the [**IADsSecurityDescriptor::get\_DiscretionaryAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) method returns an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointer.</span></span> <span data-ttu-id="0cc32-113">在該 **IDispatch** 指標上呼叫 **QueryInterface** 以取得 [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)介面，並在該介面上使用方法來存取 DACL 中的個別 ace。</span><span class="sxs-lookup"><span data-stu-id="0cc32-113">Call **QueryInterface** on that **IDispatch** pointer to get an [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) interface, and use the methods on that interface to access the individual ACEs in the DACL.</span></span> <span data-ttu-id="0cc32-114">修改 DACL 的程式描述于 [設定物件的存取權限](setting-access-rights-on-an-object.md)。</span><span class="sxs-lookup"><span data-stu-id="0cc32-114">The procedure for modifying a DACL is described in [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="0cc32-115">若要列舉 Ace，請使用 [**IADsAccessControlList：： get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-get__newenum)方法。</span><span class="sxs-lookup"><span data-stu-id="0cc32-115">To enumerate the ACEs, use the [**IADsAccessControlList::get\_\_NewEnum**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-get__newenum) method.</span></span> <span data-ttu-id="0cc32-116">方法會傳回 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 指標。</span><span class="sxs-lookup"><span data-stu-id="0cc32-116">The method returns an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer.</span></span> <span data-ttu-id="0cc32-117">呼叫該 **IUnknown** 指標上的 **QueryInterface** 來取得 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)介面。</span><span class="sxs-lookup"><span data-stu-id="0cc32-117">Call **QueryInterface** on that **IUnknown** pointer to get an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface.</span></span> <span data-ttu-id="0cc32-118">使用 [**IEnumVARIANT：： Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) 方法來列舉 ACL 中的 ace。</span><span class="sxs-lookup"><span data-stu-id="0cc32-118">Use the [**IEnumVARIANT::Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) method to enumerate the ACEs in the ACL.</span></span> <span data-ttu-id="0cc32-119">每個 ACE 都會以包含 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)指標的 **VARIANT** 傳回， (**vt** 成員是 **vt \_ 分派**) 。</span><span class="sxs-lookup"><span data-stu-id="0cc32-119">Each ACE is returned as a **VARIANT** containing an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointer (the **vt** member is **VT\_DISPATCH**).</span></span> <span data-ttu-id="0cc32-120">在該 **IDispatch** 指標上呼叫 **QueryInterface** ，以取得 ACE 的 [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry)介面。</span><span class="sxs-lookup"><span data-stu-id="0cc32-120">Call **QueryInterface** on that **IDispatch** pointer to get an [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) interface for the ACE.</span></span> <span data-ttu-id="0cc32-121">您可以使用 **IADsAccessControlEntry** 介面的方法來設定或取得 ACE 的元件。</span><span class="sxs-lookup"><span data-stu-id="0cc32-121">You can use the methods of the **IADsAccessControlEntry** interface to set or retrieve the components of an ACE.</span></span>

<span data-ttu-id="0cc32-122">如需有關 Dacl 和 Ace 的詳細資訊，請參閱平臺軟體發展工具組中的下列主題 (SDK) 。</span><span class="sxs-lookup"><span data-stu-id="0cc32-122">For more information about DACLs and ACEs, see the following topics in the Platform Software Development Kit (SDK).</span></span>

-   [<span data-ttu-id="0cc32-123"> (Acl 的存取控制清單) </span><span class="sxs-lookup"><span data-stu-id="0cc32-123">Access-Control Lists (ACLs)</span></span>](/windows/desktop/SecAuthZ/access-control-lists)
-   [<span data-ttu-id="0cc32-124"> (Ace 的存取控制專案) </span><span class="sxs-lookup"><span data-stu-id="0cc32-124">Access-Control Entries (ACEs)</span></span>](/windows/desktop/SecAuthZ/access-control-entries)

 

 