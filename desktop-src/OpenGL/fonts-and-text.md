---
title: '字體和文字 (OpenGL) '
description: Microsoft 在 Windows 中執行 OpenGL 在單一緩衝的 OpenGL 視窗中支援 GDI 圖形。
ms.assetid: 25a45e1a-6c1e-416b-8993-daeefc1100f3
keywords:
- Windows 上的 OpenGL，字型
- Windows 上的 OpenGL，文字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fba4ffe996bd88a6285f615ddacb31e57fc311
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383665"
---
# <a name="fonts-and-text-opengl"></a><span data-ttu-id="26f7e-105">字體和文字 (OpenGL) </span><span class="sxs-lookup"><span data-stu-id="26f7e-105">Fonts and Text (OpenGL)</span></span>

<span data-ttu-id="26f7e-106">Microsoft 在 Windows 中執行 OpenGL 在單一緩衝的 OpenGL 視窗中支援 GDI 圖形。</span><span class="sxs-lookup"><span data-stu-id="26f7e-106">Microsoft's implementation of OpenGL in Windows supports GDI graphics in a single-buffered OpenGL window.</span></span> <span data-ttu-id="26f7e-107">它不支援雙緩衝 OpenGL 視窗中的 GDI 圖形。</span><span class="sxs-lookup"><span data-stu-id="26f7e-107">It does not support GDI graphics in a double-buffered OpenGL window.</span></span> <span data-ttu-id="26f7e-108">因此，您只能呼叫標準 GDI 字型和文字函式，以在單一緩衝的 OpenGL 視窗中繪製文字;您無法呼叫這些函式，以在雙重緩衝的 OpenGL 視窗中繪製文字。</span><span class="sxs-lookup"><span data-stu-id="26f7e-108">Thus, you can call only the standard GDI font and text functions to draw text in a single-buffered OpenGL window; you cannot call those functions to draw text in a double-buffered OpenGL window.</span></span>

<span data-ttu-id="26f7e-109">這項限制對於雙重緩衝視窗中的文字有因應措施：建立字元點陣圖影像的 OpenGL 顯示清單，然後執行這些顯示清單來繪製字元。</span><span class="sxs-lookup"><span data-stu-id="26f7e-109">There is a workaround for this restriction on text in double-buffered windows: build OpenGL display lists for bitmap images of characters, and then execute those display lists to draw characters.</span></span> <span data-ttu-id="26f7e-110">此程式有三個主要步驟：</span><span class="sxs-lookup"><span data-stu-id="26f7e-110">There are three main steps in this process:</span></span>

1.  <span data-ttu-id="26f7e-111">選取裝置內容的字型，並視需要設定字型的屬性。</span><span class="sxs-lookup"><span data-stu-id="26f7e-111">Select a font for a device context, setting the font's properties as desired.</span></span>
2.  <span data-ttu-id="26f7e-112">根據裝置內容字型中的字元，建立一組點陣圖顯示清單，應用程式將繪製的每個圖像都有一個顯示清單。</span><span class="sxs-lookup"><span data-stu-id="26f7e-112">Create a set of bitmap display lists based on the glyphs in the device context's font, one display list for each glyph that the application will draw.</span></span>
3.  <span data-ttu-id="26f7e-113">使用這些點陣圖顯示清單，在字串中繪製每個字元。</span><span class="sxs-lookup"><span data-stu-id="26f7e-113">Draw each glyph in a string, using those bitmap display lists.</span></span>

<span data-ttu-id="26f7e-114">若要建立顯示清單，請呼叫 [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) 和 [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) 函數。</span><span class="sxs-lookup"><span data-stu-id="26f7e-114">To create the display lists, call the [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) and [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) functions.</span></span> <span data-ttu-id="26f7e-115">若要使用這些顯示清單來繪製字串中的字元，請呼叫 [**glCallLists**](glcalllists.md)。</span><span class="sxs-lookup"><span data-stu-id="26f7e-115">To draw characters in a string using those display lists, call [**glCallLists**](glcalllists.md).</span></span>

<span data-ttu-id="26f7e-116">若要建立容易當地語系化的應用程式，並謹慎使用資源，必須小心地管理這些圖像顯示清單的建立和儲存。</span><span class="sxs-lookup"><span data-stu-id="26f7e-116">To create applications that are easy to localize and that use resources sparingly, the creation and storage of these glyph image display lists must be managed carefully.</span></span> <span data-ttu-id="26f7e-117">不同于英文的許多語言都有字母，其字元碼範圍會超過相當大的值集。</span><span class="sxs-lookup"><span data-stu-id="26f7e-117">Many languages, unlike English, have alphabets whose character codes range over a relatively large set of values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26f7e-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="26f7e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26f7e-119">字型和文字函數</span><span class="sxs-lookup"><span data-stu-id="26f7e-119">Font and Text Functions</span></span>](font-and-text-functions.md)
</dt> </dl>

 

 




