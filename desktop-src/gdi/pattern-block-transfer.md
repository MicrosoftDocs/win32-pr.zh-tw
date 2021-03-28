---
description: PatBlt 函式的名稱 (模式區區塊轉送的縮寫) 表示此函式只會在填滿指定的矩形之前，複寫筆刷 (或模式) 。
ms.assetid: 601e1e79-a328-4e63-958a-ca26129e03f8
title: 模式區塊傳輸
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54424348c28b83d1d0d1075072e80b18049546ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991190"
---
# <a name="pattern-block-transfer"></a><span data-ttu-id="20e14-103">模式區塊傳輸</span><span class="sxs-lookup"><span data-stu-id="20e14-103">Pattern Block Transfer</span></span>

<span data-ttu-id="20e14-104">[**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt)函式的名稱 (模式區區塊轉送的縮寫) 表示此函式只會在填滿指定的矩形之前，複寫筆刷 (或模式) 。</span><span class="sxs-lookup"><span data-stu-id="20e14-104">The name of the [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) function (an abbreviation for pattern block transfer) implies that this function simply replicates the brush (or pattern) until it fills a specified rectangle.</span></span> <span data-ttu-id="20e14-105">不過，函式的功能其實更強大。</span><span class="sxs-lookup"><span data-stu-id="20e14-105">However, the function is actually much more powerful.</span></span> <span data-ttu-id="20e14-106">在複寫筆刷之前，它會使用點陣作業 (ROP) ，將模式的色彩資料與影片顯示器上現有圖元的色彩資料合併。</span><span class="sxs-lookup"><span data-stu-id="20e14-106">Before replicating the brush, it combines the color data for the pattern with the color data for the existing pixels on the video display by using a raster operation (ROP).</span></span> <span data-ttu-id="20e14-107">ROP 是位運算，適用于複寫筆刷的色彩資料位，以及顯示裝置上目標矩形的色彩資料位。</span><span class="sxs-lookup"><span data-stu-id="20e14-107">An ROP is a bitwise operation that is applied to the bits of color data for the replicated brush and the bits of color data for the target rectangle on the display device.</span></span> <span data-ttu-id="20e14-108">有 256 ROPs;不過， **PatBlt** 函式只會辨識出需要模式和目的地 (不是需要來源) 的函式。</span><span class="sxs-lookup"><span data-stu-id="20e14-108">There are 256 ROPs; however, the **PatBlt** function recognizes only those that require a pattern and a destination (not those that require a source).</span></span> <span data-ttu-id="20e14-109">下表指出最常見的 ROPs。</span><span class="sxs-lookup"><span data-stu-id="20e14-109">The following table identifies the most common ROPs.</span></span>



| <span data-ttu-id="20e14-110">人事 登記</span><span class="sxs-lookup"><span data-stu-id="20e14-110">ROP</span></span>       | <span data-ttu-id="20e14-111">Description</span><span class="sxs-lookup"><span data-stu-id="20e14-111">Description</span></span>                                                                         |
|-----------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="20e14-112">PATCOPY</span><span class="sxs-lookup"><span data-stu-id="20e14-112">PATCOPY</span></span>   | <span data-ttu-id="20e14-113">將模式複製到目的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="20e14-113">Copies the pattern to the destination bitmap.</span></span>                                       |
| <span data-ttu-id="20e14-114">PATINVERT</span><span class="sxs-lookup"><span data-stu-id="20e14-114">PATINVERT</span></span> | <span data-ttu-id="20e14-115">使用布林 XOR 運算子，將目的地點陣圖與模式合併。</span><span class="sxs-lookup"><span data-stu-id="20e14-115">Combines the destination bitmap with the pattern by using the Boolean XOR operator.</span></span> |
| <span data-ttu-id="20e14-116">DSTINVERT</span><span class="sxs-lookup"><span data-stu-id="20e14-116">DSTINVERT</span></span> | <span data-ttu-id="20e14-117">反轉目的地點陣圖。</span><span class="sxs-lookup"><span data-stu-id="20e14-117">Inverts the destination bitmap.</span></span>                                                     |
| <span data-ttu-id="20e14-118">黑暗</span><span class="sxs-lookup"><span data-stu-id="20e14-118">BLACKNESS</span></span> | <span data-ttu-id="20e14-119">將所有輸出變成二進位零。</span><span class="sxs-lookup"><span data-stu-id="20e14-119">Turns all output to binary zeros.</span></span>                                                   |
| <span data-ttu-id="20e14-120">白</span><span class="sxs-lookup"><span data-stu-id="20e14-120">WHITENESS</span></span> | <span data-ttu-id="20e14-121">將所有輸出變成二進位檔。</span><span class="sxs-lookup"><span data-stu-id="20e14-121">Turns all output to binary ones.</span></span>                                                    |



 

<span data-ttu-id="20e14-122">如需詳細資訊，請參閱 [點陣操作程式碼](raster-operation-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="20e14-122">For more information, see [Raster Operation Codes](raster-operation-codes.md).</span></span>

 

 



