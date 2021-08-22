---
title: 將 Helper 權杖新增至 BITS 傳送工作的範例
description: 您可以使用額外的安全性權杖，設定背景智慧型傳送服務 (位) 的傳送作業。 BITS 傳送工作會使用此協助程式權杖進行驗證並存取資源。
ms.assetid: 08670c6d-e589-41be-842d-597f460d9c97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4adab6ca8cebeeca9b9883e89db28205dfdab1ea43e05c01fd119c14c26d374
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528818"
---
# <a name="example-adding-a-helper-token-to-a-bits-transfer-job"></a>範例：將 Helper 權杖新增至 BITS 傳送工作

您可以使用額外的安全性權杖，設定背景智慧型傳送服務 (位) 的傳送作業。 BITS 傳送工作會使用此協助程式權杖進行驗證並存取資源。

如需詳細資訊，請參閱 [BITS 傳送工作的協助程式權杖](helper-tokens-for-bits-transfer-jobs.md)。

下列程式會在本機使用者的內容中建立 BITS 傳送工作、取得第二位使用者的認證、使用這些認證建立 helper 權杖，然後在 BITS 傳送工作上設定協助程式權杖。

此範例會使用範例中所定義的標頭和執行 [：一般類別](common-classes.md)。

**將 helper 權杖新增至 BITS 傳送工作**

1.  藉由呼叫 CCoInitializer 函數來初始化 COM 參數。 如需 CCoInitializer 函數的詳細資訊，請參閱 [範例：通用類別](common-classes.md)。
2.  取得 [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) 介面的指標。 這個範例會使用 [CComPtr 類別](/cpp/atl/reference/ccomptr-class?view=vs-2019) 來管理 COM 介面指標。
3.  藉由呼叫 [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)來初始化 COM 進程安全性。 BITS 至少需要模擬的模擬層級。 如果未設定正確的模擬等級，則 BITS 會失敗，並出現 E \_ ACCESSDENIED。
4.  取得 [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) 介面的指標，並藉由呼叫 [COCREATEINSTANCE]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函數取得位的初始定位器。
5.  藉由呼叫 [**IBackgroundCopyManager：： >batchclient.joboperations.createjob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) 方法來建立 BITS 傳送工作。
6.  取得 CNotifyInterface 回呼介面的指標，然後呼叫 [**IBackgroundCopyJob：： SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) 方法以接收作業相關事件的通知。 如需 CNotifyInterface 的詳細資訊，請參閱 [範例：通用類別](common-classes.md)。
7.  呼叫 [**IBackgroundCopyJob：： SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) 方法，以設定要接收的通知類型。 在此範例中，會設定「 **bg \_ 通知 \_ 作業已 \_ 傳送** 」和「 **bg \_ 通知 \_ 工作」 \_ 錯誤** 旗標。
8.  呼叫具有適當介面識別碼的 **IBackgroundCopyJob：： QueryInterface** 方法，以取得 [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)介面的指標。
9.  嘗試登入 helper 權杖的使用者。 建立模擬控制碼，並呼叫 [LogonUser]( /windows/win32/api/winbase/nf-winbase-logonusera) 函式來填入模擬控制碼。 如果成功，請呼叫 [ImpersonateLoggedOnUser 函數](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)。 如果不成功，此範例會呼叫 [RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) 函式來終止模擬已登入的使用者，並擲回錯誤，且控制碼已關閉。
10. 呼叫 [**IBitsTokenOptions：： SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) 方法，以模擬已登入使用者的權杖。 如果此方法失敗，此範例會呼叫 [RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) 函式來終止模擬已登入的使用者，並擲回錯誤，且控制碼已關閉。
    > [!Note]
    >
    > 在 Windows 10 之前的 Windows 支援版本中1607，作業擁有者必須具有系統管理認證，才能呼叫 [**IBitsTokenOptions：： SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken)方法。
    >
    > 從 Windows 10 開始，版本1607，非管理員作業擁有者可以在其擁有的 BITS 工作上設定非系統管理員協助程式權杖。 作業擁有者仍然必須具有系統管理認證，才能使用系統管理員許可權來設定 helper 權杖。

     

11. 呼叫 [**IBitsTokenOptions：： SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) 方法，以指定要使用 helper 權杖的安全性內容存取哪些資源。
12. 模擬完成後，此範例會呼叫 [RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) 函式來終止模擬已登入的使用者，而控制碼已關閉。
13. 藉由呼叫 [**IBackgroundCopyJob：： AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)，將檔案新增至 BITS 傳送工作。
14. 新增檔案之後，請呼叫 [**IBackgroundCopyJob：： resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) 以繼續作業。
15. 設定 while 迴圈，以在作業傳送時等候回呼介面的結束訊息。 While 迴圈會使用 [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) 函式來取得自作業開始傳送以來經過的毫秒數。
16. 在 BITS 傳送工作完成之後，請呼叫 [**IBackgroundCopyJob：： complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete)來移除佇列中的作業。

下列程式碼範例會將 helper 權杖新增至 BITS 傳送工作。


```C++
#include <bits.h>
#include <bits4_0.h>
#include <stdio.h>
#include <tchar.h>
#include <lm.h>
#include <iostream>
#include <exception>
#include <string>
#include <atlbase.h>
#include <memory>
#include <new>
#include "CommonCode.h"


void HelperToken(const LPWSTR &remoteFile, const LPWSTR &localFile, const LPWSTR &domain, const LPWSTR &username, const LPWSTR &password)
{
// If CoInitializeEx fails, the exception is unhandled and the program terminates   
CCoInitializer coInitializer(COINIT_APARTMENTTHREADED);

CComPtr<IBackgroundCopyJob> pJob; 

    try
    {
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
        CComPtr<IBackgroundCopyManager> pQueueMgr;
        hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
            CLSCTX_LOCAL_SERVER,
            __uuidof(IBackgroundCopyManager),
            (void **)&pQueueMgr);

        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"CoCreateInstance");
        }

        // Create a job.
        wprintf(L"Creating Job...\n");

        GUID guidJob;
        hr = pQueueMgr->CreateJob(L"HelperTokenSample",
            BG_JOB_TYPE_DOWNLOAD,
            &guidJob,
            &pJob);


        if(FAILED(hr))
        {   
            // Failed to create job.
            throw MyException(hr, L"CreateJob");
        }

        // Set the File Completed call.
        CComPtr<CNotifyInterface> pNotify;    
        pNotify = new CNotifyInterface();
        hr = pJob->SetNotifyInterface(pNotify);
        if (FAILED(hr))
        {
            // Failed to SetNotifyInterface.
            throw MyException(hr, L"SetNotifyInterface");
        }
        hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
            BG_NOTIFY_JOB_ERROR);

        if (FAILED(hr))
        {
            // Failed to SetNotifyFlags.
            throw MyException(hr, L"SetNotifyFlags");
        }

        //Retrieve the IBitsTokenOptions interface pointer from the BITS transfer job.
        CComPtr<IBitsTokenOptions> pTokenOptions;
        hr = pJob->QueryInterface(__uuidof(IBitsTokenOptions), (void** ) &pTokenOptions);

        if (FAILED(hr))
        {
            // Failed to QueryInterface.
            throw MyException(hr, L"QueryInterface");
        }

        // Log on user of the helper token.
        wprintf(L"Credentials for helper token %s\\%s %s\n", domain, username, password);

        HANDLE hImpersonation = INVALID_HANDLE_VALUE;
        if(LogonUser(username, domain, password, LOGON32_LOGON_INTERACTIVE, LOGON32_PROVIDER_DEFAULT, &hImpersonation))
        {
            // Impersonate the logged-on user.
            if(ImpersonateLoggedOnUser(hImpersonation))
            {
                // Configure the impersonated logged-on user's token as the helper token.
                hr = pTokenOptions->SetHelperToken();        
                if (FAILED(hr))
                {
                    //Failed to set helper token.
                    CloseHandle(hImpersonation);
                    RevertToSelf();
                    throw MyException(hr, L"SetHelperToken");
                }

                hr = pTokenOptions->SetHelperTokenFlags(BG_TOKEN_LOCAL_FILE);
                if (FAILED(hr))
                {
                    //Failed to set helper token flags.
                    CloseHandle(hImpersonation);
                    RevertToSelf();
                    throw MyException(hr, L"SetHelperTokenFlags");
                }

                RevertToSelf();
            }               
            CloseHandle(hImpersonation);
        }

        // Add a file.
        // Replace parameters with variables that contain valid paths.
        wprintf(L"Adding File to Job\n");
        hr = pJob->AddFile(remoteFile,localFile);

        if(FAILED(hr))
        {   
            //Failed to add file to job.
            throw MyException(hr, L"AddFile");
        }

        //Resume the job.
        wprintf(L"Resuming Job...\n");
        hr = pJob->Resume();
        if (FAILED(hr))
        {
            // Resume failed.                   
            throw MyException(hr, L"Resume");
        }    
    }
    catch(const std::bad_alloc &)
    {
        wprintf(L"Memory allocation failed");
        if (pJob)
        {
            pJob->Cancel();
        }

        return;
    }
    catch(const MyException &ex)
    {
        wprintf(L"Error 0x%x occurred during operation", ex.Error);
        if (pJob)
        {
            pJob->Cancel();
        }

        return;
    }

    wprintf(L"Transferring file and waiting for callback.\n");

    // Wait for QuitMessage from CallBack
    DWORD dwLimit = GetTickCount() + (15 * 60 * 1000);  // set 15 minute limit
    while (dwLimit > GetTickCount())
    {
        MSG msg;

        while (PeekMessage(&msg, NULL, 0, 0, PM_REMOVE)) 
        { 
            // If it is a quit message, exit.
            if (msg.message == WM_QUIT) 
            {
                return;
            }

            // Otherwise, dispatch the message.
            DispatchMessage(&msg); 
        } // End of PeekMessage while loop
    }

    pJob->Cancel();
    return;
}

void _cdecl _tmain(int argc, LPWSTR* argv)
{   
    if (argc != 6)
    {
        wprintf(L"Usage:");
        wprintf(L"%s ", argv[0]);
        wprintf(L"[remote name] [local name] [helpertoken domain] [helpertoken userrname] [helpertoken password]\n");
        return;
    }

    HelperToken(argv[1],argv[2],argv[3],argv[4],argv[5]);

}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[BITS 傳送工作的協助程式權杖](helper-tokens-for-bits-transfer-jobs.md)
</dt> <dt>

[**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
</dt> <dt>

[範例：通用類別](common-classes.md)
</dt> </dl>

 

 