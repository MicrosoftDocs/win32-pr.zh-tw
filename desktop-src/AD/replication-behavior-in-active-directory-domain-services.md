---
title: Active Directory Domain Services 中的複寫行為
description: 複寫行為是一致且可預測的;給定複本的一組變更之後，就可以預測結果 \ 郵件; 變更將會傳播到所有其他複本。
ms.assetid: 4e9f2e43-6375-4663-93ca-55112fd00abe
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory，複寫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7548ecf146f1d23b97b9db6a0307b21a6c39d359576c2de02285331d165fad4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025136"
---
# <a name="replication-behavior-in-active-directory-domain-services"></a>Active Directory Domain Services 中的複寫行為

複寫行為是一致且可預測的;如果指定的複本有一組變更，可以預測結果，變更將會傳播到所有其他複本。 設計可靠的一般模型來預測在所有其他複本或特定複本上套用變更的時間，因為無法得知分散式系統的未來狀態，所以不可能發生這種情況。 這稱為「不具決定性的延遲」，而使用該目錄的應用程式必須瞭解並允許它。

這種情況並不複雜，可能會出現。 應用程式只需要有三個狀態：

-   版本扭曲：任何套用至指定來源複本的變更都未傳播到指定的目的地複本。 讀取來源複本的應用程式會看到新版本的資訊，而讀取目的地的應用程式會看到舊版 (或沒有任何專案，如果新資訊是在第一次) 時新增的。 版本扭曲適用于所有目錄服務取用者。
-   部分更新：套用至指定來源複本的部分變更已傳播到指定的目的地複本。 讀取來源複本的應用程式會看到新的資訊，而讀取目的地的應用程式會將舊的和新的資訊混用 (或只有一些新的資訊，如果是第一次加入的新資訊) 。 部分更新適用于使用兩個或多個相關物件來儲存其資訊的目錄服務取用者。
-   完整複寫狀態：套用至指定來源複本的所有變更都會傳播到指定的目的地複本。 來源和目的地複本上的應用程式會看到相同的資訊。

 

 




