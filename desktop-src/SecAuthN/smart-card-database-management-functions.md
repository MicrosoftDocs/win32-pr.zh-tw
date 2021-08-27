---
description: 管理智慧卡資料庫，使用指定的 resource manager 內容來更新資料庫。
ms.assetid: a2f457e1-c042-42e7-9071-cf0edd68e27a
title: 智慧卡資料庫管理功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61b107663df8b80b5883c9ce9b3f045e8d7913ac92b5acb23d9ae758dafa2ac9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917804"
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



 

 

 
