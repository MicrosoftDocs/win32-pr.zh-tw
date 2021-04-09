---
title: RPC)  (rpc NDR 引擎
description: 遠端程序呼叫 (RPC) 網路資料表示 (NDR) 引擎是 RPC 和 DCOM 元件的封送處理引擎。
ms.assetid: E452AA27-053D-4032-868B-CF2D5C0D4BE0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bf7ba92a74d2d7dc8c394c561f65337db13af99
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024452"
---
# <a name="rpc-ndr-engine-rpc"></a>RPC)  (rpc NDR 引擎

遠端程序呼叫 (RPC) 網路資料表示 (NDR) 引擎是 RPC 和 DCOM 元件的封送處理引擎。 NDR 引擎會處理遠端呼叫的所有存根相關問題。 在處理過程中，NDR 封送處理是由 MIDL 產生的存根、MIDL JIT 類型產生器，或由其他工具產生的存根或手動寫入的存根所驅動。 接著，NDR 引擎會驅動與特定傳輸通訊 (DCOM 或 RPC) 的基礎執行時間。

雖然存根是 MIDL 產生的 C 程式碼，但建議應用程式將存根視為不透明，而且強烈建議您不要修改存根內的任何內容。 如果在內容中呼叫這些 NDR 常式，則行為會是未定義的。

下列主題會更詳細地說明 RPC NDR 引擎：

-   [傳輸語法和 NDR64](transfer-syntax-and-ndr64.md)
-   [RPC NDR 格式字串](rpc-ndr-format-strings.md)
-   [RPC NDR 介面參考](rpc-ndr-interface-reference.md)

 

 




