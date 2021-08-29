---
title: 處理保留
description: URL 命名空間部分的保留專案是由系統管理員所建立，並放在持續性保留存放區中。
ms.assetid: deab6323-d114-463b-a0e7-acd173149b63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aefbc72d5ea373765db674c3d4815f2a4cfa0a6
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882812"
---
# <a name="processing-reservations"></a>處理保留

URL 命名空間部分的保留專案是由系統管理員所建立，並放在持續性保留存放區中。 HTTP 的 URL 命名空間的根目錄是由系統管理員所擁有。 針對所有主機和埠值，一律會在 **relativeUri** 命名空間的根目錄採用下列兩個保留。



| 命名空間保留                 | 保留給              |
|------------------------------------|---------------------------|
| HTTPs:// &lt; 主機 &gt; ： &lt; 埠&gt;/  | LocalSystem 系統管理員 |
| HTTPs:// &lt; 主機 &gt; ： &lt; 埠&gt;/ | LocalSystem 系統管理員 |



 

無法移除這些隱含的保留。 不過，您可以將明確的根保留委派給其他使用者。 如下所示的保留會建立這類委派：



| 命名空間保留        | 保留給 |
|---------------------------|--------------|
| `https://+:80/`           | UserA、UserC |
| `https://adatum.com:443/` | UserB        |



 

如果系統管理員移除這些委派的保留專案，命名空間的擁有權會還原為對應主機和埠值的隱含保留。

 

 




