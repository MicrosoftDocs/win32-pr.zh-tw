---
description: 控制物件存留期和狀態
ms.assetid: 172e07a2-1711-4353-9099-ff9d31a564c6
title: 控制物件存留期和狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2159f491267ac4d83a75c003005bd6bf7707d0db769d467fcfdfc3799ea08d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128820"
---
# <a name="controlling-object-lifetime-and-state"></a>控制物件存留期和狀態

集區物件可以藉由執行 [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol)來參與 com + 如何管理其集區中的活動。 建立集區物件時，會將它匯總成較大的物件，藉由在物件生命週期的一般點上呼叫下列方法來管理物件 **IObjectControl** ：

-   [**啟用**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)—每當物件傳回至用戶端時呼叫，並在特定內容中啟用。
-   [**停用**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate)—每當用戶端釋放物件時呼叫，或在 JIT 啟用物件停用時呼叫。
-   [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)—每次將物件傳回至一般集區時呼叫。

執行 [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) 是選擇性的，但交易對象除外，其應一律執行 [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) 來監視所持有資源的狀態。 不過，建議您在大部分的情況下執行 **IObjectControl** ，因為它會提供有效的方式來管理集區物件的行為，如下所述。

## <a name="performing-context-specific-initialization"></a>正在執行 Context-Specific 初始化

使用「啟動」時，您可以在針對指定用戶端 [**啟動**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)該物件的內容中初始化該物件。 例如，若要判斷物件是否有交易親和性 (其資源可能已經登錄) ，您可能會取得與內容相關聯的交易識別碼。

一般來說，您會使用 [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)來執行在物件所公開之任何方法之間一致的初始化，將它視為物件之函式的內容特定部分。

## <a name="cleaning-up-any-client-state"></a>清除任何用戶端狀態

使用「 [**停用**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate)」時，您可以擺脫可能存在的任何用戶端特定狀態，讓您的物件以完全一般的狀態回到集區，並可供任何用戶端使用，而不會危及安全性或隔離。

## <a name="controlling-reuse-of-the-object"></a>控制物件重複使用

您可以使用 [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)來監視物件的內部狀態，並報告其是否適合重複使用。 如果 **CanBePooled** 傳回 True 且未達到集區最大值，則會將物件放回一般集區中。 如果 **CanBePooled** 傳回 False，則會捨棄物件。 在交易式元件的案例中，傳回 False 將會毀滅目前的交易。

一般而言，您會保留物件的一些全域資料成員，如果您偵測到連接不正確，或某個資源的狀態不正確，請設定此項以反映目前的狀況，並透過 [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)傳回。

如果物件不會執行 [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)，則會繼續重複使用實例，直到達到集區最大層級為止。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 物件的函式字串](com--object-constructor-strings.md)
</dt> <dt>

[物件共用的運作方式](how-object-pooling-works.md)
</dt> <dt>

[使用物件共用改善效能](improving-performance-with-object-pooling.md)
</dt> <dt>

[共用交易對象](pooling-transactional-objects.md)
</dt> <dt>

[共用物件的需求](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



