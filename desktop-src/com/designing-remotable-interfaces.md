---
title: 設計可遠端處理的介面
description: 隨著分散式元件物件模型的出現，即使您只想要在進程中使用它，您的自訂介面也很重要。
ms.assetid: 2ee4d950-dfd5-4965-bd77-a600e878be59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3502604d62e6a5129ca3e3538761722909c0198f
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "103841839"
---
# <a name="designing-remotable-interfaces"></a>設計可遠端處理的介面

隨著分散式元件物件模型的出現，即使您只想要在進程中使用它，您的自訂介面也很重要。

MIDL 不只是產生介面標頭檔的方法。 它是遠端的程式設計語言，可讓您跨電腦、進程和執行緒界限使用您的介面。 這表示在將程式發行給客戶之前，您必須先確認這些條件下 MIDL 定義介面的行為。 如果您在 IDL 中犯了錯誤，且介面未正確地進行遠端處理，可能很難補救該錯誤。 您必須使用新的 IID 來修改您的介面，並保留舊的，以提供回溯相容性，或者您必須同時將每個用戶端和每部伺服器電腦轉換成。

即使您的介面永遠不會使用跨進程，它也可以跨執行緒使用。 未檢查的 IDL 檔案最糟的問題，可能會發生在不支援多個 [單一執行緒單元](single-threaded-apartments.md)) 的同進程伺服器中。 未指定執行緒模型的伺服器隱含為單一執行緒。 所有標示為單一執行緒的專案都會強制進入先呼叫 [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) 或 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)的執行緒。 如果有其他執行緒是啟始物件的執行緒，則單一執行緒伺服器上的所有介面都必須從遠端回傳至啟動執行緒，這可能會導致傳回 REGDB \_ E \_ IIDNOTREG，以回應對 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))) 的呼叫。 除非您可以完全判斷提示您的介面同時處於同進程且一律會在相同的執行緒上呼叫，否則您將會在一段時間內進行遠端存取。

最後，作為介面設計工具，您需要考慮用戶端應用程式將如何使用您的介面。 另外還有兩件事，就是判斷介面在進程和電腦界限之間是否有效：跨介面界限的方法呼叫頻率，以及在指定的方法呼叫中要傳輸的資料量。 雖然 COM 讓程式得以透明地跨進程和跨網路呼叫，但是無法讓高頻率和高頻寬呼叫在位址空間之間有效率。 在某些情況下，設計介面較適合通常只會實作為同進程伺服器，而其他介面更適合遠端使用的介面。

 

 




