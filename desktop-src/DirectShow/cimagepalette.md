---
description: CImagePalette 類別會管理影片轉譯器的調色板。 可以用來從影片格式建立邏輯調色板。 此類別的目的是要搭配 CBaseWindow 和 CDrawImage 類別使用，因此它有點特製化。
ms.assetid: dcbe5049-0e8c-4221-825a-0fd8e6efd2a5
title: CImagePalette 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette
api_type:
- COM
api_location: ''
ms.openlocfilehash: 696c51e4918815e18accbadd66c764493dc0b98e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970877"
---
# <a name="cimagepalette-class"></a><span data-ttu-id="c17c8-105">CImagePalette 類別</span><span class="sxs-lookup"><span data-stu-id="c17c8-105">CImagePalette class</span></span>

<span data-ttu-id="c17c8-106">`CImagePalette`類別會管理影片轉譯器的調色板。</span><span class="sxs-lookup"><span data-stu-id="c17c8-106">The `CImagePalette` class manages palettes for video renderers.</span></span> <span data-ttu-id="c17c8-107">可以用來從影片格式建立邏輯調色板。</span><span class="sxs-lookup"><span data-stu-id="c17c8-107">It can be used to create a logical palette from a video format.</span></span> <span data-ttu-id="c17c8-108">此類別的目的是要搭配 [**CBaseWindow**](cbasewindow.md) 和 [**CDrawImage**](cdrawimage.md) 類別使用，因此它有點特製化。</span><span class="sxs-lookup"><span data-stu-id="c17c8-108">This class is intended to be used with the [**CBaseWindow**](cbasewindow.md) and [**CDrawImage**](cdrawimage.md) classes, so it is somewhat specialized.</span></span>



| <span data-ttu-id="c17c8-109">受保護的成員變數</span><span class="sxs-lookup"><span data-stu-id="c17c8-109">Protected Member Variables</span></span>                                       | <span data-ttu-id="c17c8-110">Description</span><span class="sxs-lookup"><span data-stu-id="c17c8-110">Description</span></span>                                                                                    |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c17c8-111">**m \_ hPalette**</span><span class="sxs-lookup"><span data-stu-id="c17c8-111">**m\_hPalette**</span></span>](cimagepalette-m-hpalette.md)                  | <span data-ttu-id="c17c8-112">這個物件管理的邏輯元件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c17c8-112">Handle to the logical palette that this object manages.</span></span>                                        |
| [<span data-ttu-id="c17c8-113">**m \_ pBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="c17c8-113">**m\_pBaseWindow**</span></span>](cimagepalette-m-pbasewindow.md)            | <span data-ttu-id="c17c8-114">管理視窗之 **CBaseWindow** 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="c17c8-114">Pointer to the **CBaseWindow** object that manages the window.</span></span>                                 |
| [<span data-ttu-id="c17c8-115">**m \_ pDrawImage**</span><span class="sxs-lookup"><span data-stu-id="c17c8-115">**m\_pDrawImage**</span></span>](cimagepalette-m-pdrawimage.md)              | <span data-ttu-id="c17c8-116">**CDrawImage** 物件的指標，該物件會繪製影片影像。</span><span class="sxs-lookup"><span data-stu-id="c17c8-116">Pointer to the **CDrawImage** object that draws the video image.</span></span>                               |
| [<span data-ttu-id="c17c8-117">**m \_ pFilter**</span><span class="sxs-lookup"><span data-stu-id="c17c8-117">**m\_pFilter**</span></span>](cimagepalette-m-pfilter.md)                    | <span data-ttu-id="c17c8-118">擁有篩選準則的指標。</span><span class="sxs-lookup"><span data-stu-id="c17c8-118">Pointer to the owning filter.</span></span>                                                                  |
| <span data-ttu-id="c17c8-119">公用方法</span><span class="sxs-lookup"><span data-stu-id="c17c8-119">Public Methods</span></span>                                                   | <span data-ttu-id="c17c8-120">Description</span><span class="sxs-lookup"><span data-stu-id="c17c8-120">Description</span></span>                                                                                    |
| [<span data-ttu-id="c17c8-121">**CImagePalette**</span><span class="sxs-lookup"><span data-stu-id="c17c8-121">**CImagePalette**</span></span>](cimagepalette-cimagepalette.md)             | <span data-ttu-id="c17c8-122">函式方法。</span><span class="sxs-lookup"><span data-stu-id="c17c8-122">Constructor method.</span></span>                                                                            |
| [<span data-ttu-id="c17c8-123">**CopyPalette**</span><span class="sxs-lookup"><span data-stu-id="c17c8-123">**CopyPalette**</span></span>](cimagepalette-copypalette.md)                 | <span data-ttu-id="c17c8-124">將 **VIDEOINFO** 結構中的元件複製到任何調色盤 **VIDEOINFO** 結構。</span><span class="sxs-lookup"><span data-stu-id="c17c8-124">Copies the palette from any **VIDEOINFO** structure to any palettized **VIDEOINFO** structure.</span></span> |
| [<span data-ttu-id="c17c8-125">**MakeIdentityPalette**</span><span class="sxs-lookup"><span data-stu-id="c17c8-125">**MakeIdentityPalette**</span></span>](cimagepalette-makeidentitypalette.md) | <span data-ttu-id="c17c8-126">嘗試建立直接對應至顯示裝置中所選取之調色板的調色板。</span><span class="sxs-lookup"><span data-stu-id="c17c8-126">Attempts to make a palette that maps directly to the palette selected in the display device.</span></span>   |
| [<span data-ttu-id="c17c8-127">**MakePalette**</span><span class="sxs-lookup"><span data-stu-id="c17c8-127">**MakePalette**</span></span>](cimagepalette-makepalette.md)                 | <span data-ttu-id="c17c8-128">從色彩表以影片格式建立邏輯調色板。</span><span class="sxs-lookup"><span data-stu-id="c17c8-128">Creates a logical palette from the color table in a video format.</span></span>                              |
| [<span data-ttu-id="c17c8-129">**PreparePalette**</span><span class="sxs-lookup"><span data-stu-id="c17c8-129">**PreparePalette**</span></span>](cimagepalette-preparepalette.md)           | <span data-ttu-id="c17c8-130">根據擁有篩選器中的媒體類型，設定調色板。</span><span class="sxs-lookup"><span data-stu-id="c17c8-130">Sets up a palette, based on a media type from the owning filter.</span></span>                               |
| [<span data-ttu-id="c17c8-131">**RemovePalette**</span><span class="sxs-lookup"><span data-stu-id="c17c8-131">**RemovePalette**</span></span>](cimagepalette-removepalette.md)             | <span data-ttu-id="c17c8-132">刪除現有的邏輯調色板。</span><span class="sxs-lookup"><span data-stu-id="c17c8-132">Deletes the existing logical palette.</span></span>                                                          |



 

 

 



