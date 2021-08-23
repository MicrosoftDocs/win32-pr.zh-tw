---
description: 在存取檢查中，系統會比較執行緒存取權杖中的安全性資訊與物件安全描述項中的安全性資訊。
ms.assetid: 40871179-d383-43d0-810d-0805c88dbbd6
title: 執行緒和安全物件之間的互動
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b27ab85aa461892d0e6fdf6bdbd9adc8aa7b78a3d9bf1b3896d53ad8e2e236de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670811"
---
# <a name="interaction-between-threads-and-securable-objects"></a>執行緒和安全物件之間的互動

當執行緒嘗試使用 [安全物件](securable-objects.md)時，系統會先執行存取檢查，然後才允許執行緒繼續執行。 在存取檢查中，系統會比較執行緒 [*存取權杖*](/windows/desktop/SecGloss/a-gly) 中的安全性資訊與物件 [*安全描述項*](/windows/desktop/SecGloss/s-gly)中的安全性資訊。

-   存取權杖包含 (Sid) 的 [*安全識別碼*](/windows/desktop/SecGloss/s-gly) ，可識別與執行緒相關聯的使用者。
-   安全描述項會識別物件的擁有者，並且包含 (DACL) 的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) 。 DACL 包含 (Ace) 的 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) ，其中每個專案都會指定特定使用者或群組允許或拒絕的存取權。

系統會檢查物件的 DACL，尋找套用至使用者的 Ace，並從執行緒的存取權杖將 Sid 分組。 系統會檢查每個 ACE，直到授與或拒絕存取權，或直到沒有其他 Ace 需要檢查為止。 當然， (ACL) 的 [*存取控制清單*](/windows/desktop/SecGloss/a-gly) 可能會有數個適用于權杖 Sid 的 ace。 而且，如果發生這種情況，每個 ACE 授與的存取權限就會累積。 例如，如果一個 ACE 授與群組的讀取權限，而另一個 ACE 授與屬於群組成員之使用者的寫入權限，則使用者可以同時擁有該物件的讀取和寫入存取權。

下圖顯示這些安全性資訊區塊之間的關聯性：

![進程、ace 和 dacl 之間的關聯性](images/cssec-02.png)

 

 
