---
description: 讓您追蹤讀者內的牌。 這些常式通常會 \_ 在陣列中使用捨棄 READERSTATE 結構。
ms.assetid: b26b26bf-85ff-435f-a679-7529f19b1c1b
title: 智慧卡追蹤功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde9bebfeea2718ce634d585c2740cb510500ce3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851340"
---
# <a name="smart-card-tracking-functions"></a>智慧卡追蹤功能

下列函數可讓您追蹤讀者內的卡片。 這些常式通常會在陣列中使用 [**捨棄 \_ READERSTATE**](/windows/desktop/api/Winscard/ns-winscard-scard_readerstatea) 結構。



| 主題                                                | 描述                                                                                                                            |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardLocateCards**](/windows/desktop/api/Winscard/nf-winscard-scardlocatecardsa)         | 搜尋其 [*ATR 字串*](../secgloss/a-gly.md) 符合所提供卡片名稱的卡片。 |
| [**SCardGetStatusChange**](/windows/desktop/api/Winscard/nf-winscard-scardgetstatuschangea) | 封鎖執行，直到卡片目前的可用性變更為止。                                                                       |
| [**SCardCancel**](/windows/desktop/api/Winscard/nf-winscard-scardcancel)                   | 終止未完成的動作。                                                                                                         |



 

 

 
