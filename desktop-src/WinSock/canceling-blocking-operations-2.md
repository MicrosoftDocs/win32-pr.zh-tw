---
description: 執行緒隨時都可以呼叫 WSAIsBlocking 來判斷封鎖呼叫是否正在進行中。
ms.assetid: 6213ded4-feab-404f-86a0-3db9a0a42769
title: 取消封鎖作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 502870b8935dc97c1d6c3714808d1c6532780f7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973270"
---
# <a name="canceling-blocking-operations"></a><span data-ttu-id="e364b-103">取消封鎖作業</span><span class="sxs-lookup"><span data-stu-id="e364b-103">Canceling Blocking Operations</span></span>

<span data-ttu-id="e364b-104">執行緒隨時都可以呼叫 [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) 來判斷封鎖呼叫是否正在進行中。</span><span class="sxs-lookup"><span data-stu-id="e364b-104">A thread may, at any time, call [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) to determine whether or not a blocking call is currently in progress.</span></span> <span data-ttu-id="e364b-105"> (此函式會在 Windows 通訊端1.1 相容性填充碼內執行，因此不會有 SPI 對應項。 ) 顯然只有在虛擬封鎖（而不是真正的封鎖）由服務提供者所使用時，才可能發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="e364b-105">(This function is implemented within the Windows Sockets 1.1 compatibility shims and hence has no SPI counterpart.) Clearly this is only possible when pseudo blocking, as opposed to true blocking, is being employed by the service provider.</span></span> <span data-ttu-id="e364b-106">必要時，可以隨時呼叫 [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) ，以取消任何目前的虛擬封鎖作業。</span><span class="sxs-lookup"><span data-stu-id="e364b-106">When necessary, [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) may be called at any time to cancel any current pseudo blocking operation.</span></span>

 

 
