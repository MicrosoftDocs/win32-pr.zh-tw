---
description: 某些公式需要計數器屬性和基底屬性。
ms.assetid: c14be351-e712-40bd-bab7-5b9ef6cd8a00
ms.tgt_platform: multiple
title: 基底計數器類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e481fbf093245813d0ce0de2b5f7906316c2378
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194350"
---
# <a name="base-counter-types"></a><span data-ttu-id="9cdd3-103">基底計數器類型</span><span class="sxs-lookup"><span data-stu-id="9cdd3-103">Base Counter Types</span></span>

<span data-ttu-id="9cdd3-104">某些公式需要計數器屬性和基底屬性。</span><span class="sxs-lookup"><span data-stu-id="9cdd3-104">Some formulas require both a counter property and base property.</span></span> <span data-ttu-id="9cdd3-105">基底值是計數器類型公式中的分母。</span><span class="sxs-lookup"><span data-stu-id="9cdd3-105">The base value is the denominator in the formula for the counter type.</span></span> <span data-ttu-id="9cdd3-106">在衍生自 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)的原始資料 [效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes)中，基底屬性必須緊接在計數器屬性之後。</span><span class="sxs-lookup"><span data-stu-id="9cdd3-106">In raw data [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata), the base property must immediately follow the counter property.</span></span> <span data-ttu-id="9cdd3-107">基底屬性和先前的計數器必須有相同的名稱，並附加 **\_ 基底**。</span><span class="sxs-lookup"><span data-stu-id="9cdd3-107">The base property must have the same name as the preceding counter, with **\_Base** appended.</span></span>

<span data-ttu-id="9cdd3-108">例如， [**Win32 \_ PerfRawData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md)中的 **AvgDiskBytesPerRead** 屬性包含在讀取作業期間從磁片傳輸的原始值（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="9cdd3-108">For example, the **AvgDiskBytesPerRead** property in [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) contains the raw value, in bytes, transferred from the disk during read operations.</span></span> <span data-ttu-id="9cdd3-109">它有基底屬性 **AvgDiskBytesPerRead \_ 基底**，其代表累積的作業數目。</span><span class="sxs-lookup"><span data-stu-id="9cdd3-109">It has a base property, **AvgDiskBytesPerRead\_Base**, which represents the accumulated number of operations.</span></span> <span data-ttu-id="9cdd3-110">當 WMI 套用指定之計數器類型的公式時， **效能 \_ 平均 \_ 基底** **AvgDiskBytesPerRead** 會除以 **AvgDiskBytesPerRead \_ 基底** ，以產生平均值。</span><span class="sxs-lookup"><span data-stu-id="9cdd3-110">When WMI applies the formula for the specified counter type, **PERF\_AVERAGE\_BASE**, **AvgDiskBytesPerRead** is divided by **AvgDiskBytesPerRead\_Base** to produce the average value.</span></span> <span data-ttu-id="9cdd3-111">此值會出現在 [系統監視器] 中，並儲存在對應的 [ [**Win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) ] 屬性中。</span><span class="sxs-lookup"><span data-stu-id="9cdd3-111">This value appears in System Monitor and is stored in the corresponding [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) property.</span></span> <span data-ttu-id="9cdd3-112">基底屬性只會用於原始資料類別。</span><span class="sxs-lookup"><span data-stu-id="9cdd3-112">Base properties are only used in raw data classes.</span></span>

<span data-ttu-id="9cdd3-113">在衍生自 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)的類別中， **計數器** 限定詞會指定原始類別中的分子屬性，而 **基底** 限定詞會指定基底分母屬性。</span><span class="sxs-lookup"><span data-stu-id="9cdd3-113">In classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), the **Counter** qualifier specifies the numerator property in the raw class and the **Base** qualifier specifies the base denominator property.</span></span>

<span data-ttu-id="9cdd3-114">下表列出 **CounterType** 常數值。</span><span class="sxs-lookup"><span data-stu-id="9cdd3-114">The following table lists the **CounterType** constant values.</span></span>



| <span data-ttu-id="9cdd3-115">CounterType 常數</span><span class="sxs-lookup"><span data-stu-id="9cdd3-115">CounterType Constant</span></span>                                                                                      | <span data-ttu-id="9cdd3-116">Description</span><span class="sxs-lookup"><span data-stu-id="9cdd3-116">Description</span></span>                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cdd3-117">[效能 \_平均 \_ 基底](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))十進位1073939458</span><span class="sxs-lookup"><span data-stu-id="9cdd3-117">[PERF\_AVERAGE\_BASE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 1073939458</span></span><br/>        | <span data-ttu-id="9cdd3-118">用來計算效能 **\_ 平均 \_ 計時器** 和效能 **\_ 平均 \_ 大量** 計數器類型的基底值。</span><span class="sxs-lookup"><span data-stu-id="9cdd3-118">Base value used to calculate the **PERF\_AVERAGE\_TIMER** and **PERF\_AVERAGE\_BULK** counter types.</span></span>                                                                                             |
| <span data-ttu-id="9cdd3-119">[效能 \_計數器 \_ 多重 \_ 基底](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))十進位1107494144</span><span class="sxs-lookup"><span data-stu-id="9cdd3-119">[PERF\_COUNTER\_MULTI\_BASE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 1107494144</span></span><br/> | <span data-ttu-id="9cdd3-120">用來計算 **性能 \_ 計數器 \_ 多重 \_ 計時器** 的基底值、 **性能 \_ 計數器 \_ 多個計時器的 \_ \_ 庫存**、效能 **\_ 100NSEC \_ 多重 \_ 計時器**，以及效能 **\_ 100NSEC \_ 多重 \_ 計時器 \_** 的類型計數器類型。</span><span class="sxs-lookup"><span data-stu-id="9cdd3-120">Base value used to calculate the **PERF\_COUNTER\_MULTI\_TIMER**, **PERF\_COUNTER\_MULTI\_TIMER\_INV**, **PERF\_100NSEC\_MULTI\_TIMER**, and **PERF\_100NSEC\_MULTI\_TIMER\_INV** counter types.</span></span> |
| <span data-ttu-id="9cdd3-121">[效能 \_大型 \_ 原始 \_ 基底](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))十進位1073939712</span><span class="sxs-lookup"><span data-stu-id="9cdd3-121">[PERF\_LARGE\_RAW\_BASE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 1073939712</span></span><br/>     | <span data-ttu-id="9cdd3-122">在計算效能 **\_ 原始 \_ 分數** 64 位時，所找到的基底值。</span><span class="sxs-lookup"><span data-stu-id="9cdd3-122">Base value found in the calculation of **PERF\_RAW\_FRACTION**, 64 bits.</span></span>                                                                                                                         |
| <span data-ttu-id="9cdd3-123">[效能 \_原始 \_ 基底](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))十進位1073939459</span><span class="sxs-lookup"><span data-stu-id="9cdd3-123">[PERF\_RAW\_BASE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 1073939459</span></span><br/>            | <span data-ttu-id="9cdd3-124">用來計算 **性能 \_ 原始 \_ 分數** 計數器類型的基底值。</span><span class="sxs-lookup"><span data-stu-id="9cdd3-124">Base value used to calculate the **PERF\_RAW\_FRACTION** counter type.</span></span>                                                                                                                           |
| <span data-ttu-id="9cdd3-125">[效能 \_範例 \_ 基底](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))十進位1073939457</span><span class="sxs-lookup"><span data-stu-id="9cdd3-125">[PERF\_SAMPLE\_BASE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 1073939457</span></span><br/>         | <span data-ttu-id="9cdd3-126">用來計算效能 **\_ 範例 \_ 計數器** 和效能 **\_ 樣本 \_ 分數** 計數器類型的基底值。</span><span class="sxs-lookup"><span data-stu-id="9cdd3-126">Base value used to calculate the **PERF\_SAMPLE\_COUNTER** and **PERF\_SAMPLE\_FRACTION** counter types.</span></span>                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="9cdd3-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="9cdd3-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cdd3-128">WMI 效能計數器類型</span><span class="sxs-lookup"><span data-stu-id="9cdd3-128">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> <dt>

<span data-ttu-id="9cdd3-129">[計數器類型](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="9cdd3-129">[Counter Types](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))</span></span>
</dt> </dl>

 

