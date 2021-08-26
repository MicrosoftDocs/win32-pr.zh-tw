---
description: COM + 物件的函式字串是由系統管理員為元件指定的初始化字串。
ms.assetid: b4915dae-c97c-4d36-95ee-bb10dcb40845
title: COM + 物件的函數位符串概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9baef62780950e93043a48c2ccf13910faf7c692dc534f984ffd028e0b342dcd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029518"
---
# <a name="com-object-constructor-strings-concepts"></a>COM + 物件的函數位符串概念

COM + 物件的函式字串是由系統管理員為元件指定的初始化字串。 您可以使用物件的函式字串來撰寫具有某種程度的單一元件，讓它可以在稍後針對特定工作進行自訂;也就是說，您可以執行參數化物件結構。

例如，您可以使用這項功能來撰寫保存一般 ODBC 連接的元件，並于稍後為系統管理員指定元件的確切 DSN。 如果系統組態變更，您可以據此變更函式字串。

> [!Note]  
> 物件的函式字串不應該用來儲存安全性機密資訊。

 

您可以搭配 [物件](com--object-pooling.md) 共用使用物件的函式字串，以在您如何集區和重複使用資源的方式中達到更高程度的資料細微性。 例如，您可能會建立多個不同的元件（除了使用其他的函式字串和 Clsid），以維護不同的物件集區，以保留不同用戶端群組可用的連接。 如果連接是以系結至特定安全性角色的方式開啟，例如在資料庫上以特定的驗證開啟連接時（例如，在一般情況下將它們轉譯為不可重複使用），這會很有用。

若要這樣做，您可以使用 [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct)撰寫依賴物件函式字串的單一泛型元件，並將它重新編譯以產生數個可自訂的元件，每個元件都有不同的 CLSID。 然後，您可以系統管理員量身打造每個元件，以開啟與函式字串的適當連線、將它們設定為集區，並將其保留在每個 CLSID 的相異集區中。

明確撰寫元件以辨識您輸入的字串時，您可以指定一個函式字串。 元件可以使用 [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct)，以程式設計方式存取這些字串。

只有在物件結構已啟用系統管理的情況下，才會在物件建立時傳入函式字串。 COM + 會呼叫它所執行的 [**IObjectConstruct：：構造**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectconstruct-construct) 方法。 在該方法中，您可以使用 [**IObjectConstructString**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstructstring)存取函式字串。 空字串可以是有效的專案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 物件共用](com--object-pooling.md)
</dt> <dt>

[指定元件的物件表示函式字串](specifying-an-object-constructor-string-for-a-component.md)
</dt> <dt>

[使用物件的函式字串來建立元件](using-an-object-constructor-string-to-construct-a-component.md)
</dt> </dl>

 

 



