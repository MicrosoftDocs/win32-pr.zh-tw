---
description: Stretchmode 屬性會指定如何延展不符合輸出維度的影像。
ms.assetid: 9a26bb8b-2b1c-424a-ae30-e175c60c76a1
title: stretchmode 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48a629a34dc1875a7f1d3669e32c53d0e8d3d29c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850968"
---
# <a name="stretchmode-attribute"></a><span data-ttu-id="72932-103">stretchmode 屬性</span><span class="sxs-lookup"><span data-stu-id="72932-103">stretchmode Attribute</span></span>

> [!Note]  
> <span data-ttu-id="72932-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="72932-104">\[Deprecated.</span></span> <span data-ttu-id="72932-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="72932-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="72932-106">`stretchmode`屬性會指定如何延展不符合輸出維度的影像。</span><span class="sxs-lookup"><span data-stu-id="72932-106">The `stretchmode` attribute specifies how to stretch an image that does not match the output dimensions.</span></span>

## <a name="possible-values"></a><span data-ttu-id="72932-107">可能的值</span><span class="sxs-lookup"><span data-stu-id="72932-107">Possible Values</span></span>

<span data-ttu-id="72932-108">必須具有下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="72932-108">Must have one of the following values.</span></span>

-   <span data-ttu-id="72932-109">「延展」：影像會伸展以符合輸出框架大小，而不會保留長寬比。</span><span class="sxs-lookup"><span data-stu-id="72932-109">"stretch": The image is stretched to fit the output frame size without preserving aspect ratio.</span></span> <span data-ttu-id="72932-110">(預設值)</span><span class="sxs-lookup"><span data-stu-id="72932-110">(Default)</span></span>
-   <span data-ttu-id="72932-111">「裁剪」：影像會裁剪以符合輸出框架大小。</span><span class="sxs-lookup"><span data-stu-id="72932-111">"crop": The image is cropped to fit the output frame size.</span></span>
-   <span data-ttu-id="72932-112">"preserveaspectratio"：保留原始的外觀比例，且沿著較短的維度有黑色的黑邊。</span><span class="sxs-lookup"><span data-stu-id="72932-112">"preserveaspectratio": The original aspect ratio is preserved, with a black letterbox along the shorter dimension.</span></span>
-   <span data-ttu-id="72932-113">"preserveaspectrationoletterbox"：影像會調整大小以填滿整個目標框架，同時保留外觀比例。</span><span class="sxs-lookup"><span data-stu-id="72932-113">"preserveaspectrationoletterbox": The image is resized to fill the entire target frame while preserving the aspect ratio.</span></span>

## <a name="applies-to"></a><span data-ttu-id="72932-114">套用至</span><span class="sxs-lookup"><span data-stu-id="72932-114">Applies To</span></span>

[<span data-ttu-id="72932-115">**clip**</span><span class="sxs-lookup"><span data-stu-id="72932-115">**clip**</span></span>](clip-element.md)

## <a name="see-also"></a><span data-ttu-id="72932-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72932-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72932-117">XTL 屬性</span><span class="sxs-lookup"><span data-stu-id="72932-117">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="72932-118">**IAMTimelineSrc::SetStretchMode**</span><span class="sxs-lookup"><span data-stu-id="72932-118">**IAMTimelineSrc::SetStretchMode**</span></span>](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 



