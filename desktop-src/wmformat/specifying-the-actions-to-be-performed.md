---
title: 指定要執行的動作
description: 指定要執行的動作
ms.assetid: b6b094b1-276d-4f90-adc7-0f3507fdfe27
keywords:
- Advanced Systems Format (ASF) ，指定動作
- ASF (Advanced Systems Format) ，指定動作
- 數位版權管理 (DRM) ，指定動作
- DRM (數位版權管理) ，指定動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2bd39a04d9ac87c4492749ca5e250d587c0e25
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374510"
---
# <a name="specifying-the-actions-to-be-performed"></a><span data-ttu-id="26ed4-107">指定要執行的動作</span><span class="sxs-lookup"><span data-stu-id="26ed4-107">Specifying the Actions To Be Performed</span></span>

<span data-ttu-id="26ed4-108">當您第一次呼叫 [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader)來建立讀取器物件時，第二個參數是 [**WMT \_ 許可權**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights)值的位 **or** 。</span><span class="sxs-lookup"><span data-stu-id="26ed4-108">When you first call [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) to create the reader object, the second parameter is a bitwise **OR** of [**WMT\_RIGHTS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) values.</span></span> <span data-ttu-id="26ed4-109">您可以使用此參數來指定 (s) 應用程式將在第一個開啟的檔案上執行的動作。</span><span class="sxs-lookup"><span data-stu-id="26ed4-109">Use this parameter to specify which action(s) the application will take on the first file to be opened.</span></span> <span data-ttu-id="26ed4-110">這些動作會直接對應到可在授權中指定的許可權。</span><span class="sxs-lookup"><span data-stu-id="26ed4-110">These actions correspond directly to rights that can be specified in the license.</span></span> <span data-ttu-id="26ed4-111">在後續對 [**IWMReader：： Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)的呼叫中，您可以藉由呼叫 [**IWMDRMReader：： SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty)來修改所要求的許可權、指定 [**DRM \_ 許可權**](drm-rights.md) 屬性的已定義常數，以及使用類型) **WCHAR** 的字串常值 (，並以分號分隔來識別許可權。</span><span class="sxs-lookup"><span data-stu-id="26ed4-111">On subsequent calls to [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), you can modify the rights that you are requesting by calling [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty), specifying the defined constant for the [**DRM\_Rights**](drm-rights.md) property, and using string literals (of type **WCHAR**) separated by semicolons to identify the rights.</span></span> <span data-ttu-id="26ed4-112">下列程式碼片段會要求四個許可權：播放檔案、將它複製到裝置，然後播放為共同作業播放清單的一部分。</span><span class="sxs-lookup"><span data-stu-id="26ed4-112">The following code snippet requests four rights: play the file, copy it to a device, and play it as part of a collaborative playlist.</span></span>


```C++
WCHAR wszRights[] = L"Play;Copy;CollaborativePlay";
p_WMDRMReader->SetDRMProperty(g_wszWMDRM_Rights, WMT_TYPE_STRING,
                              (BYTE*)wszRights, sizeof(wszRights));
```



> [!Note]  
> <span data-ttu-id="26ed4-113">請勿混淆 [ [**drm \_ 許可權**](drm-rights.md) ] 屬性與 [ [**drm \_ 旗標**](drm-flags.md) ] 屬性，這是用來指定從 CD 複製內容時，要套用到本機 DRM 第1版授權的 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="26ed4-113">Do not confuse the [**DRM\_Rights**](drm-rights.md) property with the [**DRM\_Flags**](drm-flags.md) property, which is a **DWORD** used to specify which rights to apply to a local DRM version 1 license when copying content from a CD.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="26ed4-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="26ed4-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26ed4-115">**讀取受保護的檔案**</span><span class="sxs-lookup"><span data-stu-id="26ed4-115">**Reading Protected Files**</span></span>](reading-protected-files.md)
</dt> </dl>

 

 




