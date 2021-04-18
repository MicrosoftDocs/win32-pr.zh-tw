---
title: 函式參考
description: 本節說明在 Microsoft RPC 中支援 (RPC) 執行時間函式的遠端程序呼叫。
ms.assetid: 135bef8d-1794-420e-a111-604d02dbcc06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163c68f56a483d3eb7f62596c4a3d78ba2b5774a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462245"
---
# <a name="function-reference"></a><span data-ttu-id="86aca-103">函式參考</span><span class="sxs-lookup"><span data-stu-id="86aca-103">Function Reference</span></span>

<span data-ttu-id="86aca-104">本節說明在 Microsoft RPC 中支援 (RPC) 執行時間函式的遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="86aca-104">This section documents the Remote Procedure Call (RPC) run-time functions supported in Microsoft RPC.</span></span> <span data-ttu-id="86aca-105">本節說明每個函式的用途、語法、輸入參數和傳回值。</span><span class="sxs-lookup"><span data-stu-id="86aca-105">This section describes each function's purpose, syntax, input parameters, and return values.</span></span> <span data-ttu-id="86aca-106">它也會提供額外的資訊，以協助您在應用程式中使用 RPC 函數。</span><span class="sxs-lookup"><span data-stu-id="86aca-106">It also provides additional information to help you use RPC functions in an application.</span></span>

<span data-ttu-id="86aca-107">傳遞至 rpc 函數的所有指標都必須包含 **\_ \_ RPC 最 \_ 遠** 的屬性。</span><span class="sxs-lookup"><span data-stu-id="86aca-107">All pointers passed to RPC functions must include the **\_ \_RPC\_FAR** attribute.</span></span> <span data-ttu-id="86aca-108">例如，指標 rpc 系 **結 \_ \_ 控制碼 \*** 會變成 **\* \***  **\_ \_ \_ \_ \_ \* rpc** 的 rpc 系結控制碼，而 char Ptr 會變成 **char \_ \_ rpc \_ 遠超過 \* \_ \_ \_ \* rpc** 的 *Ptr*。</span><span class="sxs-lookup"><span data-stu-id="86aca-108">For example, the pointer **RPC\_BINDING\_HANDLE \*** becomes **RPC\_BINDING\_HANDLE \_ \_RPC\_FAR \*** and **char \* \*** *Ptr* becomes **char \_ \_RPC\_FAR \* \_ \_RPC\_FAR \*** *Ptr*.</span></span>

<span data-ttu-id="86aca-109">本節提供下列群組中的函數參考：</span><span class="sxs-lookup"><span data-stu-id="86aca-109">This section presents the function references in the following groups:</span></span>

-   [<span data-ttu-id="86aca-110">RPC 函數</span><span class="sxs-lookup"><span data-stu-id="86aca-110">RPC Functions</span></span>](rpc-functions.md)
-   [<span data-ttu-id="86aca-111">RPC 回呼和通知函數</span><span class="sxs-lookup"><span data-stu-id="86aca-111">RPC Callback and Notification Functions</span></span>](rpc-callback-and-notification-functions.md)

 

 




