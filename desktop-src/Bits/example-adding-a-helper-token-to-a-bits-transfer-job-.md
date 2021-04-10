---
title: 將 Helper 權杖新增至 BITS 傳送工作的範例
description: 您可以使用額外的安全性權杖，設定背景智慧型傳送服務 (位) 的傳送作業。 BITS 傳送工作會使用此協助程式權杖進行驗證並存取資源。
ms.assetid: 08670c6d-e589-41be-842d-597f460d9c97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dab12fe93ae54d91d02bef5e59e99d267571413e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024024"
---
# <a name="example-adding-a-helper-token-to-a-bits-transfer-job"></a><span data-ttu-id="b878c-104">範例：將 Helper 權杖新增至 BITS 傳送工作</span><span class="sxs-lookup"><span data-stu-id="b878c-104">Example: Adding a Helper Token to a BITS Transfer Job</span></span>

<span data-ttu-id="b878c-105">您可以使用額外的安全性權杖，設定背景智慧型傳送服務 (位) 的傳送作業。</span><span class="sxs-lookup"><span data-stu-id="b878c-105">You can configure a Background Intelligent Transfer Service (BITS) transfer job with an additional security token.</span></span> <span data-ttu-id="b878c-106">BITS 傳送工作會使用此協助程式權杖進行驗證並存取資源。</span><span class="sxs-lookup"><span data-stu-id="b878c-106">The BITS transfer job uses this helper token for authentication and to access resources.</span></span>

<span data-ttu-id="b878c-107">如需詳細資訊，請參閱 [BITS 傳送工作的協助程式權杖](helper-tokens-for-bits-transfer-jobs.md)。</span><span class="sxs-lookup"><span data-stu-id="b878c-107">For more information, see [Helper tokens for BITS transfer jobs](helper-tokens-for-bits-transfer-jobs.md).</span></span>

<span data-ttu-id="b878c-108">下列程式會在本機使用者的內容中建立 BITS 傳送工作、取得第二位使用者的認證、使用這些認證建立 helper 權杖，然後在 BITS 傳送工作上設定協助程式權杖。</span><span class="sxs-lookup"><span data-stu-id="b878c-108">The following procedure creates a BITS transfer job in the context of the local user, gets credentials of a second user, creates a helper token with these credentials, and then sets the helper token on the BITS transfer job.</span></span>

<span data-ttu-id="b878c-109">此範例會使用範例中所定義的標頭和執行 [：一般類別](common-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="b878c-109">This example uses the header and implementation defined in [Example: Common Classes](common-classes.md).</span></span>

<span data-ttu-id="b878c-110">**將 helper 權杖新增至 BITS 傳送工作**</span><span class="sxs-lookup"><span data-stu-id="b878c-110">**To add a helper token to a BITS transfer job**</span></span>

1.  <span data-ttu-id="b878c-111">藉由呼叫 CCoInitializer 函數來初始化 COM 參數。</span><span class="sxs-lookup"><span data-stu-id="b878c-111">Initialize COM parameters by calling the CCoInitializer function.</span></span> <span data-ttu-id="b878c-112">如需 CCoInitializer 函數的詳細資訊，請參閱 [範例：通用類別](common-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="b878c-112">For more information about the CCoInitializer function, see [Example: Common Classes](common-classes.md).</span></span>
2.  <span data-ttu-id="b878c-113">取得 [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="b878c-113">Get a pointer to the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface.</span></span> <span data-ttu-id="b878c-114">這個範例會使用 [CComPtr 類別](/cpp/atl/reference/ccomptr-class?view=vs-2019) 來管理 COM 介面指標。</span><span class="sxs-lookup"><span data-stu-id="b878c-114">This example uses the [CComPtr Class](/cpp/atl/reference/ccomptr-class?view=vs-2019) to manage COM interface pointers.</span></span>
3.  <span data-ttu-id="b878c-115">藉由呼叫 [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)來初始化 COM 進程安全性。</span><span class="sxs-lookup"><span data-stu-id="b878c-115">Initialize COM process security by calling [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="b878c-116">BITS 至少需要模擬的模擬層級。</span><span class="sxs-lookup"><span data-stu-id="b878c-116">BITS requires at least the IMPERSONATE level of impersonation.</span></span> <span data-ttu-id="b878c-117">如果未設定正確的模擬等級，則 BITS 會失敗，並出現 E \_ ACCESSDENIED。</span><span class="sxs-lookup"><span data-stu-id="b878c-117">BITS fails with E\_ACCESSDENIED if the correct impersonation level is not set.</span></span>
4.  <span data-ttu-id="b878c-118">取得 [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) 介面的指標，並藉由呼叫 [COCREATEINSTANCE]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函數取得位的初始定位器。</span><span class="sxs-lookup"><span data-stu-id="b878c-118">Get a pointer to the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface, and obtain the initial locator to BITS by calling the [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>
5.  <span data-ttu-id="b878c-119">藉由呼叫 [**IBackgroundCopyManager：： >batchclient.joboperations.createjob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) 方法來建立 BITS 傳送工作。</span><span class="sxs-lookup"><span data-stu-id="b878c-119">Create a BITS transfer job by calling the [**IBackgroundCopyManager::CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method.</span></span>
6.  <span data-ttu-id="b878c-120">取得 CNotifyInterface 回呼介面的指標，然後呼叫 [**IBackgroundCopyJob：： SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) 方法以接收作業相關事件的通知。</span><span class="sxs-lookup"><span data-stu-id="b878c-120">Get a pointer to the CNotifyInterface callback interface, and call the [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) method to receive notification of job-related events.</span></span> <span data-ttu-id="b878c-121">如需 CNotifyInterface 的詳細資訊，請參閱 [範例：通用類別](common-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="b878c-121">For more information about CNotifyInterface, see [Example: Common Classes](common-classes.md).</span></span>
7.  <span data-ttu-id="b878c-122">呼叫 [**IBackgroundCopyJob：： SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) 方法，以設定要接收的通知類型。</span><span class="sxs-lookup"><span data-stu-id="b878c-122">Call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) method to set the types of notifications to receive.</span></span> <span data-ttu-id="b878c-123">在此範例中，會設定「 **bg \_ 通知 \_ 作業已 \_ 傳送** 」和「 **bg \_ 通知 \_ 工作」 \_ 錯誤** 旗標。</span><span class="sxs-lookup"><span data-stu-id="b878c-123">In this example, the **BG\_NOTIFY\_JOB\_TRANSFERRED** and **BG\_NOTIFY\_JOB\_ERROR** flags are set.</span></span>
8.  <span data-ttu-id="b878c-124">呼叫具有適當介面識別碼的 **IBackgroundCopyJob：： QueryInterface** 方法，以取得 [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="b878c-124">Get a pointer to the [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) interface by calling the **IBackgroundCopyJob::QueryInterface** method with the proper interface identifier.</span></span>
9.  <span data-ttu-id="b878c-125">嘗試登入 helper 權杖的使用者。</span><span class="sxs-lookup"><span data-stu-id="b878c-125">Attempt to log on the user of the helper token.</span></span> <span data-ttu-id="b878c-126">建立模擬控制碼，並呼叫 [LogonUser]( /windows/win32/api/winbase/nf-winbase-logonusera) 函式來填入模擬控制碼。</span><span class="sxs-lookup"><span data-stu-id="b878c-126">Create an impersonation handle, and call the [LogonUser Function]( /windows/win32/api/winbase/nf-winbase-logonusera) to populate the impersonation handle.</span></span> <span data-ttu-id="b878c-127">如果成功，請呼叫 [ImpersonateLoggedOnUser 函數](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)。</span><span class="sxs-lookup"><span data-stu-id="b878c-127">If successful, call the [ImpersonateLoggedOnUser Function](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser).</span></span> <span data-ttu-id="b878c-128">如果不成功，此範例會呼叫 [RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) 函式來終止模擬已登入的使用者，並擲回錯誤，且控制碼已關閉。</span><span class="sxs-lookup"><span data-stu-id="b878c-128">If unsuccessful, the example calls the [RevertToSelf Function](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) to terminate the impersonation of the logged-on user, an error is thrown, and the handle is closed.</span></span>
10. <span data-ttu-id="b878c-129">呼叫 [**IBitsTokenOptions：： SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) 方法，以模擬已登入使用者的權杖。</span><span class="sxs-lookup"><span data-stu-id="b878c-129">Call the [**IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) method to impersonate the token of the logged-on user.</span></span> <span data-ttu-id="b878c-130">如果此方法失敗，此範例會呼叫 [RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) 函式來終止模擬已登入的使用者，並擲回錯誤，且控制碼已關閉。</span><span class="sxs-lookup"><span data-stu-id="b878c-130">If this method fails, the example calls the [RevertToSelf Function](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) to terminate the impersonation of the logged-on user, an error is thrown, and the handle is closed.</span></span>
    > [!Note]
    >
    > <span data-ttu-id="b878c-131">在 Windows 10 之前的 Windows 版本中1607，作業擁有者必須具有系統管理認證，才能呼叫 [**IBitsTokenOptions：： SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) 方法。</span><span class="sxs-lookup"><span data-stu-id="b878c-131">In supported versions of Windows before Windows 10, version 1607, the job owner must have administrative credentials to call the [**IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) method.</span></span>
    >
    > <span data-ttu-id="b878c-132">從 Windows 10 開始，版本1607，非管理員作業擁有者可以在其擁有的 BITS 工作上設定非系統管理員協助程式權杖。</span><span class="sxs-lookup"><span data-stu-id="b878c-132">Starting with Windows 10, version 1607, non-administrator job owners can set non-administrator helper tokens on BITS jobs they own.</span></span> <span data-ttu-id="b878c-133">作業擁有者仍然必須具有系統管理認證，才能使用系統管理員許可權來設定 helper 權杖。</span><span class="sxs-lookup"><span data-stu-id="b878c-133">Job owners must still have administrative credentials to set helper tokens with administrator privileges.</span></span>

     

11. <span data-ttu-id="b878c-134">呼叫 [**IBitsTokenOptions：： SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) 方法，以指定要使用 helper 權杖的安全性內容存取哪些資源。</span><span class="sxs-lookup"><span data-stu-id="b878c-134">Call the [**IBitsTokenOptions::SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) method to specify which resources to access using the helper token's security context.</span></span>
12. <span data-ttu-id="b878c-135">模擬完成後，此範例會呼叫 [RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) 函式來終止模擬已登入的使用者，而控制碼已關閉。</span><span class="sxs-lookup"><span data-stu-id="b878c-135">After the impersonation is complete, the example calls the [RevertToSelf Function](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) to terminate the impersonation of logged on user, and the handle is closed.</span></span>
13. <span data-ttu-id="b878c-136">藉由呼叫 [**IBackgroundCopyJob：： AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)，將檔案新增至 BITS 傳送工作。</span><span class="sxs-lookup"><span data-stu-id="b878c-136">Add files to the BITS transfer job by calling [**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile).</span></span>
14. <span data-ttu-id="b878c-137">新增檔案之後，請呼叫 [**IBackgroundCopyJob：： resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) 以繼續作業。</span><span class="sxs-lookup"><span data-stu-id="b878c-137">After the file is added, call [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) to resume the job.</span></span>
15. <span data-ttu-id="b878c-138">設定 while 迴圈，以在作業傳送時等候回呼介面的結束訊息。</span><span class="sxs-lookup"><span data-stu-id="b878c-138">Set up a while loop to wait for the quit message from the callback interface while the job is transferring.</span></span> <span data-ttu-id="b878c-139">While 迴圈會使用 [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) 函式來取得自作業開始傳送以來經過的毫秒數。</span><span class="sxs-lookup"><span data-stu-id="b878c-139">The while loop uses the [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) function to retrieve the number of milliseconds that have elapsed since the job started transferring.</span></span>
16. <span data-ttu-id="b878c-140">在 BITS 傳送工作完成之後，請呼叫 [**IBackgroundCopyJob：： complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete)來移除佇列中的作業。</span><span class="sxs-lookup"><span data-stu-id="b878c-140">After the BITS transfer job is complete, remove the job from the queue by calling [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span></span>

<span data-ttu-id="b878c-141">下列程式碼範例會將 helper 權杖新增至 BITS 傳送工作。</span><span class="sxs-lookup"><span data-stu-id="b878c-141">The following code example adds a helper token to a BITS transfer job.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b878c-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="b878c-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b878c-143">BITS 傳送工作的協助程式權杖</span><span class="sxs-lookup"><span data-stu-id="b878c-143">Helper tokens for BITS transfer jobs</span></span>](helper-tokens-for-bits-transfer-jobs.md)
</dt> <dt>

[<span data-ttu-id="b878c-144">**IBitsTokenOptions**</span><span class="sxs-lookup"><span data-stu-id="b878c-144">**IBitsTokenOptions**</span></span>](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
</dt> <dt>

[<span data-ttu-id="b878c-145">範例：通用類別</span><span class="sxs-lookup"><span data-stu-id="b878c-145">Example: Common Classes</span></span>](common-classes.md)
</dt> </dl>

 

 