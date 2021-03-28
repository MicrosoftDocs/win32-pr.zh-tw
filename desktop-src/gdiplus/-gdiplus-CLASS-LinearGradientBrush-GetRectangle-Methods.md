---
description: 本主題列出 LinearGradientBrush 類別的 GetRectangle 方法。 如需 LinearGradientBrush 類別之方法的完整清單，請參閱 LinearGradientBrush 方法。
ms.assetid: 56ec2372-0fd3-4220-a283-5d9691fe2e69
title: 'LinearGradientBrush. GetRectangle 方法 (Gdiplusheaders .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 1d22dfbe8c32c4f8ccb7e902455ae68d7018590c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192364"
---
# <a name="lineargradientbrushgetrectangle-methods"></a><span data-ttu-id="e200f-104">LinearGradientBrush. GetRectangle 方法</span><span class="sxs-lookup"><span data-stu-id="e200f-104">LinearGradientBrush.GetRectangle methods</span></span>

<span data-ttu-id="e200f-105">本主題列出 [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) 類別的 GetRectangle 方法。</span><span class="sxs-lookup"><span data-stu-id="e200f-105">This topic lists the GetRectangle methods of the [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) class.</span></span> <span data-ttu-id="e200f-106">如需 **LinearGradientBrush** 類別之方法的完整清單，請參閱 [LinearGradientBrush 方法](-gdiplus-class-lineargradientbrush-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="e200f-106">For a complete list of methods for the **LinearGradientBrush** class, see [LinearGradientBrush Methods](-gdiplus-class-lineargradientbrush-methods.md).</span></span>

### <a name="overload-list"></a><span data-ttu-id="e200f-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="e200f-107">Overload list</span></span>



| <span data-ttu-id="e200f-108">方法</span><span class="sxs-lookup"><span data-stu-id="e200f-108">Method</span></span>                                                                                       | <span data-ttu-id="e200f-109">描述</span><span class="sxs-lookup"><span data-stu-id="e200f-109">Description</span></span>                                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e200f-110">[**GetRectangle (Rect \*)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-getrectangle(outrect))</span><span class="sxs-lookup"><span data-stu-id="e200f-110">[**GetRectangle(Rect\*)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-getrectangle(outrect))</span></span>   | <span data-ttu-id="e200f-111">[**LinearGradientBrush：： GetRectangle**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-getrectangle(outrect))方法會取得定義漸層界限的矩形。</span><span class="sxs-lookup"><span data-stu-id="e200f-111">The [**LinearGradientBrush::GetRectangle**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-getrectangle(outrect)) method gets the rectangle that defines the boundaries of the gradient.</span></span> <br/> |
| <span data-ttu-id="e200f-112">[**GetRectangle (RectF \*)**](/previous-versions//ms535352(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e200f-112">[**GetRectangle(RectF\*)**](/previous-versions//ms535352(v=vs.85))</span></span> | <span data-ttu-id="e200f-113">[**LinearGradientBrush：： GetRectangle**](/previous-versions//ms535352(v=vs.85))方法會取得定義漸層界限的矩形。</span><span class="sxs-lookup"><span data-stu-id="e200f-113">The [**LinearGradientBrush::GetRectangle**](/previous-versions//ms535352(v=vs.85)) method gets the rectangle that defines the boundaries of the gradient.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e200f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e200f-114">Requirements</span></span>



| <span data-ttu-id="e200f-115">需求</span><span class="sxs-lookup"><span data-stu-id="e200f-115">Requirement</span></span> | <span data-ttu-id="e200f-116">值</span><span class="sxs-lookup"><span data-stu-id="e200f-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e200f-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e200f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e200f-118">僅限 windows XP、Windows 2000 Professional \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e200f-118">Windows XP, Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e200f-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e200f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e200f-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e200f-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="e200f-121">產品</span><span class="sxs-lookup"><span data-stu-id="e200f-121">Product</span></span><br/>                  | <span data-ttu-id="e200f-122">GDI + 1。0</span><span class="sxs-lookup"><span data-stu-id="e200f-122">GDI+ 1.0</span></span><br/>                                                                                             |
| <span data-ttu-id="e200f-123">標頭</span><span class="sxs-lookup"><span data-stu-id="e200f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e200f-124"><dt>Gdiplusheaders (包含 Gdiplus.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="e200f-124"><dt>Gdiplusheaders.h (include Gdiplus.h)</dt></span></span> </dl> |
| <span data-ttu-id="e200f-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="e200f-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="e200f-126"><dt>Gdiplus.dll .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e200f-126"><dt>Gdiplus.lib</dt></span></span> </dl>                          |



 

 
