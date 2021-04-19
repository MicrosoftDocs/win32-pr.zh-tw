---
description: 若要從系統移除您的應用程式效能計數器，請執行下列步驟。
ms.assetid: 40fc9831-1025-4052-a941-70767ee4e10f
title: 正在刪除效能計數器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba257a1a44b5272543b7e61dcdc4b4e96225c160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977321"
---
# <a name="deleting-performance-counters"></a>正在刪除效能計數器

若要從系統移除您應用程式的效能計數器，請執行下列步驟。

1.  使用電腦隨附的 **unlodctr** 工具，從登錄中移除計數器相關資料。 請注意， **unlodctr** 工具必須要有應用程式的 **效能** 金鑰才能成功。 如需詳細資訊，請參閱 [從登錄中移除計數器名稱和描述](removing-counter-names-and-descriptions-from-the-registry.md)。
2.  刪除應用程式 **服務** 金鑰下的 **效能** 和 **連結** 索引鍵。 若要刪除這些金鑰，請使用 Regedt32.exe 公用程式或呼叫 [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya)。

 

 
