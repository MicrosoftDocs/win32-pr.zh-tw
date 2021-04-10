---
description: 自動登入密碼應該使用 LsaStorePrivateData 函式來保護。
ms.assetid: 7bd4d725-de17-4801-bd06-8d47a777409d
title: 保護自動登入密碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25508af4de64554e664426db3e786a1eca34579b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944971"
---
# <a name="protecting-the-automatic-logon-password"></a><span data-ttu-id="6cf1d-103">保護自動登入密碼</span><span class="sxs-lookup"><span data-stu-id="6cf1d-103">Protecting the Automatic Logon Password</span></span>

<span data-ttu-id="6cf1d-104">自動登入密碼應該使用 [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) 函式來保護。</span><span class="sxs-lookup"><span data-stu-id="6cf1d-104">The automatic logon password should be protected by using the [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) function.</span></span>

<span data-ttu-id="6cf1d-105">下列範例顯示如何保護自動登入密碼。</span><span class="sxs-lookup"><span data-stu-id="6cf1d-105">The following example shows how to protect the automatic logon password.</span></span> <span data-ttu-id="6cf1d-106">此範例會藉由呼叫 [**LsaOpenPolicy**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopenpolicy)函式，來抓取 [**原則**](../secmgmt/policy-object.md)物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6cf1d-106">The example retrieves a handle to the [**Policy**](../secmgmt/policy-object.md) object by calling the [**LsaOpenPolicy**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopenpolicy) function.</span></span> <span data-ttu-id="6cf1d-107">如需 **原則** 物件和 **原則** 物件控制碼的詳細資訊，請分別參閱 **原則** 物件和 [開啟原則物件控制碼](../secmgmt/opening-a-policy-object-handle.md)。</span><span class="sxs-lookup"><span data-stu-id="6cf1d-107">For more information about the **Policy** object and **Policy** object handles, see **Policy** object and [Opening a Policy Object Handle](../secmgmt/opening-a-policy-object-handle.md), respectively.</span></span> <span data-ttu-id="6cf1d-108">然後，此範例會藉由呼叫 [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) 函數來設定受保護的密碼。</span><span class="sxs-lookup"><span data-stu-id="6cf1d-108">The example then sets the protected password by calling the [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) function.</span></span> <span data-ttu-id="6cf1d-109">請注意，如果呼叫者針對受保護的密碼值傳遞 **Null** ，則程式碼會清除現有受保護的密碼。</span><span class="sxs-lookup"><span data-stu-id="6cf1d-109">Note that if the caller passes in **NULL** for the protected password value, then the code clears the existing protected password.</span></span> <span data-ttu-id="6cf1d-110">在結束之前，程式碼會關閉 **原則** 物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6cf1d-110">Before exiting, the code closes the handle to the **Policy** object.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

DWORD UpdateDefaultPassword(WCHAR * pwszSecret)
{

    LSA_OBJECT_ATTRIBUTES ObjectAttributes;
    LSA_HANDLE LsaPolicyHandle = NULL;

    LSA_UNICODE_STRING lusSecretName;
    LSA_UNICODE_STRING lusSecretData;
    USHORT SecretNameLength;
    USHORT SecretDataLength;

    NTSTATUS ntsResult = STATUS_SUCCESS;
    DWORD dwRetCode = ERROR_SUCCESS;

    //  Object attributes are reserved, so initialize to zeros.
    ZeroMemory(&ObjectAttributes, sizeof(ObjectAttributes));

    //  Get a handle to the Policy object.
    ntsResult = LsaOpenPolicy(
        NULL,    // local machine
        &ObjectAttributes, 
        POLICY_CREATE_SECRET,
        &LsaPolicyHandle);

    if( STATUS_SUCCESS != ntsResult )
    {
        //  An error occurred. Display it as a win32 error code.
        dwRetCode = LsaNtStatusToWinError(ntsResult);
        wprintf(L"Failed call to LsaOpenPolicy %lu\n", dwRetCode);
        return dwRetCode;
    } 

    //  Initialize an LSA_UNICODE_STRING for the name of the
    //  private data ("DefaultPassword").
    SecretNameLength = (USHORT)wcslen(L"DefaultPassword");
    lusSecretName.Buffer = L"DefaultPassword";
    lusSecretName.Length = SecretNameLength * sizeof(WCHAR);
    lusSecretName.MaximumLength =
        (SecretNameLength+1) * sizeof(WCHAR);

    //  If the pwszSecret parameter is NULL, then clear the secret.
    if( NULL == pwszSecret )
    {
        wprintf(L"Clearing the secret...\n");
        ntsResult = LsaStorePrivateData(
            LsaPolicyHandle,
            &lusSecretName,
            NULL);
        dwRetCode = LsaNtStatusToWinError(ntsResult);
    }
    else
    {
        wprintf(L"Setting the secret...\n");
        //  Initialize an LSA_UNICODE_STRING for the value
        //  of the private data. 
        SecretDataLength = (USHORT)wcslen(pwszSecret);
        lusSecretData.Buffer = pwszSecret;
        lusSecretData.Length = SecretDataLength * sizeof(WCHAR);
        lusSecretData.MaximumLength =
            (SecretDataLength+1) * sizeof(WCHAR);
        ntsResult = LsaStorePrivateData(
            LsaPolicyHandle,
            &lusSecretName,
            &lusSecretData);
        dwRetCode = LsaNtStatusToWinError(ntsResult);
    }

    LsaClose(LsaPolicyHandle);

    if (dwRetCode != ERROR_SUCCESS)
        wprintf(L"Failed call to LsaStorePrivateData %lu\n",
            dwRetCode);
    
    return dwRetCode;

}

```



<span data-ttu-id="6cf1d-111">請注意，如果 Winlogon 找不到 [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) 函式所儲存的密碼，則會使用 winlogon 金鑰的 **DefaultPassword** 值 (如果存在於自動登入密碼) 。</span><span class="sxs-lookup"><span data-stu-id="6cf1d-111">Note that if Winlogon cannot find a password stored by the [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) function, it will use the **DefaultPassword** value of the Winlogon key (if it exists) for the automatic logon password.</span></span>

<span data-ttu-id="6cf1d-112">如需自動登入和 Winlogon 登錄機碼的詳細資訊，請參閱 [MSGina.dll 功能](msgina-dll-features.md)。</span><span class="sxs-lookup"><span data-stu-id="6cf1d-112">For more information about automatic logon and the Winlogon registry key, see [MSGina.dll Features](msgina-dll-features.md).</span></span>

<span data-ttu-id="6cf1d-113">如需保護密碼的詳細資訊，請參閱 [處理密碼](../secbp/handling-passwords.md)。</span><span class="sxs-lookup"><span data-stu-id="6cf1d-113">For more information about protecting passwords, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

 

 
