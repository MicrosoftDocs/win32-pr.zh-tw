---
description: ICE39 會驗證資料庫的摘要資訊資料流程。
ms.assetid: 9de72de6-fd9c-4d94-92f7-61b85dff0f6a
title: ICE39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e72e7b4a73f3a134ec108b07666cc1c4e9af23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979900"
---
# <a name="ice39"></a>ICE39

ICE39 會驗證資料庫的 [摘要資訊資料流程](summary-information-stream.md) 。

ICE39 會檢查下列屬性的格式：

-   [**字數統計摘要**](word-count-summary.md)
-   [**頁面計數摘要**](page-count-summary.md)
-   [**範本摘要**](template-summary.md)
-   [**修訂編號摘要**](revision-number-summary.md)
-   [**建立時間/日期摘要**](create-time-date-summary.md)
-   [**上次儲存的時間/日期摘要**](last-saved-time-date-summary.md)
-   [**上次列印的摘要**](last-printed-summary.md)

如果 [ [**字數統計摘要**](word-count-summary.md) ] 屬性指定要壓縮來源，ICE39 會在檔案 [資料表](file-table.md)的 [屬性] 資料行中將任何檔案標示為已壓縮時，張貼警告。 請參閱 [使用封包和壓縮的來源](using-cabinets-and-compressed-sources.md)。

如果 [ [**字數統計**](word-count-summary.md) ] 屬性指定封裝符合 UAC 規範，且 [MsiPackageCertificate 資料表](msipackagecertificate-table.md) 不是空的，ICE39 會張貼警告。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



