---
title: 'ID2D1DeviceCoNtext2 CreateImageSourceFromWic 方法 (D2d1 \_ 3 .h) '
description: 從 WIC 點陣圖來源建立影像來源物件，同時擴展影像來源內的所有圖元記憶體。 映射會在使用最少記憶體的情況下載入並儲存。
ms.assetid: af02630d-a9ca-f5b4-6f2a-31a73ef603e5
keywords:
- CreateImageSourceFromWic 方法 Direct2D
topic_type:
- apiref
api_location:
- d2d1_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 20773912886840a185e1b9fc71576f89e9a40fde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984869"
---
# <a name="id2d1devicecontext2createimagesourcefromwic-methods"></a><span data-ttu-id="20f37-105">ID2D1DeviceCoNtext2：： CreateImageSourceFromWic 方法</span><span class="sxs-lookup"><span data-stu-id="20f37-105">ID2D1DeviceContext2::CreateImageSourceFromWic methods</span></span>

<span data-ttu-id="20f37-106">從 WIC 點陣圖來源建立影像來源物件，同時擴展影像來源內的所有圖元記憶體。</span><span class="sxs-lookup"><span data-stu-id="20f37-106">Creates an image source object from a WIC bitmap source, while populating all pixel memory within the image source.</span></span> <span data-ttu-id="20f37-107">映射會在使用最少記憶體的情況下載入並儲存。</span><span class="sxs-lookup"><span data-stu-id="20f37-107">The image is loaded and stored while using a minimal amount of memory.</span></span>

### <a name="overload-list"></a><span data-ttu-id="20f37-108">多載清單</span><span class="sxs-lookup"><span data-stu-id="20f37-108">Overload list</span></span>



| <span data-ttu-id="20f37-109">方法</span><span class="sxs-lookup"><span data-stu-id="20f37-109">Method</span></span>                                                                                                                                                                                       | <span data-ttu-id="20f37-110">描述</span><span class="sxs-lookup"><span data-stu-id="20f37-110">Description</span></span>                                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20f37-111">[**CreateImageSourceFromWic (IWICBitmapSource \* 、D2D1 \_ 映射 \_ 來源 \_ 載入 \_ 選項、ID2D1ImageSourceFromWic \* \*)**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_id2d1imagesourcefromwic))</span><span class="sxs-lookup"><span data-stu-id="20f37-111">[**CreateImageSourceFromWic (IWICBitmapSource\*, D2D1\_IMAGE\_SOURCE\_LOADING\_OPTIONS, ID2D1ImageSourceFromWic\*\*)**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_id2d1imagesourcefromwic))</span></span>                   | <span data-ttu-id="20f37-112">方法的版本，可讓您指定 WIC 點陣圖來源、輸出影像來源物件，以及使用預設 Alpha 模式載入選項。</span><span class="sxs-lookup"><span data-stu-id="20f37-112">Version of the method that allows you to specify the WIC bitmap source, the output image source object, and loading options with default alpha mode.</span></span><br/>   |
| <span data-ttu-id="20f37-113">[**CreateImageSourceFromWic (IWICBitmapSource \* 、D2D1 \_ 影像 \_ 來源 \_ 載入 \_ 選項、D2D1 \_ ALPHA \_ 模式、ID2D1ImageSourceFromWic \* \*)**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_d2d1_alpha_mode_id2d1imagesourcefromwic))</span><span class="sxs-lookup"><span data-stu-id="20f37-113">[**CreateImageSourceFromWic (IWICBitmapSource\*, D2D1\_IMAGE\_SOURCE\_LOADING\_OPTIONS, D2D1\_ALPHA\_MODE, ID2D1ImageSourceFromWic\*\*)**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_d2d1_alpha_mode_id2d1imagesourcefromwic))</span></span> | <span data-ttu-id="20f37-114">方法的版本，可讓您指定 WIC 點陣圖來源、輸出影像來源物件和載入選項，以及 Alpha 模式。</span><span class="sxs-lookup"><span data-stu-id="20f37-114">Version of the method that allows you to specify the WIC bitmap source, the output image source object, and loading options, and alpha mode.</span></span><br/>           |
| <span data-ttu-id="20f37-115">[**CreateImageSourceFromWic (IWICBitmapSource \* 、ID2D1ImageSourceFromWic \* \*)**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_id2d1imagesourcefromwic))</span><span class="sxs-lookup"><span data-stu-id="20f37-115">[**CreateImageSourceFromWic (IWICBitmapSource\*, ID2D1ImageSourceFromWic\*\*)**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_id2d1imagesourcefromwic))</span></span>                                                          | <span data-ttu-id="20f37-116">方法的版本，可讓您指定 WIC 點陣圖來源，以及具有預設載入 opitons 和 Alpha 模式的輸出影像來源物件。</span><span class="sxs-lookup"><span data-stu-id="20f37-116">Version of the method that allows you to specify the WIC bitmap source and the output image source object with default loading opitons and alpha mode.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="20f37-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="20f37-117">Requirements</span></span>



| <span data-ttu-id="20f37-118">需求</span><span class="sxs-lookup"><span data-stu-id="20f37-118">Requirement</span></span> | <span data-ttu-id="20f37-119">值</span><span class="sxs-lookup"><span data-stu-id="20f37-119">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="20f37-120">標頭</span><span class="sxs-lookup"><span data-stu-id="20f37-120">Header</span></span><br/> | <dl> <span data-ttu-id="20f37-121"><dt>D2d1 \_ 3。h</dt></span><span class="sxs-lookup"><span data-stu-id="20f37-121"><dt>D2d1\_3.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20f37-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="20f37-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20f37-123">**ID2D1DeviceCoNtext2**</span><span class="sxs-lookup"><span data-stu-id="20f37-123">**ID2D1DeviceContext2**</span></span>](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1devicecontext2)
</dt> </dl>

<span data-ttu-id="20f37-124">�</span><span class="sxs-lookup"><span data-stu-id="20f37-124">�</span></span>

<span data-ttu-id="20f37-125">�</span><span class="sxs-lookup"><span data-stu-id="20f37-125">�</span></span>
