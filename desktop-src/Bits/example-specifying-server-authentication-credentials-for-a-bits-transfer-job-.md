---
title: 指定 BITS 傳送工作的伺服器驗證認證
description: 您可以針對背景智慧型傳送服務 (BITS) 傳送工作指定不同的驗證配置。
ms.assetid: 31db38f6-3639-4042-97f2-4f9d78942e15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c4373cdf0c8b4c8afe7dff367fda9387eec0b54
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024076"
---
# <a name="specify-server-authentication-credentials-for-a-bits-transfer-job"></a><span data-ttu-id="8c314-103">指定 BITS 傳送工作的伺服器驗證認證</span><span class="sxs-lookup"><span data-stu-id="8c314-103">Specify server authentication credentials for a BITS transfer job</span></span>

<span data-ttu-id="8c314-104">您可以針對背景智慧型傳送服務 (BITS) 傳送工作指定不同的驗證配置。</span><span class="sxs-lookup"><span data-stu-id="8c314-104">You can specify different authentication schemes for a Background Intelligent Transfer Service (BITS) transfer job.</span></span>

<span data-ttu-id="8c314-105">下列程式會取得驗證配置，並建立驗證身分識別結構。</span><span class="sxs-lookup"><span data-stu-id="8c314-105">The following procedure gets an authentication scheme and creates an authentication identity structure.</span></span> <span data-ttu-id="8c314-106">然後，應用程式會建立 BITS 下載作業，並設定作業的認證。</span><span class="sxs-lookup"><span data-stu-id="8c314-106">Then the application creates a BITS download job and sets the credentials for the job.</span></span> <span data-ttu-id="8c314-107">建立作業之後，應用程式會取得回呼介面的指標，並輪詢 BITS 傳送工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="8c314-107">After the job is created, the application gets a pointer to a callback interface and polls for the status of the BITS transfer job.</span></span> <span data-ttu-id="8c314-108">作業完成後，就會從佇列中移除。</span><span class="sxs-lookup"><span data-stu-id="8c314-108">After the job is complete, it is removed from the queue.</span></span>

<span data-ttu-id="8c314-109">此範例會使用範例中所定義的標頭和執行 [：一般類別](common-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="8c314-109">This example uses the header and implementation defined in [Example: Common Classes](common-classes.md).</span></span>

<span data-ttu-id="8c314-110">**指定 BITS 傳送工作的伺服器驗證認證**</span><span class="sxs-lookup"><span data-stu-id="8c314-110">**To specify server authentication credentials for a BITS transfer job**</span></span>

1.  <span data-ttu-id="8c314-111">建立將 [**BG \_ 驗證 \_ 配置**](/windows/desktop/api/Bits1_5/ne-bits1_5-bg_auth_scheme) 值對應至配置名稱的容器結構。</span><span class="sxs-lookup"><span data-stu-id="8c314-111">Create a container structure that maps [**BG\_AUTH\_SCHEME**](/windows/desktop/api/Bits1_5/ne-bits1_5-bg_auth_scheme) values to scheme names.</span></span>

    ```C++
    struct
    {
        LPCWSTR        Name;
        BG_AUTH_SCHEME Scheme;
    }
    SchemeNames[] =
    {
        { L"basic",      BG_AUTH_SCHEME_BASIC },
        { L"digest",     BG_AUTH_SCHEME_DIGEST },
        { L"ntlm",       BG_AUTH_SCHEME_NTLM },
        { L"negotiate",  BG_AUTH_SCHEME_NEGOTIATE },
        { L"passport",   BG_AUTH_SCHEME_PASSPORT },

        { NULL,         BG_AUTH_SCHEME_BASIC }
    };
    ```

    

2.  <span data-ttu-id="8c314-112">藉由呼叫 CCoInitializer 函數來初始化 COM 參數。</span><span class="sxs-lookup"><span data-stu-id="8c314-112">Initialize COM parameters by calling the CCoInitializer function.</span></span> <span data-ttu-id="8c314-113">如需 CCoInitializer 函數的詳細資訊，請參閱 [範例：通用類別](common-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="8c314-113">For more information about the CCoInitializer function, see [Example: Common Classes](common-classes.md).</span></span>
3.  <span data-ttu-id="8c314-114">準備 [**BG \_ 驗證 \_**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) 認證結構。</span><span class="sxs-lookup"><span data-stu-id="8c314-114">Prepare a [**BG\_AUTH\_CREDENTIALS**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) structure.</span></span> <span data-ttu-id="8c314-115">此範例會使用 [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) 函數來清除與機密資訊相關聯的記憶體位置。</span><span class="sxs-lookup"><span data-stu-id="8c314-115">The example uses the [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function to clear the memory locations associated with the sensitive information.</span></span> <span data-ttu-id="8c314-116">[SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85))函式定義于 WinBase 中。</span><span class="sxs-lookup"><span data-stu-id="8c314-116">The [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function is defined in WinBase.h.</span></span>
4.  <span data-ttu-id="8c314-117">您可以使用 GetScheme 函數來取得用來連接到伺服器的驗證配置。</span><span class="sxs-lookup"><span data-stu-id="8c314-117">Use the GetScheme function to get the authentication scheme to use to connect to the server.</span></span>

    ```C++
    bool GetScheme( LPCWSTR s, BG_AUTH_SCHEME *scheme )
    {
        int i;

        i = 0;
        while (SchemeNames[i].Name != NULL)
        {
            if (0 == _wcsicmp( s, SchemeNames[i].Name ))
            {

                *scheme = SchemeNames[i].Scheme;
                return true;
            }

            ++i;
        }

        return false;
    }
    ```

    

5.  <span data-ttu-id="8c314-118">使用 GetScheme 函式所傳回的驗證配置和傳遞至 ServerAuthentication 函式的使用者名稱和密碼，來填入 [**BG \_ AUTH \_**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) 認證結構。</span><span class="sxs-lookup"><span data-stu-id="8c314-118">Populate the [**BG\_AUTH\_CREDENTIALS**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) structure with the authentication scheme returned by the GetScheme function and the user name and password that were passed into the ServerAuthentication function.</span></span>
6.  <span data-ttu-id="8c314-119">取得 [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) 介面的指標， (pJob) 。</span><span class="sxs-lookup"><span data-stu-id="8c314-119">Get a pointer to the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface (pJob).</span></span>
7.  <span data-ttu-id="8c314-120">藉由呼叫 [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)來初始化 COM 進程安全性。</span><span class="sxs-lookup"><span data-stu-id="8c314-120">Initialize COM process security by calling [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="8c314-121">BITS 至少需要模擬的模擬層級。</span><span class="sxs-lookup"><span data-stu-id="8c314-121">BITS requires at least the IMPERSONATE level of impersonation.</span></span> <span data-ttu-id="8c314-122">如果未設定正確的模擬等級，則 BITS 會失敗，並出現 E \_ ACCESSDENIED。</span><span class="sxs-lookup"><span data-stu-id="8c314-122">BITS fails with E\_ACCESSDENIED if the correct impersonation level is not set.</span></span>
8.  <span data-ttu-id="8c314-123">取得 [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) 介面的指標，並藉由呼叫 [COCREATEINSTANCE]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函數取得位的初始定位器。</span><span class="sxs-lookup"><span data-stu-id="8c314-123">Get a pointer to the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface, and obtain the initial locator to BITS by calling the [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>
9.  <span data-ttu-id="8c314-124">藉由呼叫 [**IBackgroundCopyManager：： >batchclient.joboperations.createjob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) 方法來建立 BITS 傳送工作。</span><span class="sxs-lookup"><span data-stu-id="8c314-124">Create a BITS transfer job by calling the [**IBackgroundCopyManager::CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method.</span></span>
10. <span data-ttu-id="8c314-125">取得 CNotifyInterface 回呼介面的指標，並呼叫 [**IBackgroundCopyJob：： SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) 方法以接收作業相關事件的通知。</span><span class="sxs-lookup"><span data-stu-id="8c314-125">Get a pointer to the CNotifyInterface callback interface and call the [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) method to receive notification of job-related events.</span></span> <span data-ttu-id="8c314-126">如需 CNotifyInterface 的詳細資訊，請參閱 [範例：通用類別](common-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="8c314-126">For more information about CNotifyInterface, see [Example: Common Classes](common-classes.md).</span></span>
11. <span data-ttu-id="8c314-127">呼叫 [**IBackgroundCopyJob：： SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) 方法，以設定要接收的通知類型。</span><span class="sxs-lookup"><span data-stu-id="8c314-127">Call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) method to set the types of notifications to receive.</span></span> <span data-ttu-id="8c314-128">在此範例中，會設定「 **bg \_ 通知 \_ 作業已 \_ 傳送** 」和「 **bg \_ 通知 \_ 工作」 \_ 錯誤** 旗標。</span><span class="sxs-lookup"><span data-stu-id="8c314-128">In this example, the **BG\_NOTIFY\_JOB\_TRANSFERRED** and **BG\_NOTIFY\_JOB\_ERROR** flags are set.</span></span>
12. <span data-ttu-id="8c314-129">取得 [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="8c314-129">Get a pointer to the [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) interface.</span></span> <span data-ttu-id="8c314-130">使用 **IBackgroundCopyJob2** 指標來設定作業的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="8c314-130">Use the **IBackgroundCopyJob2** pointer to set additional properties on the job.</span></span> <span data-ttu-id="8c314-131">此程式會使用 [**IBackgroundCopyJob2：： SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) 方法來設定 BITS 傳送工作的認證。</span><span class="sxs-lookup"><span data-stu-id="8c314-131">This program uses the [**IBackgroundCopyJob2::SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) method to set the credentials for the BITS transfer job.</span></span>
13. <span data-ttu-id="8c314-132">藉由呼叫 [**IBackgroundCopyJob：： AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)，將檔案新增至 BITS 傳送工作。</span><span class="sxs-lookup"><span data-stu-id="8c314-132">Add files to the BITS transfer job by calling [**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile).</span></span> <span data-ttu-id="8c314-133">在此範例中， **IBackgroundCopyJob：： AddFile** 方法會使用傳遞至 ServerAuthentication 函數的 RemoteFile 和 localFile 變數。</span><span class="sxs-lookup"><span data-stu-id="8c314-133">In this example, the **IBackgroundCopyJob::AddFile** method uses the remoteFile and localFile variables that were passed into the ServerAuthentication function.</span></span>
14. <span data-ttu-id="8c314-134">新增檔案之後，請呼叫 [**IBackgroundCopyJob：： resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) 以繼續作業。</span><span class="sxs-lookup"><span data-stu-id="8c314-134">After the file is added, call [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) to resume the job.</span></span>
15. <span data-ttu-id="8c314-135">設定 while 迴圈，以在作業傳送時等候回呼介面的結束訊息。</span><span class="sxs-lookup"><span data-stu-id="8c314-135">Set up a while loop to wait for Quit Message from the callback interface while the job is transferring.</span></span>

    > [!Note]  
    > <span data-ttu-id="8c314-136">只有當 COM 單元為單一執行緒的單元時，才需要執行此步驟。</span><span class="sxs-lookup"><span data-stu-id="8c314-136">This step is necessary only if the COM apartment is a single-threaded apartment.</span></span> <span data-ttu-id="8c314-137">如需詳細資訊，請參閱 [單一執行緒單元](../com/single-threaded-apartments.md)。</span><span class="sxs-lookup"><span data-stu-id="8c314-137">For more information, see [Single-Threaded Apartments](../com/single-threaded-apartments.md).</span></span>

     

    ```C++
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
    ```

    

    <span data-ttu-id="8c314-138">先前的迴圈會使用 [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) 函式，來取得自作業開始傳送以來經過的毫秒數。</span><span class="sxs-lookup"><span data-stu-id="8c314-138">The preceding loop uses the [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) function to retrieve the number of milliseconds that have elapsed since the job started transferring.</span></span>

16. <span data-ttu-id="8c314-139">在 BITS 傳送工作完成之後，請呼叫 [**IBackgroundCopyJob：： complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete)來移除佇列中的作業。</span><span class="sxs-lookup"><span data-stu-id="8c314-139">After the BITS transfer job is complete, remove the job from the queue by calling [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span></span>

<span data-ttu-id="8c314-140">下列程式碼範例會指定 BITS 傳送工作的伺服器驗證認證。</span><span class="sxs-lookup"><span data-stu-id="8c314-140">The following code example specifies server authentication credentials for a BITS transfer job.</span></span>


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

//
// Retrieve BG_AUTH_SCHEME from scheme name.
//
//
struct
{
    LPCWSTR        Name;
    BG_AUTH_SCHEME Scheme;
}
SchemeNames[] =
{
    { L"basic",      BG_AUTH_SCHEME_BASIC },
    { L"digest",     BG_AUTH_SCHEME_DIGEST },
    { L"ntlm",       BG_AUTH_SCHEME_NTLM },
    { L"negotiate",  BG_AUTH_SCHEME_NEGOTIATE },
    { L"passport",   BG_AUTH_SCHEME_PASSPORT },

    { NULL,         BG_AUTH_SCHEME_BASIC }
};

bool GetScheme( LPCWSTR s, BG_AUTH_SCHEME *scheme )
{
    int i;

    i = 0;
    while (SchemeNames[i].Name != NULL)
    {
        if (0 == _wcsicmp( s, SchemeNames[i].Name ))
        {

            *scheme = SchemeNames[i].Scheme;
            return true;
        }

        ++i;
    }

    return false;
}

void ServerAuthentication(const LPWSTR &remoteFile, const LPWSTR &localFile, const LPWSTR &scheme, const LPWSTR &username, const LPWSTR &password)
{

 // If CoInitializeEx fails, the exception is unhandled and the program terminates  
 CCoInitializer coInitializer(COINIT_APARTMENTTHREADED);
    
    // Prepare the credentials structure.
    BG_AUTH_CREDENTIALS cred;
    ZeroMemory(&cred, sizeof(cred));
    if (!GetScheme(scheme,&cred.Scheme))
    {
        wprintf(L"Invalid authentication scheme specified\n");
        return;
    }

    cred.Target = BG_AUTH_TARGET_SERVER;
    cred.Credentials.Basic.UserName = username;
    if (0 == _wcsicmp(cred.Credentials.Basic.UserName, L"NULL"))
    {
        cred.Credentials.Basic.UserName = NULL;
    }

    cred.Credentials.Basic.Password = password;
    if (0 == _wcsicmp(cred.Credentials.Basic.Password, L"NULL"))
    {
        cred.Credentials.Basic.Password = NULL;
    }

    CComPtr<IBackgroundCopyJob> pJob;
    try
    {
        //The impersonation level must be at least RPC_C_IMP_LEVEL_IMPERSONATE.
        HRESULT hr = CoInitializeSecurity(NULL, 
            -1, 
            NULL, 
            NULL,
            RPC_C_AUTHN_LEVEL_CONNECT,
            RPC_C_IMP_LEVEL_IMPERSONATE,
            NULL, 
            EOAC_DYNAMIC_CLOAKING, 
            0);
        if (FAILED(hr))
        {
            throw MyException(hr, L"CoInitializeSecurity");
        }

        // Connect to BITS.
        CComPtr<IBackgroundCopyManager> pQueueMgr;
        hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
            CLSCTX_LOCAL_SERVER,
            __uuidof(IBackgroundCopyManager),
            (void**)&pQueueMgr);

        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"CoCreateInstance");
        }

        // Create a job.
        wprintf(L"Creating Job...\n");

        GUID guidJob;
        hr = pQueueMgr->CreateJob(L"BitsAuthSample",
            BG_JOB_TYPE_DOWNLOAD,
            &guidJob,
            &pJob);

        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"CreateJob");
        }

        // Set the File Completed call.
        CComPtr<CNotifyInterface> pNotify;
        pNotify = new CNotifyInterface();
        hr = pJob->SetNotifyInterface(pNotify);
        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"SetNotifyInterface");
        }
        hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
            BG_NOTIFY_JOB_ERROR);

        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"SetNotifyFlags");
        }

        // Set credentials.
        CComPtr<IBackgroundCopyJob2> job2;
        hr = pJob.QueryInterface(&job2);
        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"QueryInterface");
        }

        hr = job2->SetCredentials(&cred);
        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"SetCredentials");
        }

        // Add a file.
        wprintf(L"Adding File to Job\n");
        hr = pJob->AddFile(remoteFile, localFile);
        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"AddFile");
        }

        //Resume the job.
        wprintf(L"Resuming Job...\n");
        hr = pJob->Resume();
        if (FAILED(hr))
        {
            // Failed to connect.
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
        wprintf(L"Error %x occurred during operation", ex.Error);
        if (pJob)
        {
            pJob->Cancel();
        }

        return;
    }

    wprintf(L"Transferring file and waiting for callback.\n");

    // Wait for QuitMessage from CallBack.
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
        wprintf(L"%s", argv[0]);
        wprintf(L" [remote name] [local name] [server authentication scheme =\"NTLM\"|\"NEGOTIATE\"|\"BASIC\"|\"DIGEST\"] [username] [password]\n");
        return;
    }

    ServerAuthentication(argv[1], argv[2], argv[3], argv[4], argv[5]); 

}
```



## <a name="related-topics"></a><span data-ttu-id="8c314-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="8c314-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c314-142">**IBackgroundCopyManager**</span><span class="sxs-lookup"><span data-stu-id="8c314-142">**IBackgroundCopyManager**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)
</dt> <dt>

[<span data-ttu-id="8c314-143">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="8c314-143">**IBackgroundCopyJob**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[<span data-ttu-id="8c314-144">**IBackgroundCopyJob2**</span><span class="sxs-lookup"><span data-stu-id="8c314-144">**IBackgroundCopyJob2**</span></span>](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2)
</dt> <dt>

[<span data-ttu-id="8c314-145">範例：通用類別</span><span class="sxs-lookup"><span data-stu-id="8c314-145">Example: Common Classes</span></span>](common-classes.md)
</dt> </dl>

 

 