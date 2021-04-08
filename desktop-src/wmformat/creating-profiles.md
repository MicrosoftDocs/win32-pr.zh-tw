---
title: 建立設定檔
description: 建立設定檔
ms.assetid: af4a8efe-d797-4d19-961d-b917e4c7c81a
keywords:
- Windows Media Format SDK，設定檔
- 設定檔，建立
- 設定檔，IWMProfileManager 介面
- IWMProfileManager，建立設定檔
- 設定檔，WMCreateProfileManager 函式
- WMCreateProfileManager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45eeca9e99e09bd709b7e9fdf1aeffe8d35ca14a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023013"
---
# <a name="creating-profiles"></a>建立設定檔

在許多情況下，您會想要建立一個空白設定檔來設定您的需求。 在其他情況下，您可以更輕鬆地編輯現有的設定檔，例如系統設定檔。 如需使用系統設定檔的詳細資訊，請參閱 [使用系統設定檔](using-system-profiles.md)。

建立可供您設定的空白設定檔需要設定檔管理員物件。 若要取得配置檔案管理員物件的 [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) 介面，請呼叫 [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) 函數。

若要建立空的設定檔，請呼叫 [**IWMProfileManager：： CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile)。 當您建立空白設定檔時，您唯一指定的就是設定檔所符合的 Windows Media 格式 SDK 版本。 除非您有特定的需要使用舊版，否則您應該一律使用最新版本。 版本會指示設定檔的結構;先前的版本不支援某些屬性。

下列範例程式碼顯示如何建立新的設定檔。 若要在您的應用程式中編譯此程式碼，請包含 stdio.h .h。 如需使用此程式碼的詳細資訊，請參閱 [使用程式碼範例](using-the-code-examples.md)。


```C++
HRESULT CreateProfile(IWMProfileManager* pProfileMgr, IWMProfile** ppProfile)
{
    HRESULT hr = S_OK;

    // Create the empty profile.
    hr = pProfileMgr->CreateEmptyProfile(WMT_VER_9_0, ppProfile);
    if(FAILED(hr))
    {
        printf("Could not create the profile.\n");
        return hr;
    }

    return S_OK;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMProfile 介面**](iwmprofile.md)
</dt> <dt>

[**IWMProfileManager 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**使用設定檔**](working-with-profiles.md)
</dt> </dl>

 

 




