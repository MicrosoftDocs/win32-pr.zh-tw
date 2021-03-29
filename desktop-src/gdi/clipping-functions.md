---
description: 下列函式會與裁剪一起使用。
ms.assetid: de9e5786-63d8-47be-8522-e96d7c0f8634
title: 裁剪函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bf202d5ba102095c6bfddb3c3928cab1e55a230
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972756"
---
# <a name="clipping-functions"></a><span data-ttu-id="70f19-103">裁剪函式</span><span class="sxs-lookup"><span data-stu-id="70f19-103">Clipping Functions</span></span>

<span data-ttu-id="70f19-104">下列函式會與裁剪一起使用。</span><span class="sxs-lookup"><span data-stu-id="70f19-104">The following functions are used with clipping.</span></span>



| <span data-ttu-id="70f19-105">函式</span><span class="sxs-lookup"><span data-stu-id="70f19-105">Function</span></span>                                       | <span data-ttu-id="70f19-106">描述</span><span class="sxs-lookup"><span data-stu-id="70f19-106">Description</span></span>                                                                                                                                                                               |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70f19-107">**ExcludeClipRect**</span><span class="sxs-lookup"><span data-stu-id="70f19-107">**ExcludeClipRect**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-excludecliprect)     | <span data-ttu-id="70f19-108">建立新的裁剪區域，其中包含現有的裁剪區域減去指定的矩形。</span><span class="sxs-lookup"><span data-stu-id="70f19-108">Creates a new clipping region that consists of the existing clipping region minus the specified rectangle.</span></span>                                                                                |
| [<span data-ttu-id="70f19-109">**ExtSelectClipRgn**</span><span class="sxs-lookup"><span data-stu-id="70f19-109">**ExtSelectClipRgn**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extselectcliprgn)   | <span data-ttu-id="70f19-110">使用指定的模式結合指定的區域與目前的裁剪區域。</span><span class="sxs-lookup"><span data-stu-id="70f19-110">Combines the specified region with the current clipping region using the specified mode.</span></span>                                                                                                  |
| [<span data-ttu-id="70f19-111">**GetClipBox**</span><span class="sxs-lookup"><span data-stu-id="70f19-111">**GetClipBox**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getclipbox)               | <span data-ttu-id="70f19-112">抓取可在裝置上的目前可見區域周圍繪製之嚴謹周框的尺寸。</span><span class="sxs-lookup"><span data-stu-id="70f19-112">Retrieves the dimensions of the tightest bounding rectangle that can be drawn around the current visible area on the device.</span></span>                                                              |
| [<span data-ttu-id="70f19-113">**GetClipRgn**</span><span class="sxs-lookup"><span data-stu-id="70f19-113">**GetClipRgn**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getcliprgn)               | <span data-ttu-id="70f19-114">抓取控制碼，該控制碼會識別指定之裝置內容目前應用程式定義的裁剪區域。</span><span class="sxs-lookup"><span data-stu-id="70f19-114">Retrieves a handle identifying the current application-defined clipping region for the specified device context.</span></span>                                                                          |
| [<span data-ttu-id="70f19-115">**GetMetaRgn**</span><span class="sxs-lookup"><span data-stu-id="70f19-115">**GetMetaRgn**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getmetargn)               | <span data-ttu-id="70f19-116">抓取指定之裝置內容的目前 metaregion。</span><span class="sxs-lookup"><span data-stu-id="70f19-116">Retrieves the current metaregion for the specified device context.</span></span>                                                                                                                        |
| [<span data-ttu-id="70f19-117">**GetRandomRgn**</span><span class="sxs-lookup"><span data-stu-id="70f19-117">**GetRandomRgn**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getrandomrgn)           | <span data-ttu-id="70f19-118">將指定之裝置內容的系統裁剪區域複製到特定區域。</span><span class="sxs-lookup"><span data-stu-id="70f19-118">Copies the system clipping region of a specified device context to a specific region.</span></span>                                                                                                     |
| [<span data-ttu-id="70f19-119">**IntersectClipRect**</span><span class="sxs-lookup"><span data-stu-id="70f19-119">**IntersectClipRect**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-intersectcliprect) | <span data-ttu-id="70f19-120">從目前裁剪區域和指定矩形的交集建立新的裁剪區域。</span><span class="sxs-lookup"><span data-stu-id="70f19-120">Creates a new clipping region from the intersection of the current clipping region and the specified rectangle.</span></span>                                                                           |
| [<span data-ttu-id="70f19-121">**OffsetClipRgn**</span><span class="sxs-lookup"><span data-stu-id="70f19-121">**OffsetClipRgn**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-offsetcliprgn)         | <span data-ttu-id="70f19-122">依據指定的位移移動裝置內容的裁剪區域。</span><span class="sxs-lookup"><span data-stu-id="70f19-122">Moves the clipping region of a device context by the specified offsets.</span></span>                                                                                                                   |
| [<span data-ttu-id="70f19-123">**PtVisible**</span><span class="sxs-lookup"><span data-stu-id="70f19-123">**PtVisible**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-ptvisible)                 | <span data-ttu-id="70f19-124">判斷指定的點是否在裝置內容的裁剪區域內。</span><span class="sxs-lookup"><span data-stu-id="70f19-124">Determines whether the specified point is within the clipping region of a device context.</span></span>                                                                                                 |
| [<span data-ttu-id="70f19-125">**RectVisible**</span><span class="sxs-lookup"><span data-stu-id="70f19-125">**RectVisible**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible)             | <span data-ttu-id="70f19-126">判斷指定的矩形是否有任何部分位於裝置內容的裁剪區域內。</span><span class="sxs-lookup"><span data-stu-id="70f19-126">Determines whether any part of the specified rectangle lies within the clipping region of a device context.</span></span>                                                                               |
| [<span data-ttu-id="70f19-127">**SelectClipPath**</span><span class="sxs-lookup"><span data-stu-id="70f19-127">**SelectClipPath**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath)       | <span data-ttu-id="70f19-128">選取目前的路徑作為裝置內容的裁剪區域，並使用指定的模式結合新區域與任何現有的裁剪區域。</span><span class="sxs-lookup"><span data-stu-id="70f19-128">Selects the current path as a clipping region for a device context, combining the new region with any existing clipping region by using the specified mode.</span></span>                               |
| [<span data-ttu-id="70f19-129">**SelectClipRgn**</span><span class="sxs-lookup"><span data-stu-id="70f19-129">**SelectClipRgn**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn)         | <span data-ttu-id="70f19-130">選取區域做為指定之裝置內容的目前裁剪區域。</span><span class="sxs-lookup"><span data-stu-id="70f19-130">Selects a region as the current clipping region for the specified device context.</span></span>                                                                                                         |
| [<span data-ttu-id="70f19-131">**SetMetaRgn**</span><span class="sxs-lookup"><span data-stu-id="70f19-131">**SetMetaRgn**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setmetargn)               | <span data-ttu-id="70f19-132">使用目前的 metaregion 與指定之裝置內容的目前裁剪區域交集，並將結合的區域儲存為指定之裝置內容的新 metaregion。</span><span class="sxs-lookup"><span data-stu-id="70f19-132">Intersects the current clipping region for the specified device context with the current metaregion and saves the combined region as the new metaregion for the specified device context.</span></span> |



 

 

 



