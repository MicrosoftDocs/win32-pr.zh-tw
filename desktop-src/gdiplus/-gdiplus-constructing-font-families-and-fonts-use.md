---
description: Windows GDI + 會將具有相同字型但樣式不同的字型組合成字型系列。
ms.assetid: 57428fae-6af4-47a5-a499-717dc378767a
title: 建立字型系列和字型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2761923847a15be6b1ad51eec0d683129b70b349
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991371"
---
# <a name="constructing-font-families-and-fonts"></a><span data-ttu-id="a33cf-103">建立字型系列和字型</span><span class="sxs-lookup"><span data-stu-id="a33cf-103">Constructing Font Families and Fonts</span></span>

<span data-ttu-id="a33cf-104">Windows GDI + 會將具有相同字型但樣式不同的字型組合成字型系列。</span><span class="sxs-lookup"><span data-stu-id="a33cf-104">Windows GDI+ groups fonts with the same typeface but different styles into font families.</span></span> <span data-ttu-id="a33cf-105">例如，Arial 字型家族包含下列字型：</span><span class="sxs-lookup"><span data-stu-id="a33cf-105">For example, the Arial font family contains the following fonts:</span></span>

-   <span data-ttu-id="a33cf-106">Arial 標準</span><span class="sxs-lookup"><span data-stu-id="a33cf-106">Arial Regular</span></span>
-   <span data-ttu-id="a33cf-107">Arial 粗體</span><span class="sxs-lookup"><span data-stu-id="a33cf-107">Arial Bold</span></span>
-   <span data-ttu-id="a33cf-108">Arial 斜體</span><span class="sxs-lookup"><span data-stu-id="a33cf-108">Arial Italic</span></span>
-   <span data-ttu-id="a33cf-109">Arial 粗體斜體</span><span class="sxs-lookup"><span data-stu-id="a33cf-109">Arial Bold Italic</span></span>

<span data-ttu-id="a33cf-110">GDI + 使用四種樣式來形成系列：標準、粗體、斜體和粗體斜體。</span><span class="sxs-lookup"><span data-stu-id="a33cf-110">GDI+ uses four styles to form families: regular, bold, italic, and bold italic.</span></span> <span data-ttu-id="a33cf-111">像 *窄* 和 *圓角* 的形容詞不會被視為樣式;它們是系列名稱的一部分。</span><span class="sxs-lookup"><span data-stu-id="a33cf-111">Adjectives such as *narrow* and *rounded* are not considered styles; rather they are part of the family name.</span></span> <span data-ttu-id="a33cf-112">例如，Arial 窄是一種字型家族，其成員如下所示：</span><span class="sxs-lookup"><span data-stu-id="a33cf-112">For example, Arial Narrow is a font family whose members are the following:</span></span>

-   <span data-ttu-id="a33cf-113">Arial 窄的一般</span><span class="sxs-lookup"><span data-stu-id="a33cf-113">Arial Narrow Regular</span></span>
-   <span data-ttu-id="a33cf-114">Arial 窄粗體</span><span class="sxs-lookup"><span data-stu-id="a33cf-114">Arial Narrow Bold</span></span>
-   <span data-ttu-id="a33cf-115">Arial 窄斜體</span><span class="sxs-lookup"><span data-stu-id="a33cf-115">Arial Narrow Italic</span></span>
-   <span data-ttu-id="a33cf-116">Arial 窄粗體斜體</span><span class="sxs-lookup"><span data-stu-id="a33cf-116">Arial Narrow Bold Italic</span></span>

<span data-ttu-id="a33cf-117">您必須先建立 [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) 物件和 [**字型**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) 物件，才能使用 gdi + 來繪製文字。</span><span class="sxs-lookup"><span data-stu-id="a33cf-117">Before you can draw text with GDI+, you need to construct a [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object and a [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object.</span></span> <span data-ttu-id="a33cf-118">**FontFamily** 物件會指定字型 (例如，Arial) ，而 **字型** 物件則指定大小、樣式和單位。</span><span class="sxs-lookup"><span data-stu-id="a33cf-118">The **FontFamily** objects specifies the typeface (for example, Arial), and the **Font** object specifies the size, style, and units.</span></span>

<span data-ttu-id="a33cf-119">下列範例會建立大小為16圖元的一般樣式 Arial 字型：</span><span class="sxs-lookup"><span data-stu-id="a33cf-119">The following example constructs a regular style Arial font with a size of 16 pixels:</span></span>


```
FontFamily fontFamily(L"Arial");
Font font(&fontFamily, 16, FontStyleRegular, UnitPixel);
            
```



<span data-ttu-id="a33cf-120">在上述程式碼中，傳遞至 [**字型**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) 函式的第一個引數是 [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) 物件的位址。</span><span class="sxs-lookup"><span data-stu-id="a33cf-120">In the preceding code, the first argument passed to the [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) constructor is the address of the [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object.</span></span> <span data-ttu-id="a33cf-121">第二個引數會指定以第四個引數所識別的單位來測量的字型大小。</span><span class="sxs-lookup"><span data-stu-id="a33cf-121">The second argument specifies the size of the font measured in units identified by the fourth argument.</span></span> <span data-ttu-id="a33cf-122">第三個引數會識別樣式。</span><span class="sxs-lookup"><span data-stu-id="a33cf-122">The third argument identifies the style.</span></span>

<span data-ttu-id="a33cf-123">[\* \* \* \* UnitPixel \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-unit) \* 是 **單位** 列舉的成員，而 [\* \* \* \* FontStyleRegular \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-fontstyle) \* 是 **FontStyle** 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="a33cf-123">[\*\*\*\*UnitPixel\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-unit) is a member of the **Unit** enumeration, and [\*\*\*\*FontStyleRegular\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-fontstyle) is a member of the **FontStyle** enumeration.</span></span> <span data-ttu-id="a33cf-124">這兩個列舉都是在 Gdiplusenums 中宣告。</span><span class="sxs-lookup"><span data-stu-id="a33cf-124">Both enumerations are declared in Gdiplusenums.h.</span></span>

 

 



