---
title: show servicestate
description: 顯示 HTTP 服務的快照集。
ms.assetid: a50a3ef5-5e62-412e-a443-11d453778f70
keywords:
- 顯示 servicestate HTTP
topic_type:
- apiref
api_name:
- show servicestate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f79bfdb946d286c31ce284efa09e75ad93c34438
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "106967872"
---
# <a name="show-servicestate"></a><span data-ttu-id="bd041-104">show servicestate</span><span class="sxs-lookup"><span data-stu-id="bd041-104">show servicestate</span></span>

<span data-ttu-id="bd041-105">顯示 HTTP 服務的快照集。</span><span class="sxs-lookup"><span data-stu-id="bd041-105">Shows a snapshot of the HTTP service.</span></span>

``` syntax
show servicestate [[view=]{session|requestq}] [[verbose=]{yes|no}]
 
```

## <a name="parameters"></a><span data-ttu-id="bd041-106">參數</span><span class="sxs-lookup"><span data-stu-id="bd041-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd041-107"><span id="__view___session_requestq__"></span><span id="__VIEW___SESSION_REQUESTQ__"></span>**\[\[view = \] {session \| requestq}\]**</span><span class="sxs-lookup"><span data-stu-id="bd041-107"><span id="__view___session_requestq__"></span><span id="__VIEW___SESSION_REQUESTQ__"></span>**\[\[view=\]{session\|requestq}\]**</span></span>
</dt> <dd>

<span data-ttu-id="bd041-108">根據伺服器會話或要求佇列，查看 HTTP 服務狀態的快照集。</span><span class="sxs-lookup"><span data-stu-id="bd041-108">View snapshot of HTTP service state based on server session or request queues.</span></span>

</dd> <dt>

<span data-ttu-id="bd041-109"><span id="__verbose___yes_no__"></span><span id="__VERBOSE___YES_NO__"></span>**\[\[詳細資訊 = \] {yes \| 否}\]**</span><span class="sxs-lookup"><span data-stu-id="bd041-109"><span id="__verbose___yes_no__"></span><span id="__VERBOSE___YES_NO__"></span>**\[\[verbose=\]{yes\|no}\]**</span></span>
</dt> <dd>

<span data-ttu-id="bd041-110">查看顯示內容資訊的詳細資訊資訊。</span><span class="sxs-lookup"><span data-stu-id="bd041-110">View verbose information showing property information too.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="bd041-111">範例</span><span class="sxs-lookup"><span data-stu-id="bd041-111">Examples</span></span>

<span data-ttu-id="bd041-112">**顯示 servicestate view = session**</span><span class="sxs-lookup"><span data-stu-id="bd041-112">**show servicestate view=session**</span></span>

<span data-ttu-id="bd041-113">**顯示 servicestate view = requestq verbose = yes**</span><span class="sxs-lookup"><span data-stu-id="bd041-113">**show servicestate view=requestq verbose=yes**</span></span>

 

 




