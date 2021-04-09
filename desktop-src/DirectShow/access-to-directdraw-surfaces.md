---
description: 存取 DirectDraw 表面
ms.assetid: 21002c9f-8b8b-49f3-9ea3-3703780e3412
title: 存取 DirectDraw 表面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac1acdd122fa7d21fd49868c45f065f59b06ad8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846744"
---
# <a name="access-to-directdraw-surfaces"></a><span data-ttu-id="ea99a-103">存取 DirectDraw 表面</span><span class="sxs-lookup"><span data-stu-id="ea99a-103">Access to DirectDraw Surfaces</span></span>

<span data-ttu-id="ea99a-104">VMR 提供給上游篩選器的媒體範例物件支援 [**IVMRSurface**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) 介面。</span><span class="sxs-lookup"><span data-stu-id="ea99a-104">The Media Sample objects provided by the VMR to upstream filters support the [**IVMRSurface**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) interface.</span></span> <span data-ttu-id="ea99a-105">若要取得介面，請呼叫 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面上的 QueryInterface 並指定 IID \_ IVMRSurface。</span><span class="sxs-lookup"><span data-stu-id="ea99a-105">To obtain the interface, call QueryInterface on the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface and specify IID\_IVMRSurface.</span></span> <span data-ttu-id="ea99a-106">上游篩選器接著可以使用 IVMRSurface 方法來存取及操作由 VMR 所建立的介面。</span><span class="sxs-lookup"><span data-stu-id="ea99a-106">Upstream filters can then use the IVMRSurface methods to access and manipulate the surface that has been created by the VMR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea99a-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="ea99a-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea99a-108">使用 VMR 來進行 DirectShow 篩選器開發人員</span><span class="sxs-lookup"><span data-stu-id="ea99a-108">Using the VMR for DirectShow Filter Developers</span></span>](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



