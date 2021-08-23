---
description: 認證管理員類似于網路提供者，因為它提供多個提供者路由器呼叫的進入點， (MPR) 。 事實上，有些網路提供者也是認證管理員。
ms.assetid: a1105754-a57f-4a0d-9797-bec22b99900c
title: 認證管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57a33b1a47ff17123a1974823d7fee1421df7755850d46d2992fec51f62f5fac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008826"
---
# <a name="credential-manager"></a>認證管理員

認證管理員類似于網路提供者，因為它提供 [*多個提供者路由器*](/windows/desktop/SecGloss/m-gly) 呼叫的進入點， (MPR) 。 事實上，有些網路提供者也是認證管理員。

您是否在與網路提供者函式相同的 DLL 中執行認證管理功能，取決於您的應用程式需求。 當驗證資訊變更時，認證管理員會收到通知。 例如，當使用者登入或帳戶密碼變更時，認證管理員會收到通知。 當登入處理常式（例如 [*Winlogon*](/windows/desktop/SecGloss/w-gly)）正在登入或變更帳戶的密碼時，它會呼叫適當的 MPR Windows 網路 (WNet) 功能。 然後，MPR 會為每個認證管理員呼叫適當的進入點。 這些認證管理函式一律會在系統內容 LocalSystem 中呼叫，而不是在使用者內容中呼叫。 如需 WNet 函式的詳細資訊，請參閱[Windows 網路](/windows/desktop/WNet/windows-networking-wnet-)功能。 如需認證管理員必須執行之介面的詳細資訊，請參閱 [**認證管理 API**](credential-management-api.md)。

 

 
