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
# <a name="working-with-localized-system-profiles"></a><span data-ttu-id="67a84-108">使用當地語系化的系統設定檔</span><span class="sxs-lookup"><span data-stu-id="67a84-108">Working with Localized System Profiles</span></span>

<span data-ttu-id="67a84-109">Windows Media Format SDK 包含系統設定檔，其中包含數種語言的名稱和描述。</span><span class="sxs-lookup"><span data-stu-id="67a84-109">The Windows Media Format SDK includes system profiles with names and descriptions in several languages.</span></span> <span data-ttu-id="67a84-110">當地語系化的系統設定檔 prx 檔案會安裝到 \[ SDKRoot \] \\ WMSDK \\ WMFSDK9 \\ LocalizedProfiles 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="67a84-110">The localized system profile .prx files are installed into the \[SDKRoot\]\\WMSDK\\WMFSDK9\\LocalizedProfiles folder.</span></span> <span data-ttu-id="67a84-111">若要使用 **IWMProfileManagerLanguage** 方法來存取特定檔案，您必須將它移至系統根目錄以及其他系統設定檔。</span><span class="sxs-lookup"><span data-stu-id="67a84-111">To access a particular file with the **IWMProfileManagerLanguage** methods, you must move it into the system root directory along with the other system profile files.</span></span> <span data-ttu-id="67a84-112">如需當地語系化的系統組態檔案清單，請參閱 [當地語系化的系統組態](localized-system-profiles.md)檔。</span><span class="sxs-lookup"><span data-stu-id="67a84-112">For a list of the localized system profile files, see [Localized System Profiles](localized-system-profiles.md).</span></span>

<span data-ttu-id="67a84-113">您可以使用 [**IWMProfileManagerLanguage**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) 介面的方法來設定或取得系統設定檔語言。</span><span class="sxs-lookup"><span data-stu-id="67a84-113">You can set or retrieve the system profile language using the methods of the [**IWMProfileManagerLanguage**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) interface.</span></span> <span data-ttu-id="67a84-114">語言會指定為 LANGID 值，其中包含主要語言識別項和次要語言識別項。</span><span class="sxs-lookup"><span data-stu-id="67a84-114">The language is specified as a LANGID value, which consists of a primary language identifier and a secondary language identifier.</span></span> <span data-ttu-id="67a84-115">下列程式碼示範如何取出目前的語言。</span><span class="sxs-lookup"><span data-stu-id="67a84-115">The following code demonstrates how to retrieve the current language.</span></span> <span data-ttu-id="67a84-116">預設語言是美國英文 (0x409) 。</span><span class="sxs-lookup"><span data-stu-id="67a84-116">The default language is U.S. English (0x409).</span></span> <span data-ttu-id="67a84-117">如需使用此程式碼的詳細資訊，請參閱 [使用程式碼範例](using-the-code-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="67a84-117">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="67a84-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="67a84-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67a84-119">**使用系統設定檔**</span><span class="sxs-lookup"><span data-stu-id="67a84-119">**Using System Profiles**</span></span>](using-system-profiles.md)
</dt> </dl>

 

 




