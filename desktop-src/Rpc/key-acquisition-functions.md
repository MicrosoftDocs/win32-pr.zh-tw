---
title: 金鑰取得函式
description: 根據預設，SSP 會提供加密金鑰給提出要求的伺服器程式。 每個 SSP 都會實行自己產生金鑰的系統。 SSP 產生的金鑰格式是 SSP 專屬的。
ms.assetid: 0ba7212c-6ee8-4a92-94d0-f09f84b05bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36a8c8e8cfb2f3b4f8f241b2401878576cbe7f90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840631"
---
# <a name="key-acquisition-functions"></a><span data-ttu-id="5c9c9-105">金鑰取得函式</span><span class="sxs-lookup"><span data-stu-id="5c9c9-105">Key Acquisition Functions</span></span>

<span data-ttu-id="5c9c9-106">根據預設，SSP 會提供加密金鑰給提出要求的伺服器程式。</span><span class="sxs-lookup"><span data-stu-id="5c9c9-106">By default, the SSP supplies encryption keys to server programs that request them.</span></span> <span data-ttu-id="5c9c9-107">每個 SSP 都會實行自己產生金鑰的系統。</span><span class="sxs-lookup"><span data-stu-id="5c9c9-107">Each SSP implements its own system of generating keys.</span></span> <span data-ttu-id="5c9c9-108">SSP 產生的金鑰格式是 SSP 專屬的。</span><span class="sxs-lookup"><span data-stu-id="5c9c9-108">The format of the keys that the SSP generates are specific to the SSP.</span></span>

<span data-ttu-id="5c9c9-109">RPC 能讓您覆寫產生加密金鑰的預設方法。</span><span class="sxs-lookup"><span data-stu-id="5c9c9-109">RPC provides you with the ability to override the default method of generating encryption keys.</span></span> <span data-ttu-id="5c9c9-110">您的應用程式可以呼叫 [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) 函式，並將指標傳遞給金鑰取得函數。</span><span class="sxs-lookup"><span data-stu-id="5c9c9-110">Your application can call the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function and pass it a pointer to a key acquisition function.</span></span> <span data-ttu-id="5c9c9-111">您可以撰寫金鑰取得函式，讓它使用您所選擇的任何方法來產生金鑰。</span><span class="sxs-lookup"><span data-stu-id="5c9c9-111">You can write the key acquisition function so that it generates keys using any method you choose.</span></span> <span data-ttu-id="5c9c9-112">不過，它傳遞給伺服器程式的金鑰必須符合 SSP 需要的格式。</span><span class="sxs-lookup"><span data-stu-id="5c9c9-112">However, the key it passes to the server program must match the format that the SSP requires.</span></span>

> [!Note]  
> <span data-ttu-id="5c9c9-113">大部分的應用程式都不需要使用金鑰取得函式，而且可以直接將 **Null** 提供給要求金鑰取得函式的所有參數。</span><span class="sxs-lookup"><span data-stu-id="5c9c9-113">Most applications do not need to use key acquisition functions, and can simply supply **NULL** to all parameters where a key acquisition function is requested.</span></span>

 

 

 




