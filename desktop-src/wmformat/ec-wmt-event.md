---
title: 'EC_WMT_EVENT (Windows Media Format 11 SDK) '
description: EC \_ WMT \_ 活動
ms.assetid: 51d51659-8e7d-49b7-83f2-a80e99d39d78
keywords:
- Windows Media Format SDK，EC_WMT_EVENT
- DirectShow，EC_WMT_EVENT
- EC_WMT_EVENT
- 數位版權管理 (DRM) ，EC_WMT_EVENT
- DRM (數位版權管理) ，EC_WMT_EVENT
- Advanced Systems Format (ASF) ，EC_WMT_EVENT
- ASF (Advanced Systems Format) ，EC_WMT_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe74baaba676a97e609b4c03cd4db9010bd8f6a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464068"
---
# <a name="ec_wmt_event-windows-media-format-11-sdk"></a><span data-ttu-id="fe0dd-110">EC_WMT_EVENT (Windows Media Format 11 SDK) </span><span class="sxs-lookup"><span data-stu-id="fe0dd-110">EC_WMT_EVENT (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="fe0dd-111">當應用程式使用 ASF 讀取器篩選器來播放受數位版權管理保護的 ASF 檔案時，由 Windows Media 格式 SDK 傳送 (DRM) 。</span><span class="sxs-lookup"><span data-stu-id="fe0dd-111">Sent by the Windows Media Format SDK when an application uses the ASF Reader filter to play ASF files protected by digital rights management (DRM).</span></span>

<span data-ttu-id="fe0dd-112">參數</span><span class="sxs-lookup"><span data-stu-id="fe0dd-112">Parameters</span></span>

<span data-ttu-id="fe0dd-113">*lParam1*</span><span class="sxs-lookup"><span data-stu-id="fe0dd-113">*lParam1*</span></span>

<span data-ttu-id="fe0dd-114">可以是下列其中一個 WMT \_ 狀態值。</span><span class="sxs-lookup"><span data-stu-id="fe0dd-114">Can be one of the following WMT\_STATUS values.</span></span>



| <span data-ttu-id="fe0dd-115">WMT \_ 狀態訊息</span><span class="sxs-lookup"><span data-stu-id="fe0dd-115">WMT\_STATUS Message</span></span>           | <span data-ttu-id="fe0dd-116">Description</span><span class="sxs-lookup"><span data-stu-id="fe0dd-116">Description</span></span>                                                                                                                    |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe0dd-117">WMT \_ 無 \_ 許可權</span><span class="sxs-lookup"><span data-stu-id="fe0dd-117">WMT\_NO\_RIGHTS</span></span>               | <span data-ttu-id="fe0dd-118">檔案受到 DRM 第1版的保護，應用程式沒有許可權可執行要求的動作。</span><span class="sxs-lookup"><span data-stu-id="fe0dd-118">The file is protected with DRM version 1 and the application has no rights to perform the requested action.</span></span>                    |
| <span data-ttu-id="fe0dd-119">WMT \_ 取得 \_ 授權</span><span class="sxs-lookup"><span data-stu-id="fe0dd-119">WMT\_ACQUIRE\_LICENSE</span></span>         | <span data-ttu-id="fe0dd-120">授權取得流程已完成。</span><span class="sxs-lookup"><span data-stu-id="fe0dd-120">The license acquisition process has been completed.</span></span> <span data-ttu-id="fe0dd-121"> (這不一定表示已成功取得授權。 ) </span><span class="sxs-lookup"><span data-stu-id="fe0dd-121">(This does not necessarily mean that a license was successfully acquired.)</span></span> |
| <span data-ttu-id="fe0dd-122">WMT \_ 沒有任何 \_ 許可權， \_ 例如</span><span class="sxs-lookup"><span data-stu-id="fe0dd-122">WMT\_NO\_RIGHTS\_EX</span></span>           | <span data-ttu-id="fe0dd-123">檔案受到 DRM 版本7的保護，應用程式沒有許可權可執行要求的動作。</span><span class="sxs-lookup"><span data-stu-id="fe0dd-123">The file is protected with DRM version 7 and the application has no rights to perform the requested action.</span></span>                    |
| <span data-ttu-id="fe0dd-124">WMT \_ 需要具有 \_ 個人化</span><span class="sxs-lookup"><span data-stu-id="fe0dd-124">WMT\_NEEDS\_INDIVIDUALIZATION</span></span> | <span data-ttu-id="fe0dd-125">授權只允許個別的應用程式執行要求的動作。</span><span class="sxs-lookup"><span data-stu-id="fe0dd-125">The license allows only individualized applications to perform the requested action.</span></span>                                           |
| <span data-ttu-id="fe0dd-126">WMT \_ 賦予</span><span class="sxs-lookup"><span data-stu-id="fe0dd-126">WMT\_INDIVIDUALIZE</span></span>            | <span data-ttu-id="fe0dd-127">現在正在執行或已完成的個人化程式。</span><span class="sxs-lookup"><span data-stu-id="fe0dd-127">The individualization process is now being performed or has been completed.</span></span>                                                    |



 

<span data-ttu-id="fe0dd-128">*lParam2*</span><span class="sxs-lookup"><span data-stu-id="fe0dd-128">*lParam2*</span></span>

<span data-ttu-id="fe0dd-129">**AM \_ WMT \_ 事件 \_ 資料** 結構的指標，其中包含 **.pdata** 成員指標中事件的相關資訊，以及 Windows Media 格式 SDK 所傳送的 **HRESULT** 狀態碼。</span><span class="sxs-lookup"><span data-stu-id="fe0dd-129">Pointer to an **AM\_WMT\_EVENT\_DATA** structure that contains information about the event in the **pData** member pointer, as well as an **HRESULT** status code sent by the Windows Media Format SDK.</span></span> <span data-ttu-id="fe0dd-130">*LParam2* 的值取決於 *lParam1* 的值，如下表所述。</span><span class="sxs-lookup"><span data-stu-id="fe0dd-130">The value of *lParam2* depends on the value of *lParam1*, as described in the following table.</span></span> <span data-ttu-id="fe0dd-131"> (「WM」 \_ 結構是在 Windows Media FORMAT SDK 中定義。 ) </span><span class="sxs-lookup"><span data-stu-id="fe0dd-131">(The "WM\_" structures are defined in the Windows Media Format SDK.)</span></span>



| <span data-ttu-id="fe0dd-132">如果 lParam1 為 .。。</span><span class="sxs-lookup"><span data-stu-id="fe0dd-132">If lParam1 is...</span></span>              | <span data-ttu-id="fe0dd-133">\_WMT \_ 事件 \_ 資料。 .pdata 是 .。。</span><span class="sxs-lookup"><span data-stu-id="fe0dd-133">AM\_WMT\_EVENT\_DATA.pData is...</span></span>                            |
|-------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="fe0dd-134">WMT \_ 無 \_ 許可權</span><span class="sxs-lookup"><span data-stu-id="fe0dd-134">WMT\_NO\_RIGHTS</span></span>               | <span data-ttu-id="fe0dd-135">包含挑戰 URL 的 **WCHAR** 字串指標。</span><span class="sxs-lookup"><span data-stu-id="fe0dd-135">A pointer to a **WCHAR** string containing a challenge URL.</span></span> |
| <span data-ttu-id="fe0dd-136">WMT \_ 取得 \_ 授權</span><span class="sxs-lookup"><span data-stu-id="fe0dd-136">WMT\_ACQUIRE\_LICENSE</span></span>         | <span data-ttu-id="fe0dd-137">**WM \_ 取得 \_ 授權 \_ 資料** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="fe0dd-137">A pointer to a **WM\_GET\_LICENSE\_DATA** structure.</span></span>        |
| <span data-ttu-id="fe0dd-138">WMT \_ 沒有任何 \_ 許可權， \_ 例如</span><span class="sxs-lookup"><span data-stu-id="fe0dd-138">WMT\_NO\_RIGHTS\_EX</span></span>           | <span data-ttu-id="fe0dd-139">**WM \_ 取得 \_ 授權 \_ 資料** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="fe0dd-139">A pointer to a **WM\_GET\_LICENSE\_DATA** structure.</span></span>        |
| <span data-ttu-id="fe0dd-140">WMT \_ 需要具有 \_ 個人化</span><span class="sxs-lookup"><span data-stu-id="fe0dd-140">WMT\_NEEDS\_INDIVIDUALIZATION</span></span> | <span data-ttu-id="fe0dd-141">NULL。</span><span class="sxs-lookup"><span data-stu-id="fe0dd-141">NULL.</span></span>                                                       |
| <span data-ttu-id="fe0dd-142">WMT \_ 賦予</span><span class="sxs-lookup"><span data-stu-id="fe0dd-142">WMT\_INDIVIDUALIZE</span></span>            | <span data-ttu-id="fe0dd-143">**WM \_ 賦予 \_ 狀態** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="fe0dd-143">A pointer to a **WM\_INDIVIDUALIZE\_STATUS** structure.</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="fe0dd-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="fe0dd-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe0dd-145">**數位 Rights Management 功能**</span><span class="sxs-lookup"><span data-stu-id="fe0dd-145">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="fe0dd-146">**DirectShow QASF 參考**</span><span class="sxs-lookup"><span data-stu-id="fe0dd-146">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="fe0dd-147">**啟用 DRM 支援**</span><span class="sxs-lookup"><span data-stu-id="fe0dd-147">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




