---
description: 當進程嘗試存取安全物件時，系統會逐步完成存取控制專案 (Ace) 在物件任意存取控制清單 (DACL) 直到找到允許或拒絕所要求存取權的 Ace 為止。
ms.assetid: fccf043e-e769-4f3f-b18c-252be20190d8
title: DACL 中的 Ace 順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b5d017fe6441e90cded6458d8796dee301e3fa0fda01b7d088039abd9834ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907748"
---
# <a name="order-of-aces-in-a-dacl"></a>DACL 中的 Ace 順序

當 [*進程*](/windows/desktop/SecGloss/p-gly) 嘗試存取安全物件時，系統會逐步執行 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) (ace) 在物件的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) 中， (DACL) 直到找到允許或拒絕所要求存取權的 ace 為止。 DACL 允許使用者的存取權限會視 DACL 中的 Ace 順序而有所不同。 因此，Windows XP 作業系統會在安全物件的 DACL 中定義 ace 的慣用順序。 慣用的順序提供簡單的架構，可確保拒絕存取的 ACE 實際上會拒絕存取。 如需有關檢查存取權之系統演算法的詳細資訊，請參閱 [Dacl 如何控制物件的存取權](how-dacls-control-access-to-an-object.md)。

針對 Windows Server 2003 和 Windows XP，在引進物件專屬的 ace 和自動繼承時，ace 的正確順序會很複雜。

下列步驟說明慣用的順序：

1.  所有明確的 Ace 都會放在群組中任何繼承的 Ace 之前。
2.  在明確的 Ace 群組內，會在允許存取的 Ace 之前放置拒絕存取的 Ace。
3.  繼承的 Ace 會以繼承的 Ace 順序放置。 從子物件的父系繼承的 Ace 會優先，然後是繼承自祖系的 Ace，依此類推物件的樹狀結構。
4.  針對每個繼承的 Ace 層級，會在允許存取的 Ace 之前放置拒絕存取的 Ace。

當然，ACL 中並非所有 ACE 類型都是必要的。

[**AddAccessAllowedAceEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedaceex)和 [**AddAccessAllowedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace)之類的函式會將 ACE 新增至 ACL 的結尾。 呼叫端必須負責確保以正確的順序加入 Ace。

 

 
