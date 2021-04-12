---
title: add timeout
description: 將全域超時新增至 HTTP.sys 服務。
ms.assetid: c59a64e2-36aa-4428-b727-df21f5632d0d
keywords:
- 新增 timeout HTTP
topic_type:
- apiref
api_name:
- add timeout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2637cb5db663ea36b15eb382a16b02b166e98f88
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "104373506"
---
# <a name="add-timeout"></a>add timeout

將全域超時新增至 HTTP.sys 服務。

``` syntax
add timeout [timeouttype=]{idleconnectiontimeout|headerwaittimeout}
            [value=]u-short

 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[timeouttype = \] {idleconnectiontimeout \| headerwaittimeout}**
</dt> <dd>

指定設定的超時類型。

</dd> <dt>

<span id="_value__u-short"></span><span id="_VALUE__U-SHORT"></span>**\[值 = \] * * * u-短*
</dt> <dd>

指定 timeout (的值，以秒為單位) 。 如果值為十六進位，則加入前置詞0x。

</dd> </dl>

## <a name="examples"></a>範例

**add timeout timeouttype=idleconnectiontimeout value=120**

**add timeout timeouttype=headerwaittimeout value=0x40**

 

 




