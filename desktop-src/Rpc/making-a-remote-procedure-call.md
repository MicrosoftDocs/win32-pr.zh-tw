---
title: 進行遠端程序呼叫
description: 一旦使用明確系結控制碼的分散式應用程式的用戶端程式具有系結控制碼，就可以執行遠端程式。
ms.assetid: f424bb01-e562-49eb-abaf-cc2d76a6ad8f
keywords:
- 遠端程序呼叫 RPC、工作、進行呼叫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a97095d7eda8227f2369f5e3776faf8ce04c22f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103670988"
---
# <a name="making-a-remote-procedure-call"></a><span data-ttu-id="30961-104">進行遠端程序呼叫</span><span class="sxs-lookup"><span data-stu-id="30961-104">Making a Remote Procedure Call</span></span>

<span data-ttu-id="30961-105">一旦使用明確系結控制碼的分散式應用程式的用戶端程式具有系結控制碼，就可以執行遠端程式。</span><span class="sxs-lookup"><span data-stu-id="30961-105">Once the client program of distributed applications that uses explicit binding handles has a binding handle, it can execute remote procedures.</span></span>

<span data-ttu-id="30961-106">Microsoft RPC 也提供自訂系結控制碼、隱含的系結控制碼，以及自動系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="30961-106">Microsoft RPC also offers custom binding handles, implicit binding handles, and automatic binding handles.</span></span> <span data-ttu-id="30961-107">這些系結處理可提供用戶端和伺服器程式不同層級的控制，以控制執行遠端程式的過程。</span><span class="sxs-lookup"><span data-stu-id="30961-107">These binding handles offer client and server programs different levels of control over the process of executing remote procedures.</span></span> <span data-ttu-id="30961-108">如需不同的控制碼類型以及它們所提供之彈性的詳細資訊，請參閱系結 [和控點](binding-and-handles.md)。</span><span class="sxs-lookup"><span data-stu-id="30961-108">For details on different handle types and the flexibility they offer, see [Binding and Handles](binding-and-handles.md).</span></span>

<span data-ttu-id="30961-109">若要從遠端執行程序呼叫，請以呼叫任何 C 函數的相同方式來呼叫用戶端存根函式。</span><span class="sxs-lookup"><span data-stu-id="30961-109">To execute the procedure call remotely, call the client-side stub function in the same manner any C function is called.</span></span>

 

 




