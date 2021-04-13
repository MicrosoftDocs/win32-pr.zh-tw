---
title: 使用 DRM 第1版保護檔案
description: 使用 DRM 第1版保護檔案
ms.assetid: 91de1c20-e926-4ff6-b0cd-e90fc9cbaad2
keywords:
- Windows Media Format SDK，建立受保護的檔案
- Windows Media Format SDK，受保護的檔案
- Advanced Systems Format (ASF) ，建立受保護的檔案
- ASF (Advanced Systems Format) ，建立受保護的檔案
- Advanced Systems Format (ASF) 、受保護的檔案
- ASF (Advanced 系統格式) 、受保護的檔案
- Advanced Systems Format (ASF) ，WMStubDRM .lib
- ASF (Advanced Systems Format) ，WMStubDRM .lib
- WMStubDRM .lib，建立受保護的檔案
- WMStubDRM .lib，受保護的檔案
- 數位版權管理 (DRM) ，WMStubDRM .lib
- DRM (數位版權管理) ，WMStubDRM .lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3e4d1ae9c0d3835c20f75b4e61c262a85a26f4
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104314517"
---
# <a name="protecting-files-with-drm-version-1"></a><span data-ttu-id="97369-115">使用 DRM 第1版保護檔案</span><span class="sxs-lookup"><span data-stu-id="97369-115">Protecting Files with DRM Version 1</span></span>

<span data-ttu-id="97369-116">套用這種類型的保護時，會產生僅在提出授權要求的電腦上有效的 DRM 第1版授權。</span><span class="sxs-lookup"><span data-stu-id="97369-116">When this kind of protection is applied, a DRM version 1 license is generated that is valid only on the machine from which the license request was made.</span></span> <span data-ttu-id="97369-117">因為未設定任何金鑰或金鑰種子，所以無法使用這項技術來產生受保護內容的可移植授權。</span><span class="sxs-lookup"><span data-stu-id="97369-117">Because no key or key seed is set, there is no way to generate portable licenses for content protected using this technique.</span></span> <span data-ttu-id="97369-118">不過，使用 Windows Media 格式 SDK 7.1 或更新版本時，授權可在 Microsoft 授權遷移服務復原。</span><span class="sxs-lookup"><span data-stu-id="97369-118">However, when using the Windows Media Format SDK 7.1 or later, the licenses are recoverable at the Microsoft License Migration service.</span></span>

<span data-ttu-id="97369-119">若要使用 DRM 第1版保護 ASF 檔案，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="97369-119">To protect ASF files using DRM version 1, perform the following steps:</span></span>

1.  <span data-ttu-id="97369-120">將 WMStubDRM .lib 檔案連結至您的專案，如有必要，請將 wmvcore 取消連結。</span><span class="sxs-lookup"><span data-stu-id="97369-120">Link the WMStubDRM.lib file to your project and, if necessary, unlink wmvcore.lib.</span></span>
2.  <span data-ttu-id="97369-121">呼叫 [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) 函數來建立寫入器。</span><span class="sxs-lookup"><span data-stu-id="97369-121">Call the [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) function to create the writer.</span></span> <span data-ttu-id="97369-122">第一個引數是保留的，而且必須設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="97369-122">The first argument is reserved and must be set to **NULL**.</span></span>
3.  <span data-ttu-id="97369-123">藉由呼叫 [**IWMWriter：： SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) 或 [**IWMWriter：： SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)，設定要使用之寫入器的設定檔。</span><span class="sxs-lookup"><span data-stu-id="97369-123">Set a profile for the writer to use by calling [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) or [**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid).</span></span> <span data-ttu-id="97369-124">設定任何 DRM 屬性之前，您必須先在寫入器中設定設定檔。</span><span class="sxs-lookup"><span data-stu-id="97369-124">You must set a profile in the writer before setting any DRM attributes.</span></span> <span data-ttu-id="97369-125">只有使用 Windows Media 音訊或 Windows Media 視訊編解碼器的設定檔才支援 DRM。</span><span class="sxs-lookup"><span data-stu-id="97369-125">DRM is supported only for profiles that use the Windows Media Audio or Windows Media Video codecs.</span></span>
4.  <span data-ttu-id="97369-126">使用 [**IWMHeaderInfo：： SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) 方法，設定下列 DRM 屬性。</span><span class="sxs-lookup"><span data-stu-id="97369-126">Using the [**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) method, set the following DRM properties.</span></span> <span data-ttu-id="97369-127">[ **使用 \_ drm** ] 屬性會指示 DRM 元件使用 drm 第1版來保護內容。</span><span class="sxs-lookup"><span data-stu-id="97369-127">The **Use\_DRM** property instructs the DRM components to protect the content using DRM version 1.</span></span> <span data-ttu-id="97369-128">[ **DRM \_ 旗標** ] 屬性會指定要為內容建立的本機授權包含的許可權。</span><span class="sxs-lookup"><span data-stu-id="97369-128">The **DRM\_Flags** property specifies the rights to be included in the local license that will be created for the content.</span></span> <span data-ttu-id="97369-129">**DRM \_ 層級** 值也會儲存在授權中，它會指定存取內容所需的最低層級。</span><span class="sxs-lookup"><span data-stu-id="97369-129">The **DRM\_LEVEL** value is also stored in the license; it specifies the minimum level required to access the content.</span></span> <span data-ttu-id="97369-130">150是 DRM 第1版內容的建議等級。</span><span class="sxs-lookup"><span data-stu-id="97369-130">150 is the recommended level for DRM version 1 content.</span></span>

    | <span data-ttu-id="97369-131">屬性</span><span class="sxs-lookup"><span data-stu-id="97369-131">Attribute</span></span>      | <span data-ttu-id="97369-132">值</span><span class="sxs-lookup"><span data-stu-id="97369-132">Value</span></span>                                                                                       |
    |----------------|---------------------------------------------------------------------------------------------|
    | <span data-ttu-id="97369-133">**使用 \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="97369-133">**Use\_DRM**</span></span>   | <span data-ttu-id="97369-134">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="97369-134">**TRUE**</span></span>                                                                                    |
    | <span data-ttu-id="97369-135">**DRM \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="97369-135">**DRM\_Flags**</span></span> | <span data-ttu-id="97369-136">WMT \_ RIGHT \_ 播放 \| WMT 以 \_ 右鍵 \_ 複製 \_ 至 \_ 非 \_ SDMI \_ 裝置 \| WMT \_ 從右 \_ 複製 \_ 到 \_ CD</span><span class="sxs-lookup"><span data-stu-id="97369-136">WMT\_RIGHT\_PLAYBACK \| WMT\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE \| WMT\_RIGHT\_COPY\_TO\_CD</span></span> |
    | <span data-ttu-id="97369-137">**DRM \_ 層級**</span><span class="sxs-lookup"><span data-stu-id="97369-137">**DRM\_LEVEL**</span></span> | <span data-ttu-id="97369-138">150</span><span class="sxs-lookup"><span data-stu-id="97369-138">150</span></span>                                                                                         |

    

     

<span data-ttu-id="97369-139">下列範例程式碼示範如何針對 DRM 第1版建立啟用 DRM 的寫入器，並設定 DRM 屬性。</span><span class="sxs-lookup"><span data-stu-id="97369-139">The following example code shows how to create a DRM-enabled writer for DRM version 1 and set the DRM properties.</span></span> <span data-ttu-id="97369-140">為了清楚起見，已省略錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="97369-140">Error checking has been omitted for the sake of clarify.</span></span>


```C++
BOOL  fUseDRM    = TRUE;
// These are the rights we will apply to the file. See WMT_RIGHTS for
// the full set of possible rights.

DWORD dwDRMFlags = WMT_RIGHT_PLAYBACK | 
                   WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE | 
                   WMT_RIGHT_COPY_TO_CD;

// Set the minimum required DRM level low enough
// to allow older players to access the content.
DWORD dwDRMLevel = 150;

IWMDRMWriter*  pWMDRMWriter  = NULL;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a writer object.
hr = WMCreateWriter( NULL, &pWMDRMWriter);

// Obtain the IWMHeaderInfo interface.
hr = pWMDRMWriter -> QueryInterface(IID_IWMHeaderInfo, 
                                   (void**) &pWMHeaderInfo);

// Tell the SDK runtime to protect the file using DRM version 1.
hr= pWMHeaderInfo-> SetAttribute(0,
                                 g_wszWMUse_DRM,
                                 WMT_TYPE_BOOL,
                                 (BYTE*)&fUseDRM,
                                 sizeof(BOOL));

// Specify the rights that will be stored in the local license that is
// created automatically for the content.
hr= pWMHeaderInfo->SetAttribute( 0,
                                 g_wszWMDRM_Flags, 
                                 WMT_TYPE_DWORD,
                                 (BYTE *)&dwDRMFlags,
                                 sizeof(DWORD) );

// Set the DRM_Level attribute in the file's DRM header.
hr= pWMHeaderInfo->SetAttribute( 0,
                                 g_wszWMDRM_Level, 
                                 WMT_TYPE_DWORD,
                                 (BYTE *)&dwDRMLevel,
                                 sizeof(DWORD) );
```



 

 




