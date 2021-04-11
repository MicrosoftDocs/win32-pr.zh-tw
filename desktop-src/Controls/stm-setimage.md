---
title: 'STM_SETIMAGE 訊息 (Winuser .h) '
description: 應用程式會傳送 STM \_ SETIMAGE 訊息，以將新的映射與靜態控制項產生關聯。
ms.assetid: d3e7c5d4-f621-40f6-9558-7fb699e8b489
keywords:
- STM_SETIMAGE message Windows 控制項
topic_type:
- apiref
api_name:
- STM_SETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27c4f9c216d2e987727a1e2fa9bc6de12a823d52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934045"
---
# <a name="stm_setimage-message"></a><span data-ttu-id="2e036-104">STM \_ SETIMAGE 訊息</span><span class="sxs-lookup"><span data-stu-id="2e036-104">STM\_SETIMAGE message</span></span>

<span data-ttu-id="2e036-105">應用程式會傳送 **STM \_ SETIMAGE** 訊息，以將新的映射與靜態控制項產生關聯。</span><span class="sxs-lookup"><span data-stu-id="2e036-105">An application sends an **STM\_SETIMAGE** message to associate a new image with a static control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2e036-106">參數</span><span class="sxs-lookup"><span data-stu-id="2e036-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e036-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2e036-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e036-108">指定要與靜態控制項相關聯的影像類型。</span><span class="sxs-lookup"><span data-stu-id="2e036-108">Specifies the type of image to associate with the static control.</span></span> <span data-ttu-id="2e036-109">這個參數可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="2e036-109">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="2e036-110">值</span><span class="sxs-lookup"><span data-stu-id="2e036-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="2e036-111">意義</span><span class="sxs-lookup"><span data-stu-id="2e036-111">Meaning</span></span>                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <span data-ttu-id="2e036-112"><dt>**影像 \_ 點陣圖**</dt></span><span class="sxs-lookup"><span data-stu-id="2e036-112"><dt>**IMAGE\_BITMAP**</dt></span></span> </dl>                | <span data-ttu-id="2e036-113">點陣圖。</span><span class="sxs-lookup"><span data-stu-id="2e036-113">Bitmap.</span></span><br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <span data-ttu-id="2e036-114"><dt>**影像 \_ 游標**</dt></span><span class="sxs-lookup"><span data-stu-id="2e036-114"><dt>**IMAGE\_CURSOR**</dt></span></span> </dl>                | <span data-ttu-id="2e036-115">游標。</span><span class="sxs-lookup"><span data-stu-id="2e036-115">Cursor.</span></span><br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <span data-ttu-id="2e036-116"><dt>**影像 \_ ENHMETAFILE**</dt></span><span class="sxs-lookup"><span data-stu-id="2e036-116"><dt>**IMAGE\_ENHMETAFILE**</dt></span></span> </dl> | <span data-ttu-id="2e036-117">增強的中繼檔。</span><span class="sxs-lookup"><span data-stu-id="2e036-117">Enhanced metafile.</span></span><br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <span data-ttu-id="2e036-118"><dt>**影像 \_ 圖示**</dt></span><span class="sxs-lookup"><span data-stu-id="2e036-118"><dt>**IMAGE\_ICON**</dt></span></span> </dl>                      | <span data-ttu-id="2e036-119">圖示。</span><span class="sxs-lookup"><span data-stu-id="2e036-119">Icon.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="2e036-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e036-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e036-121">要與靜態控制項相關聯之影像的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2e036-121">Handle to the image to associate with the static control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e036-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="2e036-122">Return value</span></span>

<span data-ttu-id="2e036-123">傳回值是先前與靜態控制項相關聯之影像的控制碼（如果有的話）。否則，它會是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2e036-123">The return value is a handle to the image previously associated with the static control, if any; otherwise, it is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e036-124">備註</span><span class="sxs-lookup"><span data-stu-id="2e036-124">Remarks</span></span>

<span data-ttu-id="2e036-125">若要將影像與靜態控制項產生關聯，控制項必須具有適當的樣式。</span><span class="sxs-lookup"><span data-stu-id="2e036-125">To associate an image with a static control, the control must have the proper style.</span></span> <span data-ttu-id="2e036-126">下表顯示每個影像類型所需的樣式。</span><span class="sxs-lookup"><span data-stu-id="2e036-126">The following table shows the style needed for each image type.</span></span>



| <span data-ttu-id="2e036-127">映像類型</span><span class="sxs-lookup"><span data-stu-id="2e036-127">Image type</span></span>         | <span data-ttu-id="2e036-128">靜態控制項樣式</span><span class="sxs-lookup"><span data-stu-id="2e036-128">Static control style</span></span> |
|--------------------|----------------------|
| <span data-ttu-id="2e036-129">影像 \_ 點陣圖</span><span class="sxs-lookup"><span data-stu-id="2e036-129">IMAGE\_BITMAP</span></span>      | <span data-ttu-id="2e036-130">SS \_ 點陣圖</span><span class="sxs-lookup"><span data-stu-id="2e036-130">SS\_BITMAP</span></span>           |
| <span data-ttu-id="2e036-131">影像 \_ 游標</span><span class="sxs-lookup"><span data-stu-id="2e036-131">IMAGE\_CURSOR</span></span>      | <span data-ttu-id="2e036-132">SS \_ 圖示</span><span class="sxs-lookup"><span data-stu-id="2e036-132">SS\_ICON</span></span>             |
| <span data-ttu-id="2e036-133">影像 \_ ENHMETAFILE</span><span class="sxs-lookup"><span data-stu-id="2e036-133">IMAGE\_ENHMETAFILE</span></span> | <span data-ttu-id="2e036-134">SS \_ ENHMETAFILE</span><span class="sxs-lookup"><span data-stu-id="2e036-134">SS\_ENHMETAFILE</span></span>      |
| <span data-ttu-id="2e036-135">影像 \_ 圖示</span><span class="sxs-lookup"><span data-stu-id="2e036-135">IMAGE\_ICON</span></span>        | <span data-ttu-id="2e036-136">SS \_ 圖示</span><span class="sxs-lookup"><span data-stu-id="2e036-136">SS\_ICON</span></span>             |



 

> [!IMPORTANT]
>
> <span data-ttu-id="2e036-137">在 Microsoft Win32 控制項的第6版中，使用 **.Stm \_ SETIMAGE** 訊息傳遞至靜態控制項的點陣圖，是由後續的 **STM \_ SETIMAGE** 訊息所傳回的相同點陣圖。</span><span class="sxs-lookup"><span data-stu-id="2e036-137">In version 6 of the Microsoft Win32 controls, a bitmap passed to a static control using the **STM\_SETIMAGE** message was the same bitmap returned by a subsequent **STM\_SETIMAGE** message.</span></span> <span data-ttu-id="2e036-138">用戶端負責刪除傳送至靜態控制項的任何點陣圖。</span><span class="sxs-lookup"><span data-stu-id="2e036-138">The client is responsible to delete any bitmap sent to a static control.</span></span>
>
> <span data-ttu-id="2e036-139">在 Windows XP 中，如果在 **.Stm \_ SETIMAGE** 訊息中傳遞的點陣圖包含非零 Alpha 的圖元，則靜態控制項會取得點陣圖的複本。</span><span class="sxs-lookup"><span data-stu-id="2e036-139">With Windows XP, if the bitmap passed in the **STM\_SETIMAGE** message contains pixels with nonzero alpha, the static control takes a copy of the bitmap.</span></span> <span data-ttu-id="2e036-140">下一個 **STM \_ SETIMAGE** 訊息會傳回這個複製的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="2e036-140">This copied bitmap is returned by the next **STM\_SETIMAGE** message.</span></span> <span data-ttu-id="2e036-141">用戶端程式代碼可能會獨立追蹤傳遞給靜態控制項的點陣圖，但如果它沒有檢查並釋出從 **STM \_ SETIMAGE** 訊息傳回的點陣圖，則會遺漏點陣圖。</span><span class="sxs-lookup"><span data-stu-id="2e036-141">The client code may independently track the bitmaps passed to the static control, but if it does not check and release the bitmaps returned from **STM\_SETIMAGE** messages, the bitmaps are leaked.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2e036-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e036-142">Requirements</span></span>



| <span data-ttu-id="2e036-143">需求</span><span class="sxs-lookup"><span data-stu-id="2e036-143">Requirement</span></span> | <span data-ttu-id="2e036-144">值</span><span class="sxs-lookup"><span data-stu-id="2e036-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e036-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2e036-145">Minimum supported client</span></span><br/> | <span data-ttu-id="2e036-146">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e036-146">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2e036-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2e036-147">Minimum supported server</span></span><br/> | <span data-ttu-id="2e036-148">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e036-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2e036-149">標頭</span><span class="sxs-lookup"><span data-stu-id="2e036-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e036-150"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="2e036-150"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e036-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e036-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e036-152">**STM \_ GETIMAGE**</span><span class="sxs-lookup"><span data-stu-id="2e036-152">**STM\_GETIMAGE**</span></span>](stm-getimage.md)
</dt> </dl>

 

 





