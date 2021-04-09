---
description: TrustedDomain 物件會儲存與網域之信任關係的相關資訊。
ms.assetid: fab69367-2143-49ef-a1b9-9c1d846fd4e1
title: TrustedDomain 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 837d8a9e56273a87b22b9697ef4e5917d73bcc81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847880"
---
# <a name="trusteddomain-object"></a>TrustedDomain 物件

**TrustedDomain** 物件會儲存與網域之信任關係的相關資訊。 在信任的系統上建立 **TrustedDomain** 物件，以識別受信任網域中可用來提交驗證要求和執行其他作業的帳戶，例如 (SID) 轉譯的名稱和 [*安全性識別*](/windows/desktop/SecGloss/s-gly) 元。

儲存在 **TrustedDomain** 物件中的資訊包括：

-   受信任網域的 SID。 這項資訊不可修改，而且在所有 **TrustedDomain** 物件中都必須是唯一的。
-   受信任網域的名稱。 這項資訊不可修改，而且在所有 **TrustedDomain** 物件中都必須是唯一的。
-   信任網域中用來提交驗證要求以及執行名稱和 SID 轉譯的帳戶名稱。 無法修改這個名稱。
-   用來提交驗證要求以及執行名稱和 SID 翻譯的密碼。

如需詳細資訊，請參閱 [TrustedDomain 物件類型](the-trusteddomain-object-type.md)。

 

 
