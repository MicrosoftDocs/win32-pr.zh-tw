---
title: 設定簡單的 SHA
description: 下列範例會設定簡單的系統健康情況代理程式 (SHA) ，並顯示兩個選擇性的健全狀況聲明 (SoH) 變更通知和 SoH 快取排清。
ms.assetid: 7c96e1ca-f9b2-40e6-bd89-c8ef77b48dfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94625e99f604fd282a5b1177992f6e9e413b30d35f61767ad7231315dddfab53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780738"
---
# <a name="setting-up-a-simple-sha"></a>設定簡單的 SHA

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

下列範例會設定簡單的系統健康情況代理程式 (SHA) ，並顯示兩個選擇性動作：健全狀況的聲明 (SoH) 變更通知和 SoH 快取排清。 請注意，在此範例中，錯誤處理不會包含在主要 () 函數中。

> [!Note]  
> NAP SDK 也包含一組完整的範例程式碼，可在中 \\ 找到。範例 \\ NetDS \\ NAP .。。SDK 安裝的目錄。 此範例集包含 SHA、系統健全狀況驗證程式 (SHV) 和強制用戶端 (EC) 。 它有完整的工作 NAP 案例，可設定 SHA-SHV 與 SHA-1 之間的通訊。

 


```C++
#include <windows.h>
#include <stdio.h>
#include "Callback.h"
#include <NapTypes.h>
#include <NapClientManagement.h>
#include "Strsafe.h"

static const UINT32 NapSystemHealthId = 0x000137F0;

// Set GUID infoClsid equal to {08B8B292-7033-46f3-AB97-D62B6FCDC0DE}
static const GUID infoClsid = { 0x8b8b292, 0x7033, 0x46f3, { 0xab, 0x97, 0xd6, 0x2b, 0x6f, 0xcd, 0xc0, 0xde } };
static const wchar_t SHA_FRIENDLY_NAME[] = L"SHA SDK Sample";
static const wchar_t SHA_DESCRIPTION[] = L"Microsoft SHA SDK Sample";
static const wchar_t SHA_VERSION[] = L"1.0.0.1";
static const wchar_t SHA_VENDOR_NAME[] = L"Microsoft";

// Helper Function for FillShaComponentRegistrationInfo.
HRESULT ConstructCountedString(const WCHAR* src, UINT16 len,
   CountedString* dest)
{
    HRESULT hr = S_OK;
    DWORD retCode = ERROR_SUCCESS;
    hr = AllocateMemory(dest->string, ((len+1)*sizeof(WCHAR)));
    dest->length = len;
    retCode = StringCchCopy(dest->string, len+1, src);
    return hr;
}

HRESULT FillShaComponentRegistrationInfo(NapComponentRegistrationInfo *agentInfo)
{
    HRESULT hr = S_OK;
    agentInfo->id = NapSystemHealthId;
    agentInfo->infoClsid = infoClsid;
    hr = ConstructCountedString(SHA_FRIENDLY_NAME, sizeof(SHA_FRIENDLY_NAME), &(agentInfo->friendlyName));
    hr = ConstructCountedString(SHA_DESCRIPTION, sizeof(SHA_DESCRIPTION), &(agentInfo->description));
    hr = ConstructCountedString(SHA_VERSION, sizeof(SHA_VERSION), &(agentInfo->version));
    hr = ConstructCountedString(SHA_VENDOR_NAME, sizeof(SHA_VENDOR_NAME), &(agentInfo->vendorName));
    return hr;
}

// Helper Function for releasing ShaComponentRegistrationInfo members
void FreeComponentRegistration(NapComponentRegistrationInfo *agentInfo)
{
    FreeMemory(agentInfo->friendlyName.string);
    FreeMemory(agentInfo->description.string);
    FreeMemory(agentInfo->version.string);
    FreeMemory(agentInfo->vendorName.string);
}

// Registers the SHA with the NAP Server.
HRESULT CsdkShaModule::RegisterSha()
{
    HRESULT hr = S_OK;

    // Pointer to the INapServerManagement interface
    CComPtr<INapClientManagement> m_pNAPClientMgmt = NULL;

    // Registration Information
    NapComponentRegistrationInfo m_shaInfo;
    
    ZeroMemory (&m_shaInfo, sizeof(m_shaInfo));
    hr = m_pNAPClientMgmt.CoCreateInstance(CLSID_NapClientManagement, NULL, CLSCTX_INPROC_SERVER);

    if (FAILED(hr))
    {
       DebugPrintfW(L"RegisterSdkSha: CoCreateInstance Failed with %#x",hr);
       goto Cleanup;
    }

    hr = FillShaComponentRegistrationInfo(&m_shaInfo);
    if(FAILED(hr))
    {
       DebugPrintfW(L"RegisterSdkSha:: FillShaComponentRegistrationInfo Failed with %#x",hr);
       goto Cleanup;
    }

    hr = m_pNAPClientMgmt->RegisterSystemHealthAgent(&m_shaInfo);
    if (FAILED(hr))
    {
       DebugPrintfW(L"RegisterSdkSha:: RegisterSystemHealthAgent failed %#x", hr);
       goto Cleanup;
    }
 
    Cleanup:
       FreeComponentRegistration(&m_shaInfo);
       return hr;
}

// Unregisters the SHA with the NAP Server.
HRESULT CSdkShaModule::UnRegisterSha()
{
    HRESULT hr = S_OK;
    // Pointer to the INapServerManagement interface
    CComPtr<INapClientManagement> m_pNAPClientMgmt = NULL;

    hr = m_pNAPClientMgmt.CoCreateInstance(CLSID_NapClientManagement, NULL, CLSCTX_INPROC_SERVER);

    if (FAILED(hr))
    {
       DebugPrintfW(L"UnregisterSdkSha: CoCreateInstance Failed with %#x",hr);
       goto Cleanup;
    }

    hr = m_pNAPClientMgmt->UnregisterSystemHealthAgent(QuarSampleSystemHealthId);
    if (FAILED(hr))
    {
       DebugPrintfW(L"UnregisterSdkSha: UnregisterSystemHealthAgent Failed with %#x",hr);
       goto Cleanup;
    }

    Cleanup:
       return hr;
}

// Main function
DWORD __cdecl wmain(DWORD argc, WCHAR * pArgv[])  throw()
{
    HRESULT hr = S_OK;

    // 1. Register Sha
    hr = RegisterSha();

    // 2. Start up COM and ATL.
    hr  = CoInitializeEx(NULL, COINIT_MULTITHREADED );

    // 3. Create Binding instance
    // pointer to the binding  interface
    CComPtr<INapSystemHealthAgentBinding> binding = NULL;
    hr = binding.CoCreateInstance(CLSID_NapSystemHealthAgentBinding, NULL, CLSCTX_INPROC_SERVER);

    // 4. Create Callback
    // Create Callback (The code for this interface is separate)
    IShaCallbackPtr callback = NULL;
    callback = ShaCallback::CreateInstance(binding);

    // 5. Call Initialize on the binding interface
    hr = binding->Initialize(QuarSampleSystemHealthId,callback);

    // 6. Send Notify SoH Change OR Flush Cache
    hr = binding->NotifySoHChange();
    //  hr = binding->FlushCache();

    // 7. Stopping the SHA
    hr = binding->Uninitialize();
    
    hr = UnRegisterSha();

    return 0;
}

// SHA Callback 
STDMETHODIMP ShaCallback::GetFixupInfo(FixupInfo** ppStatus)
{
    wprintf(L"\nQA called ShaCallback::GetFixupInfo()\n");
    HRESULT hr = S_OK;

    assert(ppStatus != NULL);

    // The caller should free this memory using CoTaskMemFree
    hr = AllocFixupInfo(ppStatus, NUMBER_OF_HRESULTS);
    if (FAILED(hr))
    {
       goto Cleanup;
    }

    //
    // SDK Note:
    //
    // ppStatus should be filled according to the current Fix-up status. This 
    // is just a simple example
    if (g_setHealthySoh)
    {
       (*ppStatus)->fixupMsgId = SDK_SAMPLE_GENERIC_FIXUP_SUCCESS_MSG_ID;
       (*ppStatus)->percentage = 100;
       (*ppStatus)->state = fixupStateSuccess;
    }
    else
    {
       (*ppStatus)->fixupMsgId = SDK_SAMPLE_GENERIC_FIXUP_INPROGRESS_MSG_ID;
       (*ppStatus)->percentage = 50;
       (*ppStatus)->state = fixupStateInProgress;
    }

    (*ppStatus)->resultCodes.count = NUMBER_OF_HRESULTS;   // 1 HRESULT
    *((*ppStatus)->resultCodes.results) = S_OK;

    Cleanup:
        return hr;
}

```



 

 




