---
description: 查詢智慧卡資料庫。 他們可以提供特定使用者提供的智慧卡清單、特定卡片的介面和主要服務提供者、系統定義的讀者群組，以及一組讀者群組內的讀取器。
ms.assetid: a30cbb99-522c-4752-bfcd-75be608785f1
title: 智慧卡資料庫查詢函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54050ad6e6b5b4d7e8c91f7cdefab683274d153050100545c9e1ed5452c47cdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917794"
---
# <a name="smart-card-database-query-functions"></a>智慧卡資料庫查詢函數

下列函數會查詢 [*智慧卡資料庫*](../secgloss/s-gly.md)。 他們可以提供特定使用者提供的智慧卡清單、特定卡片的介面和 [*主要服務提供者*](../secgloss/p-gly.md) 、系統定義的 [*讀者群組*](../secgloss/r-gly.md) ，以及一組讀者 [*群組內的讀取器*](../secgloss/r-gly.md) 。

當您使用這些函式時，您可以查詢完整的智慧卡資料庫，也可以藉由設定 [*資源管理員內容*](../secgloss/r-gly.md)來縮小搜尋範圍。 在呼叫查詢函式之前，會先呼叫 [**SCardEstablishCoNtext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext) 來設定資源管理員內容。

> [!Note]  
> 如果沒有指定的內容，某些資訊可能仍會因為安全性限制而無法存取。

 



| 主題                                                  | 描述                                                                                                                                                                          |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardGetProviderId**](/windows/desktop/api/Winscard/nf-winscard-scardgetproviderida)       | 取得指定卡片之 [*主要服務提供者*](../secgloss/p-gly.md) 的識別碼 (GUID) 。 |
| [**SCardListCards**](/windows/desktop/api/Winscard/nf-winscard-scardlistcardsa)               | 取得特定使用者先前向系統介紹的卡片清單。                                                                                                     |
| [**SCardListInterfaces**](/windows/desktop/api/Winscard/nf-winscard-scardlistinterfacesa)     | 取得指定卡片所提供介面 (Guid) 的識別碼。                                                                                                         |
| [**SCardListReaderGroups**](/windows/desktop/api/Winscard/nf-winscard-scardlistreadergroupsa) | 取出先前引進系統的讀者群組清單。                                                                                                 |
| [**SCardListReaders**](/windows/desktop/api/Winscard/nf-winscard-scardlistreadersa)           | 在一組指定的讀取器群組內取出讀取器清單。                                                                                                                    |



 

 

 
