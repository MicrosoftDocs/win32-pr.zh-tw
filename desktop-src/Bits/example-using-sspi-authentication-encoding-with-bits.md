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
# <a name="example-using-sspi-authentication-encoding-with-bits"></a>範例：搭配 BITS 使用 SSPI 驗證編碼

您可以使用安全性支援提供者介面 (SSPI) 驗證和背景智慧型傳送服務 (位) 方法來取得使用者的認證、將認證編碼，以及在 BITS 傳送工作上設定編碼的認證。 需要編碼才能將認證結構轉換成可傳遞給 BITS 傳送工作的字串。

如需 SSPI 驗證和方法的詳細資訊，請參閱 [sspi](../secauthn/sspi.md)。

下列程式會使用 Negotiate 安全性封裝，提示使用者提供認證。 此程式會建立驗證身分識別結構，並使用代表使用者名稱、網域和使用者密碼的編碼字串來擴展結構。 然後，程式會建立 BITS 下載作業，並將編碼的使用者名稱和密碼設定為作業的認證。 程式不再需要驗證身分識別結構之後，就會將它釋出。

此範例會使用範例中所定義的標頭和執行 [：一般類別](common-classes.md)。

**搭配 BITS 傳送工作使用 SSPI 驗證編碼**

1.  藉由呼叫 CCoInitializer 函數來初始化 COM 參數。 如需 CCoInitializer 函數的詳細資訊，請參閱 [範例：通用類別](common-classes.md)。
2.  取得 [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)、 [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)、 [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) 介面的指標。 這個範例會使用 [CComPtr 類別](/cpp/atl/reference/ccomptr-class?view=vs-2019) 來管理 COM 介面指標。
3.  建立 [CREDUI \_ 資訊](/windows/win32/api/wincred/ns-wincred-credui_infoa) 結構，其中包含自訂 [SspiPromptForCredentials](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa)函式對話方塊外觀的資訊。 然後提示輸入使用者的認證。 如需詳細資訊，請參閱 [SspiPromptForCredentials 函數](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa)。
4.  使用 [SspiEncodeAuthIdentityAsStrings](/windows/win32/api/sspi/nf-sspi-sspiencodeauthidentityasstrings) 函式，將認證結構編碼為可傳遞至 BITS 傳送作業的字串。
5.  準備 [**BG \_ 驗證 \_**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) 認證結構。
6.  藉由呼叫 [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)來初始化 COM 進程安全性。 BITS 至少需要模擬的模擬層級。 如果未設定正確的模擬等級，則 BITS 會失敗，並出現 **E \_ ACCESSDENIED** 。
7.  藉由呼叫 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函數來取得 BITS 的初始定位器。
8.  藉由呼叫 [**IBackgroundCopyManager：： >batchclient.joboperations.createjob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) 方法來建立 BITS 傳送工作。
9.  取得 [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) 介面的識別碼，然後呼叫 **IBackgroundCopyJob：： QueryInterface** 方法。
10. 使用已編碼的使用者名稱和密碼字串來填入 [**BG \_ auth \_**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) 認證結構，並將驗證配置設定為 (**BG \_ AUTH authentication \_ 配置的 \_ 協商**) 。
11. 使用 [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) 指標對 BITS 提出要求。 此程式會使用 [**IBackgroundCopyJob2：： SetCredentials**](/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) 方法來設定 BITS 傳送工作的認證。
12. 新增檔案、修改屬性或繼續 BITS 傳送工作。
13. 在 BITS 傳送工作完成之後，請呼叫 [**IBackgroundCopyJob：： complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete)來移除佇列中的作業。
14. 最後，藉由呼叫 [SspiFreeAuthIdentity](/windows/win32/api/sspi/nf-sspi-sspifreeauthidentity) 函數來釋放驗證身分識別結構。

下列程式碼範例示範如何搭配 BITS 傳送工作使用 SSPI 驗證編碼。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[SSPI](../secauthn/sspi.md)
</dt> <dt>

[**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)
</dt> <dt>

[**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2)
</dt> <dt>

[範例：通用類別](common-classes.md)
</dt> </dl>

 

 