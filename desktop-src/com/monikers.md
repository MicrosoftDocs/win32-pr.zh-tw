---
title: 名字
description: COM 中的名字標記不只是識別物件 \ 郵件的方式; 也會將標記實作為物件。
ms.assetid: ae0cd2f3-8ac0-4388-8781-e86fc4a26b3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf148d63611b5252eec9f5f5f69eacbcece8c65f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020881"
---
# <a name="monikers"></a>名字

COM 中的名字標記並不只是識別物件的方式，也就是將標記實作為物件。 這個物件提供的服務可讓元件取得以標記識別之物件的指標。 此 *進程稱為系結。*

「名字」是實 [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) 介面的物件，而且通常會在 dll 中實作為元件物件。 有兩種方式可以查看標記的使用方式：做為標記用戶端，這是使用標記來取得其他物件指標的元件;和作為「標記提供者」（provider），此元件會提供將其物件識別為「標記用戶端」的名字

無論物件是在同一部電腦或整個網路中，OLE 都會使用它來連接和啟始物件。 很重要的用途是針對網路連接。 它們也可用來識別、連接和執行 OLE 複合檔案連結化物件。 在此情況下，連結來源會作為「標記提供者」，而保留連結化物件的容器則會作為「標記用戶端」。

如需詳細資訊，請參閱下列主題：

-   [標記用戶端](moniker-clients.md)
-   [標記提供者](moniker-providers.md)
-   [OLE 標記執行](ole-moniker-implementations.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[元件物件模型](the-component-object-model.md)
</dt> </dl>

 

 




