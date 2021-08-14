---
title: 處理保留
description: URL 命名空間部分的保留專案是由系統管理員所建立，並放在持續性保留存放區中。
ms.assetid: deab6323-d114-463b-a0e7-acd173149b63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c4f0e38f5994687bfe26d1334300c0aa7fbbd3f8096abcf60e6c523e7d030a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393760"
---
# <a name="processing-reservations"></a>處理保留

URL 命名空間部分的保留專案是由系統管理員所建立，並放在持續性保留存放區中。 HTTP 的 URL 命名空間的根目錄是由系統管理員所擁有。 針對所有主機和埠值，一律會在 **relativeUri** 命名空間的根目錄採用下列兩個保留。



| 命名空間保留                 | 保留給              |
|------------------------------------|---------------------------|
| HTTPs:// <host> ：<port>/  | LocalSystem 系統管理員 |
| HTTPs:// <host> ：<port>/ | LocalSystem 系統管理員 |



 

無法移除這些隱含的保留。 不過，您可以將明確的根保留委派給其他使用者。 如下所示的保留會建立這類委派：



| 命名空間保留        | 保留給 |
|---------------------------|--------------|
| `https://+:80/`           | UserA、UserC |
| `https://adatum.com:443/` | UserB        |



 

如果系統管理員移除這些委派的保留專案，命名空間的擁有權會還原為對應主機和埠值的隱含保留。

 

 




