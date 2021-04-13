---
title: show sslcert
description: 列出 SSL 伺服器憑證系結，以及 IP 位址和埠的對應用戶端憑證原則。
ms.assetid: 8e20f55e-a357-4f9c-a24e-e234607c3196
keywords:
- 顯示 sslcert HTTP
topic_type:
- apiref
api_name:
- show sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b71c2faf370066f5ce8d5ce6a20b173a74d0f645
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "104313323"
---
# <a name="show-sslcert"></a>show sslcert

列出 SSL 伺服器憑證系結，以及 IP 位址和埠的對應用戶端憑證原則。

``` syntax
show sslcert [ipport=]IP Address:port
 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ipport = \] * * * IP 位址：埠*
</dt> <dd>

指定將顯示 SSL 憑證系結的 IPv4 或 IPv6 位址和埠。 未指定 ipport 會列出所有的系結。

</dd> </dl>

## <a name="examples"></a>範例

**顯示 sslcert ipport = \[ fe80：： 1 \] ：443**

**show sslcert ipport=1.1.1.1:443**

**show sslcert ipport=0.0.0.0:443**

**顯示 sslcert ipport = \[ ：： \] ：443**

 

 




