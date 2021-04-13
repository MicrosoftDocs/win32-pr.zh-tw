---
title: 伺服器如何準備連接
description: 當伺服器程式開始執行時，它必須先向 RPC 執行時間程式庫註冊它所包含的介面或介面。
ms.assetid: 3e78e095-f4a4-4ce7-b4a9-936a6c10316b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9787cc0f4a10da99f1401843450a6e00073e135b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301191"
---
# <a name="how-the-server-prepares-for-a-connection"></a>伺服器如何準備連接

當伺服器程式開始執行時，它必須先向 RPC 執行時間程式庫註冊它所包含的介面或介面。 然後，它會建立必要的系結資訊。 伺服器程式也必須註冊端點或接聽的端點。 然後，它就可以開始接聽用戶端呼叫。 下圖說明此程式。

![rpc 伺服器應用程式準備進行用戶端連接](images/srvrcon.png)

根據選擇的設計，伺服器應用程式可以選擇一組不同的步驟;先前的範例和圖例提供了一種方法。

本節提供伺服器進程為了準備連接所必須採取的步驟資訊。 討論區分為下列各節：

-   [註冊介面](registering-the-interface.md)
-   [讓伺服器可在網路上使用](making-the-server-available-on-the-network.md)
-   [註冊端點](registering-endpoints.md)
-   [接聽用戶端呼叫](listening-for-client-calls.md)

 

 




