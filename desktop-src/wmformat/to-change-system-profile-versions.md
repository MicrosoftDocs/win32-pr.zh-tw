---
title: 變更系統設定檔版本
description: 變更系統設定檔版本
ms.assetid: 66bf4041-47b5-41b4-abb4-eb08d05e3b28
keywords:
- 設定檔，系統
- 系統設定檔，版本
- 系統設定檔，變更版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c963a142c879242b5e2ae734dedb4073a120a57a9121c3f3f95e5838c15110a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084267"
---
# <a name="to-change-system-profile-versions"></a>變更系統設定檔版本

每當您建立配置檔案管理員物件時，它就會剖析系統設定檔。 您可以使用 [**IWMProfileManager：： GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) 和 [**IWMProfileManager：： LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) 方法來逐一查看系統設定檔，但配置檔案管理員只會計算單一版本的設定檔，並一次列出。 如果您想要使用此方法來尋找系統設定檔，您必須確定配置檔案管理員會處理您想要的版本。 使用 [**IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2) 介面的方法來設定和取出配置檔案管理員所使用的系統設定檔版本。

版本是使用 [**WMT \_ 版本**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_version) 列舉類型的成員來指定。 如果您將系統設定檔版本設定為 WMT \_ VER \_ 9 \_ 0，則呼叫會成功，但系統設定檔計數將會是零。 這是因為沒有預先定義的系統設定檔使用 Windows Media 音訊和 Video 9 系列編解碼器。 如需更新設定檔以使用最新編解碼器的詳細資訊，請參閱 [重複使用串流](reusing-stream-configurations.md)設定。

如果您依 GUID 識別碼載入系統設定檔，則配置檔案管理員所使用的系統設定檔版本並不重要。 如需有關載入系統設定檔的詳細資訊，請參閱 [載入系統設定檔](to-load-a-system-profile.md)。

下列範例程式碼示範如何設定和取出系統設定檔版本。 此範例會針對主控台輸出使用 printf，且需要包含 stdio.h。 如需使用此程式碼的詳細資訊，請參閱 [使用程式碼範例](using-the-code-examples.md)。


```C++
int main(void)
{
    HRESULT hr = S_OK;

    IWMProfileManager*  pProfileMgr  = NULL;
    IWMProfileManager2* pProfileMgr2 = NULL;

    WMT_VERSION         profileVersion;

    // Initialize COM.
    hr = CoInitialize(NULL);
    if(FAILED(hr))
    {
        printf("Could not initialize COM.");
        return 0;
    }

    // Create a profile manager object.
    hr = WMCreateProfileManager(&pProfileMgr);
    if(FAILED(hr))
    {
        printf("Could not create a profile manager object.");
        return 0;
    }

    // Get the IWMProfileManager2 interface.
    hr = pProfileMgr->QueryInterface(IID_IWMProfileManager2, 
                                     (void**) &pProfileMgr2);
    if(FAILED(hr))
    {
        printf("Could not get the IWMProfileManager2 interface.");
        SAFE_RELEASE(pProfileMgr);
        return 0;
    }

    // Release the old interface.
    SAFE_RELEASE(pProfileMgr);

    // Get the current system profile version.
    hr = pProfileMgr2->GetSystemProfileVersion(&profileVersion);
    if(FAILED(hr))
    {
        printf("Could not retrieve profile version.");
        printf("\nError code: 0x%X\n", hr);
        SAFE_RELEASE(pProfileMgr2);
        return 0;
    }
    
    // Display the current version.
    printf("Current version: ");
    switch(profileVersion)
    {
    case WMT_VER_4_0:
        printf("WMT_VER_4_0\n");
        break;
    case WMT_VER_7_0:
        printf("WMT_VER_7_0\n");
        break;
    case WMT_VER_8_0:
        printf("WMT_VER_8_0\n");
        break;
    case WMT_VER_9_0:
        printf("WMT_VER_9_0\n");
        break;
    }

    // Set the system profile version to 8.
    profileVersion = WMT_VER_8_0;

    hr = pProfileMgr2->SetSystemProfileVersion(profileVersion);
    if(FAILED(hr))
    {
        printf("Could not change profile version.");
        printf("\nError code: 0x%X\n", hr);
        SAFE_RELEASE(pProfileMgr2);
        return 0;
    }

    // Print verification.
    printf("Successfully set version to ");
    switch(profileVersion)
    {
    case WMT_VER_4_0:
        printf("WMT_VER_4_0\n");
        break;
    case WMT_VER_7_0:
        printf("WMT_VER_7_0\n");
        break;
    case WMT_VER_8_0:
        printf("WMT_VER_8_0\n");
        break;
    case WMT_VER_9_0:
        printf("WMT_VER_9_0\n");
        break;
    }

    // Clean up.
    SAFE_RELEASE(pProfileMgr2);
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用系統設定檔**](using-system-profiles.md)
</dt> </dl>

 

 




