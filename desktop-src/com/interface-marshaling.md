---
title: 介面封送處理
description: 介面封送處理
ms.assetid: 71069bd3-5f90-406a-be78-bb1af9b1c1c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cdee8762fb9ef69507fb5b2c4295531dd87a98d5174ab4e10f05a66cab718d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029868"
---
# <a name="interface-marshaling"></a>介面封送處理

除非您知道您的介面永遠不會跨整個單元、執行緒或進程界限使用，否則您必須決定如何為您的介面提供封送處理支援。 有三種方式可以提供封送處理支援：

-   撰寫您自己的 proxy/stub 程式碼，以呼叫 COM 通道，進而呼叫 RPC 執行時間程式庫。 理論上，您可以這麼做，但在實務上，幾乎不可能進行大量的工作。
-   描述介面定義語言中的介面 (IDL) 檔，並使用 MIDL 編譯器來產生 proxy/stub DLL。 這個方法會以可接受的資料類型，提供最佳效能和最大的彈性。 使用 MIDL 產生的 proxy 存根，您不僅可以控制記憶體管理，也可以控制跨不同平臺的複雜資料類型封送處理和封送處理。
-   使用 MIDL 來產生系統在執行時間用來提供封送處理支援的類型程式庫。 這是執行封送處理支援的最簡單方式。 您只需要產生類型程式庫並加以註冊。 您的介面必須是 [**oleautomation**](/windows/desktop/Midl/oleautomation) 或 [**雙重**](/windows/desktop/Midl/dual)) 的自動化相容 (，這會對您可以用來做為方法參數的資料類型類型有一些限制。 不過，在大部分情況下，讓您的介面可供以其他語言（例如 Microsoft Visual Basic 和 JAVA）撰寫的程式存取，比資料類型的限制還高。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[物件間通訊](inter-object-communication.md)
</dt> </dl>

 

 