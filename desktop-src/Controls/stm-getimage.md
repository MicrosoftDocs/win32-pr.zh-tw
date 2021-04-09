---
title: 'STM_GETIMAGE 訊息 (Winuser .h) '
description: 應用程式會傳送 STM \_ GETIMAGE 訊息，以抓取與靜態控制項相關聯之影像的控制碼 (圖示或點陣圖) 。
ms.assetid: eb5fe67a-09be-4c13-89c6-0e2f23e8c081
keywords:
- STM_GETIMAGE message Windows 控制項
topic_type:
- apiref
api_name:
- STM_GETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77fe0c3d00a2a957530160a5ce5a21b8a1cf84e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024649"
---
# <a name="stm_getimage-message"></a><span data-ttu-id="60e88-104">STM \_ GETIMAGE 訊息</span><span class="sxs-lookup"><span data-stu-id="60e88-104">STM\_GETIMAGE message</span></span>

<span data-ttu-id="60e88-105">應用程式會傳送 **STM \_ GETIMAGE** 訊息，以抓取與靜態控制項相關聯之影像的控制碼 (圖示或點陣圖) 。</span><span class="sxs-lookup"><span data-stu-id="60e88-105">An application sends an **STM\_GETIMAGE** message to retrieve a handle to the image (icon or bitmap) associated with a static control.</span></span>

## <a name="parameters"></a><span data-ttu-id="60e88-106">參數</span><span class="sxs-lookup"><span data-stu-id="60e88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60e88-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="60e88-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="60e88-108">指定要取出的影像類型。</span><span class="sxs-lookup"><span data-stu-id="60e88-108">Specifies the type of image to retrieve.</span></span> <span data-ttu-id="60e88-109">這個參數可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="60e88-109">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="60e88-110">值</span><span class="sxs-lookup"><span data-stu-id="60e88-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="60e88-111">意義</span><span class="sxs-lookup"><span data-stu-id="60e88-111">Meaning</span></span>                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <span data-ttu-id="60e88-112"><dt>**影像 \_ 點陣圖**</dt></span><span class="sxs-lookup"><span data-stu-id="60e88-112"><dt>**IMAGE\_BITMAP**</dt></span></span> </dl>                | <span data-ttu-id="60e88-113">點陣圖。</span><span class="sxs-lookup"><span data-stu-id="60e88-113">Bitmap.</span></span><br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <span data-ttu-id="60e88-114"><dt>**影像 \_ 游標**</dt></span><span class="sxs-lookup"><span data-stu-id="60e88-114"><dt>**IMAGE\_CURSOR**</dt></span></span> </dl>                | <span data-ttu-id="60e88-115">游標。</span><span class="sxs-lookup"><span data-stu-id="60e88-115">Cursor.</span></span><br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <span data-ttu-id="60e88-116"><dt>**影像 \_ ENHMETAFILE**</dt></span><span class="sxs-lookup"><span data-stu-id="60e88-116"><dt>**IMAGE\_ENHMETAFILE**</dt></span></span> </dl> | <span data-ttu-id="60e88-117">增強的中繼檔。</span><span class="sxs-lookup"><span data-stu-id="60e88-117">Enhanced metafile.</span></span><br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <span data-ttu-id="60e88-118"><dt>**影像 \_ 圖示**</dt></span><span class="sxs-lookup"><span data-stu-id="60e88-118"><dt>**IMAGE\_ICON**</dt></span></span> </dl>                      | <span data-ttu-id="60e88-119">圖示。</span><span class="sxs-lookup"><span data-stu-id="60e88-119">Icon.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="60e88-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="60e88-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="60e88-121">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="60e88-121">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60e88-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="60e88-122">Return value</span></span>

<span data-ttu-id="60e88-123">傳回值是影像的控制碼（如果有的話）。否則，它會是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="60e88-123">The return value is a handle to the image, if any; otherwise, it is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="60e88-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="60e88-124">Requirements</span></span>



| <span data-ttu-id="60e88-125">需求</span><span class="sxs-lookup"><span data-stu-id="60e88-125">Requirement</span></span> | <span data-ttu-id="60e88-126">值</span><span class="sxs-lookup"><span data-stu-id="60e88-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60e88-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="60e88-127">Minimum supported client</span></span><br/> | <span data-ttu-id="60e88-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60e88-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="60e88-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="60e88-129">Minimum supported server</span></span><br/> | <span data-ttu-id="60e88-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60e88-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="60e88-131">標頭</span><span class="sxs-lookup"><span data-stu-id="60e88-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="60e88-132"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="60e88-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60e88-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="60e88-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60e88-134">**STM \_ SETIMAGE**</span><span class="sxs-lookup"><span data-stu-id="60e88-134">**STM\_SETIMAGE**</span></span>](stm-setimage.md)
</dt> </dl>

 

 





