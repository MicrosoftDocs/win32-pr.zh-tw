---
title: 開發高效能 RPC 伺服器
description: 本節中的資訊適用于遠端通訊協定序列 ncacn \_ ip \_ tcp、ncacn \_ HTTP、ncacn \_ np，以及 Windows 2000 和 Windows XP。
ms.assetid: 7b4239af-951b-4d1b-8ac3-224279f6929e
keywords:
- 遠端程序呼叫 RPC、最佳作法、開發高效能伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 841c52587410b10ae17f2ebd858863327aaf5ab1def92600259c8e49edc87946
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021767"
---
# <a name="developing-a-high-performance-rpc-server"></a>開發高效能 RPC 伺服器

本節中的資訊適用于遠端通訊協定序列： [**ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp)、 [**ncacn \_ HTTP**](/windows/desktop/Midl/ncacn-http)、 [**ncacn \_ np**](/windows/desktop/Midl/ncacn-np)，以及 Windows 2000 和 Windows XP。

本節討論 RPC 伺服器效能的三個主要層面：

-   [網路延遲和輸送量](network-latency-and-throughput.md)
-   [延展性](scalability.md)
-   [其他 RPC 效能提示](miscellaneous-rpc-performance-tips.md)

程式碼路徑長度是 RPC 的另一個主要效能考慮。 程式碼路徑長度通常很清楚，而且由於該主題的文獻和工具廣泛提供，因此本文無法解決此情況。

考慮 RPC 效能時，要記住的重要且已建立的一般效能規則如下：找出系統中的瓶頸，並解決此問題。 管制瓶頸可能不是 RPC 程式設計，如果是這種情況，則在解決瓶頸之前，RPC 中的效能微調將不會導致效能提高。 例如，因資源爭用而造成的系統不需要更有效率地使用網路。

如果您的系統是部署在不同的環境中，最好是確定它的所有層面都能妥善調整，因為不同的環境可能會產生各種效能瓶頸。

 

 