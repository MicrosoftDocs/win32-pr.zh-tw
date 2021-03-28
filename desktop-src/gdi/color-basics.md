---
description: 裝置的色彩功能（例如顯示器和印表機）可以範圍從單色到數千種色彩。
ms.assetid: 3d71c24c-77f4-4344-91c3-439052402fae
title: 色彩基本知識
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 992953bef75b2bab1f33dbd044a9c80387b5ccd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191955"
---
# <a name="color-basics"></a><span data-ttu-id="0115b-103">色彩基本知識</span><span class="sxs-lookup"><span data-stu-id="0115b-103">Color Basics</span></span>

<span data-ttu-id="0115b-104">裝置的色彩功能（例如顯示器和印表機）可以範圍從單色到數千種色彩。</span><span class="sxs-lookup"><span data-stu-id="0115b-104">The color capabilities of devices, such as displays and printers, can range from monochrome to thousands of colors.</span></span> <span data-ttu-id="0115b-105">由於應用程式可能需要在此範圍內產生裝置的輸出，因此應該準備好處理不同的色彩功能。</span><span class="sxs-lookup"><span data-stu-id="0115b-105">Because an application may need to generate output for devices throughout this range, it should be prepared to handle varying color capabilities.</span></span>

<span data-ttu-id="0115b-106">應用程式可以使用 [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) 函式來取得 NUMCOLORS 值，以探索指定裝置可用的色彩數目。</span><span class="sxs-lookup"><span data-stu-id="0115b-106">An application can discover the number of colors available for a given device by using the [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function to retrieve the NUMCOLORS value.</span></span> <span data-ttu-id="0115b-107">此值會指定應用程式可使用的色彩計數。</span><span class="sxs-lookup"><span data-stu-id="0115b-107">This value specifies the count of colors available for use by the application.</span></span> <span data-ttu-id="0115b-108">此計數通常會對應至輸出裝置的實體屬性，例如印表機中的墨水數目，或顯示器介面卡可以傳輸至監視器的相異色彩信號數目。</span><span class="sxs-lookup"><span data-stu-id="0115b-108">Usually, this count corresponds to a physical property of the output device, such as the number of inks in the printer or the number of distinct color signals the display adapter can transmit to the monitor.</span></span>

<span data-ttu-id="0115b-109">雖然 NUMCOLORS 值會指定色彩的計數，但並不會識別可用的色彩。</span><span class="sxs-lookup"><span data-stu-id="0115b-109">Although the NUMCOLORS value specifies the count of colors, it does not identify what the available colors are.</span></span> <span data-ttu-id="0115b-110">應用程式可以藉由列舉所有具有 PS 固態類型的畫筆來探索可用的色彩 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0115b-110">An application can discover what colors are available by enumerating all pens having the PS\_SOLID type.</span></span> <span data-ttu-id="0115b-111">因為支援指定裝置的設備磁碟機通常會有完整範圍的純色，而且因為系統要求實心畫筆只有裝置可以產生的色彩，所以列舉這些畫筆通常相當於列舉色彩。</span><span class="sxs-lookup"><span data-stu-id="0115b-111">Because the device driver that supports a given device usually has a full range of solid pens and because the system requires that solid pens have only colors that the device can generate, enumerating these pens is often equivalent to enumerating the colors.</span></span> <span data-ttu-id="0115b-112">應用程式可以使用 [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) 函數來列舉畫筆。</span><span class="sxs-lookup"><span data-stu-id="0115b-112">An application can enumerate the pens by using the [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) function.</span></span> <span data-ttu-id="0115b-113">如需程式碼範例，請參閱 [列舉色彩](enumerating-colors.md)。</span><span class="sxs-lookup"><span data-stu-id="0115b-113">For a code example, see [Enumerating Colors](enumerating-colors.md).</span></span>

<span data-ttu-id="0115b-114">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="0115b-114">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="0115b-115">色彩值</span><span class="sxs-lookup"><span data-stu-id="0115b-115">Color Values</span></span>](color-values.md)
-   [<span data-ttu-id="0115b-116">色彩近似值和遞色</span><span class="sxs-lookup"><span data-stu-id="0115b-116">Color Approximations and Dithering</span></span>](color-approximations-and-dithering.md)
-   [<span data-ttu-id="0115b-117">點陣圖中的色彩</span><span class="sxs-lookup"><span data-stu-id="0115b-117">Color in Bitmaps</span></span>](color-in-bitmaps.md)
-   [<span data-ttu-id="0115b-118">色彩混合</span><span class="sxs-lookup"><span data-stu-id="0115b-118">Color Mixing</span></span>](color-mixing.md)

 

 



