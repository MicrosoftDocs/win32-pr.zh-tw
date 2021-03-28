---
description: 本主題列出 Graphics 類別的 ExcludeClip 方法。 如需圖形類別之方法的完整清單，請參閱圖形。
ms.assetid: ee2b1bc7-6623-4144-b8fb-2ab9fbe28f59
title: 'ExcludeClip 方法 (Gdiplusgraphics .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 70011bfe1aba7ef8e7c14b58f61bfcbd9549c8fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "104992458"
---
# <a name="graphicsexcludeclip-methods"></a><span data-ttu-id="821a6-104">ExcludeClip 方法</span><span class="sxs-lookup"><span data-stu-id="821a6-104">Graphics.ExcludeClip methods</span></span>

<span data-ttu-id="821a6-105">本主題列出 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 類別的 ExcludeClip 方法。</span><span class="sxs-lookup"><span data-stu-id="821a6-105">This topic lists the ExcludeClip methods of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="821a6-106">如需 **圖形** 類別之方法的完整清單，請參閱 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)。</span><span class="sxs-lookup"><span data-stu-id="821a6-106">For a complete list of methods for the **Graphics** class, see [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).</span></span>

### <a name="overload-list"></a><span data-ttu-id="821a6-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="821a6-107">Overload list</span></span>



| <span data-ttu-id="821a6-108">方法</span><span class="sxs-lookup"><span data-stu-id="821a6-108">Method</span></span>                                                                         | <span data-ttu-id="821a6-109">描述</span><span class="sxs-lookup"><span data-stu-id="821a6-109">Description</span></span>                                                                                                                                                                                                  |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="821a6-110">[**ExcludeClip (Rect&)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstrect_))</span><span class="sxs-lookup"><span data-stu-id="821a6-110">[**ExcludeClip(Rect&)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstrect_))</span></span>   | <span data-ttu-id="821a6-111">[**Graphics：： ExcludeClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstrect_))方法會將裁剪區域更新為本身不會與指定的矩形相交的部分。</span><span class="sxs-lookup"><span data-stu-id="821a6-111">The [**Graphics::ExcludeClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstrect_)) method updates the clipping region to the portion of itself that does not intersect the specified rectangle.</span></span><br/>  |
| <span data-ttu-id="821a6-112">[**ExcludeClip (RectF&)**](/previous-versions//ms535975(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="821a6-112">[**ExcludeClip(RectF&)**](/previous-versions//ms535975(v=vs.85))</span></span> | <span data-ttu-id="821a6-113">[**Graphics：： ExcludeClip**](/previous-versions//ms535975(v=vs.85))方法會將裁剪區域更新為本身不會與指定的矩形相交的部分。</span><span class="sxs-lookup"><span data-stu-id="821a6-113">The [**Graphics::ExcludeClip**](/previous-versions//ms535975(v=vs.85)) method updates the clipping region to the portion of itself that does not intersect the specified rectangle.</span></span><br/> |
| <span data-ttu-id="821a6-114">[**ExcludeClip (區域 \*)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstregion))</span><span class="sxs-lookup"><span data-stu-id="821a6-114">[**ExcludeClip(Region\*)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstregion))</span></span>   | <span data-ttu-id="821a6-115">[**Graphics：： ExcludeClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstregion))方法會以本身的部分（不會與指定的區域重迭）來更新裁剪區域。</span><span class="sxs-lookup"><span data-stu-id="821a6-115">The [**Graphics::ExcludeClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstregion)) method updates the clipping region with the portion of itself that does not overlap the specified region.</span></span><br/>        |



## <a name="requirements"></a><span data-ttu-id="821a6-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="821a6-116">Requirements</span></span>



| <span data-ttu-id="821a6-117">需求</span><span class="sxs-lookup"><span data-stu-id="821a6-117">Requirement</span></span> | <span data-ttu-id="821a6-118">值</span><span class="sxs-lookup"><span data-stu-id="821a6-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="821a6-119">標頭</span><span class="sxs-lookup"><span data-stu-id="821a6-119">Header</span></span><br/> | <dl> <span data-ttu-id="821a6-120"><dt>Gdiplusgraphics。h</dt></span><span class="sxs-lookup"><span data-stu-id="821a6-120"><dt>Gdiplusgraphics.h</dt></span></span> </dl> |



 

 
