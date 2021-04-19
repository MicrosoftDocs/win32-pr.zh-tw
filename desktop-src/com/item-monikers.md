---
title: 專案的名字
description: 另一個已執行 OLE 的標記類別是專案標記，可用來識別包含在另一個物件中的物件。
ms.assetid: ddcf3669-4ad0-4a4e-80a6-eb78058cff09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57b692502ba44519a2c51a661ef62a51e133ac04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967395"
---
# <a name="item-monikers"></a>專案的名字

另一個已執行 OLE 的標記類別是 *專案標記*，可用來識別包含在另一個物件中的物件。 其中一種包含的物件是內嵌在複合檔案中的 OLE 物件。 複合檔案可以藉由將任意名稱（例如 "embedobj1"、"embedobj2" 等等）指派給每一個，來識別它所包含的内嵌物件。 另一種類型的包含物件是檔中的使用者選取專案，例如試算表中的資料格範圍，或文字檔中的字元範圍。 包含選取專案的物件稱為 *虛擬物件* ，因為它不會被視為相異物件，直到使用者標示選取範圍為止。 試算表可能會使用名稱（例如 "1A： 7F"）來識別儲存格範圍，而文字處理檔可能會使用書簽的名稱來識別字元範圍。

專案的標記主要適用于串連或 *組成* 的另一個標記，以識別容器。 通常會建立專案的名字標記，然後將它組成 (例如) 檔案的標記，以建立與物件之完整路徑相等的專案。 例如，您可以撰寫檔案標記 "c： \\ work \\report.doc" (它會識別容器物件) 具有專案標記 "embedobj1" (這會識別容器內的物件，) 可 \\ \\ \\ 唯一識別特定檔案中的特定物件。 您也可以串連其他專案的專案識別碼，以識別深層嵌套的物件。 例如，如果 "embedobj1" 是試算表物件的名稱，若要在該試算表物件中識別特定範圍的資料格，您可以附加另一個專案的標記，以建立相當於 "c： \\ work \\report.doc\\ Embedobj1 \\ 1a： 7F" 的標記。

結合檔案的標記時，專案的標記會形成完整的路徑。 專案的名字標記會將路徑名稱的概念延伸到檔案系統之外，並定義路徑名稱來識別個別物件，而不只是檔案。

專案的名字和檔案的名字之間有顯著的差異。 檔案標記中包含的路徑對了解檔案系統的任何人都有意義，而專案標記中包含的部分路徑只對特定的容器有意義。 每個人都知道 "c： \\ work \\report.doc" 的參考，但只有一個特定的容器物件知道 "1A： 7F" 的參考。 一個容器無法解讀另一個應用程式所建立的專案標記;唯一知道專案標記所參考之物件的容器是一開始將專案標記指派給物件的容器。 基於這個理由，藉由檔案和專案標記的組合所命名的物件來源，不僅必須實 [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)，也不能用來系結檔案的名字標記，還可以 [**IOleItemContainer**](/windows/desktop/api/OleIdl/nn-oleidl-ioleitemcontainer) 在檔案內容中，協助將專案標記的名稱解析為適當的物件。

使用標記的優點是，只要專案的名字標記是複合專案的一部分，使用「標記」（item）來尋找物件的使用者就不需要瞭解專案標記中包含的名稱。 一般情況下，專案的標記本身本身並不合理。 相反地，您會將專案標記撰寫至檔案的標記。 然後，您會在複合上呼叫 [**IMoniker：： BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) ，以系結其內的個別名字，並解讀名稱。

為了建立專案的「名字標記」物件，並將其指標傳回至「標記提供者」，OLE 提供 helper 函數 [**CreateItemMoniker**](/windows/desktop/api/Objbase/nf-objbase-createitemmoniker)。 此函式會建立專案的標記物件，並將其指標傳回給提供者。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[反標記](anti-monikers.md)
</dt> <dt>

[類別名字標記](class-monikers.md)
</dt> <dt>

[複合的名字](composite-monikers.md)
</dt> <dt>

[檔案名字](file-monikers.md)
</dt> <dt>

[指標標記](pointer-monikers.md)
</dt> </dl>

 

 




