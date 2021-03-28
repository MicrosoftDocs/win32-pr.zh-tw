---
description: Windows GDI + 提供各種品質層級來繪製文字。 通常，高品質轉譯所需的處理時間比較低的品質呈現更多。
ms.assetid: 780d97ec-f446-4d19-837f-517a7d6dd27d
title: 使用文字消除鋸齒
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24c7b7c59a436db6c16251aa8e866648eed5cc51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991454"
---
# <a name="antialiasing-with-text"></a><span data-ttu-id="013c9-104">使用文字消除鋸齒</span><span class="sxs-lookup"><span data-stu-id="013c9-104">Antialiasing with Text</span></span>

<span data-ttu-id="013c9-105">Windows GDI + 提供各種品質層級來繪製文字。</span><span class="sxs-lookup"><span data-stu-id="013c9-105">Windows GDI+ provides various quality levels for drawing text.</span></span> <span data-ttu-id="013c9-106">通常，高品質轉譯所需的處理時間比較低的品質呈現更多。</span><span class="sxs-lookup"><span data-stu-id="013c9-106">Typically, higher quality rendering takes more processing time than lower quality rendering.</span></span>

<span data-ttu-id="013c9-107">品質層級是 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 類別的屬性。</span><span class="sxs-lookup"><span data-stu-id="013c9-107">The quality level is a property of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="013c9-108">若要設定品質層級，請呼叫 **圖形** 物件的 [**Graphics：： SetTextRenderingHint**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint)方法。</span><span class="sxs-lookup"><span data-stu-id="013c9-108">To set the quality level, call the [**Graphics::SetTextRenderingHint**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) method of a **Graphics** object.</span></span> <span data-ttu-id="013c9-109">**Graphics：： SetTextRenderingHint** 方法會接收 [**TextRenderingHint**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)列舉的其中一個元素，而該專案是在 Gdiplusenums 中宣告的。</span><span class="sxs-lookup"><span data-stu-id="013c9-109">The **Graphics::SetTextRenderingHint** method receives one of the elements of the [**TextRenderingHint**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint) enumeration, which is declared in Gdiplusenums.h.</span></span>

<span data-ttu-id="013c9-110">GDI + 提供傳統的消除鋸齒功能，以及以 Microsoft ClearType 顯示器技術為基礎的一種新的消除鋸齒功能，僅適用于 Windows XP 和 Windows Server 2003 和更新版本的 Windows。</span><span class="sxs-lookup"><span data-stu-id="013c9-110">GDI+ provides traditional antialiasing and a new kind of antialiasing based on Microsoft ClearType display technology only available on Windows XP and Windows Server 2003 and later versions of Windows.</span></span> <span data-ttu-id="013c9-111">ClearType 凹凸貼圖改進了具有數位介面（例如膝上型電腦中的監視器和高品質的一般桌面顯示器）之彩色 LCD 監視器的可讀性。</span><span class="sxs-lookup"><span data-stu-id="013c9-111">ClearType smoothing improves readability on color LCD monitors that have a digital interface, such as the monitors in laptops and high-quality flat desktop displays.</span></span> <span data-ttu-id="013c9-112">CRT 螢幕的可讀性也稍微改進。</span><span class="sxs-lookup"><span data-stu-id="013c9-112">Readability on CRT screens is also somewhat improved.</span></span>

<span data-ttu-id="013c9-113">ClearType 取決於 LCD 條紋的方向和順序。</span><span class="sxs-lookup"><span data-stu-id="013c9-113">ClearType is dependent on the orientation and ordering of the LCD stripes.</span></span> <span data-ttu-id="013c9-114">目前，ClearType 僅針對以 RGB 排序的分隔號紋執行。</span><span class="sxs-lookup"><span data-stu-id="013c9-114">Currently, ClearType is implemented only for vertical stripes that are ordered RGB.</span></span> <span data-ttu-id="013c9-115">如果您使用 tablet PC，可以在任何方向導向顯示器，或是使用可從橫向轉換成直向的螢幕時，這可能是一項考慮。</span><span class="sxs-lookup"><span data-stu-id="013c9-115">This might be a concern if you are using a tablet PC, where the display can be oriented in any direction, or if you are using a screen that can be turned from landscape to portrait.</span></span>

<span data-ttu-id="013c9-116">下列範例會以兩種不同的品質設定來繪製文字：</span><span class="sxs-lookup"><span data-stu-id="013c9-116">The following example draws text with two different quality settings:</span></span>


```
FontFamily  fontFamily(L"Times New Roman");
Font        font(&fontFamily, 32, FontStyleRegular, UnitPixel);
SolidBrush  solidBrush(Color(255, 0, 0, 255));
WCHAR       string1[] = L"SingleBitPerPixel";
WCHAR       string2[] = L"AntiAlias";

graphics.SetTextRenderingHint(TextRenderingHintSingleBitPerPixel);
graphics.DrawString(string1, -1, &font, PointF(10.0f, 10.0f), &solidBrush);

graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
graphics.DrawString(string2, -1, &font, PointF(10.0f, 60.0f), &solidBrush);
            
```



<span data-ttu-id="013c9-117">下圖顯示上述程式碼的輸出。</span><span class="sxs-lookup"><span data-stu-id="013c9-117">The following illustration shows the output of the preceding code.</span></span>

![字串的螢幕擷取畫面，其中的字元與平滑邊緣的字元具有不規則邊緣對比](images/fontstext10.png)

 

 



