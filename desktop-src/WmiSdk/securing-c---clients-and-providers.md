---
description: C + + 提供者和用戶端應用程式都必須執行許多相同的作業來維護 WMI 安全性。
ms.assetid: 0199f469-2666-4794-b364-36c54aa360a8
ms.tgt_platform: multiple
title: 保護 c + + 用戶端和提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4151440f9e85f7cd9e6590842ffd3d103242410b38f52287dba83ba3bb3faec5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316157"
---
# <a name="securing-c-clients-and-providers"></a>保護 c + + 用戶端和提供者

C + + 提供者和用戶端應用程式都必須執行許多相同的作業來維護 WMI 安全性。

用戶端應用程式在連線至 WMI 時，必須正確 [設定 DCOM 模擬](setting-the-default-process-security-level-using-c-.md) 和 [驗證](setting-authentication-in-wmi.md) 層級。 [非同步呼叫](setting-security-on-an-asynchronous-call.md)的回呼有安全性風險，因此用戶端應用程式必須[執行存取檢查](performing-access-checks.md)，以確保回呼來自信任的來源。 用戶端需要保護 [暫時性和永久事件取用者](securing-wmi-events.md)。

提供者可能會 [執行存取檢查](performing-access-checks.md) ，以確保它所建立的資源只能由適當的用戶端存取。

提供者和用戶端也可以設定 [特定 proxy](setting-the-security-on-iwbemservices-and-other-proxies.md) 連接的安全性。 兩者也可以啟用 [許可權](executing-privileged-operations.md)。 事件提供者必須確保用戶端取用者有權 [接收要求的事件](providing-events-securely.md)。

用戶端或提供者可能需要建立需要不同驗證服務的遠端連線，例如 NTLM 而非 Kerberos。

 

 



