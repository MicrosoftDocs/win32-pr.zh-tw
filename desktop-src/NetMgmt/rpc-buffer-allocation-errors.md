---
title: RPC 緩衝區配置錯誤
description: 因為 RPC 執行時間程式庫會為傳送和接收緩衝區配置記憶體，所以函式應該會預期 RPC 配置錯誤。
ms.assetid: be9105df-1183-48d6-8cea-391ca628c8b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbe48c113d644447b5ff7b69988f2534d7de3a9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300804"
---
# <a name="rpc-buffer-allocation-errors"></a><span data-ttu-id="17ef7-103">RPC 緩衝區配置錯誤</span><span class="sxs-lookup"><span data-stu-id="17ef7-103">RPC Buffer Allocation Errors</span></span>

<span data-ttu-id="17ef7-104">因為 RPC 執行時間程式庫會為傳送和接收緩衝區配置記憶體，所以函式應該會預期 RPC 配置錯誤。</span><span class="sxs-lookup"><span data-stu-id="17ef7-104">Because the RPC run-time library allocates memory for send and receive buffers, the function should expect RPC allocation errors.</span></span> <span data-ttu-id="17ef7-105">發生 RPC 配置錯誤時，可繼續的控制碼會失效。</span><span class="sxs-lookup"><span data-stu-id="17ef7-105">In the event of an RPC allocation error, a resumable handle is invalidated.</span></span> <span data-ttu-id="17ef7-106">這是一項需求，因為無法 rewindable 可繼續的函式。</span><span class="sxs-lookup"><span data-stu-id="17ef7-106">This is a requirement because resumable functions are not rewindable.</span></span>

 

 




