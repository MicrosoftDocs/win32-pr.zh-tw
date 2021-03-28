---
description: TrueType 字型檔案包含 PANOSE 數位，可讓應用程式用來選擇與規格相符的字型。
ms.assetid: 39fd56da-c744-432d-9623-92fc7d9bf5f5
title: 使用 PANOSE 號碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dfa6a185e2afb05aec5fdf0e200300c7cf686a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194452"
---
# <a name="using-panose-numbers"></a><span data-ttu-id="81f4a-103">使用 PANOSE 號碼</span><span class="sxs-lookup"><span data-stu-id="81f4a-103">Using PANOSE Numbers</span></span>

<span data-ttu-id="81f4a-104">TrueType 字型檔案包含 PANOSE 數位，可讓應用程式用來選擇與規格相符的字型。</span><span class="sxs-lookup"><span data-stu-id="81f4a-104">TrueType font files include PANOSE numbers, which applications can use to choose a font that closely matches their specifications.</span></span> <span data-ttu-id="81f4a-105">PANOSE 系統會將臉部分類為10個不同的屬性。</span><span class="sxs-lookup"><span data-stu-id="81f4a-105">The PANOSE system classifies faces by 10 different attributes.</span></span> <span data-ttu-id="81f4a-106">如需這些屬性的詳細資訊，請參閱 [**PANOSE**](/windows/win32/api/wingdi/ns-wingdi-panose)。</span><span class="sxs-lookup"><span data-stu-id="81f4a-106">For more information about these attributes, see [**PANOSE**](/windows/win32/api/wingdi/ns-wingdi-panose).</span></span> <span data-ttu-id="81f4a-107">**PANOSE** 結構是 [**OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica)結構的一部分， (其值會藉由呼叫 [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa)函數) 來填入。</span><span class="sxs-lookup"><span data-stu-id="81f4a-107">A **PANOSE** structure is part of the [**OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) structure (whose values are filled in by calling the [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) function).</span></span>

<span data-ttu-id="81f4a-108">PANOSE 屬性會依比例個別分級。</span><span class="sxs-lookup"><span data-stu-id="81f4a-108">The PANOSE attributes are rated individually on a scale.</span></span> <span data-ttu-id="81f4a-109">產生的值會串連以產生數位。</span><span class="sxs-lookup"><span data-stu-id="81f4a-109">The resulting values are concatenated to produce a number.</span></span> <span data-ttu-id="81f4a-110">如果字型的這個數位和數學標準來測量 PANOSE 空間中的距離，應用程式可以決定最接近的相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="81f4a-110">Given this number for a font and a mathematical metric to measure distances in the PANOSE space, an application can determine the nearest neighbors.</span></span>

 

 



