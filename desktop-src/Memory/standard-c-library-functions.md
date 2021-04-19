---
description: 應用程式可以安全地使用 C 執行時間程式庫的記憶體管理功能 (malloc、free 等等) 和 c + + (new、delete 等) 。
ms.assetid: c58ed263-577d-47c5-93cb-5a7c83604171
title: 標準 C 程式庫函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303333b32f5645f19d8d22a072d25692cea4607f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972271"
---
# <a name="standard-c-library-functions"></a><span data-ttu-id="0c176-103">標準 C 程式庫函式</span><span class="sxs-lookup"><span data-stu-id="0c176-103">Standard C Library Functions</span></span>

<span data-ttu-id="0c176-104">應用程式可以安全地使用 C 執行時間程式庫的記憶體管理功能 (**malloc**、 **free** 等等) 和 c + + (**new**、 **delete** 等) 。</span><span class="sxs-lookup"><span data-stu-id="0c176-104">Applications can safely use the memory management features of the C run-time library (**malloc**, **free**, and so on) and C++ (**new**, **delete**, and so on).</span></span> <span data-ttu-id="0c176-105">C 執行時間程式庫函式在16位 Windows 下沒有可能的問題。</span><span class="sxs-lookup"><span data-stu-id="0c176-105">The C run-time library functions do not have the potential problems they have under 16-bit Windows.</span></span> <span data-ttu-id="0c176-106">記憶體管理不再是問題，因為系統可以在不影響虛擬位址的情況下，藉由移動實體記憶體的頁面來自由管理記憶體。</span><span class="sxs-lookup"><span data-stu-id="0c176-106">Memory management is no longer a problem because the system is free to manage memory by moving pages of physical memory without affecting the virtual addresses.</span></span> <span data-ttu-id="0c176-107">同樣地，接近和遠指標之間的差異不再相關。</span><span class="sxs-lookup"><span data-stu-id="0c176-107">Similarly, the distinction between near and far pointers is no longer relevant.</span></span> <span data-ttu-id="0c176-108">因此，您可以使用標準 C 程式庫函數進行記憶體管理。</span><span class="sxs-lookup"><span data-stu-id="0c176-108">Therefore, you can use the standard C library functions for memory management.</span></span> <span data-ttu-id="0c176-109">不過，記憶體管理函式確實提供了 C 執行時間程式庫中無法使用的功能。</span><span class="sxs-lookup"><span data-stu-id="0c176-109">However, the memory management functions do provide functionality that is unavailable in the C run-time library.</span></span>

 

 



