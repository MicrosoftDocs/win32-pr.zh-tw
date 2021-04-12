---
title: 連接用戶端和伺服器
description: 若要進行通訊，用戶端和伺服器程式必須在連線的網路或網路之間建立通訊會話。
ms.assetid: 1164252a-7615-4958-9d2f-cf35c0db513a
keywords:
- 遠端程序呼叫 RPC、工作、連接用戶端和伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98a22ea7a9a6dd30f2b9495b6d2ee868aac217f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462281"
---
# <a name="connecting-the-client-and-the-server"></a>連接用戶端和伺服器

若要進行通訊，用戶端和伺服器程式必須在連線的網路或網路之間建立通訊會話。 一旦建立連線之後，用戶端就可以呼叫伺服器程式中的遠端程式，就好像它們是用戶端程式的本機程式一樣。

本節提供有關如何在用戶端與伺服器之間建立遠端程序呼叫之連接的概念。 它不會提供本主題的深入討論。 本章節中的所有概念將在稍後的章節和 RPC 函數參考一節中詳細說明。

本節中的討論區分為下列主題：

-   [基本 RPC 系結術語](essential-rpc-binding-terminology.md)
-   [伺服器如何準備連接](how-the-server-prepares-for-a-connection.md)
-   [用戶端建立連接的方式](how-the-client-establishes-a-connection.md)

請注意，討論會假設明確的系結控制碼。 但是，如果您的應用程式使用其他類型的系結控制碼，您可能必須修改本節所述的步驟。 如需詳細資訊，請參閱系結 [和控制碼](binding-and-handles.md)。

 

 




