---
title: 授權服務
description: 授權服務是 SSP 用來授權遠端程式存取權的方法。 Ssp 可以提供一個以上的授權服務。 不過，它們通常會選取一個做為預設值。
ms.assetid: 5ea3cde9-96e9-4208-bb61-d0f98f23b90c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 548f834c69726425a52a033e0dbb08bf6f1f3a38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021758"
---
# <a name="authorization-services"></a>授權服務

授權服務是 SSP 用來授權遠端程式存取權的方法。 Ssp 可以提供一個以上的授權服務。 不過，它們通常會選取一個做為預設值。

您的應用程式可以使用目前 SSP 的預設授權方法，也可以指定一個。 目前，Microsoft RPC 支援兩種授權方法。 其中一個是讓伺服器根據用戶端程式的名稱提供授權。 另一種是讓伺服器將用戶端的驗證認證與伺服器的存取控制清單進行比較 (ACL) 。

如需授權服務的清單，請參閱授權服務的 [常數](authorization-service-constants.md)。

> [!Note]  
> 建議開發人員使用 RPC \_ C \_ 授權 \_ 無。

 

 

 




