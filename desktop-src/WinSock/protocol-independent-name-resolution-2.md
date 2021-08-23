---
description: 與通訊協定無關的名稱解析和 Windows 通訊端 (Winsock) 。
ms.assetid: f55219b9-1518-4b49-a0da-6a3fa025cca3
title: Protocol-Independent 名稱解析
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f214619d4bf54f3ac39d24008f07aa12715fc75ac1bf6ea74280ed80d31d7bb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993598"
---
# <a name="protocol-independent-name-resolution"></a>Protocol-Independent 名稱解析

在開發與通訊協定無關的用戶端/伺服器應用程式時，有兩個基本的需求存在於名稱解析和註冊方面：

-   伺服器一半的應用程式 ( 服務) 在 (內登錄其存在，或可) 一或多個命名空間存取。
-   用戶端應用程式在命名空間中尋找服務的能力，並取得所需的傳輸通訊協定和定址資訊。

針對習慣開發以 TCP/IP 為基礎的應用程式的人，這似乎只需要查閱主機位址，然後使用同意的埠號碼。 不過，其他網路設定則允許服務的位置、用於服務的通訊協定，以及在執行時間探索到的其他屬性。 為了配合現有名稱服務中的廣泛多樣性功能，Windows 通訊端2介面採用本節中的主題所述的模型。

本節說明 Winsock 開發人員可用的通訊協定獨立名稱解析功能。 下列清單說明本節中的主題：

-   [名稱解析模型](name-resolution-model-2.md)
-   [名稱解析函數的摘要](summary-of-name-resolution-functions-2.md)
-   [名稱解析資料結構](name-resolution-data-structures-2.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[註冊和名稱解析](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



