---
title: IADsDeleteOps 介面
description: IADsDeleteOps 介面用於基礎目錄存放區的監督和維護常式。 它可以在單一操作中刪除分葉物件和整個子樹。
ms.assetid: 821b71c2-e9f5-4ca8-9366-e8a3f1907670
ms.tgt_platform: multiple
keywords:
- IADsDeleteOps 介面 ADSI
- 使用 IADsDeleteOps ADSI
- ADSI ADSI，範例程式碼 C/c + +，使用 IADsDeleteOps 來刪除整個群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6332dd28e903996e8688d6c6fc672df080822595
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106964949"
---
# <a name="iadsdeleteops-interface"></a><span data-ttu-id="adea1-107">IADsDeleteOps 介面</span><span class="sxs-lookup"><span data-stu-id="adea1-107">IADsDeleteOps Interface</span></span>

<span data-ttu-id="adea1-108">[**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops)介面用於基礎目錄存放區的監督和維護常式。</span><span class="sxs-lookup"><span data-stu-id="adea1-108">The [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops) interface is used in supervisory and maintenance routines for the underlying directory store.</span></span> <span data-ttu-id="adea1-109">它可以在單一操作中刪除分葉物件和整個子樹。</span><span class="sxs-lookup"><span data-stu-id="adea1-109">It can delete leaf objects and entire subtrees in a single operation.</span></span>

<span data-ttu-id="adea1-110">如果不支援此介面，從 Active Directory 中刪除物件時，將需要以遞迴方式列舉和刪除每個包含的物件。</span><span class="sxs-lookup"><span data-stu-id="adea1-110">If this interface were not supported, deleting an object from Active Directory would require that each contained object be recursively enumerated and deleted.</span></span> <span data-ttu-id="adea1-111">使用這個介面時，可以使用單一作業來刪除任何容器物件及其所有包含的物件和子物件。</span><span class="sxs-lookup"><span data-stu-id="adea1-111">With this interface, any container object, with all its contained objects and subobjects, can be deleted with a single operation.</span></span>

<span data-ttu-id="adea1-112">下列程式碼範例會刪除 "Eng" 容器和所有子物件。</span><span class="sxs-lookup"><span data-stu-id="adea1-112">The following code example deletes the "Eng" container and all child objects.</span></span>


```C++
HRESULT hr;
IADsDeleteOps *pDeleteOps;
LPWSTR pwszUsername = NULL;
LPWSTR pwszPassword = NULL;

// Insert code to securely retrieve the pwszUsername and pwszPassword
// or leave as NULL to use the default security context of the 
// calling application.
 
// Bind to the LDAP provider.
hr = ADsOpenObject(L"LDAP://CN=Eng,CN=Users,DC=Fabrikam,DC=Com", 
    pwszUsername,
    pwszPassword,
    0,
    ADS_SECURE_AUTHENTICATION,
    IID_IADsDeleteOps, 
    (void**)&pDeleteOps);
if(S_OK == hr)
{
    // Delete the container and all child objects.
    pDeleteOps->DeleteObject(0);

    // Release the interface.
    pDeleteOps->Release();
}

if(pwszUsername)
{
    SecureZeroMemory(pwszUsername, lstrlen(pwszUsername) * sizeof(TCHAR));
}
if(pwszPassword)
{
    SecureZeroMemory(pwszPassword, lstrlen(pwszPassword) * sizeof(TCHAR));
}
```



<span data-ttu-id="adea1-113">下列程式碼範例會刪除 "Eng" 容器和所有子物件。</span><span class="sxs-lookup"><span data-stu-id="adea1-113">The following code example deletes the "Eng" container and all child objects.</span></span>


```VB
Dim DeleteOps As IADsDeleteOps

' Bind to the LDAP provider.
Set DeleteOps = GetObject("LDAP://CN=Eng,CN=Users,DC=Fabrikam,DC=Com")

' Delete the container and all child objects.
DeleteOps.DeleteObject (0)
```



 

 




