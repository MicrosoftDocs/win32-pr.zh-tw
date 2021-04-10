---
description: SID 元件
ms.assetid: 528412e7-c2b6-4ddd-86de-999252972421
title: SID 元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd44d0534cc56c6ef998c150810f14b3eda289d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026319"
---
# <a name="sid-components"></a>SID 元件

SID 值包含的元件提供了可唯一識別受信任者之 [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) 結構和元件的相關資訊。 SID 是由下列元件所組成：

-   [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid)結構的修訂層級
-   識別發行 SID 之授權單位的48位識別碼授權單位值
-   Subauthority 或 [*相對識別碼*](/windows/desktop/SecGloss/r-gly) 的可變數 (RID) 值，可唯一識別信任者相對於發出 SID 的授權單位

識別碼授權單位值和 subauthority 值的組合可確保兩個 Sid 都不相同，即使兩個不同的 SID 發行授權單位發出相同的 RID 值組合也一樣。 每個 SID 發行授權單位只會發出一次指定的 RID。

Sid 會以二進位格式儲存在 [**sid**](/windows/desktop/api/Winnt/ns-winnt-sid) 結構中。 若要顯示 SID，您可以呼叫 [**ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida) 函式，將二進位 SID 轉換成字串格式。 若要將 SID 字串轉換回有效的功能 SID，請呼叫 [**ConvertStringSidToSid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida) 函數。

這些函式會使用下列 Sid 的標準化字串標記法，讓您更輕鬆地將其元件視覺化：

S-*R* - *I* - *S*.。。

在這個標記法中，常值字元 "S" 會將一系列的數位識別為 SID， *R* 是修訂層級， *I* 是識別碼授權值，而 *S*.。。 這是一或多個 subauthority 值。

下列範例會使用此標記法來顯示本機系統管理員群組已知的網域相對 SID：

S-1-5-32-544

在此範例中，SID 具有下列元件。 括弧中的常數是知名的識別碼授權單位和 Winnt 中定義的 [*RID*](/windows/desktop/SecGloss/r-gly) 值：

-   修訂層級1
-   識別碼授權單位值為 5 (SECURITY \_ NT \_ 授權單位) 
-   第一個 subauthority 值 32 (安全性內 \_ 建 \_ 網域 \_ RID) 
-   第二個 subauthority 值 544 (網域 \_ 別名 \_ RID \_ 管理員) 

 

 
