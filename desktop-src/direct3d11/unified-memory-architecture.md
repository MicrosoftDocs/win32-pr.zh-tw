---
title: 統一記憶體架構
description: 查詢是否支援統一記憶體架構 (UMA) 可協助判斷如何處理某些資源。
ms.assetid: E43892F9-E7CD-4D18-BDDE-3C4F03F8F4EA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99baeab51838b9b3382884a681ec9b579fa700a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931965"
---
# <a name="unified-memory-architecture"></a><span data-ttu-id="7fc86-103">統一記憶體架構</span><span class="sxs-lookup"><span data-stu-id="7fc86-103">Unified Memory Architecture</span></span>

<span data-ttu-id="7fc86-104">查詢是否支援統一記憶體架構 (UMA) 可協助判斷如何處理某些資源。</span><span class="sxs-lookup"><span data-stu-id="7fc86-104">Querying for whether Unified Memory Architecture (UMA) is supported can help determine how to handle some resources.</span></span>

<span data-ttu-id="7fc86-105">您可以從 [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) 結構中讀取由驅動程式設定的布林值，以判斷硬體是否支援 UMA。</span><span class="sxs-lookup"><span data-stu-id="7fc86-105">A boolean, set by the driver, can be read from the [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) structure to determine if the hardware supports UMA.</span></span>

<span data-ttu-id="7fc86-106">在 UMA 上執行的應用程式可能會想要讓 CPU 存取的資源超過可用的資源。</span><span class="sxs-lookup"><span data-stu-id="7fc86-106">Applications running on UMA may want to have more resources with CPU access enabled than if it is not available.</span></span> <span data-ttu-id="7fc86-107">UMA 可讓應用程式避免複製資源資料，而不是只針對非 UMA 圖形介面卡保持有效率。</span><span class="sxs-lookup"><span data-stu-id="7fc86-107">UMA enables applications to avoiding copying resource data around, instead of staying efficient solely for non-UMA graphics adapters.</span></span> [<span data-ttu-id="7fc86-108">Direct3D 11.3 功能</span><span class="sxs-lookup"><span data-stu-id="7fc86-108">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)

## <a name="related-topics"></a><span data-ttu-id="7fc86-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="7fc86-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fc86-110">Direct3D 11.3 功能</span><span class="sxs-lookup"><span data-stu-id="7fc86-110">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> </dl>

 

 




