---
description: 深入瞭解： Server2003Grbits. WaitAllLevel0Commit 欄位
title: 'Server2003Grbits. WaitAllLevel0Commit 欄位 (欄位，Server2003) '
TOCTitle: WaitAllLevel0Commit field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.WaitAllLevel0Commit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits.waitalllevel0commit(v=EXCHG.10)
ms:contentKeyID: 55104104
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.WaitAllLevel0Commit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.WaitAllLevel0Commit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16390069adf81ead8e819bc5148a88e30900b508
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849537"
---
# <a name="server2003grbitswaitalllevel0commit-field"></a><span data-ttu-id="6aa73-103">Server2003Grbits. WaitAllLevel0Commit 欄位</span><span class="sxs-lookup"><span data-stu-id="6aa73-103">Server2003Grbits.WaitAllLevel0Commit field</span></span>

<span data-ttu-id="6aa73-104">所有先前由尚未排清至交易記錄檔的會話所認可的交易，都會立即進行清除。</span><span class="sxs-lookup"><span data-stu-id="6aa73-104">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="6aa73-105">此 API 會等到交易已排清之後，再返回呼叫端。</span><span class="sxs-lookup"><span data-stu-id="6aa73-105">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="6aa73-106">即使會話目前不在交易中，也可以使用此選項。</span><span class="sxs-lookup"><span data-stu-id="6aa73-106">This option may be used even if the session is not currently in a transaction.</span></span> <span data-ttu-id="6aa73-107">此選項不能與任何其他選項搭配使用。</span><span class="sxs-lookup"><span data-stu-id="6aa73-107">This option cannot be used in combination with any other option.</span></span>

<span data-ttu-id="6aa73-108">**命名空間：**  [Microsoft Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6aa73-108">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="6aa73-109">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="6aa73-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6aa73-110">語法</span><span class="sxs-lookup"><span data-stu-id="6aa73-110">Syntax</span></span>

``` vb
'Declaration
Public Const WaitAllLevel0Commit As CommitTransactionGrbit
'Usage
Dim value As CommitTransactionGrbit

value = Server2003Grbits.WaitAllLevel0Commit
```

``` csharp
public const CommitTransactionGrbit WaitAllLevel0Commit
```

## <a name="see-also"></a><span data-ttu-id="6aa73-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6aa73-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6aa73-112">參考</span><span class="sxs-lookup"><span data-stu-id="6aa73-112">Reference</span></span>

[<span data-ttu-id="6aa73-113">Server2003Grbits 類別</span><span class="sxs-lookup"><span data-stu-id="6aa73-113">Server2003Grbits class</span></span>](./server2003grbits-class.md)

[<span data-ttu-id="6aa73-114">Server2003Grbits 成員</span><span class="sxs-lookup"><span data-stu-id="6aa73-114">Server2003Grbits members</span></span>](./server2003grbits-members.md)

[<span data-ttu-id="6aa73-115">Server2003 命名空間。</span><span class="sxs-lookup"><span data-stu-id="6aa73-115">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
