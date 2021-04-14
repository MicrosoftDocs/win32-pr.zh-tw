---
title: ADSI 介面
description: 本主題說明 ADSI 介面所使用的類別。
ms.assetid: 8c735dbf-41d7-4fbb-b372-9abe4e1b8fdd
ms.tgt_platform: multiple
keywords:
- ADSI 介面 ADSI
- ADSI ADSI、參考、介面
- 介面 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2930292defa99301fb74f37c933a9af24b73f1fd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371853"
---
# <a name="adsi-interfaces"></a>ADSI 介面

Active Directory 服務介面 (ADSI) 支援一組豐富的介面，可根據下列類別分類：

-   [核心](core-interfaces.md)。 這些介面會提供 ADSI 物件的基本物件管理功能。 核心功能包括提供目錄存放區的進入點、將屬性載入屬性快取，以及認可基礎目錄的變更。
-   [架構](schema-interfaces.md)。 這些介面提供管理和延伸目錄架構的方法。
-   [屬性](property-cache-interfaces.md)快取。 這些介面會定義方法，以操作屬性快取中的屬性。
-   [持續性物件](persistent-object-interfaces.md)。 這些介面會操作基礎目錄服務的命名空間中的持續性資料。 ADSI 物件會執行這些類型的介面，以提供其持續性資料的存取權，包括使用者帳戶、檔案共用、組織階層和列印佇列中的作業清單。
-   [動態物件](dynamic-object-interfaces.md)。 這些介面會使用目錄服務中的動態資料。 基礎目錄服務中未表示的目錄物件會執行這類介面。 動態資料的範例包括透過網路發出的命令。
-   [安全性](security-interfaces.md)。 這些介面可讓 ADSI 用戶端建立其認證給伺服器，並使用目錄服務所支援的安全性功能，例如存取控制清單或安全描述項。
-   [非自動化](non-automation-interfaces.md)。 這些介面允許非自動化用戶端 (例如，C/c + + 應用程式) 低額外負荷的目錄物件存取權，方法是提供 Vtable 存取方法來管理和搜尋目錄服務物件。
-   [延伸](extension-interfaces.md)模組。 這些介面可讓 ADSI 用戶端擴充現有 ADSI 類別的功能，為目錄服務提供自訂的解決方案。
-   [公用程式](utility-interfaces.md)。 這些介面提供管理 ADSI 物件的 advanced helper 函數。
-   [資料類型](data-type-interfaces.md)。 這些介面會提供存取 ADSI 資料類型的方法。

 

 




