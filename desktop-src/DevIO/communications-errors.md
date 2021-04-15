---
description: 在其他情況下，可以使用少於所要求的字元數來完成讀取或寫入作業，即使尚未發生超時時間也一樣。
ms.assetid: 05f84661-34ff-4e1f-9ec8-e4682138dfee
title: 通訊錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eeace990620928ce898a3e8a31049a0083cdf07
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468229"
---
# <a name="communications-errors"></a><span data-ttu-id="838d6-103">通訊錯誤</span><span class="sxs-lookup"><span data-stu-id="838d6-103">Communications Errors</span></span>

<span data-ttu-id="838d6-104">在其他情況下，可以使用少於所要求的字元數來完成讀取或寫入作業，即使尚未發生超時時間也一樣。</span><span class="sxs-lookup"><span data-stu-id="838d6-104">There are other circumstances where a read or write operation can be completed with fewer than the requested number of characters, even though a time-out has not occurred.</span></span> <span data-ttu-id="838d6-105">下列是一些範例：</span><span class="sxs-lookup"><span data-stu-id="838d6-105">Following are some examples:</span></span>

-   <span data-ttu-id="838d6-106">有些驅動程式支援使用特殊字元，這項作業會立即完成讀取作業，只使用收到的字元數。</span><span class="sxs-lookup"><span data-stu-id="838d6-106">Some drivers support the use of special characters, which complete a read operation immediately with only the characters that have been read up to the point when they are received.</span></span>
-   <span data-ttu-id="838d6-107">您可以呼叫 [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) 函數，以提前終止暫止的讀取或寫入作業。</span><span class="sxs-lookup"><span data-stu-id="838d6-107">The [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) function can be called to prematurely terminate pending read or write operations.</span></span> <span data-ttu-id="838d6-108">此函數也可以刪除輸出或輸入緩衝區的內容，或兩者。</span><span class="sxs-lookup"><span data-stu-id="838d6-108">This function can also delete the contents of the output or input buffers, or both.</span></span>
-   <span data-ttu-id="838d6-109">如果在讀取或寫入作業期間發生通訊錯誤，則會終止通訊資源上的所有 i/o 作業。</span><span class="sxs-lookup"><span data-stu-id="838d6-109">If a communications error occurs during a read or write operation, all I/O operations on the communications resource are terminated.</span></span> <span data-ttu-id="838d6-110">中斷條件、同位檢查錯誤或框架錯誤都是這類錯誤的範例。</span><span class="sxs-lookup"><span data-stu-id="838d6-110">Break conditions, parity errors, or framing errors are examples of such errors.</span></span> <span data-ttu-id="838d6-111">發生錯誤時，處理常式必須呼叫 [**ClearCommError**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror) 函式來清除錯誤旗標，然後才能開始其他 i/o 作業。</span><span class="sxs-lookup"><span data-stu-id="838d6-111">When an error occurs, the process must call the [**ClearCommError**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror) function to clear the error flag before it can begin additional I/O operations.</span></span> <span data-ttu-id="838d6-112">**ClearCommError** 會報告發生的特定錯誤，以及裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="838d6-112">**ClearCommError** reports the specific error that occurred and the current status of the device.</span></span>

 

 



