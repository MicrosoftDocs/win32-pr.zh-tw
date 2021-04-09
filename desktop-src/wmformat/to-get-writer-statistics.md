---
title: 取得寫入器統計資料
description: 取得寫入器統計資料
ms.assetid: 81d7f567-0d99-4199-9248-1a497dc2eaab
keywords:
- Advanced Systems Format (ASF) 、寫入器統計資料
- ASF (Advanced 系統格式) 、寫入器統計資料
- 寫入器統計資料，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c6620a2410b08d4d605c4dc116366c24b1e52c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "103933008"
---
# <a name="to-get-writer-statistics"></a><span data-ttu-id="1993b-106">取得寫入器統計資料</span><span class="sxs-lookup"><span data-stu-id="1993b-106">To Get Writer Statistics</span></span>

<span data-ttu-id="1993b-107">寫入器可以提供有關撰寫作業的統計資訊。</span><span class="sxs-lookup"><span data-stu-id="1993b-107">The writer can provide statistical information about writing operations.</span></span> <span data-ttu-id="1993b-108">有兩種方法可以收集寫入器統計資料： [**IWMWriterAdvanced：： GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics) 和 [**IWMWriterAdvanced3：： GetStatisticsEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex)。</span><span class="sxs-lookup"><span data-stu-id="1993b-108">There are two methods for gathering writer statistics: [**IWMWriterAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics) and [**IWMWriterAdvanced3::GetStatisticsEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex).</span></span> <span data-ttu-id="1993b-109">**GetStatisticsEx** 抓取的資訊比 **GetStatistics** 所抓取的資訊更明確。</span><span class="sxs-lookup"><span data-stu-id="1993b-109">The information retrieved by **GetStatisticsEx** is more specific than the information retrieved by **GetStatistics**.</span></span>

<span data-ttu-id="1993b-110">這兩種方法都會以統計資訊填入結構。</span><span class="sxs-lookup"><span data-stu-id="1993b-110">Both methods populate structures with statistical information.</span></span> <span data-ttu-id="1993b-111">**GetStatistics** 會使用 [**wm \_ 寫入器 \_ 統計資料**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics) 結構，而 **GetStatisticsEx** 會使用 [**wm \_ 寫入器 \_ 統計資料 \_ EX**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex) 結構。</span><span class="sxs-lookup"><span data-stu-id="1993b-111">**GetStatistics** uses the [**WM\_WRITER\_STATISTICS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics) structure, and **GetStatisticsEx** uses the [**WM\_WRITER\_STATISTICS\_EX**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex) structure.</span></span> <span data-ttu-id="1993b-112">**GetStatisticsEx** 不會複製 **GetStatistics** 所取得的資料。</span><span class="sxs-lookup"><span data-stu-id="1993b-112">**GetStatisticsEx** does not duplicate the data obtained by **GetStatistics**.</span></span> <span data-ttu-id="1993b-113">如需最完整的資訊，您應該呼叫這兩種方法。</span><span class="sxs-lookup"><span data-stu-id="1993b-113">For the most complete information, you should call both methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1993b-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="1993b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1993b-115">**IWMWriterAdvanced 介面**</span><span class="sxs-lookup"><span data-stu-id="1993b-115">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="1993b-116">**IWMWriterAdvanced3 介面**</span><span class="sxs-lookup"><span data-stu-id="1993b-116">**IWMWriterAdvanced3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)
</dt> <dt>

[<span data-ttu-id="1993b-117">**寫入 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="1993b-117">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




