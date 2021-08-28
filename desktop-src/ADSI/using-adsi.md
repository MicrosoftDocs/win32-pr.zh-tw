---
title: 使用 Active Directory 服務介面
description: " (ADSI) 的 Active Directory 服務介面，可讓目錄服務的用戶端應用程式使用一組介面，來與提供 ADSI 執行的任何命名空間進行通訊。"
ms.assetid: 58bde1ea-30d1-4601-a6fb-df0bb837e2ab
ms.tgt_platform: multiple
keywords:
- 使用 Active Directory 服務介面 ADSI
- ADSI ADSI，使用
- Active Directory 服務介面 ADSI，使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15495f9fa21f436570381ea8f0b2a7c7fff5f4efed645a5f3465a3b5d2929776
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648848"
---
# <a name="using-active-directory-service-interfaces"></a>使用 Active Directory 服務介面

 (ADSI) 的 Active Directory 服務介面，可讓目錄服務的用戶端應用程式使用一組介面，來與提供 ADSI 執行的任何命名空間進行通訊。 ADSI 用戶端會使用定義完善的 Active Directory 服務介面來取代網路專屬的 API 呼叫，以取得更簡單的命名空間服務存取權。

Active Directory 服務介面符合元件物件模型 (COM) 並支援標準 COM 功能。

ADSI 提供的介面符合與名稱系結控制器（例如 JAVA、Microsoft Visual Basic 開發系統，以及 Visual Basic 腳本撰寫版 (VBScript) ）的自動化。 ADSI 也可以提供介面，以將不符合自動化規範的介面效能優化，以與 C 和 c + + 等語言環境搭配使用。

ADSI 也提供非自動化介面 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) 和 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)，以支援目錄物件管理和查詢。

此外，ADSI 也提供自己的 OLE DB 提供者，因此任何已使用 OLE DB 的用戶端（包括使用 ActiveX Data Objects 的用戶端）都可以直接查詢目錄服務。

使用 Active Server Pages 的 Web 應用程式也可以透過 ADSI 來設計目錄服務的存取權。

ADSI 用戶端可以用程式設計方式探索網站上的所有 ADSI 提供者，並使用相同的介面來與每個命名空間進行通訊。 當安裝其他提供者時，ADSI 用戶端也可以透過新的命名空間進行通訊，而不需要重新編譯。

此程式設計指南說明 ADSI 的運作方式，並提供在 ADSI 中執行特定工作的資訊。 我們將討論下列主題：

-   [系結至 ADSI 物件](binding-to-an-adsi-object.md)
-   [建立和刪除物件](creating-and-deleting-objects.md)
-   [使用 ADSI 存取及運算元據](accessing-and-manipulating-data-with-adsi.md)
-   [使用 ADSI 架構](using-the-adsi-schema.md)
-   [集合和群組](collections-and-groups.md)
-   [列舉 ADSI 物件](enumerating-adsi-objects.md)
-   [搜尋 Active Directory](searching-active-directory.md)
-   [ADSI 安全性模型](adsi-security-model.md)
-   [ADSI 擴充功能](adsi-extensions.md)
-   [使用 ADSI 搭配 Exchange](using-adsi-with-exchange.md)
-   [ADSI 公用程式介面](adsi-utility-interfaces.md)
-   [使用 JAVA/COM 編寫 ADSI 程式設計](programming-adsi-with-javacom.md)

 

 




