---
title: add iplisten
description: 指定要新增至 IP 接聽清單的 IPv4 或 IPv6 位址。
ms.assetid: 38253818-c029-4a46-ab52-095cbfdeeaf4
keywords:
- 新增 iplisten HTTP
topic_type:
- apiref
api_name:
- add iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2133a3f590c46c9e27b518d7621c158b86895961acb07670f6603e03513d1cc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014976"
---
# <a name="add-iplisten"></a>add iplisten

指定要新增至 IP 接聽清單的 IPv4 或 IPv6 位址。

``` syntax
add iplisten [ ipaddress=] IPAddress
 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="__ipaddress___IPAddress"></span><span id="__ipaddress___ipaddress"></span><span id="__ipADDRESS___IPADDRESS"></span>**\[ ipaddress = \]** *ipaddress*
</dt> <dd>

指定要新增至 IP 接聽清單的 IPv4 或 IPv6 位址。

</dd> </dl>

## <a name="remarks"></a>備註

將新的 IP 位址新增至 IP 接聽清單。 其中不包括連接埠號碼。 IP 接聽清單可用來界定 HTTP 服務所繫結的位址清單範圍。 "0.0.0.0" 表示任何 IPv4 位址，"::" 表示任何 IPv6 位址。

## <a name="examples"></a>範例

**add iplisten ipaddress=fe80::1**

**add iplisten ipaddress=1.1.1.1**

**add iplisten ipaddress=0.0.0.0**

**add iplisten ipaddress=::**

 

 




