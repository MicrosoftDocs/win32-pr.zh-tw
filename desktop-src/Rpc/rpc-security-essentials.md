---
title: RPC 安全性基本知識
description: 若要完成任何遠端程序呼叫，所有分散式應用程式都必須在用戶端與伺服器之間建立系結。
ms.assetid: 7b8adba2-19aa-4179-b6b3-ef27f4383bd4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56fdd64352df4bbefc1ec41960b78109b22510c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840651"
---
# <a name="rpc-security-essentials"></a>RPC 安全性基本知識

若要完成任何遠端程序呼叫，所有分散式應用程式都必須在用戶端與伺服器之間建立系結。 如需系結的詳細資訊，請參閱系結 [和控制碼](binding-and-handles.md)。 若要完成安全的遠端程序呼叫，需要額外的步驟。 首先，伺服器必須在 DCE 術語) 中選擇安全性提供者 (authentication 服務。 然後，它必須決定其驗證機制。 之後，用戶端會取得伺服器的系結，並從 RPC 執行時間要求安全的遠端程序呼叫，並指定各種安全性選項，例如安全性提供者、安全性 QOS 選項等等。

本節說明使用 RPC 函數為已驗證的分散式應用程式建立用戶端和伺服器時所需的基本概念和資訊。 它會組織成下列主題：

-   [主體名稱](principal-names.md)
-   [驗證層級](authentication-levels.md)
-   [驗證服務](authentication-services.md)
-   [用戶端驗證認證](client-authentication-credentials.md)
-   [授權服務](authorization-services.md)
-   [服務品質](quality-of-service.md)
-   [授權函數](authorization-functions.md)
-   [金鑰取得函式](key-acquisition-functions.md)
-   [用戶端模擬](client-impersonation.md)

 

 




