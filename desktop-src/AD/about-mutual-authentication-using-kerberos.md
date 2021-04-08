---
title: 關於使用 Kerberos 進行相互驗證
description: 在相互驗證中，用戶端和服務必須先驗證各自的身分識別，再執行應用程式功能。
ms.assetid: 5ce923d6-bede-4acb-b297-e93f2f506ea9
ms.tgt_platform: multiple
keywords:
- 關於使用 Kerberos AD 的相互驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9685dad0bd20f233b8dcb0ecf12af338f318646f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020753"
---
# <a name="about-mutual-authentication-using-kerberos"></a>關於使用 Kerberos 進行相互驗證

在相互驗證中，用戶端和服務必須先驗證各自的身分識別，再執行應用程式功能。 這兩個合作物件都不能執行其他作業，除非已驗證身分識別;也就是說，服務必須能夠驗證用戶端，而不需要查詢用戶端，而且用戶端必須能夠在不查詢服務的情況下驗證服務。

可以驗證用戶端的服務值是知名的。 例如，檔案服務會模擬用戶端，以判斷用戶端可以存取的檔案。

可以驗證服務的用戶端值比較不容易理解。 驗證服務可讓用戶端信任從服務取得的資料，並且在將機密資料傳送至服務時安全。 在支援用戶端安全性內容委派的用戶端/服務應用程式中，用戶端驗證服務的能力特別重要;也就是，用戶端會授權服務在存取其他服務或網路資源時作為其委派。

服務會驗證用戶端，如下所示：用戶端會在先前建立的內容中執行（例如，在已登入使用者的會話中執行），或明確向基礎安全性提供者出示認證，藉以建立本機安全性內容。 服務無法接受來自任何未經驗證之用戶端的連接。

用戶端用來驗證服務的 Kerberos 機制如下所示：當安裝服務時，以系統管理員許可權執行的服務安裝程式會為每個服務實例註冊一或多個唯一的 Spn。 這些名稱會在服務實例將用來登入之使用者或電腦帳戶物件的 Active Directory 網網域控制站 (DC) 中註冊。 當用戶端要求服務的連接時，它會使用已知的資料或使用者提供的資料來撰寫服務實例的 SPN。 接著，用戶端會使用 SSPI negotiate 套件，將 SPN 呈現給用戶端網域帳戶的金鑰發佈中心 (KDC) 。 KDC 會在樹系中搜尋已註冊 SPN 的使用者或電腦帳戶。 如果 SPN 註冊在一個以上的帳戶上，驗證就會失敗。 否則，KDC 會使用註冊 SPN 之帳戶的密碼來加密訊息。 KDC 會將這個加密的訊息傳遞給用戶端，然後再將它傳遞給服務實例。 服務會使用 SSPI 協商套件來解密訊息，然後將訊息傳回用戶端，並傳送給用戶端的 KDC。 KDC 會在解密的訊息符合其原始訊息時驗證服務。

-   如需撰寫和註冊 Spn 的詳細資訊，請參閱。[服務主體名稱](service-principal-names.md)
-   如需撰寫 Windows 通訊端服務之 SPN 的詳細資訊和程式碼範例，以服務連接點發佈本身，請參閱 [使用 SCP 撰寫服務的 spn](composing-the-spns-for-a-service-with-an-scp.md)。
-   如需撰寫 RPC 服務之 SPN 的詳細資訊和程式碼範例，請參閱 [撰寫 RpcNs 服務的 spn](composing-spns-for-an-rpcns-service.md)。

 

 




