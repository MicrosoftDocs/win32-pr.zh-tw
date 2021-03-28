---
description: 如同裁剪區域，剪輯路徑是應用程式可以選取到裝置內容中的另一個繪圖物件。
ms.assetid: 35c4052b-3f11-40bc-9cc9-6f999326a656
title: 剪輯路徑
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc4a93b0047110a6adb2f68d413e89cb1e97fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972757"
---
# <a name="clip-paths"></a><span data-ttu-id="0b835-103">剪輯路徑</span><span class="sxs-lookup"><span data-stu-id="0b835-103">Clip Paths</span></span>

<span data-ttu-id="0b835-104">如同裁剪區域，剪輯路徑是應用程式可以選取到裝置內容中的另一個繪圖物件。</span><span class="sxs-lookup"><span data-stu-id="0b835-104">Like a clipping region, a clip path is another graphics object that an application can select into a device context.</span></span> <span data-ttu-id="0b835-105">與裁剪區域不同的是，剪輯路徑一律是由應用程式所建立，而且會用來裁剪成一或多個不規則圖形。</span><span class="sxs-lookup"><span data-stu-id="0b835-105">Unlike a clipping region, a clip path is always created by an application and it is used for clipping to one or more irregular shapes.</span></span> <span data-ttu-id="0b835-106">例如，應用程式可以使用在文字字串中形成字元外框的線條和曲線來定義剪輯路徑。</span><span class="sxs-lookup"><span data-stu-id="0b835-106">For example, an application can use the lines and curves that form the outlines of characters in a string of text to define a clip path.</span></span>

<span data-ttu-id="0b835-107">若要建立剪輯路徑，首先必須建立描述所需不規則圖形的路徑。</span><span class="sxs-lookup"><span data-stu-id="0b835-107">To create a clip path, it's first necessary to create a path that describes the required irregular shape.</span></span> <span data-ttu-id="0b835-108">路徑是藉由在呼叫 [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) 函式之後，以及在呼叫 [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) 函式之前，呼叫適當的圖形裝置介面 (GDI) 繪圖函式來建立。</span><span class="sxs-lookup"><span data-stu-id="0b835-108">Paths are created by calling the appropriate graphics device interface (GDI) drawing functions after calling the [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) function and before calling the [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) function.</span></span> <span data-ttu-id="0b835-109">這個函式集合稱為路徑括弧。</span><span class="sxs-lookup"><span data-stu-id="0b835-109">This collection of functions is called a path bracket.</span></span> <span data-ttu-id="0b835-110">如需路徑和路徑括弧的詳細資訊，請參閱 [路徑](paths.md)。</span><span class="sxs-lookup"><span data-stu-id="0b835-110">For more information about paths and path brackets, see [Paths](paths.md).</span></span>

<span data-ttu-id="0b835-111">建立路徑之後，您可以藉由呼叫 [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) 函式、識別裝置內容，並指定使用模式，將它轉換成剪輯路徑。</span><span class="sxs-lookup"><span data-stu-id="0b835-111">After the path is created, it can be converted to a clip path by calling the [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) function, identifying a device context, and specifying a usage mode.</span></span> <span data-ttu-id="0b835-112">使用模式會決定系統如何結合新的剪輯路徑與裝置內容的原始裁剪區域。</span><span class="sxs-lookup"><span data-stu-id="0b835-112">The usage mode determines how the system combines the new clip path with the device context's original clipping region.</span></span> <span data-ttu-id="0b835-113">下表描述使用模式。</span><span class="sxs-lookup"><span data-stu-id="0b835-113">The following table describes the usage modes.</span></span>



| <span data-ttu-id="0b835-114">[模式]</span><span class="sxs-lookup"><span data-stu-id="0b835-114">Mode</span></span>      | <span data-ttu-id="0b835-115">描述</span><span class="sxs-lookup"><span data-stu-id="0b835-115">Description</span></span>                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b835-116">R G N \_ 和</span><span class="sxs-lookup"><span data-stu-id="0b835-116">RGN\_AND</span></span>  | <span data-ttu-id="0b835-117">剪輯路徑包含裝置內容之裁剪區域和目前路徑 (重迭區域) 的交集。</span><span class="sxs-lookup"><span data-stu-id="0b835-117">The clip path includes the intersection (overlapping areas) of the device context's clipping region and the current path.</span></span>    |
| <span data-ttu-id="0b835-118">R G N \_ 複製</span><span class="sxs-lookup"><span data-stu-id="0b835-118">RGN\_COPY</span></span> | <span data-ttu-id="0b835-119">剪輯路徑是目前的路徑。</span><span class="sxs-lookup"><span data-stu-id="0b835-119">The clip path is the current path.</span></span>                                                                                           |
| <span data-ttu-id="0b835-120">R G N \_ 差異</span><span class="sxs-lookup"><span data-stu-id="0b835-120">RGN\_DIFF</span></span> | <span data-ttu-id="0b835-121">剪輯路徑包含裝置內容的裁剪區域，其中已排除目前路徑的任何交集部分。</span><span class="sxs-lookup"><span data-stu-id="0b835-121">The clip path includes the device context's clipping region with any intersecting parts of the current path excluded.</span></span>        |
| <span data-ttu-id="0b835-122">R G N \_ 或</span><span class="sxs-lookup"><span data-stu-id="0b835-122">RGN\_OR</span></span>   | <span data-ttu-id="0b835-123">剪輯路徑包含裝置內容之裁剪區域和目前路徑的聯集 (組合區域) 。</span><span class="sxs-lookup"><span data-stu-id="0b835-123">The clip path includes the union (combined areas) of the device context's clipping region and the current path.</span></span>              |
| <span data-ttu-id="0b835-124">R G N \_ XOR</span><span class="sxs-lookup"><span data-stu-id="0b835-124">RGN\_XOR</span></span>  | <span data-ttu-id="0b835-125">剪輯路徑包含裝置內容之裁剪區域和目前路徑的聯集，但不包括交集。</span><span class="sxs-lookup"><span data-stu-id="0b835-125">The clip path includes the union of the device context's clipping region and the current path but excludes the intersection.</span></span> |



 

 

 



