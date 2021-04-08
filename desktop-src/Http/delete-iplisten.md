---
title: delete iplisten
description: 指定要從 IP 接聽清單中刪除的 IPv4 或 IPv6 位址。
ms.assetid: 1d0935a5-77de-4fdf-8d3b-88c8578bd5c7
keywords:
- 刪除 iplisten HTTP
topic_type:
- apiref
api_name:
- delete iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed7356d8dea3b4313a46c7d7906de15b7389edc
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "104022703"
---
# <a name="delete-iplisten"></a>delete iplisten

指定要從 IP 接聽清單中刪除的 IPv4 或 IPv6 位址。

``` syntax
delete iplisten [ address=] IPAddress
 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="_address___IPAddress"></span><span id="_address___ipaddress"></span><span id="_ADDRESS___IPADDRESS"></span>**\[ 位址 = \]** *IPAddress*
</dt> <dd>

指定要從 IP 接聽清單中刪除的 IPv4 或 IPv6 位址。

</dd> </dl>

## <a name="remarks"></a>備註

刪除 ip 接聽清單的 IP 位址。 其中不包括連接埠號碼。 IP 接聽清單可用來界定 HTTP 服務所繫結的位址清單範圍。 "0.0.0.0" 表示任何 IPv4 位址，"::" 表示任何 IPv6 位址。

## <a name="examples"></a>範例

**delete iplisten address = fe80：：1**

**delete iplisten address = 1.1.1。1**

**delete iplisten address = 0.0.0。0**

**delete iplisten address =：：**

 

 




