---
title: 更新架構快取
description: 寫入 Active Directory 伺服器的所有資訊都會針對架構進行驗證。
ms.assetid: 948f8ec5-7207-4566-bd79-60cdd54231bf
ms.tgt_platform: multiple
keywords:
- 更新架構快取 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff477ce97aab2e0e49522309d386a7e1c37b31e3b8171ef20c626fdaaa5b53a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024526"
---
# <a name="updating-the-schema-cache"></a>更新架構快取

寫入 Active Directory 伺服器的所有資訊都會針對架構進行驗證。 基於效能考慮，架構會保留在目錄伺服器 (域) 控制器的記憶體中。 記憶體中的版本會在磁片上的版本更新後自動更新。 自動更新會在最後一次變更套用後五分鐘完成;在5分鐘的時間範圍內對架構套用另一項變更，會將計時器重設為另5分鐘。 此行為可讓快取保持一致，但可能會造成混淆，因為在快取更新之前，變更不會出現在架構中，即使已在磁片上套用也一樣。

若要在架構更新後更新 Active Directory 的架構快取，或如果您想要立即使用非架構作業的架構更新，請新增 **schemaUpdateNow** 屬性， (它是) 至根 DSE (空白 DN) 值1的操作屬性。 架構快取更新會立即開始。 呼叫正在封鎖中。 如果呼叫傳回時未發生錯誤，則會更新快取，而且所有架構更新都可以使用。 傳回錯誤表示快取更新失敗。 必須使用這項功能的應用程式應設計成可容納封鎖寫入，特別是當程式或腳本以互動方式執行時，提供使用者意見反應。

下列程式碼範例是範例 LDIFDE 腳本，示範如何觸發快取重載。

``` syntax
dn:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

如需如何以程式設計方式更新架構快取的詳細資訊，請參閱更新架構快取的 [範例程式碼](example-code-for-updating-the-schema-cache.md)。

 

 




