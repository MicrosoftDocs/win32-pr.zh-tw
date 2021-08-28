---
title: 載入系統設定檔
description: 載入系統設定檔
ms.assetid: 2398a44d-c5c7-4fa2-b0ed-1cfb75d8822c
keywords:
- 設定檔，系統
- 系統設定檔，載入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: becd98903921b81ce1eaf7d2317659c7760bb99c4e55e07efe336719d5d34ed4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807478"
---
# <a name="to-load-a-system-profile"></a>載入系統設定檔

若要變更系統設定檔，您必須將它載入至設定檔物件。 配置檔案管理員提供兩種載入系統設定檔的選項：依識別碼和依索引。

系統設定檔識別碼是在建立時指派給系統設定檔的 GUID 值。 如需與第8版系統設定檔相關聯的 GUID 常數清單，請參閱 [系統設定檔](system-profiles.md)。 您可以在標頭檔 WMSysPrf 中找到先前版本的 GUID 常數。 如需 Windows 媒體格式 SDK 隨附的此檔案和其他標頭檔的詳細資訊，請參閱連結[庫檔案和編譯器設定](library-files-and-compiler-settings.md)。

下列範例程式碼示範如何使用系統設定檔識別碼載入系統設定檔。 若要讓此程式碼能夠運作，您必須包含 WMSysPrf .h 和 stdio.h。 如需使用此程式碼的詳細資訊，請參閱 [使用程式碼範例](using-the-code-examples.md)。


```C++
IWMProfileManager* pProfileMgr = NULL;
IWMProfile*        pProfile    = NULL;

HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a profile manager.
hr = WMCreateProfileManager(&pProfileMgr);

// Retrieve the data for the general-purpose broadband video profile.
hr = pProfileMgr->LoadProfileByID(WMProfile_V80_100Video, &pProfile);

// TODO: Perform whatever customizations are needed. For details about
// editing profiles, see Using Custom Profiles.

// Clean up.
pProfile->Release();
pProfile = NULL;
pProfileMgr->Release();
pProfileMgr = NULL;
```



如果您不知道要使用哪一個設定檔，您可以使用 [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)介面的 [**GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount)和 [**LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile)方法，逐一查看特定版本的所有系統設定檔。 這些方法一次只處理一個版本的系統設定檔。 如需變更系統設定檔版本的詳細資訊，請參閱 [變更系統設定檔版本](to-change-system-profile-versions.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用系統設定檔**](using-system-profiles.md)
</dt> </dl>

 

 




