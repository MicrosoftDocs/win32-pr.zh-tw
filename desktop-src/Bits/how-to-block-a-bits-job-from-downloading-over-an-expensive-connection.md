---
title: 透過昂貴的連接控制 BITS 下載
description: 封鎖透過昂貴的連線（例如漫遊行動電話連結）進行下載。
ms.assetid: 66C20B32-1348-44D9-81F3-43CCED0CEA34
keywords:
- 下載 BITS，如何
- 下載 BITS，避免昂貴
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 6326838f08f1879929d9a6be67ef94c4aa035e00
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "103841752"
---
# <a name="control-a-bits-download-over-an-expensive-connection"></a><span data-ttu-id="13f08-105">透過昂貴的連接控制 BITS 下載</span><span class="sxs-lookup"><span data-stu-id="13f08-105">Control a BITS download over an expensive connection</span></span>

<span data-ttu-id="13f08-106">本主題說明如何封鎖 BITS 作業，使其無法透過昂貴的連線（例如漫遊行動電話連結）進行下載。</span><span class="sxs-lookup"><span data-stu-id="13f08-106">This topic shows how to block a BITS job from downloading over an expensive connection such as a roaming cellular link.</span></span> <span data-ttu-id="13f08-107">BITS 是一個非同步 API，可讓應用程式建立作業、將 Url 新增至該作業，以及呼叫工作物件的 [**Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) 函數。</span><span class="sxs-lookup"><span data-stu-id="13f08-107">BITS is an asynchronous API where the application creates a job, adds URLs to that job, and calls the job object's [**Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) function.</span></span> <span data-ttu-id="13f08-108">從該時間點開始，BITS 會根據作業優先順序和傳輸原則等因素，選擇何時下載作業。</span><span class="sxs-lookup"><span data-stu-id="13f08-108">From that point, BITS chooses when the job downloads based on factors such as job priority and the transfer policy.</span></span> <span data-ttu-id="13f08-109">完成下載作業之後，如果應用程式已註冊完成通知) ，BITS 會通知應用程式 URL 已下載 (。</span><span class="sxs-lookup"><span data-stu-id="13f08-109">After the job has finished downloading, BITS notifies the application that the URL has been downloaded (if the application has registered for completion notification).</span></span> <span data-ttu-id="13f08-110">在作業的存留期內，如果使用者的網路變更（例如，如果使用者正在移動，且目前產生漫遊費用），則 BITS 會暫停工作，直到網路狀況達到最佳狀態為止。</span><span class="sxs-lookup"><span data-stu-id="13f08-110">During the job's lifetime, if the end user's network changes—such as if the user is traveling and is currently incurring roaming fees—then BITS will suspend the job until network conditions are optimal.</span></span> <span data-ttu-id="13f08-111">下列逐步指示示範如何建立作業，並指定適當的傳輸原則設定。</span><span class="sxs-lookup"><span data-stu-id="13f08-111">The following step-by-step instructions show how to create the job and specify the appropriate transfer policy settings.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="13f08-112">必要條件</span><span class="sxs-lookup"><span data-stu-id="13f08-112">Prerequisites</span></span>

-   <span data-ttu-id="13f08-113">Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="13f08-113">Microsoft Visual Studio</span></span>

## <a name="instructions"></a><span data-ttu-id="13f08-114">指示</span><span class="sxs-lookup"><span data-stu-id="13f08-114">Instructions</span></span>

### <a name="step-1-include-the-required-bits-header-files"></a><span data-ttu-id="13f08-115">步驟1：包含必要的 BITS 標頭檔</span><span class="sxs-lookup"><span data-stu-id="13f08-115">Step 1: Include the required BITS header files</span></span>

<span data-ttu-id="13f08-116">將下列標頭指示詞插入原始程式檔的頂端。</span><span class="sxs-lookup"><span data-stu-id="13f08-116">Insert the following header directives at the top of the source file.</span></span>


```C++
#include <bits.h>
#include <bits5_0.h>
```



### <a name="step-2-initialize-com"></a><span data-ttu-id="13f08-117">步驟2：初始化 COM</span><span class="sxs-lookup"><span data-stu-id="13f08-117">Step 2: Initialize COM</span></span>

<span data-ttu-id="13f08-118">在具現化 [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) 介面 (用來建立 BITS 作業) 之前，您必須先初始化 com、設定 com 執行緒模型，然後指定至少 RPC \_ C \_ IMP \_ 層級的模擬層級 \_ 。</span><span class="sxs-lookup"><span data-stu-id="13f08-118">Before instantiating the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface (used to create a BITS job), you must initialize COM, set the COM threading model, and specify an impersonation level of at least RPC\_C\_IMP\_LEVEL\_IMPERSONATE.</span></span>


```C++
// Initialize COM and specify the COM threading model.
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
if (SUCCEEDED(hr))
{
 // Specify an impersonation level of at least RPC_C_IMP_LEVEL_IMPERSONATE.
 hr = CoInitializeSecurity(NULL, -1, NULL, NULL,
                           RPC_C_AUTHN_LEVEL_CONNECT,
                           RPC_C_IMP_LEVEL_IMPERSONATE,
                           NULL, EOAC_NONE, 0);
 if (SUCCEEDED(hr))
 {
  ...
```



### <a name="step-3-instantiate-the-ibackgroundcopymanager-interface"></a><span data-ttu-id="13f08-119">步驟3：具現化 IBackgroundCopyManager 介面</span><span class="sxs-lookup"><span data-stu-id="13f08-119">Step 3: Instantiate the IBackgroundCopyManager interface</span></span>

<span data-ttu-id="13f08-120">您可以使用 [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) 介面來建立傳送作業、取出包含佇列中作業的列舉值物件，以及從佇列中取出個別的作業。</span><span class="sxs-lookup"><span data-stu-id="13f08-120">Use the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface to create transfer jobs, retrieve an enumerator object that contains the jobs in the queue, and retrieve individual jobs from the queue.</span></span>


```C++
IBackgroundCopyManager* pQueueMgr;

hr = CoCreateInstance(__uuidof(BackgroundCopyManager),
                      NULL,
                      CLSCTX_LOCAL_SERVER,
                      __uuidof(IBackgroundCopyManager),
                      (void **)&pQueueMgr);
```



### <a name="step-4-create-the-bits-job"></a><span data-ttu-id="13f08-121">步驟4：建立 BITS 作業</span><span class="sxs-lookup"><span data-stu-id="13f08-121">Step 4: Create the BITS job</span></span>

<span data-ttu-id="13f08-122">只有建立作業的使用者或具有系統管理員許可權的使用者可以將檔案新增至作業，並變更作業的屬性。</span><span class="sxs-lookup"><span data-stu-id="13f08-122">Only the user who creates the job or a user with administrator privileges can add files to the job and change the job's properties.</span></span>


```C++
GUID guidJob;
IBackgroundCopyJob* pBackgroundCopyJob;

hr = pQueueMgr->CreateJob(L"TransferPolicy",
                          BG_JOB_TYPE_DOWNLOAD,
                          &guidJob,
                          (IBackgroundCopyJob **)&pBackgroundCopyJob);
```



### <a name="step-5-specify-the-transfer-policy-setting-for-the-job"></a><span data-ttu-id="13f08-123">步驟5：指定作業的傳輸原則設定</span><span class="sxs-lookup"><span data-stu-id="13f08-123">Step 5: Specify the transfer policy setting for the job</span></span>

<span data-ttu-id="13f08-124">這是您指定成本狀態傳輸原則的地方。</span><span class="sxs-lookup"><span data-stu-id="13f08-124">This is where you specify the cost state transfer policy.</span></span> <span data-ttu-id="13f08-125">您可以 \_ \_ 使用位 **or** 組合來設定數個 BITS 成本狀態旗標，以達成所需的結果。</span><span class="sxs-lookup"><span data-stu-id="13f08-125">You can set several BITS\_COST\_STATE flags by using a bitwise **OR** combination to achieve the desired results.</span></span>


```C++
BITS_JOB_PROPERTY_VALUE propval;
IBackgroundCopyJob5* pBackgroundCopyJob5;

propval.Dword = BITS_COST_STATE_USAGE_BASED
              | BITS_COST_STATE_OVERCAP_THROTTLED
              | BITS_COST_STATE_BELOW_CAP
              | BITS_COST_STATE_CAPPED_USAGE_UNKNOWN
              | BITS_COST_STATE_UNRESTRICTED;

hr = pBackgroundCopyJob->QueryInterface(__uuidof(IBackgroundCopyJob5),
                                        reinterpret_cast<void**>(&pBackgroundCopyJob5));
if(SUCCEEDED(hr))
{
 pBackgroundCopyJob5->SetProperty(BITS_JOB_PROPERTY_ID_COST_FLAGS, propval);
}
```



## <a name="example"></a><span data-ttu-id="13f08-126">範例</span><span class="sxs-lookup"><span data-stu-id="13f08-126">Example</span></span>

<span data-ttu-id="13f08-127">下列程式碼範例示範如何設定 BITS 作業的傳輸原則，以便在符合特定條件時（例如當使用者漫遊或超過每月的資料傳輸限制時）進行作業的處理。</span><span class="sxs-lookup"><span data-stu-id="13f08-127">The following code example shows how to set a BITS job's transfer policy so that the processing of the job doesn't occur while certain conditions are met—such as when the user is roaming or has exceeded their monthly data transfer limit.</span></span>


```C++
//*********************************************************
//
//    Copyright (c) Microsoft. All rights reserved.
//    This code is licensed under the Microsoft Public License.
//    THIS CODE IS PROVIDED *AS IS* WITHOUT WARRANTY OF
//    ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY
//    IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR
//    PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.
//
//*********************************************************

#define WIN32_LEAN_AND_MEAN             // Exclude rarely-used stuff from Windows headers
#include <windows.h>
#include <bits.h>
#include <stdio.h> // define wprintf


int main()
{
 HRESULT hr = S_OK;
 GUID guidJob;
 IBackgroundCopyJob5* pBackgroundCopyJob5;  
 IBackgroundCopyJob* pBackgroundCopyJob;
 IBackgroundCopyManager* pQueueMgr;
 BITS_JOB_PROPERTY_VALUE propval;

 // Specify the COM threading model.
 hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
 if (SUCCEEDED(hr))
 {
  // The impersonation level must be at least RPC_C_IMP_LEVEL_IMPERSONATE.
  hr = CoInitializeSecurity(NULL, -1, NULL, NULL,
                            RPC_C_AUTHN_LEVEL_CONNECT,
                            RPC_C_IMP_LEVEL_IMPERSONATE,
                            NULL, EOAC_NONE, 0);

  if (SUCCEEDED(hr))
  {
   hr = CoCreateInstance(__uuidof(BackgroundCopyManager), 
                         NULL,
                         CLSCTX_LOCAL_SERVER,
                         __uuidof(IBackgroundCopyManager),
                         (void **)&pQueueMgr);

   if (FAILED(hr))
   {
    // Failed to connect to BITS.
    wprintf(L"Failed to connect to BITS with error %x\n",hr);
    goto done;
   }

   // Create a BITS job.
   wprintf(L"Creating Job...\n");

   hr = pQueueMgr->CreateJob(L"TransferPolicy",
                             BG_JOB_TYPE_DOWNLOAD,
                             &guidJob,
                             (IBackgroundCopyJob **)&pBackgroundCopyJob);

   if (FAILED(hr))
   {
    wprintf(L"Failed to Create Job, error = %x\n",hr);
    goto cancel;
   }

   wprintf(L" Job is succesfully created ...\n");

   // Set the Transfer Policy for the job.
   propval.Dword = BITS_COST_STATE_USAGE_BASED 
                 | BITS_COST_STATE_OVERCAP_THROTTLED
                 | BITS_COST_STATE_BELOW_CAP
                 | BITS_COST_STATE_CAPPED_USAGE_UNKNOWN
                 | BITS_COST_STATE_UNRESTRICTED;

   hr = pBackgroundCopyJob->QueryInterface(
         __uuidof(IBackgroundCopyJob5),
         reinterpret_cast<void**>(&pBackgroundCopyJob5)
        );

   if (FAILED(hr))
   {
    wprintf(L"Failed to Create Job, error = %x\n",hr);
    goto cancel;
   }
   pBackgroundCopyJob5->SetProperty(BITS_JOB_PROPERTY_ID_COST_FLAGS, propval);

   // Get the Transfer Policy for the new job.
   BITS_JOB_PROPERTY_VALUE actual_propval;

   wprintf(L"Getting TransferPolicy Property ...\n");

   hr = pBackgroundCopyJob5->GetProperty(BITS_JOB_PROPERTY_ID_COST_FLAGS, 
                                         &actual_propval);
   if (FAILED(hr))
   {
    // SetSSLSecurityFlags failed.
    wprintf(L"GetProperty failed with error %x\n",hr);
    goto cancel;
   }

   DWORD job_transferpolicy = actual_propval.Dword;
   wprintf(L"get TransferPolicy Property returned %#x\n", job_transferpolicy);
  }
done:
  CoUninitialize();
 }
 return 1;

cancel:
 pBackgroundCopyJob->Cancel(); 
 pBackgroundCopyJob->Release();
 goto done;
}
```



 

 




