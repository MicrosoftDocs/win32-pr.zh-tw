---
description: CSourcePosition 是一個抽象類別，可在來源篩選器上執行 IMediaPosition 介面。
ms.assetid: 838d2efd-6870-4412-98e2-fb2628e14bf3
title: CSourcePosition 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourcePosition
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0b88289381641edcef5922557862729acbb81f54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106991589"
---
# <a name="csourceposition-class"></a><span data-ttu-id="fcb6e-103">CSourcePosition 類別</span><span class="sxs-lookup"><span data-stu-id="fcb6e-103">CSourcePosition class</span></span>

<span data-ttu-id="fcb6e-104">`CSourcePosition` 是在來源篩選器上執行 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) 介面的抽象類別。</span><span class="sxs-lookup"><span data-stu-id="fcb6e-104">`CSourcePosition` is an abstract class for implementing the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) interface on a source filter.</span></span>

<span data-ttu-id="fcb6e-105">這個類別已經過時。</span><span class="sxs-lookup"><span data-stu-id="fcb6e-105">This class is obsolete.</span></span> <span data-ttu-id="fcb6e-106">如果來源篩選準則是可搜尋的，則應該公開 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 介面，而不是 **IMediaPosition**。</span><span class="sxs-lookup"><span data-stu-id="fcb6e-106">If your source filter is seekable, it should expose the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface instead of **IMediaPosition**.</span></span> <span data-ttu-id="fcb6e-107">您可以針對此用途使用 [**CSourceSeeking**](csourceseeking.md) 基類。</span><span class="sxs-lookup"><span data-stu-id="fcb6e-107">You can use the [**CSourceSeeking**](csourceseeking.md) base class for this purpose.</span></span>

 

 



