---
title: 使用 Kerberos 進行相互驗證
description: 相互驗證是一種安全性功能，其中用戶端程式必須向服務證明其身分識別，且服務必須向用戶端證明其身分識別，才能透過用戶端/服務連線傳輸任何應用程式流量。
ms.assetid: 775dd350-5c70-4d97-aa2f-d21e9aecc778
ms.tgt_platform: multiple
keywords:
- Active Directory，使用雙向驗證
- Active Directory，使用，安全性，相互驗證
- 安全性廣告
- 安全性 AD，相互驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cf2e68c1983dde9221cc3fa89866b5358ee6eb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "106978574"
---
# <a name="mutual-authentication-using-kerberos"></a>使用 Kerberos 進行相互驗證

相互驗證是一種安全性功能，其中用戶端程式必須向服務證明其身分識別，且服務必須向用戶端證明其身分識別，才能透過用戶端/服務連線傳輸任何應用程式流量。

Active Directory Domain Services 和 Windows 提供服務主體名稱 (SPN) 的支援，這是 Kerberos 機制中的重要元件，可供用戶端用來驗證服務。 SPN 是唯一的名稱，用來識別服務的實例，並與服務實例執行所在的登入帳戶相關聯。 SPN 的元件可讓用戶端在沒有服務登入帳戶的情況下撰寫服務的 SPN。 這可讓用戶端要求服務驗證其帳戶，即使用戶端沒有帳戶名稱也一樣。

本節包含下列主題的總覽：

-   使用 Kerberos 進行相互驗證。
-   撰寫唯一的 SPN。
-   服務安裝程式如何在與服務實例相關聯的帳戶物件上註冊 Spn。
-   用戶端應用程式如何在 Active Directory Domain Services 中使用服務實例的服務連接點 (SCP) 物件，來取出用來撰寫服務 SPN 的資料。
-   用戶端應用程式如何搭配安全性支援提供者介面使用服務 SPN (SSPI) 來驗證服務。
-   Windows 通訊端用戶端/服務應用程式的程式碼範例，該應用程式會使用 SCP 和 SSPI 來執行相互驗證。
-   RPC 用戶端/服務的程式碼範例，此範例會使用 RPC 名稱服務和 RPC 驗證來執行相互驗證。
-   Windows 通訊端註冊和解析 (RnR) 服務如何使用 Spn 來執行相互驗證。

本節討論如何使用 Active Directory 網域服務進行相互驗證，特別是在相互驗證中，服務連接點和服務主體名稱的用途。 這並不是有關如何使用 SSPI 進行相互驗證或適用于 RPC 和 Windows 通訊端應用程式的驗證和安全性支援的完整討論。

如需詳細資訊，請參閱

-   [使用服務連接點發佈](publishing-with-service-connection-points.md)
-   [SSPI](/windows/desktop/SecAuthN/sspi)
-   [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
-   [RPC](/windows/desktop/Rpc/rpc-start-page)

 

 