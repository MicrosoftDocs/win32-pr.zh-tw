---
description: 用來建立分散式應用程式的其他 Microsoft 工具
ms.assetid: 518ca5b5-4285-4d69-abfe-bf6444a1deb5
title: 用來建立分散式應用程式的其他 Microsoft 工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed9114454dbbeaa3c8f21cc1ea5166f93760fdd99772425f0245d7b8883f2db3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070398"
---
# <a name="other-microsoft-tools-for-building-distributed-applications"></a>用來建立分散式應用程式的其他 Microsoft 工具

除了 COM + 中的工具之外，Microsoft 還提供下列工具來協助開發人員建立分散式應用程式：

-   Microsoft Data Access Components (MDAC) 。 Microsoft 提供數個可從無數來源抓取資料的途徑。 例如，OLE DB 提供一組用於建立資料庫元件的 COM 介面。 系統會定義介面，讓資料提供者可以根據基礎資料存放區的功能來執行不同層級的支援。 由於 OLE DB 是以 COM 為基礎，因此可以輕鬆擴充，並將擴充功能實作為新的介面。 OLE DB 也包含應用層級的程式設計介面，稱為 ActiveX Data Objects (ADO) 。 ADO 會公開雙重介面，因此可以輕鬆地從指令碼語言使用，以及 Microsoft Visual C++、Visual Basic 和其他開發人員工具。

    > [!Note]  
    > 開發人員也可以選擇使用泛型、廠商中立的 API，例如 Microsoft 開放式資料庫連接 (ODBC) 應用程式開發介面 (API) 。 ODBC API 是一種 C 語言介面，可讓您使用結構化查詢語言 (SQL)  (SQL) 來存取 DBMS 中的資料。 ODBC 驅動程式管理員會提供程式設計介面和執行時間元件，以找出 DBMS 特定的驅動程式。 ODBC 驅動程式通常是由 DBMS 廠商提供，可將 ODBC 驅動程式管理員的一般呼叫轉譯成原生資料存取方法的呼叫。 使用 ODBC API 的主要優點是，您只需要學習一個 API 來存取廣泛的 Dbms。

     

-   Microsoft SQL Server。 除了提供穩固且 eloquent 的關係資料庫系統之外，Microsoft SQL Server 可以提供具有連接共用和安全性的分散式應用程式，而該應用程式可與 Windows 的安全性模型整合。

-   COM 交易整合 (COMTI) 。 COMTI 可以用來將大型主機系統整合到 Windows 系統，包括 com + 應用程式。 COMTI 使用標準通訊協定 (例如，LU 6.2) 在 Windows 電腦和大型主機與 minicomputers 之間進行通訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 設計假設和原則](com--design-assumptions-and-principles.md)
</dt> <dt>

[使用 UML 設計 COM + 應用程式](designing-the-com--application-using-uml.md)
</dt> <dt>

[使用 COM + 的一般設計提示](general-design-tips-for-using-com-.md)
</dt> <dt>

[優化與 COM + 商務邏輯層的互動](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> </dl>

 

 



