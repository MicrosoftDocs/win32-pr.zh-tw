---
description: 瞭解如何建立可在檔案資料流程中讀取和寫入屬性的屬性處理常式。 每個處理常式都與指定的檔案類型相關聯。
ms.assetid: 9dacd399-2cf3-40dd-9501-f26f0281500d
title: 執行屬性處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aadfabf451d5a90ba88925d28f3f460aaeeb28f
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481833"
---
# <a name="implementing-property-handlers"></a>執行屬性處理常式

在 Windows Vista 和更新版本中，中繼資料成為組織專案的方法，例如檔案、電子郵件或連絡人。 為了讓系統能夠根據其中繼資料來搜尋專案，以及使用者可以讀取或寫入中繼資料的位置，Windows Vista 引進了新的屬性系統。 這個系統中的中繼資料是由一組可擴充的屬性來表示。 在這組主題中，我們會說明如何建立可在檔案資料流程中讀取和寫入屬性的處理常式。 這些處理常式稱為「屬性處理常式」（property），而每個處理常式都與指定的檔案類型相關聯，並以副檔名來識別。

下列主題討論定義屬性和屬性處理常式所需的需求和策略。

-   [瞭解屬性處理常式](./building-property-handlers-properties.md)
-   [使用種類名稱](./building-property-handlers-user-friendly-kind-names.md)
-   [使用屬性清單](./building-property-handlers-property-lists.md)
-   [初始化屬性處理常式](./building-property-handlers-property-handlers.md)
-   [註冊和散發屬性處理常式](./prophand-reg-dist.md)
-   [屬性處理常式的最佳作法和常見問題](./prophand-bestprac-faq.yml)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立自訂屬性](./building-property-handlers-property-schemas.md)
</dt> <dt>

[屬性描述架構](./propdesc-schema-entry.md)
</dt> </dl>

 

 
