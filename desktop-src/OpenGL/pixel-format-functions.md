---
title: 像素格式函數
description: 下列 Windows 函數會管理像素格式。
ms.assetid: 78a6be75-72f6-4aef-a6bc-5f052c6fe2e9
keywords:
- WGL 函式，像素格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e219fc6a2aafecdcda43708cdb4c77553c88f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840768"
---
# <a name="pixel-format-functions"></a><span data-ttu-id="50b95-104">像素格式函數</span><span class="sxs-lookup"><span data-stu-id="50b95-104">Pixel Format Functions</span></span>

<span data-ttu-id="50b95-105">下列 Windows 函數會管理像素格式。</span><span class="sxs-lookup"><span data-stu-id="50b95-105">The following Windows functions manage pixel formats.</span></span>



| <span data-ttu-id="50b95-106">Windows 函數</span><span class="sxs-lookup"><span data-stu-id="50b95-106">Windows Function</span></span>                                               | <span data-ttu-id="50b95-107">Description</span><span class="sxs-lookup"><span data-stu-id="50b95-107">Description</span></span>                                                                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50b95-108">**ChoosePixelFormat**</span><span class="sxs-lookup"><span data-stu-id="50b95-108">**ChoosePixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                 | <span data-ttu-id="50b95-109">取得裝置內容的像素格式，此格式最符合指定的像素格式。</span><span class="sxs-lookup"><span data-stu-id="50b95-109">Obtains the device context's pixel format that is the closest match to a specified pixel format.</span></span>                                                                      |
| [<span data-ttu-id="50b95-110">**SetPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="50b95-110">**SetPixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                       | <span data-ttu-id="50b95-111">將裝置內容的目前像素格式設定為像素格式索引所指定的像素格式。</span><span class="sxs-lookup"><span data-stu-id="50b95-111">Sets a device context's current pixel format to the pixel format specified by a pixel format index.</span></span>                                                                   |
| [<span data-ttu-id="50b95-112">**GetPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="50b95-112">**GetPixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                       | <span data-ttu-id="50b95-113">取得裝置內容目前像素格式的像素格式索引。</span><span class="sxs-lookup"><span data-stu-id="50b95-113">Obtains the pixel format index of a device context's current pixel format.</span></span>                                                                                            |
| [<span data-ttu-id="50b95-114">**DescribePixelFormat**</span><span class="sxs-lookup"><span data-stu-id="50b95-114">**DescribePixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)             | <span data-ttu-id="50b95-115">針對裝置內容和像素格式索引，以像素格式的屬性填入 [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) 資料結構。</span><span class="sxs-lookup"><span data-stu-id="50b95-115">Given a device context and a pixel format index, fills in a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure with the pixel format's properties.</span></span> |
| [<span data-ttu-id="50b95-116">**GetEnhMetaFilePixelFormat**</span><span class="sxs-lookup"><span data-stu-id="50b95-116">**GetEnhMetaFilePixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilepixelformat) | <span data-ttu-id="50b95-117">抓取增強型中繼檔的像素格式資訊。</span><span class="sxs-lookup"><span data-stu-id="50b95-117">Retrieves pixel format information for an enhanced metafile.</span></span>                                                                                                          |



 

<span data-ttu-id="50b95-118">[**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)函式會傳回以一為基礎的像素格式索引，以識別最符合裝置內容支援的像素格式。</span><span class="sxs-lookup"><span data-stu-id="50b95-118">The [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) function returns a one-based pixel format index that identifies the best match from the device context's supported pixel formats.</span></span>

<span data-ttu-id="50b95-119">[**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)函式會使用以一為基礎的像素格式索引來識別所要的格式。</span><span class="sxs-lookup"><span data-stu-id="50b95-119">The [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) function identifies the desired format using a one-based pixel format index.</span></span> <span data-ttu-id="50b95-120">一般來說，您會呼叫 **ChoosePixelFormat** 來尋找最符合的像素格式，然後使用 **ChoosePixelFormat** 的結果來呼叫 **SetPixelFormat** 。</span><span class="sxs-lookup"><span data-stu-id="50b95-120">Typically, you call **ChoosePixelFormat** to find a best-match pixel format, and then call **SetPixelFormat** with the result of **ChoosePixelFormat**.</span></span>

<span data-ttu-id="50b95-121">如果您針對參考視窗的裝置內容呼叫 **SetPixelFormat** ， **SetPixelFormat** 也會變更視窗的像素格式。</span><span class="sxs-lookup"><span data-stu-id="50b95-121">If you call **SetPixelFormat** for a device context that references a window, **SetPixelFormat** also changes the pixel format of the window.</span></span> <span data-ttu-id="50b95-122">設定視窗的像素格式可能會導致視窗管理員和多執行緒應用程式的大複雜，因此不允許這種情況。</span><span class="sxs-lookup"><span data-stu-id="50b95-122">Setting the pixel format of a window more than once can lead to significant complications for the Window Manager and for multithread applications, so it is not allowed.</span></span> <span data-ttu-id="50b95-123">您只能將視窗的像素格式設定為一次;之後，就無法變更視窗的像素格式。</span><span class="sxs-lookup"><span data-stu-id="50b95-123">You can set the pixel format of a window only one time; after that, the window's pixel format cannot be changed.</span></span>

<span data-ttu-id="50b95-124">[**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)函式會傳回以一為基礎的像素格式索引。</span><span class="sxs-lookup"><span data-stu-id="50b95-124">The [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) function returns a one-based pixel format index.</span></span>

<span data-ttu-id="50b95-125">[**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)函式會以下列參數作為參數：</span><span class="sxs-lookup"><span data-stu-id="50b95-125">The [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) function takes the following as parameters:</span></span>

-   <span data-ttu-id="50b95-126">裝置內容的控制碼</span><span class="sxs-lookup"><span data-stu-id="50b95-126">A handle to a device context</span></span>
-   <span data-ttu-id="50b95-127">像素格式索引</span><span class="sxs-lookup"><span data-stu-id="50b95-127">A pixel format index</span></span>
-   <span data-ttu-id="50b95-128">[**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)資料結構的指標</span><span class="sxs-lookup"><span data-stu-id="50b95-128">A pointer to a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure</span></span>

<span data-ttu-id="50b95-129">[**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)函式會以適當設定的 **PIXELFORMATDESCRIPTOR** 成員傳回。</span><span class="sxs-lookup"><span data-stu-id="50b95-129">The [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) function returns with the members of **PIXELFORMATDESCRIPTOR** appropriately set.</span></span>

<span data-ttu-id="50b95-130">**GetEnhMetaFilePixelFormat** 函式會傳回中繼檔的像素格式大小，並抓取中繼檔的像素格式資訊。</span><span class="sxs-lookup"><span data-stu-id="50b95-130">The **GetEnhMetaFilePixelFormat** function returns the size of a metafile's pixel format and retrieves the pixel format information of the metafile.</span></span>

 

 




