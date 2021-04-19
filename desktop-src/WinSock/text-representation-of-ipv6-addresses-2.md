---
description: 此區段會從 &\# 0034; IPv6 定址架構&\# 0034; 由 R 複製。
ms.assetid: 52faecb9-0d7a-40fa-a021-3cc6816a4db8
title: IPv6 位址的文字標記法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df97c1c8933f3708fee56e34e05f918d531d2a13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978897"
---
# <a name="text-representation-of-ipv6-addresses"></a>IPv6 位址的文字標記法

此區段是從「IPv6 定址架構」（Hinden 和 Deering）複製而來。 有三種傳統形式可將 IPv6 位址表示為文字字串：

-   慣用的表單是 x：x： x：x： x：x： x：x，其中 ' x ' 是位址之 8 16 位部分的十六進位值。

    範例：

    <dl> FEDC： BA98：7654：3210： FEDC： BA98：7654：3210  
    1080：0：0：0：8：800：200C：417A  
    </dl>

> [!Note]  
> 不需要在個別欄位中撰寫前置零，但每個欄位中必須至少有一個數位 (但第二個表單) 所述的案例除外。

 

-   由於配置了某些 IPv6 位址樣式的方法，因此位址通常會包含長度為零位的長字串。 為了讓您更輕鬆地撰寫包含零位的位址，有一種特殊的語法可壓縮零。 使用雙冒號 ( "：：" ) 指出多個16位零的群組。

    例如，多播位址

    <dl> FF01：0：0：0：0：0：0：43  
    </dl>

    可能會表示為：

    <dl> FF01：：43  
    </dl>

    雙引號 ( "：：" ) 只能在位址中出現一次。 可以用來壓縮位址中的前置或尾端零。

-   在處理 IPv4 和 IPv6 節點的混合式環境時，可能更方便的替代形式是 x：x： x：x： x：x： d. d. d. d，其中 ' x ' 是位址中六個高序位16位部分的十六進位值，而 ' d ' 是位址 (標準 IPv4 表示) 的四個低序位8位部分的十進位值。

    範例：

    <dl> 0：0：0：0：0：0：13.1.68。3  
    0：0：0：0：0： FFFF：129.144.52.38  
    </dl>

    或壓縮格式：

    <dl> ::13.1.68.3  
    ：： FFFF：129.144.52.38  
    </dl>

 

 



