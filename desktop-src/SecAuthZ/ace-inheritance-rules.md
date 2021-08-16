---
description: 系統會根據一組繼承規則，將可繼承的存取控制專案 (Ace) 傳播到子物件。
ms.assetid: 08f76aaa-8379-4ba8-9735-7568001bcd53
title: ACE 繼承規則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba77e5d9fcbef9125108e8f0be76cd5b7c79a2f99ba524c81f3fd1da84336f04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785360"
---
# <a name="ace-inheritance-rules"></a>ACE 繼承規則

系統會根據一組繼承規則，將可繼承的 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) (ace) 傳播到子物件。 系統會根據 [dacl 中的慣用 ace 順序](order-of-aces-in-a-dacl.md)，將繼承的 ace 放在 [*任意的存取控制清單*](/windows/desktop/SecGloss/d-gly)中 (dacl) 子系。 系統會 \_ 在所有繼承的 ace 中設定繼承的 ace 旗標。

依繼承旗標的組合而定，容器和非容器子物件所繼承的 Ace 會有所不同。 這些繼承規則對 Dacl 和 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly) 的運作相同 (sacl) 。



| 父 ACE 旗標                                  | 對子 ACL 的影響                                                                                                                                                                                                                      |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 物件 \_ \_ 只繼承 ACE                        | 非容器子物件：繼承為有效的 ACE。 容器子物件：容器會繼承僅限繼承的 ACE，除非 \_ 也設定了 NO 傳播 \_ 繼承 \_ ace 位旗標。<br/>                                       |
| \_ \_ 僅限容器繼承 ACE                     | 非容器子物件：對子物件沒有任何作用。 容器子物件：子物件會繼承有效的 ACE。 除非 \_ 也設定了 NO 傳播 \_ 繼承 \_ ace 位旗標，否則繼承的 ACE 是可繼承的。<br/> |
| CONTAINER \_ inherit \_ ACE 和 OBJECT \_ inherit \_ ace | 非容器子物件：繼承為有效的 ACE。 容器子物件：子物件會繼承有效的 ACE。 除非 \_ 也設定了 NO 傳播 \_ 繼承 \_ ace 位旗標，否則繼承的 ACE 是可繼承的。<br/> |
| 未設定任何繼承旗標                         | 對子容器或非容器的物件沒有任何影響。                                                                                                                                                                                    |



 

如果繼承的 ACE 是子物件的有效 ACE，系統就會將任何一般許可權對應到子物件的特定許可權。 同樣地，系統會將一般 [*安全識別碼*](/windows/desktop/SecGloss/s-gly) (sid) （例如 CREATOR \_ 擁有者）對應到適當的 SID。 如果繼承的 ACE 是僅限繼承的 ACE，則任何泛型許可權或泛型 Sid 都會保持不變，如此一來，當下一代子物件繼承 ACE 時，即可適當地對應。

如果容器物件繼承的 ACE 在容器上都是有效的，且由其子系繼承，容器可能會繼承兩個 Ace。 如果可繼承 ACE 包含泛型資訊，就會發生這種情況。 容器會繼承僅限繼承的 ACE，其中包含泛型資訊，以及已對應泛型資訊的僅限有效 ACE。

物件專屬的 [ACE](object-specific-aces.md) 具有 **InheritedObjectType** 成員，可以包含 GUID 來識別可繼承 ACE 的物件類型。

如果未指定 **InheritedObjectType** GUID，物件特定 ace 的繼承規則會與標準 ace 的繼承規則相同。

如果指定了 **InheritedObjectType** GUID，則如果已 \_ 設定 OBJECT inherit \_ ace，且已設定容器繼承 ace 的容器（如果已設定了 CONTAINER \_ inherit ace 的話），則會以符合 GUID 的物件來繼承 ace \_ 。 請注意，目前只有 DS 物件支持對象特定的 Ace，而 DS 會將所有物件類型視為容器。

 

