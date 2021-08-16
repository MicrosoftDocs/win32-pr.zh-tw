---
description: 並存元件可與下列類型的資訊清單和設定檔搭配使用。 資訊清單和設定為 XML 檔案。
ms.assetid: 8b969a8f-586c-4556-87be-92db6c61e8ce
title: "  資訊清單檔案參考"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87636a8a4e5398cf9bb274d5ea8b9e7620104989322a20138a162ca45d9caf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142061"
---
# <a name="manifest-files-reference"></a>  資訊清單檔案參考

並存元件可與下列類型的資訊清單和設定檔搭配使用。 資訊清單和設定為 XML 檔案。



| file:///                                                               | 描述                                                                                                                                                                                                   |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [組件資訊清單](assembly-manifests.md)                           | 描述並存元件的名稱、版本、資源和元件相依性。                                                                                                               |
| [應用程式資訊清單](application-manifests.md)                     | 描述應用程式在執行時間應系結的共用並存元件名稱和版本，也可能包含應用程式所使用之私用並存元件的中繼資料。 |
| [應用程式組態檔](application-configuration-files.md) | 使用 [每個應用程式](per-application-configuration.md)設定，重新導向元件相依性的元件版本。                                                                            |
| [Publisher設定檔](publisher-configuration-files.md)     | 使用 [發行者](publisher-configuration.md)設定，重新導向每個元件的元件相依性元件版本。                                                              |



 

如需資訊清單檔案架構的清單，請參閱 [資訊清單檔案架構](manifest-file-schema.md)。

如需應用程式佈建檔架構的清單，請參閱 [應用程式佈建檔架構](application-configuration-file-schema.md)。

如需發行者設定檔架構的清單，請參閱[Publisher 設定檔架構](publisher-configuration-file-schema.md)。

其他技術可延伸 Windows 版本控制和設定資訊清單所使用的格式。 開發人員應該參考用來取得資訊清單格式相關資訊之技術的相關檔。 例如：

-   [ClickOnce](/visualstudio/deployment/clickonce-reference?view=vs-2015)
-   [Common Language Runtime](/dotnet/standard/clr)
-   [使用者帳戶控制 (UAC)](/previous-versions/bb756929(v=msdn.10))

 

 
