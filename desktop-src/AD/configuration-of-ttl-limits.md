---
title: 設定 TTL 限制
description: 用戶端可以要求介於1到 31557600 (的 TTL 值，也就是1秒到1年的) 。
ms.assetid: 4009702c-7992-4e20-9d37-384f8137ba8f
ms.tgt_platform: multiple
keywords:
- 設定 TTL 限制 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2786258d060ef4261dcd9fbfad359c71f2dbaeb
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881609"
---
# <a name="configuration-of-ttl-limits"></a>設定 TTL 限制

用戶端可以要求介於1到 31557600 (的 TTL 值，也就是1秒到1年的) 。 這個屬性值範圍將會由 **entryTTL** 屬性的 **attributeSchema** 定義中的 **rangeLower** 和 **rangeUpper** 屬性值強制執行。 根據 RFC 2589，目錄伺服器不需要接受此值，而且可能會傳回不同的 TTL 值給用戶端。 用戶端必須能夠使用此伺服器指示的值做為其用戶端重新整理期間 (CRP) 這會控制用戶端對動態專案執行重新整理作業所需的頻率。

Active Directory Domain Services 讓系統管理員能夠設定樹系的預設和最小 TTL 值。 如果未明確指定 TTL，預設 TTL 值會指派給新建立的動態專案。 TTL 的最小值會覆寫低於設定的最小值的任何用戶端指定的 TTL 值。 不需要提供可設定的最大 TTL 值，因為 **attributeSchema** 物件中的 **rangeUpper** 屬性值會加上最大值。 允許系統管理員設定這些值，可讓他們設定 TTL 值以強制執行低重新整理流量，或在其他極端的情況下提供高度最新的目錄。

這兩個可設定 TTL 參數的預設值如下所示：

-   預設 TTL 值 = 86400 秒 (1 天) 
-   最小 TTL 值 = 900 秒 (15 分鐘) 

可設定的 TTL 參數將會儲存為 AVA (屬性值判斷提示) 專案的屬性（attribute）值判斷提示專案（ &lt; &gt; = &lt; 位於設定分割區 &gt; 中下列 DN 所提供的 NTDS-Service 物件的 **設定** 屬性中）：


```C++
CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,DC=...
```



確切的 AVA 語法（針對兩個可設定的 TTL 參數）如下所示，其中 NNNN 以秒為單位來表示：


```C++
DynamicObjectDefaultTTLSeconds=NNNN
```




```C++
DynamicObjectMinTTLSeconds=NNNN
```



系統管理員可以透過命令列公用程式 ntdsutil 來設定這些值。

 

 




