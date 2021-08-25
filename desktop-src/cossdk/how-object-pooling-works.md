---
description: 當您設定要共用的元件時，COM + 會在集區中維護其實例，並準備好針對任何要求元件的用戶端啟用。 任何物件建立要求都會透過集區管理員來處理。
ms.assetid: 34978b50-cd20-42fd-ad46-410190478ef8
title: 物件共用的運作方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df937dd8e3d7a2fb111c7825df101cd2b53f6f39a94326efb1eafe878d74daa6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954038"
---
# <a name="how-object-pooling-works"></a>物件共用的運作方式

當您設定要共用的元件時，COM + 會在集區中維護其實例，並準備好針對任何要求元件的用戶端啟用。 任何物件建立要求都會透過集區管理員來處理。

集區會以每個元件為基礎進行設定和維護。 集區是由共用相同 CLSID 的同質物件所組成。 唯一的例外是交易對象，其 subpools 會在交易暫止時，維護包含具有交易親和性之物件的物件。

當應用程式啟動時，只要物件建立成功，集區就會填入您所指定的最低層級。 當元件的用戶端要求進入時，就會從集區以 first 優先的基礎來滿足這些要求。 如果沒有可用的集區物件，且集區尚未達到指定的最大層級，就會為用戶端建立和啟用新的物件。

當集區達到其最大等級時，用戶端要求會排入佇列，並接收來自集區的第一個可用物件。 物件數目（包括已啟用和已停用）永遠不會超過最大的集區值。 物件建立要求會在系統管理員指定的期間之後過期，讓您可以控制用戶端等候物件建立的時間長度。 發生逾時錯誤時，用戶端會 \_ 從 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)取回錯誤 E TIMEOUT。

在可能的情況下，COM + 會在用戶端釋放之後，嘗試重複使用物件，直到集區達到其最大層級為止。 物件負責監視其狀態，以判斷它是否可以重複使用，並應該針對 [**IObjectControl：： CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)傳回適當的值。

建立集區物件時，會將它匯總成較大的物件，以管理物件的存留期。 外部物件會在物件的生命週期中，于適當的時間呼叫 [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) 的方法，如下所示：

-   每當物件傳回給用戶端時，就會呼叫 [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) 方法，而該物件會在特定內容中啟用。
-   只要用戶端釋出物件，或在 JIT 啟動的物件停用時，就會呼叫 [**停用**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) 方法。
-   只要將物件傳回至一般集區，就會呼叫 [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) 方法。 如果物件偵測到某些可重複使用的資源處於不正常的狀態，它應該會針對此方法傳回 **FALSE** ，而集區管理員會捨棄物件。

物件不一定需要執行 [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol)。 如果不是，則會一律重複使用實例，直到達到集區的最大層級為止。

如需有關如何設定要共用之元件的詳細資訊，請參閱設定 [要共用的元件](configuring-a-component-to-be-pooled.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 物件的函式字串](com--object-constructor-strings.md)
</dt> <dt>

[控制物件存留期和狀態](controlling-object-lifetime-and-state.md)
</dt> <dt>

[使用物件共用改善效能](improving-performance-with-object-pooling.md)
</dt> <dt>

[共用交易對象](pooling-transactional-objects.md)
</dt> <dt>

[共用物件的需求](requirements-for-poolable-objects.md)
</dt> </dl>

 

 
