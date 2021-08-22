---
description: 若要判斷計數器是否已安裝在特定電腦上，請使用完整的計數器路徑來呼叫 PdhValidatePath。 \_如果計數器位於指定的電腦上，此函數會傳回錯誤成功。
ms.assetid: 5533a8d8-3621-4ce7-984c-c3895adef531
title: 判斷計數器是否位於電腦上
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2cc6672125f961fc2759d264caa6c33ab68f46347c915e82d1666f667692fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061196"
---
# <a name="determining-whether-a-counter-is-located-on-a-computer"></a>判斷計數器是否位於電腦上

若要判斷計數器是否已安裝在特定電腦上，請使用完整的計數器路徑來呼叫 [**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) 。 \_如果計數器位於指定的電腦上，此函數會傳回錯誤成功。

[**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) 會驗證整個路徑;因此，如果路徑中有任何物件、實例或計數器不存在，則傳回值會指出。 **PdhValidatePath** 會依下列順序驗證指定的計數器路徑：電腦、效能物件、實例和計數器。

 

 



