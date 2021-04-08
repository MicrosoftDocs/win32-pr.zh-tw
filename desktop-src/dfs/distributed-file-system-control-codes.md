---
title: 分散式檔案系統控制代碼
description: 分散式檔案系統 DFS 控制碼
ms.assetid: 1d9bebe6-f494-41e5-8a8d-51bf98eaa374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe054f87210c40da595dd731b263c485311729a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933369"
---
# <a name="distributed-file-system-control-codes"></a><span data-ttu-id="d7ac0-103">分散式檔案系統控制代碼</span><span class="sxs-lookup"><span data-stu-id="d7ac0-103">Distributed File System Control Codes</span></span>

<span data-ttu-id="d7ac0-104">以下是 DFS) 控制代碼的分散式檔案系統 (：</span><span class="sxs-lookup"><span data-stu-id="d7ac0-104">The following are the Distributed File System (DFS) control codes:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d7ac0-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="d7ac0-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="d7ac0-106">**FSCTL_DFS_GET_PKT_ENTRY_STATE**</span><span class="sxs-lookup"><span data-stu-id="d7ac0-106">**FSCTL_DFS_GET_PKT_ENTRY_STATE**</span></span>](fsctl-dfs-get-pkt-entry-state.md)
</dt> <dd>

<span data-ttu-id="d7ac0-107">[**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md)控制程式代碼可以取得與 [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)函式相同的資訊，但可在某些設定中提供更佳的效能，而這些設定在 DFS 伺服器上會有高延遲。</span><span class="sxs-lookup"><span data-stu-id="d7ac0-107">The [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) control code can get the same information as the [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) function but can provide better performance in some configurations with high latencies to the DFS servers.</span></span> <span data-ttu-id="d7ac0-108">除非有效能問題，否則不建議使用 **FSCTL_DFS_GET_PKT_ENTRY_STATE** 控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="d7ac0-108">It is not recommended to use the **FSCTL_DFS_GET_PKT_ENTRY_STATE** control code unless there are performance issues.</span></span>

<span data-ttu-id="d7ac0-109">若要執行此作業，請呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。</span><span class="sxs-lookup"><span data-stu-id="d7ac0-109">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function.</span></span>

</dd> </dl>