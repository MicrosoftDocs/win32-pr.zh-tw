---
description: 篩選圖形及其元件
ms.assetid: 3747bfcd-1e4a-404c-a493-26d3c20bab21
title: 篩選圖形及其元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473fb3dfe327eb43bb2065417c7be80f7537d06a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985292"
---
# <a name="the-filter-graph-and-its-components"></a><span data-ttu-id="80cab-103">篩選圖形及其元件</span><span class="sxs-lookup"><span data-stu-id="80cab-103">The Filter Graph and Its Components</span></span>

<span data-ttu-id="80cab-104">本文說明 DirectShow 的主要元件。</span><span class="sxs-lookup"><span data-stu-id="80cab-104">This article describes the major components of DirectShow.</span></span> <span data-ttu-id="80cab-105">它是應用程式開發人員及撰寫自訂 DirectShow 篩選器的開發人員的簡介。</span><span class="sxs-lookup"><span data-stu-id="80cab-105">It is intended as an introduction for application developers and for developers writing custom DirectShow filters.</span></span> <span data-ttu-id="80cab-106">應用程式開發人員通常可以忽略許多關於 DirectShow 的低層級詳細資料。</span><span class="sxs-lookup"><span data-stu-id="80cab-106">Application developers can usually ignore many of the low-level details of DirectShow.</span></span> <span data-ttu-id="80cab-107">不過，最好先閱讀這一節，以瞭解 DirectShow 架構。</span><span class="sxs-lookup"><span data-stu-id="80cab-107">However, it is still a good idea to read this section, to have a general understanding of the DirectShow architecture.</span></span>

<span data-ttu-id="80cab-108">本文包含下列各節：</span><span class="sxs-lookup"><span data-stu-id="80cab-108">This article contains the following sections:</span></span>

-   [<span data-ttu-id="80cab-109">關於 DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="80cab-109">About DirectShow Filters</span></span>](about-directshow-filters.md)
-   [<span data-ttu-id="80cab-110">關於篩選圖形管理員</span><span class="sxs-lookup"><span data-stu-id="80cab-110">About the Filter Graph Manager</span></span>](about-the-filter-graph-manager.md)
-   [<span data-ttu-id="80cab-111">關於媒體類型</span><span class="sxs-lookup"><span data-stu-id="80cab-111">About Media Types</span></span>](about-media-types.md)
-   [<span data-ttu-id="80cab-112">關於媒體範例和配置器</span><span class="sxs-lookup"><span data-stu-id="80cab-112">About Media Samples and Allocators</span></span>](about-media-samples-and-allocators.md)
-   [<span data-ttu-id="80cab-113">硬體裝置參與篩選圖形的方式</span><span class="sxs-lookup"><span data-stu-id="80cab-113">How Hardware Devices Participate in the Filter Graph</span></span>](how-hardware-devices-participate-in-the-filter-graph.md)

 

 



