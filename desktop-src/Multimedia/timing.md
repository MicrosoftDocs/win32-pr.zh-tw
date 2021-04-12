---
title: Windows 多媒體)  (時間
description: 計時
ms.assetid: 9ab284c7-eebc-4b44-b9e1-cc95efde22c1
keywords:
- DrawDib，計時
- DrawDibTime 函式
- DrawDib，調試
- 調試 DrawDib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adddd43ff5067d08334a40f2e52e79109c8a8bb7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464072"
---
# <a name="timing-windows-multimedia"></a><span data-ttu-id="5875d-107">Windows 多媒體)  (時間</span><span class="sxs-lookup"><span data-stu-id="5875d-107">Timing (Windows Multimedia)</span></span>

<span data-ttu-id="5875d-108">在偵錯工具中，您可以取得完成重複 DrawDib 作業所需的時間量的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5875d-108">As part of debugging an application, you can obtain information about the amount of time required to complete repetitive DrawDib operations.</span></span> <span data-ttu-id="5875d-109">[**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime)函數會傳回下列作業的計時資訊：</span><span class="sxs-lookup"><span data-stu-id="5875d-109">The [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) function returns timing information for the following operations:</span></span>

-   <span data-ttu-id="5875d-110">繪製點陣圖</span><span class="sxs-lookup"><span data-stu-id="5875d-110">Drawing a bitmap</span></span>
-   <span data-ttu-id="5875d-111">解壓縮點陣圖</span><span class="sxs-lookup"><span data-stu-id="5875d-111">Decompressing a bitmap</span></span>
-   <span data-ttu-id="5875d-112">遞色點陣圖</span><span class="sxs-lookup"><span data-stu-id="5875d-112">Dithering a bitmap</span></span>
-   <span data-ttu-id="5875d-113">延展點陣圖</span><span class="sxs-lookup"><span data-stu-id="5875d-113">Stretching a bitmap</span></span>
-   <span data-ttu-id="5875d-114">使用 [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) 函數傳送點陣圖</span><span class="sxs-lookup"><span data-stu-id="5875d-114">Transferring a bitmap by using the [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) function</span></span>
-   <span data-ttu-id="5875d-115">使用 [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) 函數傳送點陣圖</span><span class="sxs-lookup"><span data-stu-id="5875d-115">Transferring a bitmap by using the [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) function</span></span>

<span data-ttu-id="5875d-116">在抓取一組值之後， [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) 會重設每項作業的計數和值。</span><span class="sxs-lookup"><span data-stu-id="5875d-116">After retrieving a set of values, [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) resets the count and value for each operation.</span></span>

<span data-ttu-id="5875d-117">[**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime)函式僅適用于 DrawDib 函數的偵錯工具版本。</span><span class="sxs-lookup"><span data-stu-id="5875d-117">The [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) function is available only in the debug version of the DrawDib functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5875d-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="5875d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5875d-119">影像轉譯</span><span class="sxs-lookup"><span data-stu-id="5875d-119">Image Rendering</span></span>](image-rendering.md)
</dt> </dl>

 

 
