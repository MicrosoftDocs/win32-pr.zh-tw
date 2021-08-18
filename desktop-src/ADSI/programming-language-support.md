---
title: 程式設計語言支援
description: 您可以撰寫許多語言的 ADSI 用戶端應用程式。
ms.assetid: 47460d57-936d-4c5f-8ff6-a4d9d60d0b68
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ebe355e3274821bf81a666380bfe70ca0f3f7b49e2bc9de10bf2aa4796b5288
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023298"
---
# <a name="programming-language-support"></a>程式設計語言支援

您可以撰寫許多語言的 ADSI 用戶端應用程式。 針對大部分的系統管理工作，ADSI 會定義可從符合自動化的語言存取的介面和物件。 例如，microsoft Visual Basic 開發系統、microsoft Visual Basic 腳本版本 (VBScript) 和 JAVA，以及更多效能和效率的語言，例如 C 和 c + +。

與 Active Server Pages 和 VBScript 的流暢整合，可讓您輕鬆地撰寫可存取目錄服務的網際網路應用程式。 為了與 OLE DB 的應用程式整合，ADSI 藉由支援 OLE DB 查詢介面的子集來提供 OLE DB 提供者。 OLE DB 提供者支援 Active Directory 的唯讀存取。

針對網際網路應用程式，使用 [Active Server 中的腳本] 頁面 (ASP) 檔案可以在伺服器上建立及操作 ADSI 物件，並在網頁中顯示結果。 在 Microsoft Management Console 中，目錄-服務管理嵌入式管理單元可以使用 ADSI 來尋找感興趣的目錄服務。 簡單地說，Active Directory 服務介面可以存取廣泛且多樣化的一組目錄服務，包括尚未建立的目錄服務。

為了存取使用傳統 Api 的結構，ADSI 架構定義了低層級介面，不支援從 C 和 c + + 等語言存取的自動化。 這些介面只是目錄服務的網路通訊協定的 COM 包裝函式。

將程式碼寫入已發行的介面，可讓您的應用程式連接到所有已安裝 ADSI 提供者的目錄服務，並整合所產生的資料。 只要稍微變更或完全不變更您的程式碼，您的應用程式就可以在安裝新的 ADSI 提供者時，繼續存取您網路上的其他目錄服務。

下圖顯示 ADSI 如何融入應用程式環境。 無論應用程式是以 Visual Basic、c/c + +、VBScript、Microsoft JScript 開發系統，或是使用 Active Server Pages 的 web 應用程式所撰寫，Active Directory 服務介面都能讓您在不需要使用原生網路 api 的情況下，對基礎目錄服務提供乾淨且容易使用的存取權。

![程式設計語言的 adsi 支援](images/ds2layr.png)

如上圖所示，不支援 Automation 的用戶端可以存取所有 ADSI 介面，包括具有命名慣例的純 COM 介面 **IDirectoryXXX** ，以及具有命名慣例 **IADSXXX** 的 Automation com 介面。 由於用戶端主要是要求來自目錄服務的資訊，因此透過 OLE DB 和 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 的 ADSI 彈性查詢模型會有效。

 

 




