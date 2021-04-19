---
description: LSA 提供的函式可讓系統管理員用來查詢和設定本機電腦和網域的全域原則資訊。
ms.assetid: bbe27d16-0a6b-435a-ae80-5e983047b511
title: 管理原則資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fdc76137f41c592370dbeecafd243f11012cb1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988366"
---
# <a name="managing-policy-information"></a><span data-ttu-id="6941e-103">管理原則資訊</span><span class="sxs-lookup"><span data-stu-id="6941e-103">Managing Policy Information</span></span>

<span data-ttu-id="6941e-104">LSA 提供的函式可讓系統管理員用來查詢和設定本機電腦和網域的全域原則資訊。</span><span class="sxs-lookup"><span data-stu-id="6941e-104">The LSA provides functions that administrators can use to query and set global policy information for the local computer and the domain.</span></span>

<span data-ttu-id="6941e-105">在您可以管理原則資訊之前，您的應用程式必須先取得本機 [**原則**](policy-object.md) 物件的控制碼，如 [開啟原則物件控制碼](opening-a-policy-object-handle.md)所示範。</span><span class="sxs-lookup"><span data-stu-id="6941e-105">Before you can manage policy information, your application must get a handle to the local [**Policy**](policy-object.md) object, as demonstrated in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span> <span data-ttu-id="6941e-106">管理原則資訊的函式需要此控制碼。</span><span class="sxs-lookup"><span data-stu-id="6941e-106">This handle is required by the functions that manage policy information.</span></span>

<span data-ttu-id="6941e-107">若要取得本機安全性原則的相關資訊，請呼叫 [**LsaQueryInformationPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy)。</span><span class="sxs-lookup"><span data-stu-id="6941e-107">To retrieve information about the local security policy, call [**LsaQueryInformationPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy).</span></span> <span data-ttu-id="6941e-108">若要設定本機安全性原則，請呼叫 [**LsaSetInformationPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasetinformationpolicy)。</span><span class="sxs-lookup"><span data-stu-id="6941e-108">To set local security policy, call [**LsaSetInformationPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasetinformationpolicy).</span></span> <span data-ttu-id="6941e-109">[**原則 \_ 資訊 \_ 類別**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class)列舉的描述會詳細說明可查詢或設定的原則資訊類型。</span><span class="sxs-lookup"><span data-stu-id="6941e-109">The description of the [**POLICY\_INFORMATION\_CLASS**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class) enumeration details the types of policy information that can be queried or set.</span></span>

<span data-ttu-id="6941e-110">下列範例示範如何取得系統的帳戶網域資訊，並提供系統的 [**原則**](policy-object.md) 物件控制碼。</span><span class="sxs-lookup"><span data-stu-id="6941e-110">The following example demonstrates how to obtain a system's account domain information, given a handle to the system's [**Policy**](policy-object.md) object.</span></span>


```C++
#include <windows.h>

BOOL GetAccountDomainInfo(LSA_HANDLE PolicyHandle)
{
  NTSTATUS ntsResult = STATUS_SUCCESS;
  PPOLICY_ACCOUNT_DOMAIN_INFO pPADInfo = NULL;
  PWCHAR name = NULL;
  UINT nameSize;
  
  ntsResult = LsaQueryInformationPolicy(
    PolicyHandle,                   // Open handle to a Policy object.
    PolicyAccountDomainInformation, // The information to get.
    (PVOID *)&pPADInfo              // Storage for the information.
  );

  if (ntsResult == STATUS_SUCCESS)
  {  
    // There is no guarantee that the LSA_UNICODE_STRING buffer
    // is null-terminated, so copy the name to a buffer that is.
    nameSize =  pPADInfo->DomainName.Length + 1 * sizeof(WCHAR);
    name = (WCHAR *) LocalAlloc(LPTR, nameSize);
    if (!name)
    {
        wprintf(L"Failed LocalAlloc\n");
        exit(1);
    }
    wcsncpy_s(name, nameSize, pPADInfo->DomainName.Buffer,
        pPADInfo->DomainName.Length);
    wprintf(L"The account domain name is %ws\n", name);
    LocalFree(name);
    if (STATUS_SUCCESS != LsaFreeMemory(pPADInfo))
        wprintf(L"LsaFreeMemory error\n");
  }
  else
  {
    // Show the corresponding win32 error code.
    wprintf(
        L"Error obtaining account domain information - (win32) %lu\n",
        LsaNtStatusToWinError(ntsResult));
  }

  return !ntsResult;
}

```



 

 
