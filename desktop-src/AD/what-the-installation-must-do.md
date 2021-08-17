---
title: 安裝必須做什麼
description: 在步驟3中參考的新屬性必須由其 OID 參考，因為新的屬性名稱在架構快取中不存在於此位置。
ms.assetid: 57da8740-7646-4ca9-ba8d-832e4f520b13
ms.tgt_platform: multiple
keywords:
- 安裝必須進行的 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3dcf125a171fba921a5341ad5f3de8bbe5d791d4eb4dc072f551345df3218ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182171"
---
# <a name="what-the-installation-must-do"></a>安裝必須做什麼

延伸架構的應用程式必須套用更新，如下列程式所述。

**若要在擴充架構時套用更新**

1.  加入新的屬性。
2.  加入新的類別。
3.  將新屬性加入至類別。
4.  觸發快取重載。

在步驟3中參考的新屬性必須由其 OID 參考，因為新的屬性名稱在架構快取中不存在於此位置。

如果不會立即使用延伸模組，則不需要步驟 4;視系統負載而定，擴充功能將會在架構快取中出現大約5分鐘。 如需架構快取的詳細資訊，以及如何觸發快取重載，請參閱 [更新架構](updating-the-schema-cache.md)快取。

 

 




