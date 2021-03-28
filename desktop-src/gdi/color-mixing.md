---
description: 色彩混合可讓應用程式藉由結合畫筆或筆刷色彩與現有影像中的色彩來建立新的色彩。
ms.assetid: 4a5dff8c-f75f-41d2-8367-33d97d4fd010
title: 色彩混合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa85f6ea449fa13f7b7120160915ea72a0e3dd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114697"
---
# <a name="color-mixing"></a><span data-ttu-id="c0d6b-103">色彩混合</span><span class="sxs-lookup"><span data-stu-id="c0d6b-103">Color Mixing</span></span>

<span data-ttu-id="c0d6b-104">色彩混合可讓應用程式藉由結合畫筆或筆刷色彩與現有影像中的色彩來建立新的色彩。</span><span class="sxs-lookup"><span data-stu-id="c0d6b-104">Color mixing lets an application create new colors by combining the pen or brush color with colors in the existing image.</span></span> <span data-ttu-id="c0d6b-105">應用程式可以選擇繪製畫筆或筆刷色彩， (有效地繪製任何現有的影像) 或混搭色彩與已存在的色彩。</span><span class="sxs-lookup"><span data-stu-id="c0d6b-105">The application can choose either to draw the pen or brush color as is (effectively drawing over any existing image) or to mix the color with the colors already present.</span></span>

<span data-ttu-id="c0d6b-106">前景混合模式（有時稱為二元點陣運算）會決定如何混合這些色彩。</span><span class="sxs-lookup"><span data-stu-id="c0d6b-106">The foreground mix mode, sometimes called the binary raster operation, determines how these colors are mixed.</span></span> <span data-ttu-id="c0d6b-107">應用程式可以合併色彩，同時保留兩種色彩的所有元件;遮罩色彩、移除或仲裁不常見的元件;或單獨遮罩色彩，移除或仲裁常見的元件。</span><span class="sxs-lookup"><span data-stu-id="c0d6b-107">An application can merge colors, preserving all components of both colors; mask colors, removing or moderating components that are not common; or exclusively mask colors, removing or moderating components that are common.</span></span> <span data-ttu-id="c0d6b-108">這些基本混合作業有幾種變化。</span><span class="sxs-lookup"><span data-stu-id="c0d6b-108">There are several variations on these basic mixing operations.</span></span>

<span data-ttu-id="c0d6b-109">色彩混合會受限於色彩近似值。</span><span class="sxs-lookup"><span data-stu-id="c0d6b-109">Color mixing is subject to color approximation.</span></span> <span data-ttu-id="c0d6b-110">如果色彩混合的結果是裝置無法產生的色彩，系統就會使用它可以產生的色彩來接近結果。</span><span class="sxs-lookup"><span data-stu-id="c0d6b-110">If the result of color mixing is a color that the device cannot generate, the system approximates the result, using a color it can generate.</span></span> <span data-ttu-id="c0d6b-111">如果應用程式混合遞色色彩，則會混合用來建立遞色色彩的個別色彩，且結果會受限於色彩近似值。</span><span class="sxs-lookup"><span data-stu-id="c0d6b-111">If an application mixes dithered colors, the individual colors used to create the dithered color are mixed, and the results are subject to color approximation.</span></span>

<span data-ttu-id="c0d6b-112">應用程式會使用 [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) 函數來設定前景混合模式，並使用 [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) 函數來抓取目前的模式。</span><span class="sxs-lookup"><span data-stu-id="c0d6b-112">An application sets the foreground mix mode by using the [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) function and retrieves the current mode by using the [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) function.</span></span>

<span data-ttu-id="c0d6b-113">雖然有背景混合模式，但該模式不會控制色彩的混合。</span><span class="sxs-lookup"><span data-stu-id="c0d6b-113">Although there is a background mix mode, that mode does not control the mixing of colors.</span></span> <span data-ttu-id="c0d6b-114">相反地，它會指定繪製樣式線條、影線筆刷和文字時，是否要使用背景色彩。</span><span class="sxs-lookup"><span data-stu-id="c0d6b-114">Instead, it specifies whether a background color is used when drawing styled lines, hatched brushes, and text.</span></span>

 

 



