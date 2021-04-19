---
description: COOKER \_ AVERAGE counter type 公式提供計數器資料的統計中間點。
ms.assetid: 5121cd02-b122-48fd-995a-cf6c77948fd8
ms.tgt_platform: multiple
title: COOKER_AVERAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4dc26939f0e7ff889bd0f10d4b421638d53f566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988740"
---
# <a name="cooker_average"></a><span data-ttu-id="140a7-103">COOKER \_ 平均</span><span class="sxs-lookup"><span data-stu-id="140a7-103">COOKER\_AVERAGE</span></span>

<span data-ttu-id="140a7-104">COOKER \_ AVERAGE counter type 公式提供計數器資料的統計中間點。</span><span class="sxs-lookup"><span data-stu-id="140a7-104">The COOKER\_AVERAGE counter type formula provides the statistical midpoint of the data for a counter.</span></span> <span data-ttu-id="140a7-105">此計數器類型的公式會加總 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 實例中某個屬性的重複觀察，並將總和除以觀察數目。</span><span class="sxs-lookup"><span data-stu-id="140a7-105">The formula for this counter type sums repeated observations of one property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) instance, and divides the sum by the number of observations.</span></span> <span data-ttu-id="140a7-106">此計數器類型只會在 WMI 內定義，而不能用於效能監視技術，例如 [效能計數器6.0 版](/windows/desktop/PerfCtrs/performance-counters-portal)。</span><span class="sxs-lookup"><span data-stu-id="140a7-106">This counter type is defined only within WMI, and it is not available to the performance monitoring technologies, such as [Performance Counters Version 6.0](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

<span data-ttu-id="140a7-107">如需有關計數器類型公式的詳細資訊，請參閱 [計數器類型](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="140a7-107">For more information about the counter type formula, see [Counter Types](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).</span></span>

<span data-ttu-id="140a7-108">如需 WMI 高效能提供者和腳本的詳細資訊，請參閱 [Wmi 效能計數器類型](wmi-performance-counter-types.md)。</span><span class="sxs-lookup"><span data-stu-id="140a7-108">For more information about WMI high-performance providers and scripting, see [WMI Performance Counter Types](wmi-performance-counter-types.md).</span></span>

## <a name="example-code"></a><span data-ttu-id="140a7-109">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="140a7-109">Example Code</span></span>

<span data-ttu-id="140a7-110">如需程式碼範例，請參閱 [取得統計效能資料](obtaining-statistical-performance-data.md)。</span><span class="sxs-lookup"><span data-stu-id="140a7-110">For code examples, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="140a7-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="140a7-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="140a7-112">統計計數器類型</span><span class="sxs-lookup"><span data-stu-id="140a7-112">Statistical Counter Types</span></span>](statistical-counter-types.md)
</dt> <dt>

[<span data-ttu-id="140a7-113">監視效能資料</span><span class="sxs-lookup"><span data-stu-id="140a7-113">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
