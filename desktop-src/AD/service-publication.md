---
title: 服務發行
description: 服務會使用儲存在 Active Directory Domain Services 中的物件來通告本身。
ms.assetid: 69e9256f-40ee-4aed-8213-1bbda0e508af
ms.tgt_platform: multiple
keywords:
- 服務發行集廣告
- Active Directory，使用服務發行集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9437d9f4aa5184c53f2962d7b2640e933107501f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020826"
---
# <a name="service-publication"></a>服務發行

服務會使用儲存在 Active Directory Domain Services 中的物件來通告本身。 這就是所謂的 *服務發行*。 用戶端會查詢目錄以找出服務。 這稱為 *用戶端服務* 會合。 本節將討論用於服務發行的目錄物件類型，並說明如何將它們用於用戶端服務會合。

本節將討論下列主題：

-   [服務發行的總覽](about-service-publication.md)
-   [服務發行的安全性問題](security-issues-for-service-publication.md)
-   [連接點物件](connection-points.md)
-   [使用服務連接點發行 (Scp) ](publishing-with-service-connection-points.md)
-   [要在服務連接點中儲存的資訊](service-connection-point-properties.md)
-   [建立服務連接點的位置](where-to-create-a-service-connection-point.md)
-   [如何使用服務連接點發佈可複寫、主機式和資料庫服務](service-connection-points-for-replicated-host-based-and-database-services.md)
-   [建立和維護服務連接點](creating-and-maintaining-a-service-connection-point.md)
-   [用戶端如何查詢 SCP 並使用它來系結至服務實例](how-clients-find-and-use-a-service-connection-point.md)
-   [使用 RPC 名稱服務 (RpcNs) Api 來發佈 RPC 服務](publishing-with-the-rpc-name-service-rpcns.md)
-   [Windows 通訊端註冊和解析 (RnR) 發佈 Windows 通訊端服務](publishing-with-windows-sockets-registration-and-resolution.md)
-   [Com + 類別存放區中以 COM 為基礎的服務發行](publishing-com-services.md)

如需服務和用戶端彼此驗證方式的詳細資訊，請參閱 [使用 Kerberos 的相互驗證](mutual-authentication-using-kerberos.md)。 如需有關服務安全性內容和登入帳戶的詳細資訊，請參閱 [服務登入帳戶](service-logon-accounts.md)。

 

 




