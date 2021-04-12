---
description: 管理智慧卡資料庫，使用指定的 resource manager 內容來更新資料庫。
ms.assetid: a2f457e1-c042-42e7-9071-cf0edd68e27a
title: 智慧卡資料庫管理功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c424494a30c71e15647da773027311ed53a2599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319899"
---
# <a name="smart-card-database-management-functions"></a>智慧卡資料庫管理功能

下列函式會管理 [*智慧卡資料庫*](../secgloss/s-gly.md)，並使用指定的 [*resource manager 內容*](../secgloss/r-gly.md)來更新資料庫。

> [!Note]  
> 藉由在資料庫上放置存取限制，而不是將安全性機制新增至 [*智慧卡子系統*](../secgloss/s-gly.md)，來維護資料庫安全性。

 



| 主題                                                            | 描述                                                                                                                                                             |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardAddReaderToGroup**](/windows/desktop/api/Winscard/nf-winscard-scardaddreadertogroupa)           | 將 [*讀者*](../secgloss/r-gly.md) 新增至 [*讀者群組*](../secgloss/r-gly.md)。 |
| [**SCardForgetCardType**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea)               | 從系統移除智慧卡。                                                                                                                                    |
| [**SCardForgetReader**](/windows/desktop/api/Winscard/nf-winscard-scardforgetreadera)                   | 移除系統中的讀取器。                                                                                                                                        |
| [**SCardForgetReaderGroup**](/windows/desktop/api/Winscard/nf-winscard-scardforgetreadergroupa)         | 從系統移除讀取器群組。                                                                                                                                  |
| [**SCardIntroduceCardType**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea)         | 將新的卡片引進系統。                                                                                                                                     |
| [**SCardIntroduceReader**](/windows/desktop/api/Winscard/nf-winscard-scardintroducereadera)             | 為系統引進新的讀取器。                                                                                                                                   |
| [**SCardIntroduceReaderGroup**](/windows/desktop/api/Winscard/nf-winscard-scardintroducereadergroupa)   | 為系統引進新的讀取器群組。                                                                                                                             |
| [**SCardRemoveReaderFromGroup**](/windows/desktop/api/Winscard/nf-winscard-scardremovereaderfromgroupa) | 從讀取器群組移除讀取器。                                                                                                                                    |



 

 

 
