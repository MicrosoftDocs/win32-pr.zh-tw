---
title: IP 位址和電腦名稱稱
description: 假設指派給電腦的電腦名稱或 IP 位址 與單一使用者相關聯並不安全，因為多個使用者可以同時登入遠端桌面工作階段主機 (RD 工作階段主機) 伺服器。
ms.assetid: 17cfd14e-1fff-4154-89a6-8dbbf19a6cae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 574ab1ca0ae10996212fc555b22c2c21663c4b1e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316195"
---
# <a name="ip-addresses-and-computer-names"></a>IP 位址和電腦名稱稱

多個使用者可以同時登入遠端桌面工作階段主機 (RD 工作階段主機) server。 因此，假設指派給電腦的電腦名稱稱或 IP 位址與單一使用者相關聯，是不安全的。 這與單一使用者的 Windows 環境不同，因為一次只有一位使用者登入。

使用電腦名稱稱或 IP 位址進行授權或識別網路上應用程式反復專案的應用程式，在遠端桌面服務環境中將無法正常運作，因為伺服器的電腦名稱稱或 IP 位址可以與許多使用者建立關聯。

在遠端桌面服務環境中，每個用戶端終端機或終端機模擬器都有個別的 IP 位址和電腦名稱稱。 若要取得用戶端的 IP 位址和電腦名稱稱，請呼叫 [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) 函式。 其他抓取這些網路位址和電腦名稱稱的函式會取出 RD 工作階段主機伺服器的名稱和位址。 例如， [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) 函數會傳回伺服器的電腦名稱稱。

 

 