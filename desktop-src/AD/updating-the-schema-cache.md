---
title: 更新架構快取
description: 寫入 Active Directory 伺服器的所有資訊都會針對架構進行驗證。
ms.assetid: 948f8ec5-7207-4566-bd79-60cdd54231bf
ms.tgt_platform: multiple
keywords:
- 更新架構快取 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bf915d00b463b81a331ffe39b342f620a50417
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671211"
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

 

 




