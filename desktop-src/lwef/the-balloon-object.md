---
title: 球形球形物件
description: 球形球形物件
ms.assetid: d5b52310-0b4e-4fe3-a481-53687be4a89c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de0c94803e9efadde1ae4a8410273ed49437291a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104185635"
---
# <a name="the-balloon-object"></a><span data-ttu-id="b344a-103">球形球形物件</span><span class="sxs-lookup"><span data-stu-id="b344a-103">The Balloon Object</span></span>

<span data-ttu-id="b344a-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="b344a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="b344a-105">Microsoft Agent 支援使用卡通文字氣球的 [**語音**](speak-method.md) 方法文字字幕。</span><span class="sxs-lookup"><span data-stu-id="b344a-105">Microsoft Agent supports textual captioning of [**Speak**](speak-method.md) method using a cartoon word balloon.</span></span> <span data-ttu-id="b344a-106">「 [**思考**](think-method.md) 」方法可讓您在「想像」的文字氣球中顯示沒有音訊輸出的文字。</span><span class="sxs-lookup"><span data-stu-id="b344a-106">The [**Think**](think-method.md) method enables you to display text without audio output in a "thought" word balloon.</span></span>

<span data-ttu-id="b344a-107">字元的初始文字氣球視窗預設值會在 Microsoft Agent 字元編輯器中定義和編譯。</span><span class="sxs-lookup"><span data-stu-id="b344a-107">A character's initial word balloon window defaults are defined and compiled in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="b344a-108">執行之後，使用者可以覆寫氣球的 [**啟用**](enabled-property.md) 和 [**字型**](https://www.bing.com/search?q=**Font**) 屬性。</span><span class="sxs-lookup"><span data-stu-id="b344a-108">Once running, the balloon's [**Enabled**](enabled-property.md) and [**Font**](https://www.bing.com/search?q=**Font**) properties may be overridden by the user.</span></span> <span data-ttu-id="b344a-109">如果使用者變更文字氣球的屬性，則會影響所有字元。</span><span class="sxs-lookup"><span data-stu-id="b344a-109">If a user changes the word balloon's properties, they affect all characters.</span></span> <span data-ttu-id="b344a-110">「 [**說話**](speak-method.md) 」和「 [**想法**](think-method.md) 」兩個字提示都使用相同的「大小」屬性設定。</span><span class="sxs-lookup"><span data-stu-id="b344a-110">Both the [**Speak**](speak-method.md) and [**Think**](think-method.md) word balloons use the same property settings for size.</span></span> <span data-ttu-id="b344a-111">您可以透過 [**球形球形**](/windows/desktop/lwef/the-balloon-object) 物件（即 [**字元**](/windows/desktop/lwef/the-characters-object) 物件的子系）來存取字元的字組批註的屬性。</span><span class="sxs-lookup"><span data-stu-id="b344a-111">You can access the properties for a character's word balloon through the [**Balloon**](/windows/desktop/lwef/the-balloon-object) object, which is a child of the [**Character**](/windows/desktop/lwef/the-characters-object) object.</span></span>

<span data-ttu-id="b344a-112">[**球形球形**](/windows/desktop/lwef/the-balloon-object)物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="b344a-112">The [**Balloon**](/windows/desktop/lwef/the-balloon-object) object supports the following properties:</span></span>

-   [<span data-ttu-id="b344a-113">**顏色**</span><span class="sxs-lookup"><span data-stu-id="b344a-113">**BackColor**</span></span>](backcolor-property.md)
-   [<span data-ttu-id="b344a-114">**BorderColor**</span><span class="sxs-lookup"><span data-stu-id="b344a-114">**BorderColor**</span></span>](bordercolor-property.md)
-   [<span data-ttu-id="b344a-115">**CharsPerLine**</span><span class="sxs-lookup"><span data-stu-id="b344a-115">**CharsPerLine**</span></span>](charsperline-property.md)
-   [<span data-ttu-id="b344a-116">**啟用**</span><span class="sxs-lookup"><span data-stu-id="b344a-116">**Enabled**</span></span>](enabled-property.md)
-   [<span data-ttu-id="b344a-117">**FontCharSet**</span><span class="sxs-lookup"><span data-stu-id="b344a-117">**FontCharSet**</span></span>](fontcharset-property.md)
-   [<span data-ttu-id="b344a-118">**FontName**</span><span class="sxs-lookup"><span data-stu-id="b344a-118">**FontName**</span></span>](fontname-property-bal.md)
-   [<span data-ttu-id="b344a-119">**FontBold**</span><span class="sxs-lookup"><span data-stu-id="b344a-119">**FontBold**</span></span>](fontbold-property.md)
-   [<span data-ttu-id="b344a-120">**FontItalic**</span><span class="sxs-lookup"><span data-stu-id="b344a-120">**FontItalic**</span></span>](fontitalic-property.md)
-   [<span data-ttu-id="b344a-121">**FontSize**</span><span class="sxs-lookup"><span data-stu-id="b344a-121">**FontSize**</span></span>](fontsize-property-bal.md)
-   [<span data-ttu-id="b344a-122">**FontStrikeThru**</span><span class="sxs-lookup"><span data-stu-id="b344a-122">**FontStrikeThru**</span></span>](fontstrikethru-property.md)
-   [<span data-ttu-id="b344a-123">**FontUnderline**</span><span class="sxs-lookup"><span data-stu-id="b344a-123">**FontUnderline**</span></span>](fontunderline-property.md)
-   [<span data-ttu-id="b344a-124">**ForeColor**</span><span class="sxs-lookup"><span data-stu-id="b344a-124">**ForeColor**</span></span>](forecolor-property.md)
-   [<span data-ttu-id="b344a-125">**NumberOfLines**</span><span class="sxs-lookup"><span data-stu-id="b344a-125">**NumberOfLines**</span></span>](numberoflines-property.md)
-   [<span data-ttu-id="b344a-126">**風格**</span><span class="sxs-lookup"><span data-stu-id="b344a-126">**Style**</span></span>](style-property.md)
-   [<span data-ttu-id="b344a-127">**可見**</span><span class="sxs-lookup"><span data-stu-id="b344a-127">**Visible**</span></span>](visible-property-bal.md)

 

 