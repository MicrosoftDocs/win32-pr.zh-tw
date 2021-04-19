---
title: delete timeout
description: 刪除全域超時，使 HTTP.sys 服務還原為預設值。
ms.assetid: 5fcd5df4-023e-486d-b41a-639e210a128f
keywords:
- 刪除 timeout HTTP
topic_type:
- apiref
api_name:
- delete timeout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6ee436e1eb7f545a74aa56f6c146afbd1c57066
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "106967236"
---
# <a name="delete-timeout"></a>delete timeout

刪除全域超時，使 HTTP.sys 服務還原為預設值。

``` syntax
delete timeout [timeouttype=]{idleconnectiontimeout|headerwaittimeout}
 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[timeouttype = \] {idleconnectiontimeout \| headerwaittimeout}**
</dt> <dd>

指定逾時設定的類型。

</dd> </dl>

## <a name="examples"></a>範例

**delete timeout timeouttype=idleconnectiontimeout**

**delete timeout timeouttype=headerwaittimeout**

 

 




