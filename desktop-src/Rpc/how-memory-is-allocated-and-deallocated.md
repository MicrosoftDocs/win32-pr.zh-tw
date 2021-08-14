---
title: 記憶體的配置和解除配置
description: 根據預設，MIDL 編譯器產生的存根程式碼會呼叫使用者提供的函式，以配置和釋放記憶體。 這些稱為「midl \_ 使用者配置」和「midl 使用者可用」的函式 \_ \_ \_ 必須由開發人員提供，並連結到應用程式。
ms.assetid: 65af7a6d-4cfa-4175-9085-560d97cab41d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1e7b4a0fd9a765593fc6f44365e17bc45c10b1244c226abc09ff302e81ec107
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929515"
---
# <a name="how-memory-is-allocated-and-deallocated"></a>記憶體的配置和解除配置

根據預設，MIDL 編譯器產生的存根程式碼會呼叫使用者提供的函式，以配置和釋放記憶體。 這些稱為「 [**midl \_ 使用者 \_ 配置**](/windows/desktop/Midl/midl-user-allocate-1) 」和「 [**midl \_ 使用者 \_ 可用**](/windows/desktop/Midl/midl-user-free-1)」的函式必須由開發人員提供，並連結到應用程式。

所有應用程式都必須提供 [**midl \_ 使用者 \_ 配置**](/windows/desktop/Midl/midl-user-allocate-1) 和 [**midl \_ 使用者 \_ 免費**](/windows/desktop/Midl/midl-user-free-1)的實作為，即使這些函式的名稱可能不會明確出現在存根中也一樣。 唯一的例外狀況是當您在憑證相容性 (/osf) 模式中進行編譯時。 這些使用者提供的函式必須符合特定的定義函式原型，否則可以用任何方便或適用于應用程式的方式來執行。 或者，應用程式可以使用「RpcSs 記憶體管理」套件。 Microsoft RPC 執行時間程式庫提供這組函數。

下列各節描述 RPC 記憶體管理功能。

-   [**midl \_ 使用者 \_ 配置**](/windows/desktop/Midl/midl-user-allocate-1)
-   [**midl \_ 使用者 \_ 免費**](/windows/desktop/Midl/midl-user-free-1)
-   [RpcSs 記憶體管理套件](rpcss-memory-management-package.md)

 

 