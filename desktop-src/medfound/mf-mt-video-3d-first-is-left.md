---
description: 若為3D 影片格式，請指定左邊視圖的視圖。
ms.assetid: 4F33BF2D-EB32-46B6-B071-F9130D404201
title: 'MF_MT_VIDEO_3D_FIRST_IS_LEFT 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 027d91509d772a9200cdfc0ac64cce15514aa5a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104386289"
---
# <a name="mf_mt_video_3d_first_is_left-attribute"></a><span data-ttu-id="b470e-103">MF \_ MT \_ VIDEO \_ 3d \_ FIRST \_ 是 \_ LEFT 屬性</span><span class="sxs-lookup"><span data-stu-id="b470e-103">MF\_MT\_VIDEO\_3D\_FIRST\_IS\_LEFT attribute</span></span>

<span data-ttu-id="b470e-104">若為3D 影片格式，請指定左邊視圖的視圖。</span><span class="sxs-lookup"><span data-stu-id="b470e-104">For a 3D video format, specifies which view is the left view.</span></span>

## <a name="data-type"></a><span data-ttu-id="b470e-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="b470e-105">Data type</span></span>

<span data-ttu-id="b470e-106">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="b470e-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b470e-107">備註</span><span class="sxs-lookup"><span data-stu-id="b470e-107">Remarks</span></span>

<span data-ttu-id="b470e-108">針對3D 影片，每個影片範例都會包含兩個視圖，分別是指定的 *第一個視圖* 和 *第二* 個視圖。</span><span class="sxs-lookup"><span data-stu-id="b470e-108">For 3D video, each video sample contains two views, which are designated *first view* and *second view*.</span></span> <span data-ttu-id="b470e-109">在記憶體中，視圖的確切版面配置是由 [MF \_ MT \_ VIDEO \_ 3d \_ 格式](mf-mt-video-3d-format.md) 屬性所表示。</span><span class="sxs-lookup"><span data-stu-id="b470e-109">The exact layout of the views in memory is indicated by the [MF\_MT\_VIDEO\_3D\_FORMAT](mf-mt-video-3d-format.md) attribute.</span></span>



| <span data-ttu-id="b470e-110">格式</span><span class="sxs-lookup"><span data-stu-id="b470e-110">Format</span></span>               | <span data-ttu-id="b470e-111">第一個視圖</span><span class="sxs-lookup"><span data-stu-id="b470e-111">First View</span></span>              | <span data-ttu-id="b470e-112">第二個視圖</span><span class="sxs-lookup"><span data-stu-id="b470e-112">Second View</span></span>               |
|----------------------|-------------------------|---------------------------|
| <span data-ttu-id="b470e-113">以並存方式封裝</span><span class="sxs-lookup"><span data-stu-id="b470e-113">Packed side-by-side</span></span>  | <span data-ttu-id="b470e-114">緩衝區的左邊半部</span><span class="sxs-lookup"><span data-stu-id="b470e-114">Left half of the buffer</span></span> | <span data-ttu-id="b470e-115">緩衝區的上半部</span><span class="sxs-lookup"><span data-stu-id="b470e-115">Right half of the buffer</span></span>  |
| <span data-ttu-id="b470e-116">由上到下壓縮</span><span class="sxs-lookup"><span data-stu-id="b470e-116">Packed top-to-bottom</span></span> | <span data-ttu-id="b470e-117">緩衝區的上半部</span><span class="sxs-lookup"><span data-stu-id="b470e-117">Top half of the buffer</span></span>  | <span data-ttu-id="b470e-118">緩衝區的下半部</span><span class="sxs-lookup"><span data-stu-id="b470e-118">Bottom half of the buffer</span></span> |
| <span data-ttu-id="b470e-119">Multiview</span><span class="sxs-lookup"><span data-stu-id="b470e-119">Multiview</span></span>            | <span data-ttu-id="b470e-120">緩衝區索引0</span><span class="sxs-lookup"><span data-stu-id="b470e-120">Buffer index 0</span></span>          | <span data-ttu-id="b470e-121">緩衝區索引1</span><span class="sxs-lookup"><span data-stu-id="b470e-121">Buffer index 1</span></span>            |
| <span data-ttu-id="b470e-122">基底視圖</span><span class="sxs-lookup"><span data-stu-id="b470e-122">Base view</span></span>            | <span data-ttu-id="b470e-123">整個框架</span><span class="sxs-lookup"><span data-stu-id="b470e-123">Entire frame</span></span>            | <span data-ttu-id="b470e-124">不存在</span><span class="sxs-lookup"><span data-stu-id="b470e-124">Not present</span></span>               |



 

<span data-ttu-id="b470e-125">依預設，第一個視圖是左方視圖，而第二個視圖是右視圖。</span><span class="sxs-lookup"><span data-stu-id="b470e-125">By default, the first view is the left view, and the second view is the right view.</span></span> <span data-ttu-id="b470e-126">如果已交換左方和右邊的視圖，請將 \_ \_ \_ 媒體類型中的 MF MT 影片 \_ 第一個 \_ \_ 屬性設為 [FALSE]。</span><span class="sxs-lookup"><span data-stu-id="b470e-126">If the left and right views are swapped, set the MF\_MT\_VIDEO\_3D\_FIRST\_IS\_LEFT attribute to **FALSE** in the media type.</span></span>

> [!Note]  
> <span data-ttu-id="b470e-127">在 *基底視圖* 格式中 (**MFVideo3DSampleFormat \_ 基礎** 視圖) ，只會保留基底視圖，因此不適用此屬性。</span><span class="sxs-lookup"><span data-stu-id="b470e-127">In *base view* format (**MFVideo3DSampleFormat\_BaseView**), only the base view is retained, so this attribute does not apply.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b470e-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="b470e-128">Requirements</span></span>



| <span data-ttu-id="b470e-129">需求</span><span class="sxs-lookup"><span data-stu-id="b470e-129">Requirement</span></span> | <span data-ttu-id="b470e-130">值</span><span class="sxs-lookup"><span data-stu-id="b470e-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b470e-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b470e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b470e-132">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b470e-132">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="b470e-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b470e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b470e-134">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b470e-134">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="b470e-135">標頭</span><span class="sxs-lookup"><span data-stu-id="b470e-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b470e-136"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="b470e-136"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b470e-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b470e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b470e-138">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="b470e-138">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




