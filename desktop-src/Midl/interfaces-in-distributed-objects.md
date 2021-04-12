---
title: 分散式物件中的介面
description: 在分散式運算中，介面是定義和遠端函式的集合，可讓兩個或多個程式在不同的內容之間交互操作。
ms.assetid: d7cd6bf3-58ec-426d-850a-9c5456ed816d
keywords:
- 在分散式物件中的 MIDL 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cbee13dcbab9ccaa6ef6ad3ad3880daa9b14ce
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314992"
---
# <a name="interfaces-in-distributed-objects"></a>分散式物件中的介面

在分散式運算中，介面是定義和遠端函式的集合，可讓兩個或多個程式在不同的內容之間交互操作。 在 RPC 應用程式中，介面會指定：

-   用戶端和伺服器應用程式如何彼此識別。
-   如何在用戶端與伺服器之間傳輸資料。
-   用戶端應用程式可以呼叫的遠端程式。
-   遠端程式的參數和傳回值的資料類型。

Microsoft 介面定義語言 (MIDL) 適用于執行分散式應用程式中所使用的介面。 使用 MIDL 時，應用程式可以有一個或多個介面。 每個介面會指定用戶端與伺服器程式之間的唯一分散式合約。 以遠端程序呼叫為基礎的應用程式會 (RPC) 、元件物件模型 (COM) 和分散式元件物件模型 (DCOM) 使用 MIDL 來指定其介面。

MIDL 在許多方面類似 C 和 c + +。 如需撰寫 MIDL 介面的總覽，請參閱 [開發介面](/windows/desktop/Rpc/developing-the-interface)。

 

 