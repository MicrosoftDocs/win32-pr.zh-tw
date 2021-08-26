---
description: 以參數形式傳遞物件
ms.assetid: 174847c8-4545-4f61-ae13-42bdec1405e7
title: 以參數形式傳遞物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c47669d3e3e5af572b6dfd50dcbbefacf5c008971f276408fa87b37ccbed9a1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070378"
---
# <a name="passing-objects-as-parameters"></a>以參數形式傳遞物件

COM + 佇列元件服務不會針對每個現有的 COM 元件啟用佇列。 可以排入佇列的方法類型有一些限制。 由於訊息條件約束的限制，方法必須遵守下列規則：

-   它們必須只包含輸入參數。
-   它們必須不傳回任何應用程式特定的結果。

此外，可傳遞至已排入佇列之元件的輸入參數類型也有一些限制。 在執行時間，已排入佇列的元件服務會封裝用戶端的引數，並使用 [訊息佇列](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85))將這些引數傳遞至伺服器元件。 簡單類型（例如整數和布林值）可以輕易地封送處理，在沒有協助的情況下，無法封送處理更複雜的類型。

如果透過佇列元件的方法呼叫來傳遞物件做為參數，用戶端會將物件傳遞給錄製器。 錄製器會將物件封送處理為訊息佇列訊息，並將它傳遞給接聽程式。 當接聽程式拾取訊息並將它傳遞給播放程式之後，播放程式必須 reinstantiate 物件，以將其分派給用戶端所指定的方法呼叫。 根據佇列環境中用戶端和伺服器的存留期，暗示這些物件必須能夠以傳值方式封送處理。 因為 COM + 並不提供標準 COM 物件的傳遞值語義，所以錄製器和播放機需要元件的協助封送處理和 unmarshal 物件。

支援 [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) 的物件參考可用來做為已排入佇列元件上的方法呼叫的參數。 物件無法進行 reinstantiated 時的假設。 例如，伺服器可能無法使用，或伺服器元件可能會在一天之後才啟動。 不支援 **IPersistStream** 的物件將會傳回錯誤。

## <a name="visual-basic-persistable-objects"></a>Visual Basic永久性物件

Microsoft Visual Basic 6 允許建立永久性物件。 這些物件支援 [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) ，並且可以做為參數傳遞至已排入佇列的元件方法呼叫。 在 Visual Basic 物件可以傳遞至已排入佇列的元件之前，必須先初始化永久性物件。 這可以透過下列兩種方式之一來完成：

-   如果建立永久性物件的應用程式是以 Visual Basic 寫入，則 Visual Basic 執行時間會自動處理物件初始化。
-   如果建立 Visual Basic 永久性物件的應用程式是以 Visual Basic 以外的語言（例如 Microsoft Visual C++）撰寫，則應用程式必須藉由查詢永久性物件的 [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream)介面或呼叫 [**IPersistStreamInit：： InitNew**](/windows/desktop/api/ocidl/nf-ocidl-ipersiststreaminit-initnew)或 [**IPersistStream：： Load**](/windows/desktop/api/objidl/nf-objidl-ipersiststream-load)方法，明確地初始化元件。

## <a name="ado-recordsets-and-ole-db-rowsets"></a>ADO 記錄集和 OLE DB 資料列集

在元件之間傳遞 ADO **記錄集** 或 OLE DB 資料列集物件，可讓一個元件處理由另一個元件所執行之查詢的結果。 在多部電腦上部署應用程式時，這會很有説明。 **記錄集** 和資料列集物件可以做為方法參數傳遞至已排入佇列的元件，但有下列限制：

-   伺服器端 **記錄集** 物件無法使用 [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream)進行封送處理。 只有用戶端 **記錄集** 物件可以做為參數傳遞至已排入佇列的元件方法呼叫。
-   如果您直接使用 OLE DB，OLE DB 資料列集必須定義為用戶端資料列集。

 

 
