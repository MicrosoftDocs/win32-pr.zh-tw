---
description: 下列清單包含執行緒集區所呼叫的 CMSPCallMultiGraph 公用方法。
ms.assetid: f0a5f621-99c4-40f0-8a0e-0e43792e00a1
title: CMSPCallMultiGraph 由執行緒集區呼叫的公用方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3878298024164a4c940b96dceb88e0ff005d59ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971821"
---
# <a name="cmspcallmultigraph-public-methods-called-by-thread-pool"></a><span data-ttu-id="3ab6b-103">CMSPCallMultiGraph 由執行緒集區呼叫的公用方法</span><span class="sxs-lookup"><span data-stu-id="3ab6b-103">CMSPCallMultiGraph Public Methods, Called by Thread Pool</span></span>



| <span data-ttu-id="3ab6b-104">CMSPCallMultiGraph 公用方法</span><span class="sxs-lookup"><span data-stu-id="3ab6b-104">CMSPCallMultiGraph public methods</span></span>                                   | <span data-ttu-id="3ab6b-105">Description</span><span class="sxs-lookup"><span data-stu-id="3ab6b-105">Description</span></span>                                                                                                                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ab6b-106">**DispatchGraphEvent**</span><span class="sxs-lookup"><span data-stu-id="3ab6b-106">**DispatchGraphEvent**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) | <span data-ttu-id="3ab6b-107">當篩選圖形發出事件信號時呼叫。</span><span class="sxs-lookup"><span data-stu-id="3ab6b-107">Called when the filter graph signals an event.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="3ab6b-108">**HandleGraphEvent**</span><span class="sxs-lookup"><span data-stu-id="3ab6b-108">**HandleGraphEvent**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-handlegraphevent)     | <span data-ttu-id="3ab6b-109">由 [**DispatchGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) 靜態方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="3ab6b-109">Called by the [**DispatchGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) static method.</span></span> <span data-ttu-id="3ab6b-110">[**ProcessGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent)在主要 MSP 工作者執行緒上的佇列。</span><span class="sxs-lookup"><span data-stu-id="3ab6b-110">Queues [**ProcessGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent) on the main MSP worker thread.</span></span> |
| [<span data-ttu-id="3ab6b-111">**ProcessGraphEvent**</span><span class="sxs-lookup"><span data-stu-id="3ab6b-111">**ProcessGraphEvent**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent)   | <span data-ttu-id="3ab6b-112">允許 MSP 呼叫物件實例處理篩選圖形事件。</span><span class="sxs-lookup"><span data-stu-id="3ab6b-112">Allows the MSP call object instance to handle the filter graph event.</span></span>                                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="3ab6b-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="3ab6b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ab6b-114">**CMSPCallMultiGraph**</span><span class="sxs-lookup"><span data-stu-id="3ab6b-114">**CMSPCallMultiGraph**</span></span>](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallmultigraph)
</dt> </dl>

 

 



