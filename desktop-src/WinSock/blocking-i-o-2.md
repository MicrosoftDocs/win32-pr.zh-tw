---
description: Windows 通訊端2中最簡單的 i/o 形式是封鎖 i/o。
ms.assetid: 8ed7e5a8-c577-4b61-9c49-8fd065d84af4
title: 封鎖輸入/輸出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c846a22fcf9d10f562a48683c2ead723f9bd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998066"
---
# <a name="blocking-inputoutput"></a><span data-ttu-id="211d6-103">封鎖輸入/輸出</span><span class="sxs-lookup"><span data-stu-id="211d6-103">Blocking Input/Output</span></span>

<span data-ttu-id="211d6-104">Windows 通訊端2中最簡單的 i/o 形式是封鎖 i/o。</span><span class="sxs-lookup"><span data-stu-id="211d6-104">The simplest form of I/O in Windows Sockets 2 is blocking I/O.</span></span> <span data-ttu-id="211d6-105">如同 [通訊端屬性旗標和模式](socket-attribute-flags-and-modes-2.md)所述，通訊端預設會在封鎖模式中建立。</span><span class="sxs-lookup"><span data-stu-id="211d6-105">As mentioned in [Socket Attribute Flags and Modes](socket-attribute-flags-and-modes-2.md), sockets are created in blocking mode by default.</span></span> <span data-ttu-id="211d6-106">所有具有封鎖通訊端的 i/o 作業都不會傳回，直到作業完全完成為止。</span><span class="sxs-lookup"><span data-stu-id="211d6-106">Any I/O operation with a blocking socket will not return until the operation has been fully completed.</span></span> <span data-ttu-id="211d6-107">因此，任何執行緒一次只能執行一個 i/o 作業。</span><span class="sxs-lookup"><span data-stu-id="211d6-107">Thus, any thread can only execute one I/O operation at a time.</span></span> <span data-ttu-id="211d6-108">例如，如果執行緒發出接收作業，而且目前沒有資料可用，執行緒將會封鎖，直到資料變成可用並放入執行緒的緩衝區為止。</span><span class="sxs-lookup"><span data-stu-id="211d6-108">For example, if a thread issues a receive operation and no data is currently available, the thread will block until data becomes available and is placed into the thread's buffer.</span></span> <span data-ttu-id="211d6-109">雖然這很簡單，但不一定是最有效率的作法 (查看 [虛擬封鎖和真正的封鎖](pseudo-vs--true-blocking-2.md) ，) 的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="211d6-109">Although this is simple, it is not necessarily the most efficient way to do I/O (see [Pseudo Blocking and True Blocking](pseudo-vs--true-blocking-2.md) for more information).</span></span>

 

 



