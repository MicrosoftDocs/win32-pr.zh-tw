---
title: 將設定檔與寫入器搭配使用
description: 將設定檔與寫入器搭配使用
ms.assetid: 8805bc57-5f19-4544-bcb8-5af880ba8ea0
keywords:
- Windows Media Format SDK，寫入 ASF 檔案
- Windows Media Format SDK，建立 ASF 檔案
- 'Windows Media Format SDK、Advanced Systems Format (ASF) '
- Advanced Systems Format (ASF) ，寫入檔案
- ASF (Advanced Systems Format) ，寫入檔案
- Advanced Systems Format (ASF) ，建立檔案
- ASF (Advanced Systems Format) ，建立檔案
- 設定檔，建立 ASF 檔案
- 設定檔，寫入 ASF 檔案
- 設定檔，ASF 檔案建立
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d027e6ea0e669d2a5206901faefab1f5a9583153
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104023161"
---
# <a name="to-use-profiles-with-the-writer"></a><span data-ttu-id="0b4f2-113">將設定檔與寫入器搭配使用</span><span class="sxs-lookup"><span data-stu-id="0b4f2-113">To Use Profiles with the Writer</span></span>

<span data-ttu-id="0b4f2-114">寫入器會使用設定檔資料來建立 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="0b4f2-114">The writer uses profile data to create ASF files.</span></span> <span data-ttu-id="0b4f2-115">您必須指定要使用的設定檔，才能使用寫入器進行任何其他動作。</span><span class="sxs-lookup"><span data-stu-id="0b4f2-115">You must specify a profile for use before doing anything else with the writer.</span></span>

<span data-ttu-id="0b4f2-116">您可以藉由將設定檔識別碼傳遞給 [**IWMWriter：： SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid) 方法，來設定要搭配寫入器使用的系統設定檔。</span><span class="sxs-lookup"><span data-stu-id="0b4f2-116">You can set a system profile for use with the writer by passing the profile ID to the [**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid) method.</span></span>

<span data-ttu-id="0b4f2-117">若要指定要與寫入器搭配使用的自訂設定檔，您必須為包含所需設定檔資料的物件取得 [**IWMProfile**](iwmprofile.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="0b4f2-117">To specify a custom profile for use with the writer, you must obtain an [**IWMProfile**](iwmprofile.md) interface to an object containing the desired profile data.</span></span> <span data-ttu-id="0b4f2-118">您可以使用其中一個 [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) 介面的載入方法來完成這項工作。</span><span class="sxs-lookup"><span data-stu-id="0b4f2-118">You can use one of the loading methods of the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface to accomplish this.</span></span> <span data-ttu-id="0b4f2-119">當您有有效的 **IWMProfile** 介面之後，您可以將其指標傳遞至 [**IWMWriter：： SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) 方法。</span><span class="sxs-lookup"><span data-stu-id="0b4f2-119">After you have a valid **IWMProfile** interface, you can pass a pointer to it to the [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) method.</span></span> <span data-ttu-id="0b4f2-120">如需設定檔設定的詳細資訊，請參閱 [使用設定檔](working-with-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="0b4f2-120">For more information about profile settings, see [Working with Profiles](working-with-profiles.md).</span></span>

<span data-ttu-id="0b4f2-121">如果您在設定寫入器中的設定檔之後，使用 **IWMProfile** 介面變更設定檔物件，您必須再次呼叫 **SetProfile** ，否則這些變更不會反映在寫入器中。</span><span class="sxs-lookup"><span data-stu-id="0b4f2-121">If you make changes to the profile object by using the **IWMProfile** interface after setting the profile in the writer, you must call **SetProfile** again, or else the changes will not be reflected in the writer.</span></span> <span data-ttu-id="0b4f2-122">不過，呼叫 **SetProfile** 會重設所有的標頭屬性，因此請務必在呼叫這個方法之後設定任何必要的標頭屬性。</span><span class="sxs-lookup"><span data-stu-id="0b4f2-122">However, calling **SetProfile** will reset all header attributes, so be sure to set any required header attributes after calling this method.</span></span>

<span data-ttu-id="0b4f2-123">下列範例函式會將設定檔設定為「Windows Media 視訊8（適用于撥號數據機 (56 Kbps) 」）：</span><span class="sxs-lookup"><span data-stu-id="0b4f2-123">The following example function sets the profile to "Windows Media Video 8 for Dial-up Modems (56 Kbps)":</span></span>


```C++
#include <wmsysprf.h>

HRESULT SetProfileExample()
{
  HRESULT hr;
  IWMWriter *pWriter = NULL;
  hr = WMCreateWriter(NULL, &pWriter);
  if (FAILED(hr)) return hr;
  hr = pWriter->SetProfileByID(WMProfile_V80_56Video);
  return hr;
}

```



> [!Note]  
> <span data-ttu-id="0b4f2-124">沒有使用 Windows Media 音訊和 Video 9 系列編解碼器的預先定義系統設定檔。</span><span class="sxs-lookup"><span data-stu-id="0b4f2-124">There are no predefined system profiles that use the Windows Media Audio and Video 9 Series codecs.</span></span> <span data-ttu-id="0b4f2-125">如需詳細資訊，請參閱 [重複使用串流](reusing-stream-configurations.md)設定。</span><span class="sxs-lookup"><span data-stu-id="0b4f2-125">For more information, see [Reusing Stream Configurations](reusing-stream-configurations.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0b4f2-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="0b4f2-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b4f2-127">**IWMWriter::SetProfileByID**</span><span class="sxs-lookup"><span data-stu-id="0b4f2-127">**IWMWriter::SetProfileByID**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)
</dt> <dt>

[<span data-ttu-id="0b4f2-128">**使用設定檔**</span><span class="sxs-lookup"><span data-stu-id="0b4f2-128">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> <dt>

[<span data-ttu-id="0b4f2-129">**寫入 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="0b4f2-129">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




