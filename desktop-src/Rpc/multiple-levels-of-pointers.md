---
title: 多個指標層級
description: 在遠端程序呼叫中使用多個層級的指標， (RPC) 。
ms.assetid: d45b9b20-3b21-4d46-9097-8aacb4e4e921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a61a917ee29c982505c601d7b0dd0721e94e4678
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933456"
---
# <a name="multiple-levels-of-pointers"></a>多個指標層級

當有多個指標層級時，屬性會與最接近變數名稱的指標相關聯。 用戶端仍須負責配置與回應相關聯的任何記憶體。

下列範例可讓存根在不事先事先知道將傳回多少資料的情況下呼叫伺服器：

``` syntax
[
    uuid( ...),
    version(3.3),
]
interface AnInterface
{
    HRESULT GetBars([out] long * pSize,
             [out, size_is( , *pSize)]
             BAR ** ppBar);//BAR type defined elsewhere
}
```

在此範例中，存根會將唯一指標傳遞給伺服器，伺服器會將它初始化為 **Null**。 然後伺服器會配置橫條區塊、設定指標、設定 size 引數，然後傳回。 請注意，為了讓伺服器在呼叫端上有作用，您必須將 \[ ref 指標傳遞 \] 至您的 \[ 資料的 [**唯一**](/windows/desktop/Midl/unique) \] 指標。 另請注意， \[ [**大小 \_ 為**](/windows/desktop/Midl/size-is) (， \* pSize ) \] ，表示最上層指標不是大小的指標，但較低層級的指標是。

在用戶端上，存根集會在 \* 呼叫遠端程式之前，將 ppBar 設定為 **Null** 。 然後，存根會配置並拆收橫條圖物件的陣列。 Size 引數表示區塊 (的大小，以及) 的取消封送的橫條數。 當不再需要時，用戶端必須釋放所傳回的 BAR 物件陣列。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**大小 \_ 為**](/windows/desktop/Midl/size-is)
</dt> </dl>

 

 