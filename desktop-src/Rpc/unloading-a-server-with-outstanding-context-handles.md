---
title: 卸載具有未完成內容控制碼的伺服器
description: 傳統上，在不先停止裝載進程的情況下，卸載服務 RPC 呼叫的 DLL 是有問題的。
ms.assetid: d3880578-e542-418c-803a-fd00d0bfde7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1192b013a06def4bb1ee49e08e43b7165c9edfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104184026"
---
# <a name="unloading-a-server-with-outstanding-context-handles"></a><span data-ttu-id="d880e-103">卸載具有未完成內容控制碼的伺服器</span><span class="sxs-lookup"><span data-stu-id="d880e-103">Unloading a Server with Outstanding Context Handles</span></span>

<span data-ttu-id="d880e-104">傳統上，在不先停止裝載進程的情況下，卸載服務 RPC 呼叫的 DLL 是有問題的。</span><span class="sxs-lookup"><span data-stu-id="d880e-104">Traditionally, unloading a DLL that services RPC calls using context handles, without first stopping the hosting process, has been problematic.</span></span> <span data-ttu-id="d880e-105">這是因為卸載 DLL 時，執行關閉常式已不再有效。</span><span class="sxs-lookup"><span data-stu-id="d880e-105">This is because the run-down routine is no longer valid when the DLL is being unloaded.</span></span> <span data-ttu-id="d880e-106">當具有先前開啟之內容控制碼的用戶端失敗，而且 RPC 執行時間嘗試關閉內容控制碼時，嘗試呼叫向下執行常式存取會違反，而伺服器會當機。</span><span class="sxs-lookup"><span data-stu-id="d880e-106">When a client with a previously open context handle fails, and the RPC run time tries to close the context handle, its attempt to call the run-down routine access violates, and the server crashes.</span></span>

<span data-ttu-id="d880e-107">從 Windows XP 開始，已新增名為 [**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex) 的新 API。</span><span class="sxs-lookup"><span data-stu-id="d880e-107">Beginning with Windows XP, a new API called [**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex) has been added.</span></span> <span data-ttu-id="d880e-108">**RpcServerUnregisterIfEx** 會關閉正在取消註冊之介面開啟的內容控制碼; [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) 函數不會。</span><span class="sxs-lookup"><span data-stu-id="d880e-108">**RpcServerUnregisterIfEx** closes context handles opened by the interface being unregistered; the [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) function does not.</span></span> <span data-ttu-id="d880e-109">當整個進程關機時，並不需要使用 RpcServerUnregisterIfEx，但是如果有一個或多個裝載執行時間常式的 Dll 在未處理的內容控制碼存在時卸載，則需要使用 。</span><span class="sxs-lookup"><span data-stu-id="d880e-109">Using **RpcServerUnregisterIfEx** is not necessary when the entire process shuts down, but it is necessary if one or more DLLs hosting the run-down routines is unloaded while outstanding context handles exist.</span></span>

 

 




