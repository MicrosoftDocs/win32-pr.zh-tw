---
description: 共用物件必須符合特定需求，才能讓多個用戶端使用單一物件實例。
ms.assetid: 2cd4211e-be12-4197-8b43-5cb9f2321016
title: 共用物件的需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78d6834210f180ad8b514b51b6926b5cd30714fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936262"
---
# <a name="requirements-for-poolable-objects"></a>共用物件的需求

共用物件必須符合特定需求，才能讓多個用戶端使用單一物件實例。

## <a name="stateless"></a>無狀態

為了維護安全性、一致性和隔離，共用物件應該不會將用戶端特定的狀態從用戶端保留給用戶端。 您可以使用 [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol)來管理任何每個用戶端狀態，使用 [**IObjectControl：： Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) 執行內容特定的初始化，並使用 [**IObjectControl：:D eactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate)來清除任何用戶端狀態。 如需詳細資訊，請參閱 [控制物件存留期和狀態](controlling-object-lifetime-and-state.md)。

## <a name="no-thread-affinity"></a>無線程親和性

共用物件無法系結至特定的執行緒;否則，效能可能會造成災難性的後果。 基於這個理由，共用物件不能標示為在單元模型中執行;它們必須在多執行緒單元或中立的單元中執行。 此外，共用物件不應該使用執行緒區域儲存區，也不應該匯總無限制執行緒封送處理器。 如需 COM + 中線程的詳細資訊，請參閱 [Com + 執行緒模型](com--threading-models.md)。

> [!Note]  
> Microsoft Visual Basic 6.0 及更早版本的開發環境只能建立單元模型元件。 不過，在 Visual Basic .NET 中，可以將元件共用。

 

## <a name="aggregatable"></a>可彙總

共用物件必須支援匯總，也就是，它們必須支援使用非 Null 的 *pUnkOuter* 引數叫用 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)來建立。 當 COM + 啟動集區物件時，它會建立匯總來管理集區物件的存留期，並在 [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol)上呼叫方法。 如需有關撰寫可匯總物件的詳細資訊，請參閱 [匯總](/windows/desktop/com/aggregation)。

## <a name="transactional-components"></a>交易元件

參與交易的共用物件必須手動登錄 managed 資源。 在共用時，如果您的物件持有受控資源（例如資料庫連線），則當物件在指定的內容中啟動時，資源管理員將無法自動在交易中登記。 因此，物件本身必須處理偵測交易的邏輯，關閉 resource manager 的自動登記，並手動登錄其保留的任何資源。 此外，交易式集區物件應該會在 [**IObjectControl：： CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)的參數值中反映其資源的目前狀態。 如需詳細資訊，請參閱共用 [交易對象](pooling-transactional-objects.md)。

## <a name="implement-iobjectcontrol-to-manage-the-object-lifetime"></a>執行 IObjectControl 以管理物件存留期

雖然並非絕對必要，但共用物件仍應執行 [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol)。 但是，共用的交易元件必須執行 **IObjectControl**。 這些元件應該監視所持有資源的狀態，並指出無法重複使用的時間;當 [**IObjectControl：： CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) 傳回 false 時，它會毀滅交易。 如需詳細資訊，請參閱 [控制物件存留期和狀態](controlling-object-lifetime-and-state.md)。

## <a name="language-restrictions"></a>語言限制

使用 Microsoft Visual Basic 6.0 及更早版本所開發的元件無法進行集區，因為這些元件將會是單元模型執行緒。 不過，在 Visual Basic .NET 中，可以將元件共用。

## <a name="legacy-components"></a>傳統元件

只要它們為非交易式且符合適當的先前需求，即使元件並未特別以共用功能寫入，也可以共用。 不需要執行 [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol);沒有這麼做的元件，就不會參與管理其存留期。 如果未執行 [**IObjectControl：： CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) ，則會繼續重複使用物件，直到集區並達到大小上限為止。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 物件的函式字串](com--object-constructor-strings.md)
</dt> <dt>

[控制物件存留期和狀態](controlling-object-lifetime-and-state.md)
</dt> <dt>

[物件共用的運作方式](how-object-pooling-works.md)
</dt> <dt>

[使用物件共用改善效能](improving-performance-with-object-pooling.md)
</dt> <dt>

[共用交易對象](pooling-transactional-objects.md)
</dt> </dl>

 

 
