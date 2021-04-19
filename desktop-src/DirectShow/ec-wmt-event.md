---
description: 由 WM ASF 讀取器篩選器在讀取受數位版權管理保護的 ASF 檔案 (DRM) 時傳送。
ms.assetid: ac6ea7a1-238e-42ae-9f10-e1db60381357
title: 'EC_WMT_EVENT (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8ce974cd83a404242fb51486f0889ac9b79e044
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982940"
---
# <a name="ec_wmt_event-dshowh"></a><span data-ttu-id="894cd-103">EC_WMT_EVENT (Dshow) </span><span class="sxs-lookup"><span data-stu-id="894cd-103">EC_WMT_EVENT (Dshow.h)</span></span>

<span data-ttu-id="894cd-104">由 [WM ASF 讀取](wm-asf-reader-filter.md) 器篩選器在讀取受數位版權管理保護的 ASF 檔案 (DRM) 時傳送。</span><span class="sxs-lookup"><span data-stu-id="894cd-104">Sent by the [WM ASF Reader](wm-asf-reader-filter.md) filter when it reads ASF files protected by digital rights management (DRM).</span></span>

## <a name="parameters"></a><span data-ttu-id="894cd-105">參數</span><span class="sxs-lookup"><span data-stu-id="894cd-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="894cd-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="894cd-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="894cd-107">下列其中一個 **WMT \_ 狀態值** ：</span><span class="sxs-lookup"><span data-stu-id="894cd-107">One of the following **WMT\_STATUS** values:</span></span>



| <span data-ttu-id="894cd-108">值</span><span class="sxs-lookup"><span data-stu-id="894cd-108">Value</span></span>                         | <span data-ttu-id="894cd-109">描述</span><span class="sxs-lookup"><span data-stu-id="894cd-109">Description</span></span>                                                                                                       |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="894cd-110">WMT \_ 取得 \_ 授權</span><span class="sxs-lookup"><span data-stu-id="894cd-110">WMT\_ACQUIRE\_LICENSE</span></span>         | <span data-ttu-id="894cd-111">當 DRM 元件已完成授權取得程式時（無論成功或失敗）傳送。</span><span class="sxs-lookup"><span data-stu-id="894cd-111">Sent when the DRM component has completed the license acquisition process, either successfully or unsuccessfully.</span></span> |
| <span data-ttu-id="894cd-112">WMT \_ 賦予</span><span class="sxs-lookup"><span data-stu-id="894cd-112">WMT\_INDIVIDUALIZE</span></span>            | <span data-ttu-id="894cd-113">安全性升級程式已完成，可能是成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="894cd-113">The security upgrade process has completed, either successfully or unsuccessfully.</span></span>                                |
| <span data-ttu-id="894cd-114">WMT \_ 需要具有 \_ 個人化</span><span class="sxs-lookup"><span data-stu-id="894cd-114">WMT\_NEEDS\_INDIVIDUALIZATION</span></span> | <span data-ttu-id="894cd-115">檔案要求應用程式在執行要求的動作之前，先收到安全性升級。</span><span class="sxs-lookup"><span data-stu-id="894cd-115">The file requires that an application receive a security upgrade before performing the requested action.</span></span>          |
| <span data-ttu-id="894cd-116">WMT \_ 無 \_ 許可權</span><span class="sxs-lookup"><span data-stu-id="894cd-116">WMT\_NO\_RIGHTS</span></span>               | <span data-ttu-id="894cd-117">應用程式沒有許可權可對受 DRM 第1版保護的檔案執行要求的動作。</span><span class="sxs-lookup"><span data-stu-id="894cd-117">The application has no rights to perform he requested action on a file protected by DRM version 1.</span></span>                |
| <span data-ttu-id="894cd-118">WMT \_ 沒有任何 \_ 許可權， \_ 例如</span><span class="sxs-lookup"><span data-stu-id="894cd-118">WMT\_NO\_RIGHTS\_EX</span></span>           | <span data-ttu-id="894cd-119">應用程式沒有許可權可對受 DRM 版本7保護的檔案執行要求的動作。</span><span class="sxs-lookup"><span data-stu-id="894cd-119">The application has no rights to perform he requested action on a file protected by DRM version 7.</span></span>                |



 

</dd> <dt>

<span data-ttu-id="894cd-120"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="894cd-120"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="894cd-121">[**AM \_ WMT \_ 事件 \_ 資料**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data)結構的指標，其中包含事件的相關資訊或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="894cd-121">Pointer to an [**AM\_WMT\_EVENT\_DATA**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) structure that contains information about the event, or **NULL**.</span></span> <span data-ttu-id="894cd-122">此結構的 **.pdata** 成員會指向其他資料，而此資料的類型取決於 **lParam1** 的值，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="894cd-122">The **pData** member of this structure points to additional data, whose type depends on the value of **lParam1**, as shown in the following table.</span></span>



| <span data-ttu-id="894cd-123">lParam1</span><span class="sxs-lookup"><span data-stu-id="894cd-123">lParam1</span></span>                       | <span data-ttu-id="894cd-124">AM \_ WMT \_ 事件 \_ 資料。 .pdata</span><span class="sxs-lookup"><span data-stu-id="894cd-124">AM\_WMT\_EVENT\_DATA.pData</span></span>                                                                                                                       |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="894cd-125">WMT \_ 取得 \_ 授權</span><span class="sxs-lookup"><span data-stu-id="894cd-125">WMT\_ACQUIRE\_LICENSE</span></span>         | <span data-ttu-id="894cd-126">[**WM \_ 取得 \_ 授權 \_ 資料**](/windows/desktop/wmformat/wm-get-license-data)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="894cd-126">Pointer to a [**WM\_GET\_LICENSE\_DATA**](/windows/desktop/wmformat/wm-get-license-data) structure.</span></span> <span data-ttu-id="894cd-127">此結構記載于 Windows Media Format SDK 中。</span><span class="sxs-lookup"><span data-stu-id="894cd-127">This structure is documented in the Windows Media Format SDK.</span></span> |
| <span data-ttu-id="894cd-128">WMT \_ 賦予</span><span class="sxs-lookup"><span data-stu-id="894cd-128">WMT\_INDIVIDUALIZE</span></span>            | <span data-ttu-id="894cd-129">[**WM \_ 賦予 \_ 狀態**](/windows/desktop/wmformat/wm-individualize-status)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="894cd-129">Pointer to a [**WM\_INDIVIDUALIZE\_STATUS**](/windows/desktop/wmformat/wm-individualize-status) structure.</span></span>                                                        |
| <span data-ttu-id="894cd-130">WMT \_ 需要具有 \_ 個人化</span><span class="sxs-lookup"><span data-stu-id="894cd-130">WMT\_NEEDS\_INDIVIDUALIZATION</span></span> | <span data-ttu-id="894cd-131">**Null**。</span><span class="sxs-lookup"><span data-stu-id="894cd-131">**NULL**.</span></span>                                                                                                                                        |
| <span data-ttu-id="894cd-132">WMT \_ 無 \_ 許可權</span><span class="sxs-lookup"><span data-stu-id="894cd-132">WMT\_NO\_RIGHTS</span></span>               | <span data-ttu-id="894cd-133">包含挑戰 URL 的寬字元字串指標。</span><span class="sxs-lookup"><span data-stu-id="894cd-133">Pointer to a wide-character string containing a challenge URL.</span></span>                                                                                   |
| <span data-ttu-id="894cd-134">WMT \_ 沒有任何 \_ 許可權， \_ 例如</span><span class="sxs-lookup"><span data-stu-id="894cd-134">WMT\_NO\_RIGHTS\_EX</span></span>           | <span data-ttu-id="894cd-135">[**WM \_ 取得 \_ 授權 \_ 資料**](/windows/desktop/wmformat/wm-get-license-data)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="894cd-135">Pointer to a [**WM\_GET\_LICENSE\_DATA**](/windows/desktop/wmformat/wm-get-license-data) structure.</span></span>                                                               |



 

<span data-ttu-id="894cd-136">*LParam2* 的值可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="894cd-136">The value of *lParam2* might be **NULL**.</span></span> <span data-ttu-id="894cd-137">請先檢查值，然後再取值指標。</span><span class="sxs-lookup"><span data-stu-id="894cd-137">Check the value before dereferencing the pointer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="894cd-138">備註</span><span class="sxs-lookup"><span data-stu-id="894cd-138">Remarks</span></span>

<span data-ttu-id="894cd-139">如需啟用受 DRM 保護之檔案的播放詳細資訊，請參閱 Windows Media Format SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="894cd-139">See the Windows Media Format SDK documentation for more information on enabling playback of DRM-protected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="894cd-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="894cd-140">Requirements</span></span>



| <span data-ttu-id="894cd-141">需求</span><span class="sxs-lookup"><span data-stu-id="894cd-141">Requirement</span></span> | <span data-ttu-id="894cd-142">值</span><span class="sxs-lookup"><span data-stu-id="894cd-142">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="894cd-143">標頭</span><span class="sxs-lookup"><span data-stu-id="894cd-143">Header</span></span><br/> | <dl> <span data-ttu-id="894cd-144"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="894cd-144"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="894cd-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="894cd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="894cd-146">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="894cd-146">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="894cd-147">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="894cd-147">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

