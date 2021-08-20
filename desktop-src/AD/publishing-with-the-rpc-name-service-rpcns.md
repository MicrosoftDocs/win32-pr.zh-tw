---
title: 使用 RPC 名稱服務發行
description: RPC 服務可以使用 RPC 名稱服務在命名空間中發佈其識別碼， (RpcNs) Api。
ms.assetid: 0c8e1207-daeb-4dc8-b83a-a54cd59a46a7
ms.tgt_platform: multiple
keywords:
- 使用 RPC 名稱服務 AD 進行發佈
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd53922bd4ce952c18c58d1b71cb485887bdc0fd020f4113679eb114b32b6f3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025366"
---
# <a name="publishing-with-the-rpc-name-service"></a>使用 RPC 名稱服務發行

RPC 服務可以使用 RPC 名稱服務在命名空間中發佈其識別碼， (RpcNs) Api。 Windows 2000 中的 RpcNs api 會將 RPC 專案發佈 Active Directory Domain Services。 服務會建立 RPC 系結，並在命名空間中將它們發佈為具有屬性的命名空間，其中包含唯一的介面識別碼，也就是用戶端所能辨識的 GUID。 接著，用戶端可以搜尋提供所需介面的 RPC 伺服器、匯入系結，然後連接到伺服器。

如需發行 RPC 服務的詳細資訊，請參閱 [伺服器端](/windows/desktop/Rpc/server-side-binding)系結。

 

 