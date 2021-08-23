---
title: 正在儲存設定檔
description: 正在儲存設定檔
ms.assetid: 07c1ef16-6696-4314-aed8-58cda464b0db
keywords:
- Windows媒體格式 SDK，儲存設定檔
- Windows媒體格式 SDK，設定檔儲存
- 設定檔，儲存
- 設定檔，IWMProfileManager 介面
- IWMProfileManager，儲存設定檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6befb09d7e0d628462bdd22e1e905c351be58dc077959089883ce3707dc493d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547038"
---
# <a name="saving-profiles"></a>正在儲存設定檔

您可以使用 [**IWMProfileManager：： SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile) 方法，將設定檔物件的內容儲存至使用 XML 格式化的字串。 未提供任何方法來將設定檔字串儲存至檔案;您可以使用您選擇的檔案 i/o 常式。

> [!Note]  
> 您絕對不應該變更寫入檔案的設定檔字串。 您要對設定檔進行的任何變更，都應該以程式設計的方式進行。 變更 prx 檔案中的值可能會導致無法預期的結果。

 

下列範例是使用標準 C 樣式檔案 i/o 將設定檔儲存至檔案的函式。 若要編譯使用此範例的應用程式，您必須在專案中包含 stdio.h。


```C++
HRESULT ProfileToFile(IWMProfileManager* pProfileMgr, 
                      IWMProfile* pProfile)
{
    HRESULT hr = S_OK;

    FILE*   pFile;
    
    WCHAR*  pwszProfileString = NULL;
    DWORD   cchProfileString = 0;

    // Save the profile to a string.
    // First, retrieve the size of the string required.
    hr = pProfileMgr->SaveProfile(pProfile, 
                                  NULL, 
                                  &cchProfileString);
    if(FAILED(hr))
    {
        printf("Could not get the profile string size.");
        return hr;
    }

    // Allocate memory to hold the string.
    pwszProfileString = new WCHAR[cchProfileString];

    if(pwszProfileString == NULL)
    {
        printf("Could not allocate memory for the profile string.");
        return E_OUTOFMEMORY;
    }

    // Retrieve the string.
    hr = pProfileMgr->SaveProfile(pProfile, 
                                  pwszProfileString, 
                                  &cchProfileString);
    if(FAILED(hr))
    {
        printf("Could not save the profile string.");
        return hr;
    }

    // Create the output file.
    pFile = fopen("MyProfile.prx", "w");

    // Write the profile string to the file.
    fprintf(pFile, "%S\n", pwszProfileString);

    // Close the file.
    fclose(pFile);

    delete[] pwszProfileString;

    return S_OK;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用設定檔**](working-with-profiles.md)
</dt> </dl>

 

 




