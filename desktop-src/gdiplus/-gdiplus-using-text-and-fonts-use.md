---
description: Windows GDI + 提供數個類別，形成繪製文字的基礎。
ms.assetid: 12bc38c3-5fbc-4d7b-902c-92a5f5057473
title: 使用文字與字型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f28ec157888dcf45b309237eb0f7eefff17808c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511365"
---
# <a name="using-text-and-fonts"></a><span data-ttu-id="26758-103">使用文字與字型</span><span class="sxs-lookup"><span data-stu-id="26758-103">Using Text and Fonts</span></span>

<span data-ttu-id="26758-104">Windows GDI + 提供數個類別，形成繪製文字的基礎。</span><span class="sxs-lookup"><span data-stu-id="26758-104">Windows GDI+ provides several classes that form the foundation for drawing text.</span></span> <span data-ttu-id="26758-105">[**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別有數個 [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))方法，可讓您指定各種不同的文字功能，例如位置、周框、字型和格式。</span><span class="sxs-lookup"><span data-stu-id="26758-105">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class has several [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) methods that allow you to specify various features of text, such as location, bounding rectangle, font, and format.</span></span> <span data-ttu-id="26758-106">其他參與文字轉譯的類別包括 [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily)、 [**font-family**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font)、 [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)、 [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection)和 [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection)。</span><span class="sxs-lookup"><span data-stu-id="26758-106">Other classes that contribute to text rendering include [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat), [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection), and [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection).</span></span>

<span data-ttu-id="26758-107">下列主題會更詳細地涵蓋文字和字型：</span><span class="sxs-lookup"><span data-stu-id="26758-107">The following topics cover text and fonts in more detail:</span></span>

-   [<span data-ttu-id="26758-108">建立字型系列和字型</span><span class="sxs-lookup"><span data-stu-id="26758-108">Constructing Font Families and Fonts</span></span>](-gdiplus-constructing-font-families-and-fonts-use.md)
-   [<span data-ttu-id="26758-109">繪製文字</span><span class="sxs-lookup"><span data-stu-id="26758-109">Drawing Text</span></span>](-gdiplus-drawing-text-use.md)
-   [<span data-ttu-id="26758-110">格式化文字</span><span class="sxs-lookup"><span data-stu-id="26758-110">Formatting Text</span></span>](-gdiplus-formatting-text-use.md)
-   [<span data-ttu-id="26758-111">列舉已安裝的字型</span><span class="sxs-lookup"><span data-stu-id="26758-111">Enumerating Installed Fonts</span></span>](-gdiplus-enumerating-installed-fonts-use.md)
-   [<span data-ttu-id="26758-112">建立私人字型集合</span><span class="sxs-lookup"><span data-stu-id="26758-112">Creating a Private Font Collection</span></span>](-gdiplus-creating-a-private-font-collection-use.md)
-   [<span data-ttu-id="26758-113">取得字型計量</span><span class="sxs-lookup"><span data-stu-id="26758-113">Obtaining Font Metrics</span></span>](-gdiplus-obtaining-font-metrics-use.md)
-   [<span data-ttu-id="26758-114">使用文字消除鋸齒</span><span class="sxs-lookup"><span data-stu-id="26758-114">Antialiasing with Text</span></span>](-gdiplus-antialiasing-with-text-use.md)

 

 



