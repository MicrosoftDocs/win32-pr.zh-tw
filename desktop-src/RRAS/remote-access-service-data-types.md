---
title: '遠端存取服務資料類型 (Ras. h) '
description: 遠端存取服務 API 會使用下列資料類型。
ms.assetid: aaa7f971-9c23-4738-a386-9b7db859f6be
keywords:
- RASIPV4ADDR
- RASIPV6ADDR
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c8aa2fdae531c5aae0986d3289802565c6914fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934342"
---
# <a name="remote-access-service-data-types"></a>遠端存取服務資料類型

遠端存取服務 API 會使用下列資料類型。


```C++
typedef in_addr RASIPV4ADDR;
typedef in6_addr RASIPV6ADDR;
```



<dl> <dt>

**RASIPV4ADDR**
</dt> <dd>

包含 IPv4 位址的 [**in \_ 位址**](/windows/desktop/api/winsock2/ns-winsock2-in_addr) 。

> [!Note]  
> 在 Windows Vista 或更新版本的 Windows 中支援。

 

</dd> <dt>

**RASIPV6ADDR**
</dt> <dd>

包含 IPv6 位址的 [**in6 \_ 位址**](/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)) 。

> [!Note]  
> 在 Windows Vista 或更新版本的 Windows 中支援。

 

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Ras。h</dt> </dl> |



 

