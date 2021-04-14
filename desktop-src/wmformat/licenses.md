---
title: 授權
description: 授權
ms.assetid: 74717519-bfd5-4a64-88eb-680d4bdfe74a
keywords:
- 'Windows Media 格式 SDK、數位版權管理 (DRM) '
- Windows Media Format SDK，DRM 授權
- Windows Media Format SDK，DRM 的授權
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- 數位版權管理 (DRM) 、受保護的檔案授權
- DRM (數位版權管理) 、受保護的檔案授權
- 授權，DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fbf2d7c0a25b2b19241d90743f43f46a71d7e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311259"
---
# <a name="licenses"></a>授權

授權是一組資料，其描述可讀取受保護檔案中資料的條件。 每個授權都會套用至金鑰識別碼，通常會指派給單一媒體檔案。 此識別碼是用來識別授權中受保護內容的識別碼。

每個授權都會指定一或多個可以使用受保護內容執行的動作。 這些動作也稱為許可權，可透過許多方式來限制。 藉由合併開始日期、結束日期、計數和時間限制，授權簽發者可以在右方建立幾乎任何想像得到限制。

授權是由 Web 服務所發出。 取得授權時，它會儲存在用戶端電腦上的本機授權存放區中，該電腦是包含授權和其他 DRM 資料的受保護檔案。 當應用程式存取受保護的內容時，DRM 子系統會在本機授權存放區中搜尋授與適當許可權的授權。 如果找不到授權，則應用程式可以根據儲存在檔案 DRM 標頭中的資訊取得一個授權。

可以針對相同的受保護檔案發出多個授權。 當 DRM 子系統決定是否允許某項動作時，它會從所有套用的授權匯總許可權。 每個授權都可以指派優先順序。 如果某個動作套用了一個以上的授權，則會檢查最高優先順序的授權，以判斷是否需要減少計數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**概念**](drmconcepts.md)
</dt> </dl>

 

 




