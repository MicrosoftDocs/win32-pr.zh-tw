---
description: 指定此解碼器的後置處理模式。
ms.assetid: c6dab7f6-4a3e-45bb-b81c-5f4c39f9e954
title: 'MFPKEY_POSTPROCESSMODE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4002deae63f1bdaea09ca31dd95bfec1cb594fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001631"
---
# <a name="mfpkey_postprocessmode-property"></a><span data-ttu-id="a408e-103">MFPKEY \_ POSTPROCESSMODE 屬性</span><span class="sxs-lookup"><span data-stu-id="a408e-103">MFPKEY\_POSTPROCESSMODE Property</span></span>

<span data-ttu-id="a408e-104">指定此解碼器的後置處理模式。</span><span class="sxs-lookup"><span data-stu-id="a408e-104">Specifies the post processing mode for the decoder.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="a408e-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="a408e-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="a408e-106">**g \_ wszWMVCForcePostProcessMode**</span><span class="sxs-lookup"><span data-stu-id="a408e-106">**g\_wszWMVCForcePostProcessMode**</span></span>

## <a name="data-type"></a><span data-ttu-id="a408e-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="a408e-107">Data Type</span></span>

<span data-ttu-id="a408e-108">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="a408e-108">**VT\_I4**</span></span>

## <a name="remarks"></a><span data-ttu-id="a408e-109">備註</span><span class="sxs-lookup"><span data-stu-id="a408e-109">Remarks</span></span>

<span data-ttu-id="a408e-110">將此屬性設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a408e-110">Set this property to one of the following values.</span></span>



| <span data-ttu-id="a408e-111">值</span><span class="sxs-lookup"><span data-stu-id="a408e-111">Value</span></span> | <span data-ttu-id="a408e-112">意義</span><span class="sxs-lookup"><span data-stu-id="a408e-112">Meaning</span></span>                                                                                |
|-------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a408e-113">-1</span><span class="sxs-lookup"><span data-stu-id="a408e-113">-1</span></span>    | <span data-ttu-id="a408e-114">此解碼器會根據可用的 CPU 資源，以更自我調整的方式設定後置處理模式。</span><span class="sxs-lookup"><span data-stu-id="a408e-114">The decoder sets the post processing mode adaptively based on available CPU resources.</span></span> |
| <span data-ttu-id="a408e-115">0</span><span class="sxs-lookup"><span data-stu-id="a408e-115">0</span></span>     | <span data-ttu-id="a408e-116">此解碼器不會執行任何後置處理。</span><span class="sxs-lookup"><span data-stu-id="a408e-116">The decoder performs no post processing.</span></span>                                               |
| <span data-ttu-id="a408e-117">1</span><span class="sxs-lookup"><span data-stu-id="a408e-117">1</span></span>     | <span data-ttu-id="a408e-118">否則解碼器會執行快速 deblocking。</span><span class="sxs-lookup"><span data-stu-id="a408e-118">fThe decoder performs fast deblocking.</span></span>                                                 |
| <span data-ttu-id="a408e-119">2</span><span class="sxs-lookup"><span data-stu-id="a408e-119">2</span></span>     | <span data-ttu-id="a408e-120">此解碼器會執行完整 deblocking。</span><span class="sxs-lookup"><span data-stu-id="a408e-120">The decoder performs full deblocking.</span></span>                                                  |
| <span data-ttu-id="a408e-121">3</span><span class="sxs-lookup"><span data-stu-id="a408e-121">3</span></span>     | <span data-ttu-id="a408e-122">此解碼器會執行快速的 deblocking 和 deringing。</span><span class="sxs-lookup"><span data-stu-id="a408e-122">The decoder performs fast deblocking and deringing.</span></span>                                    |
| <span data-ttu-id="a408e-123">4</span><span class="sxs-lookup"><span data-stu-id="a408e-123">4</span></span>     | <span data-ttu-id="a408e-124">此解碼器會執行完整的 deblocking 和 deringing。</span><span class="sxs-lookup"><span data-stu-id="a408e-124">The decoder performs full deblocking and deringing.</span></span>                                    |



 

<span data-ttu-id="a408e-125">因為這個屬性的值是從0到4，所以解碼複雜性、CPU 資源的使用和圖片品質都會增加。</span><span class="sxs-lookup"><span data-stu-id="a408e-125">As the value of this property goes from 0 to 4, the decoding complexity, use of CPU resources, and picture quality all increase.</span></span>

## <a name="requirements"></a><span data-ttu-id="a408e-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="a408e-126">Requirements</span></span>



| <span data-ttu-id="a408e-127">需求</span><span class="sxs-lookup"><span data-stu-id="a408e-127">Requirement</span></span> | <span data-ttu-id="a408e-128">值</span><span class="sxs-lookup"><span data-stu-id="a408e-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a408e-129">用戶端</span><span class="sxs-lookup"><span data-stu-id="a408e-129">Client</span></span><br/> | <span data-ttu-id="a408e-130">Windows Vista 或 Windows 7</span><span class="sxs-lookup"><span data-stu-id="a408e-130">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="a408e-131">標頭</span><span class="sxs-lookup"><span data-stu-id="a408e-131">Header</span></span><br/> | <dl> <span data-ttu-id="a408e-132"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="a408e-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a408e-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a408e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a408e-134">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="a408e-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




