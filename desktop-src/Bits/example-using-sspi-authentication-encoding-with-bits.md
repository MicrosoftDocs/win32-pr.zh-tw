---
title: 使用 SSPI 驗證編碼與 BITS 的範例
description: 您可以使用安全性支援提供者介面 (SSPI) 驗證和背景智慧型傳送服務 (位) 方法來取得使用者的認證、將認證編碼，以及在 BITS 傳送工作上設定編碼的認證。
ms.assetid: 5c8a6df7-0056-463e-8d73-1695dc75e023
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b86248c4782789010a817755d9bc27b3e5373b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103683073"
---
# <a name="example-using-sspi-authentication-encoding-with-bits"></a><span data-ttu-id="4d85c-103">範例：搭配 BITS 使用 SSPI 驗證編碼</span><span class="sxs-lookup"><span data-stu-id="4d85c-103">Example: Using SSPI Authentication Encoding with BITS</span></span>

<span data-ttu-id="4d85c-104">您可以使用安全性支援提供者介面 (SSPI) 驗證和背景智慧型傳送服務 (位) 方法來取得使用者的認證、將認證編碼，以及在 BITS 傳送工作上設定編碼的認證。</span><span class="sxs-lookup"><span data-stu-id="4d85c-104">You can use Security Support Provider Interface (SSPI) Authentication and Background Intelligent Transfer Service (BITS) methods to get the credentials from a user, encode the credentials, and set the encoded credentials on a BITS transfer job.</span></span> <span data-ttu-id="4d85c-105">需要編碼才能將認證結構轉換成可傳遞給 BITS 傳送工作的字串。</span><span class="sxs-lookup"><span data-stu-id="4d85c-105">Encoding is required to convert credentials structure into strings that can be passed to a BITS transfer job.</span></span>

<span data-ttu-id="4d85c-106">如需 SSPI 驗證和方法的詳細資訊，請參閱 [sspi](../secauthn/sspi.md)。</span><span class="sxs-lookup"><span data-stu-id="4d85c-106">For more information about SSPI authentication and methods, see [SSPI](../secauthn/sspi.md).</span></span>

<span data-ttu-id="4d85c-107">下列程式會使用 Negotiate 安全性封裝，提示使用者提供認證。</span><span class="sxs-lookup"><span data-stu-id="4d85c-107">The following procedure prompts for credentials from the user by using the Negotiate security package.</span></span> <span data-ttu-id="4d85c-108">此程式會建立驗證身分識別結構，並使用代表使用者名稱、網域和使用者密碼的編碼字串來擴展結構。</span><span class="sxs-lookup"><span data-stu-id="4d85c-108">The program creates an authentication identity structure and populates the structure with the encoded strings that represent the user name, domain, and password of the user.</span></span> <span data-ttu-id="4d85c-109">然後，程式會建立 BITS 下載作業，並將編碼的使用者名稱和密碼設定為作業的認證。</span><span class="sxs-lookup"><span data-stu-id="4d85c-109">Then the program creates a BITS download job and sets the encoded user name and password as the credentials for the job.</span></span> <span data-ttu-id="4d85c-110">程式不再需要驗證身分識別結構之後，就會將它釋出。</span><span class="sxs-lookup"><span data-stu-id="4d85c-110">The program frees the authentication identity structure after it is no longer needed.</span></span>

<span data-ttu-id="4d85c-111">此範例會使用範例中所定義的標頭和執行 [：一般類別](common-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="4d85c-111">This example uses the header and implementation defined in [Example: Common Classes](common-classes.md).</span></span>

<span data-ttu-id="4d85c-112">**搭配 BITS 傳送工作使用 SSPI 驗證編碼**</span><span class="sxs-lookup"><span data-stu-id="4d85c-112">**To use SSPI authentication encoding with BITS transfer jobs**</span></span>

1.  <span data-ttu-id="4d85c-113">藉由呼叫 CCoInitializer 函數來初始化 COM 參數。</span><span class="sxs-lookup"><span data-stu-id="4d85c-113">Initialize COM parameters by calling the CCoInitializer function.</span></span> <span data-ttu-id="4d85c-114">如需 CCoInitializer 函數的詳細資訊，請參閱 [範例：通用類別](common-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="4d85c-114">For more information about the CCoInitializer function, see [Example: Common Classes](common-classes.md).</span></span>
2.  <span data-ttu-id="4d85c-115">取得 [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)、 [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)、 [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="4d85c-115">Get pointers for the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager), [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob), [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) interfaces.</span></span> <span data-ttu-id="4d85c-116">這個範例會使用 [CComPtr 類別](/cpp/atl/reference/ccomptr-class?view=vs-2019) 來管理 COM 介面指標。</span><span class="sxs-lookup"><span data-stu-id="4d85c-116">This example uses the [CComPtr Class](/cpp/atl/reference/ccomptr-class?view=vs-2019) to manage COM interface pointers.</span></span>
3.  <span data-ttu-id="4d85c-117">建立 [CREDUI \_ 資訊](/windows/win32/api/wincred/ns-wincred-credui_infoa) 結構，其中包含自訂 [SspiPromptForCredentials](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa)函式對話方塊外觀的資訊。</span><span class="sxs-lookup"><span data-stu-id="4d85c-117">Create a [CREDUI\_INFO](/windows/win32/api/wincred/ns-wincred-credui_infoa) structure that contains information for customizing the appearance of the dialog box for the [SspiPromptForCredentials Function](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa).</span></span> <span data-ttu-id="4d85c-118">然後提示輸入使用者的認證。</span><span class="sxs-lookup"><span data-stu-id="4d85c-118">Then prompt for credentials from the user.</span></span> <span data-ttu-id="4d85c-119">如需詳細資訊，請參閱 [SspiPromptForCredentials 函數](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa)。</span><span class="sxs-lookup"><span data-stu-id="4d85c-119">For more information, see the [SspiPromptForCredentials Function](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa).</span></span>
4.  <span data-ttu-id="4d85c-120">使用 [SspiEncodeAuthIdentityAsStrings](/windows/win32/api/sspi/nf-sspi-sspiencodeauthidentityasstrings) 函式，將認證結構編碼為可傳遞至 BITS 傳送作業的字串。</span><span class="sxs-lookup"><span data-stu-id="4d85c-120">Encode credential structure as strings that can be passed to a BITS transfer job by using the [SspiEncodeAuthIdentityAsStrings](/windows/win32/api/sspi/nf-sspi-sspiencodeauthidentityasstrings) function.</span></span>
5.  <span data-ttu-id="4d85c-121">準備 [**BG \_ 驗證 \_**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) 認證結構。</span><span class="sxs-lookup"><span data-stu-id="4d85c-121">Prepare a [**BG\_AUTH\_CREDENTIALS**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) structure.</span></span>
6.  <span data-ttu-id="4d85c-122">藉由呼叫 [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)來初始化 COM 進程安全性。</span><span class="sxs-lookup"><span data-stu-id="4d85c-122">Initialize COM process security by calling [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="4d85c-123">BITS 至少需要模擬的模擬層級。</span><span class="sxs-lookup"><span data-stu-id="4d85c-123">BITS requires at least the IMPERSONATE level of impersonation.</span></span> <span data-ttu-id="4d85c-124">如果未設定正確的模擬等級，則 BITS 會失敗，並出現 **E \_ ACCESSDENIED** 。</span><span class="sxs-lookup"><span data-stu-id="4d85c-124">BITS fails with **E\_ACCESSDENIED** if the correct impersonation level is not set.</span></span>
7.  <span data-ttu-id="4d85c-125">藉由呼叫 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函數來取得 BITS 的初始定位器。</span><span class="sxs-lookup"><span data-stu-id="4d85c-125">Obtain the initial locator to BITS by calling the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>
8.  <span data-ttu-id="4d85c-126">藉由呼叫 [**IBackgroundCopyManager：： >batchclient.joboperations.createjob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) 方法來建立 BITS 傳送工作。</span><span class="sxs-lookup"><span data-stu-id="4d85c-126">Create a BITS transfer job by calling the [**IBackgroundCopyManager::CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method.</span></span>
9.  <span data-ttu-id="4d85c-127">取得 [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) 介面的識別碼，然後呼叫 **IBackgroundCopyJob：： QueryInterface** 方法。</span><span class="sxs-lookup"><span data-stu-id="4d85c-127">Get the identifier for the [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) interface, and call the **IBackgroundCopyJob::QueryInterface** method.</span></span>
10. <span data-ttu-id="4d85c-128">使用已編碼的使用者名稱和密碼字串來填入 [**BG \_ auth \_**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) 認證結構，並將驗證配置設定為 (**BG \_ AUTH authentication \_ 配置的 \_ 協商**) 。</span><span class="sxs-lookup"><span data-stu-id="4d85c-128">Populate the [**BG\_AUTH\_CREDENTIALS**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) structure with the encoded user name and password strings, and set the authentication scheme to Negotiate (**BG\_AUTH\_SCHEME\_NEGOTIATE**).</span></span>
11. <span data-ttu-id="4d85c-129">使用 [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) 指標對 BITS 提出要求。</span><span class="sxs-lookup"><span data-stu-id="4d85c-129">Use the [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) pointer to make requests to BITS.</span></span> <span data-ttu-id="4d85c-130">此程式會使用 [**IBackgroundCopyJob2：： SetCredentials**](/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) 方法來設定 BITS 傳送工作的認證。</span><span class="sxs-lookup"><span data-stu-id="4d85c-130">This program uses the [**IBackgroundCopyJob2::SetCredentials**](/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) method to set the credentials for the BITS transfer job.</span></span>
12. <span data-ttu-id="4d85c-131">新增檔案、修改屬性或繼續 BITS 傳送工作。</span><span class="sxs-lookup"><span data-stu-id="4d85c-131">Add files, modify properties, or resume the BITS transfer job.</span></span>
13. <span data-ttu-id="4d85c-132">在 BITS 傳送工作完成之後，請呼叫 [**IBackgroundCopyJob：： complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete)來移除佇列中的作業。</span><span class="sxs-lookup"><span data-stu-id="4d85c-132">After the BITS transfer job is complete, remove the job from the queue by calling [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span></span>
14. <span data-ttu-id="4d85c-133">最後，藉由呼叫 [SspiFreeAuthIdentity](/windows/win32/api/sspi/nf-sspi-sspifreeauthidentity) 函數來釋放驗證身分識別結構。</span><span class="sxs-lookup"><span data-stu-id="4d85c-133">Finally, free the authentication identity structure by calling the [SspiFreeAuthIdentity](/windows/win32/api/sspi/nf-sspi-sspifreeauthidentity) function.</span></span>

<span data-ttu-id="4d85c-134">下列程式碼範例示範如何搭配 BITS 傳送工作使用 SSPI 驗證編碼。</span><span class="sxs-lookup"><span data-stu-id="4d85c-134">The following code example demonstrates how to use SSPI Authentication Encoding with BITS transfer jobs.</span></span>


```C++
#define SECURITY_WIN32
#define _SEC_WINNT_AUTH_TYPES

#include <windows.h>
#include <ntsecapi.h>
#include <bits.h>
#include <sspi.h>
#include <wincred.h>
#include <iostream>
#include <atlbase.h>
#include "CommonCode.h"

void PromptForCredentials(PWSTR pwTargetName)
{
    HRESULT hr;
    
    // If CoInitializeEx fails, the exception is unhandled and the program terminates
    CCoInitializer coInitializer(COINIT_APARTMENTTHREADED);
    
    CComPtr<IBackgroundCopyManager> pQueueMgr;
    CComPtr<IBackgroundCopyJob> pJob;
    CComPtr<IBackgroundCopyJob2> pJob2;

    PSEC_WINNT_AUTH_IDENTITY_OPAQUE pAuthIdentityEx2 = NULL;
    DWORD dwFlags = 0;
    BOOL fSave = FALSE;
    BOOL bReturn = TRUE;

    CREDUI_INFO creduiInfo = { 0 };
    creduiInfo.cbSize = sizeof(creduiInfo);
    // Change the message text and caption to the actual text for your dialog.
    creduiInfo.pszMessageText = pwTargetName;
    creduiInfo.pszCaptionText = L"SSPIPFC title for the dialog box";

    try {
        // Prompt for credentials from user using Negotiate security package.
        DWORD dwRet = SspiPromptForCredentials(
            pwTargetName,
            &creduiInfo,
            0,
            L"Negotiate", 
            NULL,
            &pAuthIdentityEx2,
            &fSave,
            dwFlags
            );

        if (SEC_E_OK != dwRet) 
        {
            // Prompt for credentials failed.
            throw MyException(dwRet, L"SspiPromptForCredentials");
        }

        if (NULL != pAuthIdentityEx2) 
        {
            GUID guidJob;
            BG_AUTH_CREDENTIALS authCreds;

            PCWSTR pwUserName = NULL;
            PCWSTR pwDomainName = NULL;
            PCWSTR pwPassword = NULL;

            // Encode credential structure as strings that can
            // be passed to a BITS job.
            SECURITY_STATUS secStatus = SspiEncodeAuthIdentityAsStrings(
                pAuthIdentityEx2,
                &pwUserName,
                &pwDomainName,
                &pwPassword
                );

            if(SEC_E_OK != secStatus) 
            {
                // Encode authentication identity as strings.
                throw MyException(secStatus, L"SspiEncodeAuthIdentityAsStrings");   
            }

            // Show the encoded user name and domain name.
            wprintf(
                L"User Name: %s\nDomain Name: %s",
                pwUserName,
                pwDomainName
                );

            //The impersonation level must be at least RPC_C_IMP_LEVEL_IMPERSONATE.
            HRESULT hr = CoInitializeSecurity(
                NULL,
                -1,
                NULL,
                NULL,
                RPC_C_AUTHN_LEVEL_CONNECT,
                RPC_C_IMP_LEVEL_IMPERSONATE,
                NULL,
                EOAC_DYNAMIC_CLOAKING,
                0
                );
            
            if (FAILED(hr))
            {
                throw MyException(hr, L"CoInitializeSecurity");
            }

            // Connect to BITS.
            hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
                CLSCTX_LOCAL_SERVER,
                __uuidof(IBackgroundCopyManager),
                (void**) &pQueueMgr);

            if (FAILED(hr))
            {
                // Failed to connect.
                throw MyException(hr, L"CoCreateInstance");
            }

            // Create a job.
            hr = pQueueMgr->CreateJob(
                L"EncodeSample", 
                BG_JOB_TYPE_DOWNLOAD, 
                &guidJob, 
                &pJob
                );

            if(FAILED(hr))
            {   
                // Failed to create a BITS job.
                throw MyException(hr, L"CreateJob");
            }

            // Get IBackgroundCopyJob2 interface.
            hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
            if (FAILED(hr)) 
            {
                // Failed to get a reference to the IBackgroundCopyJob2 interface.
                throw MyException(hr, L"QueryInterface(IBackgroundCopyJob2)");
            }

            // Create a BITS authentication structure from the encoded strings.
            authCreds.Target = BG_AUTH_TARGET_SERVER;
            authCreds.Scheme = BG_AUTH_SCHEME_NEGOTIATE;
            authCreds.Credentials.Basic.UserName = (LPWSTR)pwUserName;
            authCreds.Credentials.Basic.Password = (LPWSTR)pwPassword;

            // Set the credentials for the job.
            hr = pJob2->SetCredentials(&authCreds);
            if (FAILED(hr)) 
            {
                // Failed to set credentials.
                throw MyException(hr, L"SetCredentials");
            }

            // Modify the job's property values.
            // Add files to the job.
            // Activate (resume) the job in the transfer queue.

            // Remove the job from the transfer queue.
            hr = pJob->Complete();
            if (FAILED(hr)) 
            {
                // Failed to complete the job.
                throw MyException(hr, L"Complete");
            }
        }
    }
    catch(std::bad_alloc &)
    {
        wprintf(L"Memory allocation failed");
        if (pJob != NULL)
        {
            pJob->Cancel();
        }
    }
    catch(MyException &ex)
    {
        wprintf(L"Error %x occurred during operation", ex.Error);
        if (pJob != NULL)
        {
            pJob->Cancel();
        }
    }

    // Free the auth identity structure.
    if (NULL != pAuthIdentityEx2)
    {
        SspiFreeAuthIdentity(pAuthIdentityEx2);
        pAuthIdentityEx2 = NULL;
    }

    return;
}

void _cdecl _tmain(int argc, LPWSTR* argv)
{
    PromptForCredentials(L"Target");
}
```



## <a name="related-topics"></a><span data-ttu-id="4d85c-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="4d85c-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d85c-136">SSPI</span><span class="sxs-lookup"><span data-stu-id="4d85c-136">SSPI</span></span>](../secauthn/sspi.md)
</dt> <dt>

[<span data-ttu-id="4d85c-137">**IBackgroundCopyManager**</span><span class="sxs-lookup"><span data-stu-id="4d85c-137">**IBackgroundCopyManager**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)
</dt> <dt>

[<span data-ttu-id="4d85c-138">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="4d85c-138">**IBackgroundCopyJob**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[<span data-ttu-id="4d85c-139">**IBackgroundCopyJob2**</span><span class="sxs-lookup"><span data-stu-id="4d85c-139">**IBackgroundCopyJob2**</span></span>](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2)
</dt> <dt>

[<span data-ttu-id="4d85c-140">範例：通用類別</span><span class="sxs-lookup"><span data-stu-id="4d85c-140">Example: Common Classes</span></span>](common-classes.md)
</dt> </dl>

 

 