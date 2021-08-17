---
description: 若要從系統移除您的應用程式效能計數器，請執行下列步驟。
ms.assetid: 40fc9831-1025-4052-a941-70767ee4e10f
title: 正在刪除效能計數器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c34dfc64be4ded0ce07b466393851b235ca4b2f49c89e05f067041f236565fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144011"
---
# <a name="deleting-performance-counters"></a>正在刪除效能計數器

若要從系統移除您應用程式的效能計數器，請執行下列步驟。

1.  使用電腦隨附的 **unlodctr** 工具，從登錄中移除計數器相關資料。 請注意， **unlodctr** 工具必須要有應用程式的 **效能** 金鑰才能成功。 如需詳細資訊，請參閱 [從登錄中移除計數器名稱和描述](removing-counter-names-and-descriptions-from-the-registry.md)。
2.  刪除應用程式 **服務** 金鑰下的 **效能** 和 **連結** 索引鍵。 若要刪除這些金鑰，請使用 Regedt32.exe 公用程式或呼叫 [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya)。

 

 
