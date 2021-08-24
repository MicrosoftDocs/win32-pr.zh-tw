---
title: SHV 模組
description: 請注意，從 Windows 10 設定系統健全狀況驗證程式 (SHV) 模組（包括向 NAP 系統註冊及取消註冊）時，無法使用網路存取保護平臺。
ms.assetid: 0f2edd23-d44a-4a01-ae33-f7eef0e4b27f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 344b3a6d74acee0e06e3d2a9fedd4784b1c9d76ac8ba84c68ed4b7ef8ceebc56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133426"
---
# <a name="shv-module"></a>SHV 模組

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

設定系統健康狀態驗證 (SHV) 模組，包括向 NAP 系統註冊及取消註冊。

> [!Note]  
> NAP SDK 也包含一組完整的範例程式碼，可在中 \\ 找到。範例 \\ NetDS \\ NAP .。。SDK 安裝的目錄。 此範例集包括系統健康情況代理程式 (SHA) 、SHV 和強制用戶端 (EC) 。 它有完整的工作 NAP 案例，可設定 SHA-SHV 與 SHA-1 之間的通訊。

 


```C++
#include <windows.h>
#include "stdafx.h"
#include "NapUtil.h"

static const wchar_t friendlyName[] = L"SDK SHV Sample";
static const wchar_t version[] = L"1.0.0.1";
static const wchar_t description[] = L"System Health Validator(SHV)";
static const wchar_t vendor[] = L"Microsoft";

/// Registers the SDK SHV with the NAP Server.
HRESULT RegisterSdkShv()
{
    HRESULT hr = S_OK;
    CComPtr<INapServerManagement> pSHVMgmt = NULL;
    
    NapComponentRegistrationInfo shvInfo;
    ZeroMemory (&shvInfo, sizeof(shvInfo));

    hr = pSHVMgmt.CoCreateInstance(CLSID_NapServerManagement, NULL, CLSCTX_INPROC_SERVER);
    hr = FillShvComponentRegistrationInfo(&shvInfo);
    hr = pSHVMgmt->RegisterSystemHealthValidator(&shvInfo, (CLSID *)&__uuidof(CSampleShv));
    
    FreeComponentRegistration(&shvInfo);
    return hr;
}

/// Unregisters the SDK SHV with the NAP Server.
HRESULT UnregisterSdkShv()
{
    HRESULT hr = S_OK;
    CComPtr<INapServerManagement> pSHVMgmt = NULL;

    hr = pSHVMgmt.CoCreateInstance(CLSID_NapServerManagement, NULL, CLSCTX_INPROC_SERVER);
    hr = pSHVMgmt->UnregisterSystemHealthValidator(QuarSampleSystemHealthId);
    return hr;
}

/// Fill the NapComponentRegistrationInfo structure that needs to be passed during registration.
HRESULT FillShvComponentRegistrationInfo (NapComponentRegistrationInfo *shvInfo)
{
    HRESULT hr = S_OK;
    shvInfo->id = QuarSampleSystemHealthId;

    //<Temporarily till implement the Info Class>
    shvInfo->infoClsid = GUID_NULL; 

    hr = ConstructCountedString(friendlyName, sizeof(friendlyName), &(shvInfo->friendlyName));
    hr = ConstructCountedString(description, sizeof(description), &(shvInfo->description));
    hr = ConstructCountedString(version, sizeof(version), &(shvInfo->version));
    hr = ConstructCountedString(vendor, sizeof(vendor), &(shvInfo->vendorName));
    return hr;
}

// Helper Function for FillShvComponentRegistrationInfo.
HRESULT ConstructCountedString(const WCHAR* src, UINT16 len, CountedString* dest)
{
    HRESULT hr = S_OK;
    DWORD retCode = ERROR_SUCCESS;
    hr = AllocateMemory(dest->string, ((len+1)*sizeof(WCHAR)));
    dest->length = len;
    retCode = StringCchCopy(dest->string, len+1, src);
    return hr;
}

// Helper Function for releasing ShaComponentRegistrationInfo members
void FreeComponentRegistration(NapComponentRegistrationInfo *shvInfo)
{
    FreeMemory(shvInfo->friendlyName.string);
    FreeMemory(shvInfo->description.string);
    FreeMemory(shvInfo->version.string);
    FreeMemory(shvInfo->vendorName.string);
}

```



 

 




