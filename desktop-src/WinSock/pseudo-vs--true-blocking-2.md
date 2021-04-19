---
description: 在 Windows 通訊端中 Pseudoblocking 虛擬封鎖作業 (Winsock) 。
ms.assetid: fa8f29f1-bb4f-4814-ab8a-52d3c83232bb
title: 虛擬封鎖和真正封鎖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 082992aba884aebec30d35bc65d2cb6c49e29051
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989315"
---
# <a name="pseudo-blocking-and-true-blocking"></a><span data-ttu-id="f77c0-103">虛擬封鎖和真正封鎖</span><span class="sxs-lookup"><span data-stu-id="f77c0-103">Pseudo Blocking and True Blocking</span></span>

<span data-ttu-id="f77c0-104">在16個 Windows 環境中，作業系統不支援真正的封鎖;因此，無法立即完成的封鎖作業會依照下列方式處理：</span><span class="sxs-lookup"><span data-stu-id="f77c0-104">In 16 Windows environments, true blocking is not supported by the operating system; therefore, a blocking operation that cannot be completed immediately is handled as follows:</span></span>

-   <span data-ttu-id="f77c0-105">服務提供者會起始作業，然後輸入迴圈，在這種情況下，它會分派任何 Windows 訊息 (將處理器產生到另一個執行緒（如有需要）) </span><span class="sxs-lookup"><span data-stu-id="f77c0-105">The service provider initiates the operation, and then enters a loop during which it dispatches any Windows messages (yielding the processor to another thread if necessary)</span></span>
-   <span data-ttu-id="f77c0-106">然後，它會檢查 Windows 通訊端函式是否完成。</span><span class="sxs-lookup"><span data-stu-id="f77c0-106">It then checks for the completion of the Windows Sockets function.</span></span>
-   <span data-ttu-id="f77c0-107">如果函式已完成，或已叫用 [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) ，迴圈就會終止，而且封鎖函式會以適當的結果完成。</span><span class="sxs-lookup"><span data-stu-id="f77c0-107">If the function has completed, or if [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) has been invoked, the loop is terminated and the blocking function completes with an appropriate result.</span></span>

<span data-ttu-id="f77c0-108">這是「虛擬封鎖」一詞所指的，而上述的迴圈稱為預設封鎖攔截。</span><span class="sxs-lookup"><span data-stu-id="f77c0-108">This is what is meant by the term pseudo blocking, and the loop referred to above is known as the default blocking hook.</span></span>

 

 
