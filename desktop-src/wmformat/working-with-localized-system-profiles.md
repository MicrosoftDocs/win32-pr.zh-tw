---
title: 使用當地語系化的系統設定檔
description: 使用當地語系化的系統設定檔
ms.assetid: d911baf6-0731-4f02-9001-d04464a03f56
keywords:
- 設定檔，系統
- 系統設定檔，當地語系化
- 系統設定檔，IWMProfileManagerLanguage 介面
- 當地語系化的系統設定檔，關於
- IWMProfileManagerLanguage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd8c040d9804cd822b17e7caad8a8cfb5e5854c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106967657"
---
# <a name="working-with-localized-system-profiles"></a>使用當地語系化的系統設定檔

Windows Media Format SDK 包含系統設定檔，其中包含數種語言的名稱和描述。 當地語系化的系統設定檔 prx 檔案會安裝到 \[ SDKRoot \] \\ WMSDK \\ WMFSDK9 \\ LocalizedProfiles 資料夾中。 若要使用 **IWMProfileManagerLanguage** 方法來存取特定檔案，您必須將它移至系統根目錄以及其他系統設定檔。 如需當地語系化的系統組態檔案清單，請參閱 [當地語系化的系統組態](localized-system-profiles.md)檔。

您可以使用 [**IWMProfileManagerLanguage**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) 介面的方法來設定或取得系統設定檔語言。 語言會指定為 LANGID 值，其中包含主要語言識別項和次要語言識別項。 下列程式碼示範如何取出目前的語言。 預設語言是美國英文 (0x409) 。 如需使用此程式碼的詳細資訊，請參閱 [使用程式碼範例](using-the-code-examples.md)。


```C++
HRESULT GetCurrentSystemProfileLanguage(IMWProfilManager* pProfileMgr)
{
    HRESULT hr = S_OK;

    IWMProfileManagerLanguage* pProfileMgrLang = NULL;

    // Get the profile manager language interface.
    hr = pProfileMgr->QueryInterface(IID_IWMProfileManagerLanguage,
                                     (void **) &pProfileMgrLang);
    if(FAILED(hr))
    {
        printf("Couldn't get IWMProfileManagerLanguage.\n");
        SAFE_RELEASE(pProfileMgrLang);
        return hr;
    }

    // Retrieve the current language (as a LANGID value)
    WORD wLangID = 0;
    hr = pProfileMgrLang->GetUserLanguageID(&wLangID);
    if(FAILED(hr))
    {
        printf("Could not get the current language.\n");
        SAFE_RELEASE(pProfileMgrLang);
        return hr;
    }

    printf("The current language ID is 0x%X\n", wLangID);

    SAFE_RELEASE(pProfileMgrLang);
    return S_OK;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用系統設定檔**](using-system-profiles.md)
</dt> </dl>

 

 




