---
description: 如果設定此位，則對話方塊是強制回應的，相同應用程式的其他對話方塊無法放在其上方，且對話方塊會在控制項執行時將它保持在執行狀態。
ms.assetid: 14871dc7-c928-4381-a043-6beb06d25214
title: 強制回應對話方塊樣式位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3663445a81acf07aebd9961f8ddb048dc8c8f466968573ac2c45544d6bd79baa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945475"
---
# <a name="modal-dialog-style-bit"></a>強制回應對話方塊樣式位

如果設定此位，則對話方塊是強制回應的，相同應用程式的其他對話方塊無法放在其上方，且對話方塊會在控制項執行時將它保持在執行狀態。 如果未設定此位，則對話方塊為非強制回應，相同應用程式的其他對話方塊可能會在其上方移動。 建立並顯示非強制回應對話方塊之後，使用者介面會將控制權傳回到安裝程式。 然後，安裝程式會定期呼叫使用者介面來更新對話方塊，並讓它有機會處理訊息。 完成這項操作之後，控制權會傳回給安裝程式。

> [!Note]  
> 在嚮導順序中應該不會有非強制回應對話方塊，因為這會將控制權傳回給安裝程式，並提前結束嚮導順序。

 

## <a name="value"></a>值



| Decimal | 十六進位 | 常數                          |
|---------|-------------|-----------------------------------|
| 2       | 0x00000002  | **msidbDialogAttributesSysModal** |



 

 

 



