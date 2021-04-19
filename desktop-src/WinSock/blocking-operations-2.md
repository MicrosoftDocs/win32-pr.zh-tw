---
description: 在 Windows 環境中封鎖的概念，一直以來都是非常重要的。
ms.assetid: bd2ede96-34a4-4912-b9d2-ef11d37d2292
title: 封鎖作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8040865b4c6ededab925279e15d67cb89f7bc6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973063"
---
# <a name="blocking-operations"></a><span data-ttu-id="81438-103">封鎖作業</span><span class="sxs-lookup"><span data-stu-id="81438-103">Blocking Operations</span></span>

<span data-ttu-id="81438-104">在 Windows 環境中封鎖的概念，一直以來都是非常重要的。</span><span class="sxs-lookup"><span data-stu-id="81438-104">The notion of blocking in a Windows environment has historically been a very important one.</span></span> <span data-ttu-id="81438-105">在 Windows 通訊端1.1 環境中，不建議使用封鎖呼叫，因為它們比起停用與系統的持續互動。</span><span class="sxs-lookup"><span data-stu-id="81438-105">In Windows Sockets 1.1 environments, blocking calls were discouraged since they tended to disable ongoing interaction with the system.</span></span> <span data-ttu-id="81438-106">此外，它們也採用 pseudoblocking 技術，基於各種原因，不一定會如預期運作。</span><span class="sxs-lookup"><span data-stu-id="81438-106">Additionally, they employ a pseudoblocking technique which, for a variety of reasons, does not always work as intended.</span></span> <span data-ttu-id="81438-107">不過，在事先排程的 Windows 環境中，封鎖呼叫會更有意義，可由原生作業系統服務來執行，事實上通常是慣用的機制。</span><span class="sxs-lookup"><span data-stu-id="81438-107">However, in preemptively scheduled Windows environments, blocking calls make much more sense, can be implemented by native operating system services, and are in fact a generally preferred mechanism.</span></span> <span data-ttu-id="81438-108">Winsock 2 API 已不再支援 psuedoblocking，但因為 Windows 通訊端1.1 相容性填充碼必須繼續模擬這項行為，所以服務提供者必須支援這項功能，如下所述。</span><span class="sxs-lookup"><span data-stu-id="81438-108">The Winsock 2 API no longer supports psuedoblocking, but because the Windows Sockets 1.1 compatibility shims must continue to emulate this behavior, service providers must support this as described in the following.</span></span>

 

 



