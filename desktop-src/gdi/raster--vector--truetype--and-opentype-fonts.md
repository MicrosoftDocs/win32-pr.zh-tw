---
description: 點陣、向量、TrueType 和 OpenType 字型
ms.assetid: 4fe98f04-3fb0-4a03-86c3-d0ea6f07f8f0
title: 點陣、向量、TrueType 和 OpenType 字型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9b4be20ac7d02075fcd5c6cdbefe9eb516ea21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991179"
---
# <a name="raster-vector-truetype-and-opentype-fonts"></a><span data-ttu-id="f1132-103">點陣、向量、TrueType 和 OpenType 字型</span><span class="sxs-lookup"><span data-stu-id="f1132-103">Raster, Vector, TrueType, and OpenType Fonts</span></span>

<span data-ttu-id="f1132-104">應用程式可以使用四種不同的字型技術來顯示和列印文字：</span><span class="sxs-lookup"><span data-stu-id="f1132-104">Applications can use four different kinds of font technologies to display and print text:</span></span>

-   <span data-ttu-id="f1132-105">光柵</span><span class="sxs-lookup"><span data-stu-id="f1132-105">Raster</span></span>
-   <span data-ttu-id="f1132-106">向量</span><span class="sxs-lookup"><span data-stu-id="f1132-106">Vector</span></span>
-   <span data-ttu-id="f1132-107">TrueType</span><span class="sxs-lookup"><span data-stu-id="f1132-107">TrueType</span></span>
-   <span data-ttu-id="f1132-108">Microsoft OpenType</span><span class="sxs-lookup"><span data-stu-id="f1132-108">Microsoft OpenType</span></span>

<span data-ttu-id="f1132-109">這些字型之間的差異反映了每個字元或 *符號的圖像* 儲存在個別字型資源檔中的方式：</span><span class="sxs-lookup"><span data-stu-id="f1132-109">The differences between these fonts reflect the way that the *glyph* for each character or symbol is stored in the respective font-resource file:</span></span>

-   <span data-ttu-id="f1132-110">在點陣字型中，圖像是系統用來在字型中繪製單一字元或符號的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="f1132-110">In raster fonts, a glyph is a bitmap that the system uses to draw a single character or symbol in the font.</span></span>
-   <span data-ttu-id="f1132-111">在向量字型中，圖像是線條端點的集合，可定義系統用來在字型中繪製字元或符號的線段。</span><span class="sxs-lookup"><span data-stu-id="f1132-111">In vector fonts, a glyph is a collection of line endpoints that define the line segments that the system uses to draw a character or symbol in the font.</span></span>
-   <span data-ttu-id="f1132-112">在 TrueType 和 OpenType 字型中，圖像是線條和曲線命令的集合，以及提示的集合。</span><span class="sxs-lookup"><span data-stu-id="f1132-112">In TrueType and OpenType fonts, a glyph is a collection of line and curve commands as well as a collection of hints.</span></span>

<span data-ttu-id="f1132-113">系統會使用 line 和 curve 命令，為 TrueType 或 Microsoft OpenType 字型中的字元或符號定義點陣圖的外框。</span><span class="sxs-lookup"><span data-stu-id="f1132-113">The system uses the line and curve commands to define the outline of the bitmap for a character or symbol in the TrueType or Microsoft OpenType font.</span></span> <span data-ttu-id="f1132-114">系統會使用提示來調整用來繪製字元或符號之曲線的線條和圖形長度。</span><span class="sxs-lookup"><span data-stu-id="f1132-114">The system uses the hints to adjust the length of the lines and shapes of the curves used to draw the character or symbol.</span></span> <span data-ttu-id="f1132-115">這些提示和個別的調整是根據用來減少或增加點陣圖大小的縮放量。</span><span class="sxs-lookup"><span data-stu-id="f1132-115">These hints and the respective adjustments are based on the amount of scaling used to reduce or increase the size of the bitmap.</span></span> <span data-ttu-id="f1132-116">OpenType 字型相當於 TrueType 字型，不同之處在于 OpenType 字型除了 TrueType 圖像定義之外，還允許 PostScript 圖像定義。</span><span class="sxs-lookup"><span data-stu-id="f1132-116">An OpenType font is equivalent to a TrueType font except that an OpenType font allows PostScript glyph definitions in addition to TrueType glyph definitions.</span></span>

<span data-ttu-id="f1132-117">由於點陣字型中每個字元的點陣圖都是針對特定的裝置解析度所設計，因此，通常會將點陣字型視為裝置相依。</span><span class="sxs-lookup"><span data-stu-id="f1132-117">Because the bitmaps for each glyph in a raster font are designed for a specific resolution of device, raster fonts are generally considered to be device dependent.</span></span> <span data-ttu-id="f1132-118">相反地，向量字型與裝置無關，因為每個圖像都會儲存為可擴充行的集合。</span><span class="sxs-lookup"><span data-stu-id="f1132-118">Vector fonts, on the other hand, are not device dependent, because each glyph is stored as a collection of scalable lines.</span></span> <span data-ttu-id="f1132-119">不過，向量字型的繪製速度通常比點陣或 TrueType 和 OpenType 字型更慢。</span><span class="sxs-lookup"><span data-stu-id="f1132-119">However, vector fonts are generally drawn more slowly than raster or TrueType and OpenType fonts.</span></span> <span data-ttu-id="f1132-120">TrueType 和 OpenType 字型提供相對快速的繪圖速度和真正的裝置獨立性。</span><span class="sxs-lookup"><span data-stu-id="f1132-120">TrueType and OpenType fonts provide both relatively fast drawing speed and true device independence.</span></span> <span data-ttu-id="f1132-121">藉由使用與圖像相關聯的提示，開發人員可以將 TrueType 或 OpenType 字型的字元向上或向下調整，並仍維持其原始圖形。</span><span class="sxs-lookup"><span data-stu-id="f1132-121">By using the hints associated with a glyph, a developer can scale the characters from a TrueType or OpenType font up or down and still maintain their original shape.</span></span>

<span data-ttu-id="f1132-122">如先前所述，字型的字元會儲存在字型資源檔中。</span><span class="sxs-lookup"><span data-stu-id="f1132-122">As previously mentioned, the glyphs for a font are stored in a font-resource file.</span></span> <span data-ttu-id="f1132-123">字型資源檔實際上是包含資料的 DLL，沒有任何程式碼。</span><span class="sxs-lookup"><span data-stu-id="f1132-123">A font-resource file is actually a DLL that contains only data, there is no code.</span></span> <span data-ttu-id="f1132-124">針對點陣和向量字型，此資料分為兩個部分：描述字型計量和字元資料的標頭。</span><span class="sxs-lookup"><span data-stu-id="f1132-124">For raster and vector fonts, this data is divided into two parts: a header describing the font's metrics and the glyph data.</span></span> <span data-ttu-id="f1132-125">點陣或向量字型的字型資源檔是以 fon 副檔名來識別。</span><span class="sxs-lookup"><span data-stu-id="f1132-125">A font-resource file for a raster or vector font is identified by the .fon file name extension.</span></span> <span data-ttu-id="f1132-126">針對 TrueType 和 OpenType 字型，每個字型都有兩個檔案：第一個檔案包含相對較短的標頭，而第二個則包含實際的字型資料。</span><span class="sxs-lookup"><span data-stu-id="f1132-126">For TrueType and OpenType fonts, there are two files for each font: the first file contains a relatively short header and the second contains the actual font data.</span></span> <span data-ttu-id="f1132-127">第一個檔案是以受副檔名來識別，而第二個檔案則是以 ttf 副檔名來識別。</span><span class="sxs-lookup"><span data-stu-id="f1132-127">The first file is identified by an .fot extension and the second is identified by a .ttf extension.</span></span>

 

 



