---
description: 存取控制專案 (ACE) 是存取控制清單中 (ACL) 的元素。
ms.assetid: 9cf4d796-3955-456b-9db9-ae9fa83752f6
title: 存取控制專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8adcc382da130c57c55b869c47c8837c7780a7cff4e6dbdd881e55aa7b724dc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785648"
---
# <a name="access-control-entries"></a>存取控制專案

[*存取控制專案*](/windows/desktop/SecGloss/a-gly) (ACE) 是 [*存取控制清單*](/windows/desktop/SecGloss/a-gly)中 (ACL) 的元素。 ACL 可以有零或多個 Ace。 每個 ACE 都會控制或監視指定之受信任者對物件的存取。 如需有關在物件 Acl 中新增、移除或變更 Ace 的詳細資訊，請參閱 [使用 c + + 修改物件的 acl](modifying-the-acls-of-an-object-in-c--.md)。

Ace 有六種類型，所有安全物件都支援這三種類型。 其他三種類型是目錄服務物件所支援的 [特定物件 ace](object-specific-aces.md) 。

所有類型的 Ace 都包含下列存取控制資訊：

-    (SID) 的 [安全識別碼](security-identifiers.md) ，可識別套用 ACE 的 [信任者](trustees.md) 。
-   [*存取遮罩*](/windows/desktop/SecGloss/a-gly)，指定由 ACE 控制的 [存取權限](access-rights-and-access-masks.md)。
-   指出 ACE 類型的旗標。
-   一組位旗標，可決定子容器或物件是否可以從附加 ACL 的主要物件繼承 ACE。

下表列出所有安全物件所支援的三種 ACE 類型。



| 類型               | Description                                                                                                                                                                                                                                      |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 拒絕存取的 ACE  | 用於 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) (DACL) ，以拒絕信任者的存取權限。                                       |
| 存取-允許的 ACE | 在 DACL 中用來允許信任者的存取權限。                                                                                                                                                                                              |
| 系統-audit ACE   | 用於 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly) (SACL) 在信任者嘗試執行指定的存取權限時，產生審核記錄。 |



 

如需物件特定 Ace 的表格，請參閱 [物件特定的 ace](object-specific-aces.md)。

> [!Note]  
> 目前不支援系統警示物件 Ace。

 

 

 
