---
title: 執行 Active Directory 服務介面提供者
description: Active Directory 服務介面 (ADSI) 是可包裝目錄服務物件的 COM 介面，以便將它們公開給目錄服務的用戶端。 藉由提供 ADSI 的執行，您可以將用戶端的基礎擴展至一組 ADSI 用戶端應用程式。
ms.assetid: f86f36f0-44ff-41b7-8cf6-b97b721a8572
ms.tgt_platform: multiple
keywords:
- 執行 Active Directory 服務介面提供者 ADSI
- 執行 ADSI 提供者 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd3eb1275398a82a2ef179678e56cb9a7eda2e63eb4278906fc925fcb1d7cf6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118427557"
---
# <a name="implementing-active-directory-service-interfaces-providers"></a>執行 Active Directory 服務介面提供者

Active Directory 服務介面 (ADSI) 是可包裝目錄服務物件的 COM 介面，以便將它們公開給目錄服務的用戶端。 藉由提供 ADSI 的執行，您可以將用戶端的基礎擴展至一組 ADSI 用戶端應用程式。

如同任何 COM 的執行，您可以撰寫許多語言的 ADSI 提供者。 ADSI COM 介面定義為雙重介面，可同時允許執行時間和編譯時期的名稱解析，並可透過符合 Automation 規範的語言（例如 Visual Basic、Visual Basic 腳本撰寫，以及 c 和 c + + 等更具效能和效率的語言）來呼叫。 ADSI 用戶端也包含透過 Microsoft Management Console 使用 Active Server 網頁和系統管理嵌入式管理單元的 web 應用程式。

因為 ADSI 提供自己的 OLE DB 提供者，所以執行 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 所定義的搜尋功能也可讓 ADSI 用戶端查詢目錄服務中的資料。

所有目錄服務物件都可以透過支援 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)的一般 ADSI 物件來表示。 ADSI 提供所需的組建區塊，以代表任何目錄服務的功能和服務。

此外，ADSI 中繼介面代表目錄管理員所使用的一般物件。 您可以將中繼介面的屬性對應至您目錄服務所支援的屬性。 當安裝提供者並重新啟動系統時，ADSI 用戶端對 Active Directory 服務介面進行程式設計時，就能取得目錄服務的存取權。

如果您的目錄服務支援架構標記法，則支援架構管理介面可讓您的命名空間直接存取目錄服務瀏覽器。 藉由透過架構發佈您的功能，用戶端可以在線上查詢您的目錄服務，並利用您提供的服務。 由於線上架構的可用性和 COM 介面的優勢，您可以在支援舊版的用戶端軟體時，繼續提供新功能。

 

 




