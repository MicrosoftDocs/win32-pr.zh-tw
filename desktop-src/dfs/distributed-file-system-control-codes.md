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
# <a name="distributed-file-system-control-codes"></a>分散式檔案系統控制代碼

以下是 DFS) 控制代碼的分散式檔案系統 (：

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md)
</dt> <dd>

[**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md)控制程式代碼可以取得與 [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)函式相同的資訊，但可在某些設定中提供更佳的效能，而這些設定在 DFS 伺服器上會有高延遲。 除非有效能問題，否則不建議使用 **FSCTL_DFS_GET_PKT_ENTRY_STATE** 控制項程式碼。

若要執行此作業，請呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。

</dd> </dl>