---
title: 處理個人化事件
description: 處理個人化事件
ms.assetid: f533978f-f366-4900-b784-f51e88393984
keywords:
- Windows Media Format SDK，處理個人化事件
- Windows Media Format SDK，個人化事件
- Advanced Systems Format (ASF) ，處理個人化事件
- ASF (Advanced Systems Format) ，處理個人化事件
- Advanced Systems Format (ASF) 、個人化事件
- ASF (Advanced Systems Format) 、個人化事件
- 數位版權管理 (DRM) ，處理個人化事件
- DRM (數位版權管理) ，處理個人化事件
- 數位版權管理 (DRM) 、個人化事件
- DRM (數位版權管理) 、個人化事件
- 個人化事件
- 事件、個人化事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e74df94bf871ec62ec2acb94658785969812640
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106969506"
---
# <a name="handling-individualization-events"></a><span data-ttu-id="9a629-115">處理個人化事件</span><span class="sxs-lookup"><span data-stu-id="9a629-115">Handling Individualization Events</span></span>

<span data-ttu-id="9a629-116">當啟用 DRM 的應用程式嘗試開啟受保護的檔案時，DRM 元件會檢查檔案中的 [**drm \_ DRMHeader \_ IndividualizedVersion**](drm-drmheader-individualizedversion.md) 屬性，此屬性會指定存取內容所需的最低版本層級。</span><span class="sxs-lookup"><span data-stu-id="9a629-116">When a DRM-enabled application attempts to open a protected file, the DRM component examines the [**DRM\_DRMHeader\_IndividualizedVersion**](drm-drmheader-individualizedversion.md) attribute in the file, which specifies the minimum version level required to access the content.</span></span> <span data-ttu-id="9a629-117">DRM 元件的所有層級都適用于所有7.0 和更新版本的 Windows Media Player 和 Windows Media 格式 SDK。</span><span class="sxs-lookup"><span data-stu-id="9a629-117">All levels of the DRM component work with all 7.0 and later versions of Windows Media Player and the Windows Media Format SDK.</span></span> <span data-ttu-id="9a629-118">如果 DRM 元件的個別版本層級低於所需的版本，DRM 元件會將 **WMT \_ 需要 \_** 的「個人化」事件傳送至應用程式的 [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) 方法。</span><span class="sxs-lookup"><span data-stu-id="9a629-118">If the DRM component's individualized version level is lower than the required version, the DRM component will send a **WMT\_NEEDS\_INDIVIDUALIZATION** event to the application's [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method.</span></span> <span data-ttu-id="9a629-119">然後，應用程式必須顯示訊息或對話方塊，提示使用者啟動或取消安全性升級。</span><span class="sxs-lookup"><span data-stu-id="9a629-119">The application must then display a message or dialog box prompting users to either start or cancel the security upgrade.</span></span> <span data-ttu-id="9a629-120">這是必要的提示，因為基於隱私權考慮，使用者必須在其電腦上安裝安全性升級之前授與其許可權。</span><span class="sxs-lookup"><span data-stu-id="9a629-120">This prompt is necessary because, for privacy reasons, users must give their permission before a security upgrade is installed on their computer.</span></span>

> [!Note]  
> <span data-ttu-id="9a629-121">內容的標頭只會指定 DRM DRMVersion IndividualizedVersion 的前兩個數字 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="9a629-121">The header of the content specifies only the first two digits for DRM\_DRMVersion\_IndividualizedVersion.</span></span> <span data-ttu-id="9a629-122">換句話說，若要要求層級 2.2.0.1 DRM 元件，標頭會包含 "2.2"。</span><span class="sxs-lookup"><span data-stu-id="9a629-122">In other words, to require a level 2.2.0.1 DRM component, the header would contain "2.2".</span></span>

 

<span data-ttu-id="9a629-123">若要啟動安全性升級及/或觸發程式的個人化設定，請呼叫 [**IWMDRMReader：：賦予**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize) 方法，並將 *dwFlags* 參數設定為1。</span><span class="sxs-lookup"><span data-stu-id="9a629-123">To start the security upgrade and/or trigger individualization, call the [**IWMDRMReader::Individualize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize) method with the *dwFlags* parameter set to 1.</span></span>

<span data-ttu-id="9a629-124">您必須在應用程式中處理 **WMT \_ 賦予** 事件。</span><span class="sxs-lookup"><span data-stu-id="9a629-124">You must handle the **WMT\_INDIVIDUALIZE** event in your application.</span></span> <span data-ttu-id="9a629-125">DRM 元件會引發此事件多次，其具有在 *pValue* 參數中指定的個人化程式狀態，這會轉換為 [**WM \_ 賦予 \_ 狀態**](wm-individualize-status.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="9a629-125">This event will be fired multiple times by the DRM component with the status of the individualization process indicated in the *pValue* parameter, which is cast to a pointer to a [**WM\_INDIVIDUALIZE\_STATUS**](wm-individualize-status.md) structure.</span></span>

<span data-ttu-id="9a629-126">在 DRM 元件成功個人化之後，應用程式將會收到 **WMT \_ 無 \_ 許可權的 \_ EX** 事件，指出應用程式現在可以繼續取得內容的授權。</span><span class="sxs-lookup"><span data-stu-id="9a629-126">After the DRM component is successfully individualized, the application will receive a **WMT\_NO\_RIGHTS\_EX** event, indicating that the application can now proceed to acquire a license for the content.</span></span>

> [!Note]  
> <span data-ttu-id="9a629-127">此 SDK 的 x64 版本不支援 DRM。</span><span class="sxs-lookup"><span data-stu-id="9a629-127">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9a629-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="9a629-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a629-129">**處理授權取得事件**</span><span class="sxs-lookup"><span data-stu-id="9a629-129">**Handling License Acquisition Events**</span></span>](handling-license-acquisition-events.md)
</dt> <dt>

[<span data-ttu-id="9a629-130">**Individualizing DRM 應用程式**</span><span class="sxs-lookup"><span data-stu-id="9a629-130">**Individualizing DRM Applications**</span></span>](individualizing-drm-applications.md)
</dt> <dt>

[<span data-ttu-id="9a629-131">**IWMDRMReader 介面**</span><span class="sxs-lookup"><span data-stu-id="9a629-131">**IWMDRMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> </dl>

 

 




