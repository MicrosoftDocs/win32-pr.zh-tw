---
title: '影像清單建立旗標 (Shlobj.h .h) '
description: 一組位旗標，指定要建立之影像清單的類型。 這個參數可以是下列值的組合，但只能包含其中一個 ILC.OUT 的 \_ 色彩值。 由 ImageList \_ Create 和 IImageList2 Initialize 使用。
ms.assetid: DFEB1934-DB7F-4151-97F9-DDB2BCCC782A
topic_type:
- apiref
api_name:
- ILC_MASK
- ILC_COLOR
- ILC_COLORDDB
- ILC_COLOR4
- ILC_COLOR8
- ILC_COLOR16
- ILC_COLOR24
- ILC_COLOR32
- ILC_PALETTE
- ILC_MIRROR
- ILC_PERITEMMIRROR
- ILC_ORIGINALSIZE
- ILC_HIGHQUALITYSCALE
api_location:
- Shlobj.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f27f9a83c119b8e201ba41c002bf7c166ba3e4dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465041"
---
# <a name="image-list-creation-flags"></a><span data-ttu-id="62ef6-105">影像清單建立旗標</span><span class="sxs-lookup"><span data-stu-id="62ef6-105">Image List Creation Flags</span></span>

<span data-ttu-id="62ef6-106">一組位旗標，指定要建立之影像清單的類型。</span><span class="sxs-lookup"><span data-stu-id="62ef6-106">The set of bit flags that specifies the type of image list to create.</span></span> <span data-ttu-id="62ef6-107">這個參數可以是下列值的組合，但只能包含其中一個 ILC.OUT 的 \_ 色彩值。</span><span class="sxs-lookup"><span data-stu-id="62ef6-107">This parameter can be a combination of the following values, but it can include only one of the ILC\_COLOR values.</span></span> <span data-ttu-id="62ef6-108">由 [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) 和 [**IImageList2：： Initialize**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-initialize)使用。</span><span class="sxs-lookup"><span data-stu-id="62ef6-108">Used by [**ImageList\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) and [**IImageList2::Initialize**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-initialize).</span></span>



| <span data-ttu-id="62ef6-109">常數/值</span><span class="sxs-lookup"><span data-stu-id="62ef6-109">Constant/value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="62ef6-110">Description</span><span class="sxs-lookup"><span data-stu-id="62ef6-110">Description</span></span>                                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILC_MASK"></span><span id="ilc_mask"></span><dl> <span data-ttu-id="62ef6-111"><dt>**Ilc.out \_MASK**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="62ef6-111"><dt>**ILC\_MASK**</dt> <dt>0x00000001</dt></span></span> </dl>                                     | <span data-ttu-id="62ef6-112">使用遮罩。</span><span class="sxs-lookup"><span data-stu-id="62ef6-112">Use a mask.</span></span> <span data-ttu-id="62ef6-113">影像清單包含兩個位圖，其中一個點陣圖是用來做為遮罩的單色點陣圖。</span><span class="sxs-lookup"><span data-stu-id="62ef6-113">The image list contains two bitmaps, one of which is a monochrome bitmap used as a mask.</span></span> <span data-ttu-id="62ef6-114">如果未包含此值，則影像清單只會包含一個點陣圖。</span><span class="sxs-lookup"><span data-stu-id="62ef6-114">If this value is not included, the image list contains only one bitmap.</span></span><br/>      |
| <span id="ILC_COLOR"></span><span id="ilc_color"></span><dl> <span data-ttu-id="62ef6-115"><dt>**Ilc.out \_色彩**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="62ef6-115"><dt>**ILC\_COLOR**</dt> <dt>0x00000000</dt></span></span> </dl>                                  | <span data-ttu-id="62ef6-116">如果未指定任何其他 ILC.OUT \_ COLORx 旗標，請使用預設行為。</span><span class="sxs-lookup"><span data-stu-id="62ef6-116">Use the default behavior if none of the other ILC\_COLORx flags is specified.</span></span> <span data-ttu-id="62ef6-117">一般而言，預設值是 ILC.OUT \_ COLOR4，但對於較舊的顯示器驅動程式，預設值為 Ilc.out \_ COLORDDB。</span><span class="sxs-lookup"><span data-stu-id="62ef6-117">Typically, the default is ILC\_COLOR4, but for older display drivers, the default is ILC\_COLORDDB.</span></span><br/> |
| <span id="ILC_COLORDDB"></span><span id="ilc_colorddb"></span><dl> <span data-ttu-id="62ef6-118"><dt>**Ilc.out \_COLORDDB**</dt> <dt>0x000000FE</dt></span><span class="sxs-lookup"><span data-stu-id="62ef6-118"><dt>**ILC\_COLORDDB**</dt> <dt>0x000000FE</dt></span></span> </dl>                         | <span data-ttu-id="62ef6-119">使用裝置相依的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="62ef6-119">Use a device-dependent bitmap.</span></span><br/>                                                                                                                                                    |
| <span id="ILC_COLOR4"></span><span id="ilc_color4"></span><dl> <span data-ttu-id="62ef6-120"><dt>**Ilc.out \_COLOR4**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="62ef6-120"><dt>**ILC\_COLOR4**</dt> <dt>0x00000004</dt></span></span> </dl>                               | <span data-ttu-id="62ef6-121">使用4位 (16 色) 裝置獨立點陣圖 (DIB) 區段作為影像清單的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="62ef6-121">Use a 4-bit (16-color) device-independent bitmap (DIB) section as the bitmap for the image list.</span></span><br/>                                                                                  |
| <span id="ILC_COLOR8"></span><span id="ilc_color8"></span><dl> <span data-ttu-id="62ef6-122"><dt>**Ilc.out \_COLOR8**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="62ef6-122"><dt>**ILC\_COLOR8**</dt> <dt>0x00000008</dt></span></span> </dl>                               | <span data-ttu-id="62ef6-123">使用8位的 DIB 區段。</span><span class="sxs-lookup"><span data-stu-id="62ef6-123">Use an 8-bit DIB section.</span></span> <span data-ttu-id="62ef6-124">色彩表所使用的色彩與半色調調色板的色彩相同。</span><span class="sxs-lookup"><span data-stu-id="62ef6-124">The colors used for the color table are the same colors as the halftone palette.</span></span><br/>                                                                        |
| <span id="ILC_COLOR16"></span><span id="ilc_color16"></span><dl> <span data-ttu-id="62ef6-125"><dt>**Ilc.out \_COLOR16**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="62ef6-125"><dt>**ILC\_COLOR16**</dt> <dt>0x00000010</dt></span></span> </dl>                            | <span data-ttu-id="62ef6-126">使用16位 (32/64k 色彩) DIB 區段。</span><span class="sxs-lookup"><span data-stu-id="62ef6-126">Use a 16-bit (32/64k-color) DIB section.</span></span><br/>                                                                                                                                          |
| <span id="ILC_COLOR24"></span><span id="ilc_color24"></span><dl> <span data-ttu-id="62ef6-127"><dt>**Ilc.out \_COLOR24**</dt> <dt>0x00000018</dt></span><span class="sxs-lookup"><span data-stu-id="62ef6-127"><dt>**ILC\_COLOR24**</dt> <dt>0x00000018</dt></span></span> </dl>                            | <span data-ttu-id="62ef6-128">使用24位的 DIB 區段。</span><span class="sxs-lookup"><span data-stu-id="62ef6-128">Use a 24-bit DIB section.</span></span><br/>                                                                                                                                                         |
| <span id="ILC_COLOR32"></span><span id="ilc_color32"></span><dl> <span data-ttu-id="62ef6-129"><dt>**Ilc.out \_COLOR32**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="62ef6-129"><dt>**ILC\_COLOR32**</dt> <dt>0x00000020</dt></span></span> </dl>                            | <span data-ttu-id="62ef6-130">使用32位的 DIB 區段。</span><span class="sxs-lookup"><span data-stu-id="62ef6-130">Use a 32-bit DIB section.</span></span><br/>                                                                                                                                                         |
| <span id="ILC_PALETTE"></span><span id="ilc_palette"></span><dl> <span data-ttu-id="62ef6-131"><dt>**Ilc.out \_調色板**</dt> <dt>0x00000800</dt></span><span class="sxs-lookup"><span data-stu-id="62ef6-131"><dt>**ILC\_PALETTE**</dt> <dt>0x00000800</dt></span></span> </dl>                            | <span data-ttu-id="62ef6-132">未實作。</span><span class="sxs-lookup"><span data-stu-id="62ef6-132">Not implemented.</span></span><br/>                                                                                                                                                                  |
| <span id="ILC_MIRROR"></span><span id="ilc_mirror"></span><dl> <span data-ttu-id="62ef6-133"><dt>**Ilc.out \_鏡像**</dt> <dt>0x00002000</dt></span><span class="sxs-lookup"><span data-stu-id="62ef6-133"><dt>**ILC\_MIRROR**</dt> <dt>0x00002000</dt></span></span> </dl>                               | <span data-ttu-id="62ef6-134">如果進程已鏡像，則鏡像包含的圖示</span><span class="sxs-lookup"><span data-stu-id="62ef6-134">Mirror the icons contained, if the process is mirrored</span></span><br/>                                                                                                                            |
| <span id="ILC_PERITEMMIRROR"></span><span id="ilc_peritemmirror"></span><dl> <span data-ttu-id="62ef6-135"><dt>**Ilc.out \_PERITEMMIRROR**</dt> <dt>0x00008000</dt></span><span class="sxs-lookup"><span data-stu-id="62ef6-135"><dt>**ILC\_PERITEMMIRROR**</dt> <dt>0x00008000</dt></span></span> </dl>          | <span data-ttu-id="62ef6-136">導致鏡像程式碼在插入一組影像（與整個區域）時，將每個專案鏡像。</span><span class="sxs-lookup"><span data-stu-id="62ef6-136">Causes the mirroring code to mirror each item when inserting a set of images, versus the whole strip.</span></span><br/>                                                                             |
| <span id="ILC_ORIGINALSIZE"></span><span id="ilc_originalsize"></span><dl> <span data-ttu-id="62ef6-137"><dt>**Ilc.out \_ORIGINALSIZE**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="62ef6-137"><dt>**ILC\_ORIGINALSIZE**</dt> <dt>0x00010000</dt></span></span> </dl>             | <span data-ttu-id="62ef6-138">**Windows Vista （含）以後版本。**</span><span class="sxs-lookup"><span data-stu-id="62ef6-138">**Windows Vista and later.**</span></span> <span data-ttu-id="62ef6-139">Imagelist 應接受小於設定的影像，並根據新增的影像套用原始大小。</span><span class="sxs-lookup"><span data-stu-id="62ef6-139">Imagelist should accept smaller than set images and apply original size based on image added.</span></span><br/>                                                        |
| <span id="ILC_HIGHQUALITYSCALE"></span><span id="ilc_highqualityscale"></span><dl> <span data-ttu-id="62ef6-140"><dt>**Ilc.out \_HIGHQUALITYSCALE**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="62ef6-140"><dt>**ILC\_HIGHQUALITYSCALE**</dt> <dt>0x00020000</dt></span></span> </dl> | <span data-ttu-id="62ef6-141">**Windows Vista （含）以後版本。**</span><span class="sxs-lookup"><span data-stu-id="62ef6-141">**Windows Vista and later.**</span></span> <span data-ttu-id="62ef6-142">保留的。</span><span class="sxs-lookup"><span data-stu-id="62ef6-142">Reserved.</span></span><br/>                                                                                                                                            |



## <a name="requirements"></a><span data-ttu-id="62ef6-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="62ef6-143">Requirements</span></span>



| <span data-ttu-id="62ef6-144">需求</span><span class="sxs-lookup"><span data-stu-id="62ef6-144">Requirement</span></span> | <span data-ttu-id="62ef6-145">值</span><span class="sxs-lookup"><span data-stu-id="62ef6-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="62ef6-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="62ef6-146">Minimum supported client</span></span><br/> | <span data-ttu-id="62ef6-147">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62ef6-147">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="62ef6-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="62ef6-148">Minimum supported server</span></span><br/> | <span data-ttu-id="62ef6-149">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62ef6-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="62ef6-150">標頭</span><span class="sxs-lookup"><span data-stu-id="62ef6-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="62ef6-151"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="62ef6-151"><dt>Shlobj.h</dt></span></span> </dl> |



 

 





