---
description: Posix 子系統必須能夠將遇到的任何安全識別碼 () SID 轉譯為32位值（稱為 Posix ID）。
ms.assetid: cd6c89ef-c3f1-47fe-8183-320b5d24b0dd
title: 對應 Posix 識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dabb944b543fba65942eb89d526590a5aff2c26c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851519"
---
# <a name="mapping-posix-identifiers"></a>對應 Posix 識別碼

Posix 子系統必須能夠將遇到的任何 [*安全識別碼*](/windows/desktop/SecGloss/s-gly) () SID 轉譯為32位值（稱為 *Posix ID*）。 此外，它還必須能夠將識別碼分類為使用者識別碼或群組識別碼。 若要瞭解此對應的完成方式，讓我們先看看必須對應的 Sid。

Sid 有兩個元件：網域的 SID 和網域中帳戶的相對識別碼。 例如，在 SID S-1-518364-21-43-8 中，最後一個數位8是帳戶的相對識別碼 (RID) ，而 S-1-518364-21-43 是網域的 SID。

網域資訊儲存在 [**TrustedDomain**](trusteddomain-object.md) 物件中。 儲存在 **TrustedDomain** 物件中的部分資訊是要用於該網域內之 Sid 的 Posix 識別碼位移。 例如，假設 **TrustedDomain** 的定義如下：

``` syntax
    Name:    NtPgm
    Sid:    S-1-518364-21-43
    Posix Offset:    0x130000
```

此網域中帳戶的 Posix 識別碼會透過將0x130000 新增至帳戶的相對識別碼來產生。 因此，對應至 SID S-1-518364-21-43-8 的 Posix 識別碼會是0x130008。

並非所有 Posix 識別碼翻譯都使用 [**TrustedDomain**](trusteddomain-object.md) 物件。 下表顯示使用已知的位移值所對應的 Sid。



| 來源                                              | Posix 識別碼位移 |
|-----------------------------------------------------|-----------------|
| 內建網域的 Sid                       | 0x20000         |
| 帳戶網域中的 Sid                        | 0x30000         |
| 從主域 (的 Sid 僅限工作站)  | 0x40000         |



 

最後，另一組 Sid （登入 Sid）需要進行特殊處理。 這些值是由每個登入會話的 Windows 登入程式所指派，且格式為 S-1-5-5-X-Y，其中 X 和 Y 被視為單一大型 \_ 整數，每個登入會話都會遞增。 這些 Sid 會對應至常數 Posix 識別碼0xFFF。 若要對應 Posix ID 0xFFF，您可以轉譯任何最適合該情況的 [*登入識別碼*](/windows/desktop/SecGloss/l-gly) ，或者您可能會預設使用 S-1-5-5-0-0。  (例如，如果 posix 使用者將保護套用至物件，並指定 FFFx，則比起只指派 S-1-5-5-0-0 來取代該使用者的登入識別碼是最好的做法。 ) 

 

 
