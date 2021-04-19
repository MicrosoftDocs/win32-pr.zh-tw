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
# <a name="show-servicestate"></a>show servicestate

顯示 HTTP 服務的快照集。

``` syntax
show servicestate [[view=]{session|requestq}] [[verbose=]{yes|no}]
 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="__view___session_requestq__"></span><span id="__VIEW___SESSION_REQUESTQ__"></span>**\[\[view = \] {session \| requestq}\]**
</dt> <dd>

根據伺服器會話或要求佇列，查看 HTTP 服務狀態的快照集。

</dd> <dt>

<span id="__verbose___yes_no__"></span><span id="__VERBOSE___YES_NO__"></span>**\[\[詳細資訊 = \] {yes \| 否}\]**
</dt> <dd>

查看顯示內容資訊的詳細資訊資訊。

</dd> </dl>

## <a name="examples"></a>範例

**顯示 servicestate view = session**

**顯示 servicestate view = requestq verbose = yes**

 

 




