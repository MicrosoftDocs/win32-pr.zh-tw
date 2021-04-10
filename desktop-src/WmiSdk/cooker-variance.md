---
description: COOKER 變異數 \_ 計數器類型公式提供的變化性，是用來表示在 Win32 PerfRawData 實例中某一個屬性的一組原始觀察值的散佈 \_ 。
ms.assetid: 6b184a36-7d22-41ab-98e7-b185d1063bcb
ms.tgt_platform: multiple
title: COOKER_VARIANCE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef0f9de6c5241ccd486e4da76864139e3e54f5a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026548"
---
# <a name="cooker_variance"></a><span data-ttu-id="a5c5c-103">COOKER \_ 變異數</span><span class="sxs-lookup"><span data-stu-id="a5c5c-103">COOKER\_VARIANCE</span></span>

<span data-ttu-id="a5c5c-104">COOKER 變異數 \_ 計數器類型公式提供的變化性，是用來表示在 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 實例中某一個屬性的一組原始觀察值的散佈。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-104">The COOKER\_VARIANCE counter type formula provides variability that use to characterize dispersion for a set of raw observations of one property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) instance.</span></span> <span data-ttu-id="a5c5c-105">變異數的計算方式是將偏差的平方總和與每個計數器的平均值除以計數器數目。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-105">The variance is calculated by dividing the sum of the square of the deviation from the mean of each counter by the number of counters.</span></span> <span data-ttu-id="a5c5c-106">換句話說，變異數是每個計數器平均平方差的平均值。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-106">In other words, the variance is the average of the squared deviations from the mean for each counter.</span></span> <span data-ttu-id="a5c5c-107">此計數器類型只會在 WMI 內定義，而不能用於效能監視技術，例如 [效能計數器6.0 版](/windows/desktop/PerfCtrs/performance-counters-portal)。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-107">This counter type is defined only within WMI, and it is not available to the performance monitoring technologies, such as [Performance Counters Version 6.0](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

<span data-ttu-id="a5c5c-108">如需有關計數器類型公式的詳細資訊，請參閱 [計數器類型](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-108">For more information about the counter type formula, see [Counter Types](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).</span></span>

<span data-ttu-id="a5c5c-109">如需有關高效能提供者和腳本的詳細資訊，請參閱 [WMI 效能計數器類型](wmi-performance-counter-types.md)。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-109">For more information about high-performance providers and scripting, see [WMI Performance Counter Types](wmi-performance-counter-types.md).</span></span>

## <a name="example-code"></a><span data-ttu-id="a5c5c-110">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="a5c5c-110">Example Code</span></span>

<span data-ttu-id="a5c5c-111">如需程式碼範例，請參閱 [取得統計效能資料](obtaining-statistical-performance-data.md)。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-111">For code examples, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5c5c-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="a5c5c-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5c5c-113">統計計數器類型</span><span class="sxs-lookup"><span data-stu-id="a5c5c-113">Statistical Counter Types</span></span>](statistical-counter-types.md)
</dt> <dt>

[<span data-ttu-id="a5c5c-114">監視效能資料</span><span class="sxs-lookup"><span data-stu-id="a5c5c-114">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
