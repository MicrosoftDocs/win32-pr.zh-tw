---
description: 磁碟區陰影複製服務 (VSS) 會在執行中的系統（特別是伺服器）上，捕獲並複製穩定的映射以進行備份，而不過度會降低其所提供之服務的效能和穩定性。
ms.assetid: 654c67e8-2f17-4d93-aabd-fabd71c4c852
title: 關於磁碟區陰影複製服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62a170ce83b14ffe431199099e5a8927e19c1941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979000"
---
# <a name="about-the-volume-shadow-copy-service"></a>關於磁碟區陰影複製服務

磁碟區陰影複製服務 (VSS) 會在執行中的系統（特別是伺服器）上，捕獲並複製穩定的映射以進行備份，而不過度會降低其所提供之服務的效能和穩定性。

VSS 解決方案的設計目的，是為了讓開發人員能夠建立服務 ([*寫入*](vssgloss-w.md) 器) 可以使用 VSS ([*請求*](vssgloss-r.md) 者) ，以任何廠商的備份應用程式有效地備份這些服務。

-   [一般磁片區備份問題](common-volume-backup-issues.md)
-   [VSS 模型](the-vss-model.md)
-   [基本 VSS 概念](basic-vss-concepts.md)
-   [內建 VSS 寫入器](in-box-vss-writers.md)

 

 



