---
description: 本主題列出 Graphics 類別的 DrawString 方法。 如需圖形類別之方法的完整清單，請參閱圖形。
ms.assetid: b3568ed9-e359-4916-a83d-7553c021d197
title: 'DrawString 方法 (Gdiplusgraphics .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 275c256ec2c7284401d37794bccf368538cbdd80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "104974869"
---
# <a name="graphicsdrawstring-methods"></a><span data-ttu-id="1dd14-104">DrawString 方法</span><span class="sxs-lookup"><span data-stu-id="1dd14-104">Graphics.DrawString methods</span></span>

<span data-ttu-id="1dd14-105">本主題列出 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 類別的 DrawString 方法。</span><span class="sxs-lookup"><span data-stu-id="1dd14-105">This topic lists the DrawString methods of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="1dd14-106">如需 **圖形** 類別之方法的完整清單，請參閱 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)。</span><span class="sxs-lookup"><span data-stu-id="1dd14-106">For a complete list of methods for the **Graphics** class, see [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).</span></span>

### <a name="overload-list"></a><span data-ttu-id="1dd14-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="1dd14-107">Overload list</span></span>



| <span data-ttu-id="1dd14-108">方法</span><span class="sxs-lookup"><span data-stu-id="1dd14-108">Method</span></span>                                                                                                                                                       | <span data-ttu-id="1dd14-109">描述</span><span class="sxs-lookup"><span data-stu-id="1dd14-109">Description</span></span>                                                                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dd14-110">[**DrawString (WCHAR \* 、INT、font-family、font-family、 \* PointF&、筆刷 \*)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))</span><span class="sxs-lookup"><span data-stu-id="1dd14-110">[**DrawString(WCHAR\*,INT,Font\*,PointF&,Brush\*)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))</span></span>                                | <span data-ttu-id="1dd14-111">[**Graphics：:D rawstring**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))方法會根據字型和字串的原點來繪製字串。</span><span class="sxs-lookup"><span data-stu-id="1dd14-111">The [**Graphics::DrawString**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method draws a string based on a font and an origin for the string.</span></span><br/>                        |
| <span data-ttu-id="1dd14-112">[**DrawString (WCHAR \* 、INT、font-family、 \* RectF&、StringFormat \* 、筆刷 \*)**](/previous-versions//ms535991(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1dd14-112">[**DrawString(WCHAR\*,INT,Font\*,RectF&,StringFormat\*,Brush\*)**](/previous-versions//ms535991(v=vs.85))</span></span> | <span data-ttu-id="1dd14-113">[**圖形：:D rawstring**](/previous-versions//ms535991(v=vs.85))方法會根據字型、版面配置矩形和格式來繪製字串。</span><span class="sxs-lookup"><span data-stu-id="1dd14-113">The [**Graphics::DrawString**](/previous-versions//ms535991(v=vs.85)) method draws a string based on a font, a layout rectangle, and a format.</span></span> <br/> |
| <span data-ttu-id="1dd14-114">[**DrawString (WCHAR \* 、INT、font-family、 \* PointF&、StringFormat \* 、筆刷 \*)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush))</span><span class="sxs-lookup"><span data-stu-id="1dd14-114">[**DrawString(WCHAR\*,INT,Font\*,PointF&,StringFormat\*,Brush\*)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush))</span></span>    | <span data-ttu-id="1dd14-115">[**Graphics：:D rawstring**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush))方法會根據字型、字串原點和格式來繪製字串。</span><span class="sxs-lookup"><span data-stu-id="1dd14-115">The [**Graphics::DrawString**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method draws a string based on a font, a string origin, and a format.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="1dd14-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="1dd14-116">Requirements</span></span>



| <span data-ttu-id="1dd14-117">需求</span><span class="sxs-lookup"><span data-stu-id="1dd14-117">Requirement</span></span> | <span data-ttu-id="1dd14-118">值</span><span class="sxs-lookup"><span data-stu-id="1dd14-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dd14-119">標頭</span><span class="sxs-lookup"><span data-stu-id="1dd14-119">Header</span></span><br/> | <dl> <span data-ttu-id="1dd14-120"><dt>Gdiplusgraphics。h</dt></span><span class="sxs-lookup"><span data-stu-id="1dd14-120"><dt>Gdiplusgraphics.h</dt></span></span> </dl> |



 

 
