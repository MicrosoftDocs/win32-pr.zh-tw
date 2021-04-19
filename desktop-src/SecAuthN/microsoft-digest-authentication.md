---
description: 當伺服器收到來自用戶端的第一個挑戰回應時，Microsoft Digest 會執行初始驗證。
ms.assetid: c65bb134-d480-4a71-872c-30e2884237a6
title: Microsoft 摘要式驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 336d5eb9c2d114bae70c28d07ed9fef64f9d0514
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984641"
---
# <a name="microsoft-digest-authentication"></a>Microsoft 摘要式驗證

當伺服器收到來自用戶端的第一個挑戰回應時，Microsoft Digest 會執行初始驗證。 伺服器會驗證用戶端是否未經過驗證，然後藉由存取網域控制站的服務來執行初始驗證。 如需此程式的詳細說明，請參閱 [使用 Microsoft Digest 的初始驗證](initial-authentication-using-microsoft-digest.md)。

當初始驗證成功時，伺服器會收到摘要 [*工作階段金鑰*](../secgloss/s-gly.md)。 伺服器會快取此金鑰，並使用它來向用戶端驗證後續的資源要求。 這是本機驗證，也就是不需要存取網域控制站。 如需此程式的詳細說明，請參閱 [使用 Microsoft Digest 驗證後續要求](authenticating-subsequent-requests-using-microsoft-digest.md)。

使用 HTTP 時，不會在用戶端與伺服器之間維護連接。 為了減少網域控制站流量並改善效能，Microsoft Digest 會在驗證成功後快取所收到的資訊。 如需此程式的詳細資訊，請參閱 [維護連接之間的安全性內容](maintaining-the-security-context-between-connections.md)。

 

 
