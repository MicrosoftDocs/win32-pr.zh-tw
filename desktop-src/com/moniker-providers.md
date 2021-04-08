---
title: 標記提供者
description: 標記提供者
ms.assetid: 4d4820d2-bf5f-4543-b318-59481dcc51de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde584e12daddacbc940b23b21a0386aa37de2c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673100"
---
# <a name="moniker-providers"></a>標記提供者

一般情況下，當元件允許存取其中一個物件時，它應該是「標記提供者」，同時仍可控制物件的儲存體。 如果元件即將推出可識別其物件的名字標記，它必須能夠執行下列工作：

-   在 [要求] 上，建立可識別物件的標記。
-   當用戶端呼叫 [**IMoniker：： BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) 時，啟用要系結的標記。

「標記提供者」必須建立適當的「 *標記」類別* 的標記來識別物件。 「標記」類別會參考 [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) 介面的特定執行，以定義所建立的標記類型。 雖然您可以執行 **IMoniker** 來建立新的「標記」類別，但通常不需要這樣做，因為 OLE 提供數個不同的「標記」類別，每個類別都有自己的 CLSID。 如需 OLE 提供之標記類別的描述，請參閱 [Ole 標記](ole-moniker-implementations.md) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[標記用戶端](moniker-clients.md)
</dt> <dt>

[OLE 標記執行](ole-moniker-implementations.md)
</dt> </dl>

 

 




