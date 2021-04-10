---
title: 讀取受保護的檔案
description: 讀取受保護的檔案
ms.assetid: 24f839f1-ce57-4d06-b1a5-a6bea7b5b7bb
keywords:
- Windows Media Format SDK，讀取受保護的檔案
- Windows Media Format SDK，受保護的檔案
- Advanced Systems Format (ASF) ，讀取受保護的檔案
- ASF (Advanced 系統格式) ，讀取受保護的檔案
- Advanced Systems Format (ASF) 、受保護的檔案
- ASF (Advanced 系統格式) 、受保護的檔案
- Advanced Systems Format (ASF) ，WMStubDRM .lib
- ASF (Advanced Systems Format) ，WMStubDRM .lib
- WMStubDRM .lib，讀取受保護的檔案
- WMStubDRM .lib，受保護的檔案
- 數位版權管理 (DRM) ，WMStubDRM .lib
- DRM (數位版權管理) ，WMStubDRM .lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b2110708a28daae1e86ba3dac2ea1f18ad16fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681386"
---
# <a name="reading-protected-files"></a><span data-ttu-id="c565f-115">讀取受保護的檔案</span><span class="sxs-lookup"><span data-stu-id="c565f-115">Reading Protected Files</span></span>

<span data-ttu-id="c565f-116">讀取受 DRM 保護的檔案或網路資料流程基本上牽涉到嘗試開啟檔案 (或連接到資料流程) 然後處理任何可能從 DRM 元件傳送的事件。</span><span class="sxs-lookup"><span data-stu-id="c565f-116">Reading a DRM-protected file or network stream basically involves attempting to open the file (or connect to the stream) and then handling any events that might be sent from the DRM components.</span></span>

<span data-ttu-id="c565f-117">如果播放程式不是啟用 DRM 的 (不會連結至有效的 wmstubdrm .lib 程式庫) [**IWMReader：： Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) 呼叫會在嘗試開啟受保護的檔案時失敗，並傳回 NS \_ E \_ 受保護的 \_ 內容或某些相關錯誤。</span><span class="sxs-lookup"><span data-stu-id="c565f-117">If a player is not DRM-enabled (does not link to a valid wmstubdrm.lib library) the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) call fails when it tries to open a protected file and returns NS\_E\_PROTECTED\_CONTENT or some related error.</span></span>

<span data-ttu-id="c565f-118">當啟用 DRM 的應用程式嘗試開啟受 DRM 保護的檔案時，DRM 元件會自動搜尋本機系統是否有有效的授權。</span><span class="sxs-lookup"><span data-stu-id="c565f-118">When a DRM-enabled application attempts to open a DRM-protected file, the DRM component automatically searches the local system for a valid license.</span></span> <span data-ttu-id="c565f-119">如果找到一個，DRM 元件會自動以對應用程式完全透明的方式來解密檔案。</span><span class="sxs-lookup"><span data-stu-id="c565f-119">If one is found, the DRM component automatically decrypts the file in a way that is completely transparent to the application.</span></span> <span data-ttu-id="c565f-120">應用程式可在解密檔案上執行的動作取決於授權中指定的許可權。</span><span class="sxs-lookup"><span data-stu-id="c565f-120">The action that an application may perform on the decrypted file depends on the rights specified in the license.</span></span> <span data-ttu-id="c565f-121">如需可能許可權的完整說明，請參閱 Windows Media Rights Manager SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="c565f-121">For a full description of possible rights, see the Windows Media Rights Manager SDK documentation.</span></span>

<span data-ttu-id="c565f-122">如果應用程式沒有有效的檔案授權，播放程式會收到來自 DRM 元件的狀態通知。</span><span class="sxs-lookup"><span data-stu-id="c565f-122">If the application does not have a valid license for a file, the player receives a status notification from the DRM component.</span></span> <span data-ttu-id="c565f-123">然後，播放程式應用程式可以起始 [*授權*](wmformat-glossary.md) 取得程式。</span><span class="sxs-lookup"><span data-stu-id="c565f-123">The player application can then initiate the [*license acquisition*](wmformat-glossary.md) process.</span></span> <span data-ttu-id="c565f-124">收到有效的授權之後，就可以存取該檔案。</span><span class="sxs-lookup"><span data-stu-id="c565f-124">After a valid license has been received, the file can be accessed.</span></span> <span data-ttu-id="c565f-125">下列各節描述應用程式在執行授權取得程式時必須執行的基本工作：</span><span class="sxs-lookup"><span data-stu-id="c565f-125">The following sections describe the basic tasks that an application must perform in implementing the license acquisition process:</span></span>

-   [<span data-ttu-id="c565f-126">指定要執行的動作</span><span class="sxs-lookup"><span data-stu-id="c565f-126">Specifying the Actions To Be Performed</span></span>](specifying-the-actions-to-be-performed.md)
-   [<span data-ttu-id="c565f-127">處理授權取得事件</span><span class="sxs-lookup"><span data-stu-id="c565f-127">Handling License Acquisition Events</span></span>](handling-license-acquisition-events.md)
-   [<span data-ttu-id="c565f-128">Individualizing DRM 應用程式</span><span class="sxs-lookup"><span data-stu-id="c565f-128">Individualizing DRM Applications</span></span>](individualizing-drm-applications.md)
-   [<span data-ttu-id="c565f-129">處理個人化事件</span><span class="sxs-lookup"><span data-stu-id="c565f-129">Handling Individualization Events</span></span>](handling-individualization-events.md)

> [!Note]  
> <span data-ttu-id="c565f-130">此 SDK 的 x64 版本不支援 DRM。</span><span class="sxs-lookup"><span data-stu-id="c565f-130">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c565f-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="c565f-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c565f-132">**數位 Rights Management 功能**</span><span class="sxs-lookup"><span data-stu-id="c565f-132">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="c565f-133">**DRM 屬性清單**</span><span class="sxs-lookup"><span data-stu-id="c565f-133">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="c565f-134">**DRM 屬性**</span><span class="sxs-lookup"><span data-stu-id="c565f-134">**DRM Properties**</span></span>](drm-properties.md)
</dt> <dt>

[<span data-ttu-id="c565f-135">**啟用 DRM 支援**</span><span class="sxs-lookup"><span data-stu-id="c565f-135">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




