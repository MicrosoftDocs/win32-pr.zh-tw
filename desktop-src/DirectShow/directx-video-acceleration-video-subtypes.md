---
description: 使用 DirectX Video 加速 (DXVA) 的解碼器會使用下列子類型。
ms.assetid: 031b076b-cdfa-407f-8efa-391bce3075ef
title: 'DirectX Video 加速影片子類型 (Dshow .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0df0f079e795638c6802570c95e2468209a7256
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994307"
---
# <a name="directx-video-acceleration-video-subtypes"></a><span data-ttu-id="86d71-103">DirectX Video 加速影片子類型</span><span class="sxs-lookup"><span data-stu-id="86d71-103">DirectX Video Acceleration Video Subtypes</span></span>

<span data-ttu-id="86d71-104">使用 DirectX Video 加速 (DXVA) 的解碼器會使用下列子類型。</span><span class="sxs-lookup"><span data-stu-id="86d71-104">The following subtypes are used by decoders that are using DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="86d71-105">AI44 和 IA44 是以每圖元的位元組值為8的表面。</span><span class="sxs-lookup"><span data-stu-id="86d71-105">AI44 and IA44 are surfaces with a bits-per-pixel value of 8.</span></span> <span data-ttu-id="86d71-106">有4個位的 I 和 4 *位。\*\*I* 表示在16個專案的 YUV 調色板中的索引。</span><span class="sxs-lookup"><span data-stu-id="86d71-106">There are 4 bits of I and 4 bits of *A*. *I* represents an index into a 16-entry YUV palette.</span></span> <span data-ttu-id="86d71-107">*代表 4* 位的透明資訊 (也稱為每圖元 Alpha) 。</span><span class="sxs-lookup"><span data-stu-id="86d71-107">*A* represents 4 bits of transparency information (also known as per-pixel-alpha).</span></span> <span data-ttu-id="86d71-108">因此，AI44 和 IA44 表面允許16種不同的透明度值，或256不同的圖元標記法。</span><span class="sxs-lookup"><span data-stu-id="86d71-108">Therefore, AI44 and IA44 surfaces allow for 16 different colors at 16 different transparency values, or 256 different pixel representations.</span></span> <span data-ttu-id="86d71-109">使用 AI44 時，Alpha 會儲存在 hi 半形，在 IA44 中，Alpha 會儲存在 lo 位元組內。</span><span class="sxs-lookup"><span data-stu-id="86d71-109">With AI44 the alpha is stored in the hi-nibble, in IA44 the alpha is stored in the lo-nibble.</span></span> <span data-ttu-id="86d71-110">這兩種格式對於 DVD 子圖片和 Line21 與 Teletext 影像都很有用。</span><span class="sxs-lookup"><span data-stu-id="86d71-110">Both formats are very useful for DVD sub-picture images and Line21 and Teletext images.</span></span> <span data-ttu-id="86d71-111">Microsoft 偏好使用 AI44 版本，因為使用此格式可讓您更輕鬆地產生文字。</span><span class="sxs-lookup"><span data-stu-id="86d71-111">Microsoft prefers the AI44 version because it is slightly easier to generate text using this format.</span></span>

| <span data-ttu-id="86d71-112">Subtype</span><span class="sxs-lookup"><span data-stu-id="86d71-112">Subtype</span></span>            | <span data-ttu-id="86d71-113">Description</span><span class="sxs-lookup"><span data-stu-id="86d71-113">Description</span></span>                                                 |
|--------------------|-------------------------------------------------------------|
| <span data-ttu-id="86d71-114">MEDIASUBTYPE \_ AI44</span><span class="sxs-lookup"><span data-stu-id="86d71-114">MEDIASUBTYPE\_AI44</span></span> | <span data-ttu-id="86d71-115">適用于子圖片和文字覆迭。</span><span class="sxs-lookup"><span data-stu-id="86d71-115">For subpicture and text overlays.</span></span> <span data-ttu-id="86d71-116">請參閱先前的描述。</span><span class="sxs-lookup"><span data-stu-id="86d71-116">See previous description.</span></span> |
| <span data-ttu-id="86d71-117">MEDIASUBTYPE \_ IA44</span><span class="sxs-lookup"><span data-stu-id="86d71-117">MEDIASUBTYPE\_IA44</span></span> | <span data-ttu-id="86d71-118">適用于子圖片和文字覆迭。</span><span class="sxs-lookup"><span data-stu-id="86d71-118">For subpicture and text overlays.</span></span> <span data-ttu-id="86d71-119">請參閱先前的描述。</span><span class="sxs-lookup"><span data-stu-id="86d71-119">See previous description.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="86d71-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="86d71-120">Requirements</span></span>



| <span data-ttu-id="86d71-121">需求</span><span class="sxs-lookup"><span data-stu-id="86d71-121">Requirement</span></span> | <span data-ttu-id="86d71-122">值</span><span class="sxs-lookup"><span data-stu-id="86d71-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="86d71-123">標頭</span><span class="sxs-lookup"><span data-stu-id="86d71-123">Header</span></span><br/> | <dl> <span data-ttu-id="86d71-124"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="86d71-124"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86d71-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86d71-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86d71-126">影片子類型</span><span class="sxs-lookup"><span data-stu-id="86d71-126">Video Subtypes</span></span>](video-subtypes.md)
</dt> </dl>

 

 




