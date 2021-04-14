---
title: 正在儲存設定檔
description: 正在儲存設定檔
ms.assetid: 07c1ef16-6696-4314-aed8-58cda464b0db
keywords:
- Windows Media Format SDK，儲存設定檔
- Windows Media Format SDK，設定檔儲存
- 設定檔，儲存
- 設定檔，IWMProfileManager 介面
- IWMProfileManager，儲存設定檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 276b002f0b7f98de2e84f2c27a4f52bde25726bb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374395"
---
# <a name="saving-profiles"></a><span data-ttu-id="4476d-108">正在儲存設定檔</span><span class="sxs-lookup"><span data-stu-id="4476d-108">Saving Profiles</span></span>

<span data-ttu-id="4476d-109">您可以使用 [**IWMProfileManager：： SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile) 方法，將設定檔物件的內容儲存至使用 XML 格式化的字串。</span><span class="sxs-lookup"><span data-stu-id="4476d-109">You can use the [**IWMProfileManager::SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile) method to save the contents of a profile object to a string formatted with XML.</span></span> <span data-ttu-id="4476d-110">未提供任何方法來將設定檔字串儲存至檔案;您可以使用您選擇的檔案 i/o 常式。</span><span class="sxs-lookup"><span data-stu-id="4476d-110">No methods are provided to store the profile string to a file; you can use the file I/O routines of your choice.</span></span>

> [!Note]  
> <span data-ttu-id="4476d-111">您絕對不應該變更寫入檔案的設定檔字串。</span><span class="sxs-lookup"><span data-stu-id="4476d-111">You should never alter the profile string written to a file.</span></span> <span data-ttu-id="4476d-112">您要對設定檔進行的任何變更，都應該以程式設計的方式進行。</span><span class="sxs-lookup"><span data-stu-id="4476d-112">Any changes you want to make to a profile should be made programmatically.</span></span> <span data-ttu-id="4476d-113">變更 prx 檔案中的值可能會導致無法預期的結果。</span><span class="sxs-lookup"><span data-stu-id="4476d-113">Changing values in a .prx file can cause unpredictable results.</span></span>

 

<span data-ttu-id="4476d-114">下列範例是使用標準 C 樣式檔案 i/o 將設定檔儲存至檔案的函式。</span><span class="sxs-lookup"><span data-stu-id="4476d-114">The following example is a function to save a profile to a file using standard C-style file I/O.</span></span> <span data-ttu-id="4476d-115">若要編譯使用此範例的應用程式，您必須在專案中包含 stdio.h。</span><span class="sxs-lookup"><span data-stu-id="4476d-115">To compile an application that uses this example, you must include stdio.h in your project.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="4476d-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="4476d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4476d-117">**使用設定檔**</span><span class="sxs-lookup"><span data-stu-id="4476d-117">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




