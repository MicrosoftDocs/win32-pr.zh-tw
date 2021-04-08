---
description: 精確度計時器演算法計數器類型會取得比系統計時器更精確的讀數。
ms.assetid: f7159645-6287-47a3-895e-20dae6e0892a
ms.tgt_platform: multiple
title: 精確度計時器演算法計數器類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a8864587fedc915678dfa4a9e578ca051e1262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695155"
---
# <a name="precision-timer-algorithm-counter-types"></a><span data-ttu-id="3c102-103">精確度計時器演算法計數器類型</span><span class="sxs-lookup"><span data-stu-id="3c102-103">Precision Timer Algorithm Counter Types</span></span>

<span data-ttu-id="3c102-104">精確度計時器演算法計數器類型會取得比系統計時器更精確的讀數。</span><span class="sxs-lookup"><span data-stu-id="3c102-104">The precision timer algorithm counter types obtain more accurate readings than system timers.</span></span> <span data-ttu-id="3c102-105">提供資料的服務也會提供時間戳記，以消除由於從效能 DLL 捕獲系統時間戳記和收集資料所經過的小和變動時間，而造成的錯誤。</span><span class="sxs-lookup"><span data-stu-id="3c102-105">The service that provides the data also provides a timestamp, which eliminates the errors that can occur because of the small and variable time that elapses between capture of the system timestamp and collection of the data from the performance DLL.</span></span> <span data-ttu-id="3c102-106">精確度計時器的這個基底時間戳記是效能 \_ 精確度 \_ 時間戳記屬性，必須緊接在效能 \_ 精確度 \_ 計時器屬性之後。</span><span class="sxs-lookup"><span data-stu-id="3c102-106">This base timestamp for precision timers is a PERF\_PRECISION\_TIMESTAMP property, which must immediately follow the PERF\_PRECISION\_TIMER property.</span></span>



| <span data-ttu-id="3c102-107">CounterType 常數</span><span class="sxs-lookup"><span data-stu-id="3c102-107">CounterType Constant</span></span>                                                                                         | <span data-ttu-id="3c102-108">Description</span><span class="sxs-lookup"><span data-stu-id="3c102-108">Description</span></span>                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c102-109">[效能 \_PRECISION \_ SYSTEM \_ 計時器](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 541525248</span><span class="sxs-lookup"><span data-stu-id="3c102-109">[PERF\_PRECISION\_SYSTEM\_TIMER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 541525248</span></span><br/> | <span data-ttu-id="3c102-110">類似于性能 \_ 計數器 \_ 計時器，不同之處在于它會使用計數器定義的時間基底，而不是系統時間戳記。</span><span class="sxs-lookup"><span data-stu-id="3c102-110">Similar to PERF\_COUNTER\_TIMER except that it uses a counter defined time base instead of the system timestamp.</span></span>             |
| <span data-ttu-id="3c102-111">[效能 \_有效位數 \_ 100ns \_ 計時器](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))十進位542573824</span><span class="sxs-lookup"><span data-stu-id="3c102-111">[PERF\_PRECISION\_100NS\_TIMER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 542573824</span></span><br/>  | <span data-ttu-id="3c102-112">類似于效能 \_ 100NSEC \_ 計時器，不同之處在于它會使用100ns 個計數器定義的時間基底，而不是系統100ns 時間戳記。</span><span class="sxs-lookup"><span data-stu-id="3c102-112">Similar to PERF\_100NSEC\_TIMER except that it uses a 100ns counter defined time base instead of the system 100ns timestamp.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3c102-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="3c102-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c102-114">WMI 效能計數器類型</span><span class="sxs-lookup"><span data-stu-id="3c102-114">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 

