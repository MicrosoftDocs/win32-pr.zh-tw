---
title: 網域樹狀結構
description: 網域樹狀目錄由數個網域所組成，這些網域共用通用的架構和設定，形成連續的命名空間。
ms.assetid: 3deb4053-3124-4180-8ab0-35fff689a37e
ms.tgt_platform: multiple
keywords:
- 域樹 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21d2b36968615fd4e92912fdd94246ef8dda0c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183024"
---
# <a name="domain-trees"></a>網域樹狀結構

*網域樹狀目錄* 由數個網域所組成，這些網域共用通用的架構和設定，形成連續的命名空間。 樹狀結構中的網域也會依信任關係連結在一起。 Active Directory 是一或多個樹狀結構的集合。

您可以透過兩種方式來查看樹狀結構。 一個 view 是網域之間的信任關係。 另一個視圖是網域樹狀結構的命名空間。

## <a name="viewing-trust-relationships"></a>查看信任關係

您可以根據個別網域和現有的信任關係，繪製網域樹狀結構的圖表。

Windows 2000 會根據 Kerberos 安全性通訊協定，在網域之間建立信任關係。 Kerberos 信任是可轉移且階層式-如果網域 A 信任網域 B，而網域 B 信任網域 C，則網域 A 信任網域 C。

![網域樹系信任關係](images/domain-trust.png)

## <a name="viewing-the-namespace"></a>查看命名空間

您也可以根據命名空間繪製網域樹狀結構的圖表。 您可以遵循域樹命名空間階層的路徑，判斷物件的分辨名稱。 此視圖適用于將物件分組到邏輯階層中。 連續命名空間的主要優點是，來自命名空間根目錄的深層搜尋會搜尋整個階層。

![命名空間網域樹](images/namespace.png)

 

 




