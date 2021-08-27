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
ms.openlocfilehash: c66a136acf65022ccc3ba8b05d070e4855a64f7abdf9b0519f7c1628d292aa0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047598"
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

<span id="_value__u-short"></span><span id="_VALUE__U-SHORT"></span>**\[ 值 = \]** _u-短_
</dt> <dd>

指定 timeout (的值，以秒為單位) 。 如果值為十六進位，則加入前置詞0x。

</dd> </dl>

## <a name="examples"></a>範例

**add timeout timeouttype=idleconnectiontimeout value=120**

**add timeout timeouttype=headerwaittimeout value=0x40**

 

 




