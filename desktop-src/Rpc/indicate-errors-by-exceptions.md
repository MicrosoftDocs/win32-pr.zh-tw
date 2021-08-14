---
title: 依例外狀況指出錯誤
description: 針對傳統的 C 程式設計人員，通常會透過傳回值傳回錯誤，或使用會傳回錯誤碼的特殊 out 參數。
ms.assetid: 85ee217d-6e0b-4160-9cec-a652c1daa9a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 816f63f9378c3f2338c7bed6f6a9b5f785d3e138e4762c355aa1932887fd14c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928914"
---
# <a name="indicate-errors-by-exceptions"></a>依例外狀況指出錯誤

針對傳統的 C 程式設計人員，通常會透過傳回值傳回錯誤，或使用會傳回錯誤碼的特殊 \[ out \] 參數。 這會導致介面實作為下列方法：

``` syntax
long sample(...)
{
    ...
    p = new Cbar(...);
    if (p == NULL)
    {
        // cleanup
        ...
        return ERROR_OUTOFMEMORY;
    }
}
```

這種方法的問題在於，RPC 傳回值只是長整數。 它們沒有任何特殊意義的錯誤 (請注意， [**錯誤 \_ 狀態 \_ t**](/windows/desktop/Midl/error-status-t) 在伺服器) 端沒有特殊的語法，這會帶來重要的影響。

首先，RPC 不會收到作業失敗的警示;它會嘗試 unmarshal 所有 \[ in、out \] 和 \[ out \] 引數。 內容控制碼的失敗語義也不同。 傳回給用戶端的封包基本上是成功封包，且錯誤碼在封包中是深深的。 這也表示 RPC 不會使用延伸的錯誤資訊，因此用戶端軟體通常無法分辨呼叫失敗的位置。

藉由擲回結構化例外狀況處理 (SEH) 例外狀況 (非 c + +) 是更好的方法，來指出 RPC 伺服器常式中的錯誤。 擲回 SEH 例外狀況時，控制項會直接進入 RPC 執行時間。 有時，在無法正常清除的常式中，有時會發生錯誤，而且需要對其呼叫端表示錯誤。 常式應該會將錯誤傳回給它的呼叫者，然後它會將錯誤傳回給其呼叫端等等。 不過，堆疊上的最後一個伺服器常式應該在它回到 RPC 之前擲回例外狀況，以向 RPC 指出發生錯誤。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[例外狀況處理](exception-handling.md)
</dt> </dl>

 

 