---
description: 增強的中繼檔是一組記錄。
ms.assetid: af3261c7-2113-4777-97c0-504f23022550
title: 增強的中繼檔記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2097fd59497838c2a77a0209f6ae715dff2e1cf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972681"
---
# <a name="enhanced-metafile-records"></a><span data-ttu-id="1c02d-103">增強的中繼檔記錄</span><span class="sxs-lookup"><span data-stu-id="1c02d-103">Enhanced Metafile Records</span></span>

<span data-ttu-id="1c02d-104">增強的中繼檔是一組記錄。</span><span class="sxs-lookup"><span data-stu-id="1c02d-104">An enhanced metafile is an array of records.</span></span> <span data-ttu-id="1c02d-105">中繼檔記錄是可變長度的 [**ENHMETARECORD**](/windows/win32/api/wingdi/ns-wingdi-enhmetarecord) 結構。</span><span class="sxs-lookup"><span data-stu-id="1c02d-105">A metafile record is a variable-length [**ENHMETARECORD**](/windows/win32/api/wingdi/ns-wingdi-enhmetarecord) structure.</span></span> <span data-ttu-id="1c02d-106">每個增強型中繼檔記錄的開頭都是 [**EMR**](/windows/win32/api/wingdi/ns-wingdi-emr) 結構，其中包含兩個成員。</span><span class="sxs-lookup"><span data-stu-id="1c02d-106">At the beginning of every enhanced metafile record is an [**EMR**](/windows/win32/api/wingdi/ns-wingdi-emr) structure, which contains two members.</span></span> <span data-ttu-id="1c02d-107">第一個成員 iType 會識別記錄類型，也就是其參數包含在記錄中的 GDI 函數。</span><span class="sxs-lookup"><span data-stu-id="1c02d-107">The first member, iType, identifies the record type that is, the GDI function whose parameters are contained in the record.</span></span> <span data-ttu-id="1c02d-108">因為結構的長度是變數，所以另一個成員 nSize 包含記錄的大小。</span><span class="sxs-lookup"><span data-stu-id="1c02d-108">Because the structures are variable in length, the other member, nSize, contains the size of the record.</span></span> <span data-ttu-id="1c02d-109">緊接在 nSize 成員後面的是 GDI 函數的其餘參數（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="1c02d-109">Immediately following the nSize member are the remaining parameters, if any, of the GDI function.</span></span> <span data-ttu-id="1c02d-110">結構的其餘部分包含相依于記錄類型的其他資料。</span><span class="sxs-lookup"><span data-stu-id="1c02d-110">The remainder of the structure contains additional data that is dependent on the record type.</span></span>

<span data-ttu-id="1c02d-111">增強中繼檔中的第一筆記錄一律是 [**ENHMETAHEADER**](/windows/win32/api/wingdi/ns-wingdi-enhmetaheader) 結構，也就是增強型中繼檔的標頭。</span><span class="sxs-lookup"><span data-stu-id="1c02d-111">The first record in an enhanced metafile is always the [**ENHMETAHEADER**](/windows/win32/api/wingdi/ns-wingdi-enhmetaheader) structure, which is the enhanced-metafile header.</span></span> <span data-ttu-id="1c02d-112">標頭會指定下列資訊：</span><span class="sxs-lookup"><span data-stu-id="1c02d-112">The header specifies the following information:</span></span>

-   <span data-ttu-id="1c02d-113">中繼檔的大小（以位元組為單位）</span><span class="sxs-lookup"><span data-stu-id="1c02d-113">Size of the metafile, in bytes</span></span>
-   <span data-ttu-id="1c02d-114">圖片框架的尺寸（以裝置單位）</span><span class="sxs-lookup"><span data-stu-id="1c02d-114">Dimensions of the picture frame, in device units</span></span>
-   <span data-ttu-id="1c02d-115">圖片框架的維度，以 01-毫米單位為單位</span><span class="sxs-lookup"><span data-stu-id="1c02d-115">Dimensions of the picture frame, in .01-millimeter units</span></span>
-   <span data-ttu-id="1c02d-116">中繼檔中的記錄數目</span><span class="sxs-lookup"><span data-stu-id="1c02d-116">Number of records in the metafile</span></span>
-   <span data-ttu-id="1c02d-117">選擇性文字描述的位移</span><span class="sxs-lookup"><span data-stu-id="1c02d-117">Offset to an optional text description</span></span>
-   <span data-ttu-id="1c02d-118">選用區的大小</span><span class="sxs-lookup"><span data-stu-id="1c02d-118">Size of the optional palette</span></span>
-   <span data-ttu-id="1c02d-119">原始裝置的解析度（以圖元為單位）</span><span class="sxs-lookup"><span data-stu-id="1c02d-119">Resolution of the original device, in pixels</span></span>
-   <span data-ttu-id="1c02d-120">原始裝置的解析度（以毫米為單位）</span><span class="sxs-lookup"><span data-stu-id="1c02d-120">Resolution of the original device, in millimeters</span></span>

<span data-ttu-id="1c02d-121">選擇性的文字描述可在標頭記錄之後。</span><span class="sxs-lookup"><span data-stu-id="1c02d-121">An optional text description can follow the header record.</span></span> <span data-ttu-id="1c02d-122">文字描述描述圖片和作者的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c02d-122">The text description describes the picture and the author's name.</span></span> <span data-ttu-id="1c02d-123">選擇性調色板會指定用來建立增強型中繼檔的色彩。</span><span class="sxs-lookup"><span data-stu-id="1c02d-123">The optional palette specifies the colors used to create the enhanced metafile.</span></span> <span data-ttu-id="1c02d-124">其餘記錄會識別用來建立圖片的 GDI 函數。</span><span class="sxs-lookup"><span data-stu-id="1c02d-124">The remaining records identify the GDI functions used to create the picture.</span></span> <span data-ttu-id="1c02d-125">下列十六進位輸出對應至針對 [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) 函式的呼叫所產生的記錄。</span><span class="sxs-lookup"><span data-stu-id="1c02d-125">The following hexadecimal output corresponds to a record generated for a call to the [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) function.</span></span>


```C++
00000011 0000000C 00000004 
```



<span data-ttu-id="1c02d-126">值0x00000011 會指定記錄類型 (對應至檔案 \_ Wingdi 中定義的 EMR SETMAPMODE 常數) 。</span><span class="sxs-lookup"><span data-stu-id="1c02d-126">The value 0x00000011 specifies the record type (corresponds to the EMR\_SETMAPMODE constant defined in the file Wingdi.h).</span></span> <span data-ttu-id="1c02d-127">0x0000000C 值會指定記錄的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1c02d-127">The value 0x0000000C specifies the length of the record, in bytes.</span></span> <span data-ttu-id="1c02d-128">值0x00000004 會識別對應模式 (對應至 \_ [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) 函數中定義的 MM LOENGLISH 常數) 。</span><span class="sxs-lookup"><span data-stu-id="1c02d-128">The value 0x00000004 identifies the mapping mode (corresponds to the MM\_LOENGLISH constant defined in the [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) function).</span></span>

<span data-ttu-id="1c02d-129">如需其他記錄類型的清單，請參閱 [中繼檔結構](metafile-structures.md)。</span><span class="sxs-lookup"><span data-stu-id="1c02d-129">For a list of additional record types, see [Metafile Structures](metafile-structures.md).</span></span>

 

 



