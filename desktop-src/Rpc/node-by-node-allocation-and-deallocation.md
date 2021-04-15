---
title: 節點節點配置和解除配置
description: 由存根進行的節點依節點配置和解除配置資料結構是用戶端和伺服器上所有參數的預設記憶體管理方法。
ms.assetid: 04752fd9-438c-4b52-830b-ce136f83b3b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6cc6b3ff61d4db3ba716664a2ff854e94cb28fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463405"
---
# <a name="node-by-node-allocation-and-deallocation"></a><span data-ttu-id="b2c5d-103">節點節點配置和解除配置</span><span class="sxs-lookup"><span data-stu-id="b2c5d-103">Node-by-Node Allocation and Deallocation</span></span>

<span data-ttu-id="b2c5d-104">由存根進行的節點依節點配置和解除配置資料結構是用戶端和伺服器上所有參數的預設記憶體管理方法。</span><span class="sxs-lookup"><span data-stu-id="b2c5d-104">Node-by-node allocation and deallocation of data structures by the stubs is the default method of memory management for all parameters on both the client and the server.</span></span> <span data-ttu-id="b2c5d-105">在用戶端上，存根會使用對 [midl \_ 使用者 \_ 配置](/windows/desktop/Midl/midl-user-allocate-1)的個別呼叫來配置每個節點。</span><span class="sxs-lookup"><span data-stu-id="b2c5d-105">On the client side, the stub allocates each node with a separate call to [midl\_user\_allocate](/windows/desktop/Midl/midl-user-allocate-1).</span></span> <span data-ttu-id="b2c5d-106">在伺服器端，您可以盡可能使用私用記憶體，而不是呼叫 **midl \_ 使用者 \_ 配置**。</span><span class="sxs-lookup"><span data-stu-id="b2c5d-106">On the server side, rather than calling **midl\_user\_allocate**, private memory is used whenever possible.</span></span> <span data-ttu-id="b2c5d-107">如果呼叫 **midl \_ 使用者 \_ 配置** ，伺服器 stub 會呼叫 **midl \_ 使用者 \_ free** 來釋出資料。</span><span class="sxs-lookup"><span data-stu-id="b2c5d-107">If **midl\_user\_allocate** is called, the server stubs will call **midl\_user\_free** to free the data.</span></span> <span data-ttu-id="b2c5d-108">在大部分的情況下，使用節點對節點的配置和解除配置，而不使用 **\[ 配置 (所有 \_ 節點) \]** 將會導致伺服器端存根的效能提升。</span><span class="sxs-lookup"><span data-stu-id="b2c5d-108">In most cases, using node-by-node allocation and deallocation instead of using **\[allocate (all\_nodes)\]** will result in increased performance of the server side stubs.</span></span>

 

 