---
description: 使用者可以輸入登入名稱和密碼來開始登入網路。 使用者工作站上的 Kerberos 用戶端會將密碼轉換為加密金鑰，並將結果儲存在程式變數中。
ms.assetid: fcb3b601-9953-474c-9a08-1fa25706f3d7
title: 驗證服務交換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8480370dd9fe5d7c5fc10e7979de9d4e7f67f99db3e517e1ec6520a3274ef23c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073288"
---
# <a name="authentication-service-exchange"></a>驗證服務交換

使用者可以輸入登入名稱和密碼來開始登入網路。 使用者工作站上的 [*Kerberos*](/windows/desktop/SecGloss/k-gly) 用戶端會將密碼轉換為加密金鑰，並將結果儲存在程式變數中。

接著，用戶端[](/windows/desktop/SecGloss/c-gly)會透過將 KRB 型別為「 [](/windows/desktop/SecGloss/k-gly) \_ \_ 要求) Kerberos 驗證服務要求 (」的訊息傳送給 kdc 的驗證服務，以要求金鑰發佈中心 (KDC) 的 (TGS) 的票證授與服務的認證。 此訊息的第一個部分會識別所要求的使用者和 TGS 服務。 此訊息的第二個部分包含預先驗證的資料，目的在於證明使用者知道密碼。 這只是使用衍生自使用者登入密碼的 [*主要金鑰*](/windows/desktop/SecGloss/m-gly) 加密的驗證器訊息。

當 KDC 以要求的形式接收 KRB 時， \_ \_ 它會在其資料庫中尋找使用者、取得相關聯使用者的主要金鑰、解密預先驗證資料，並評估內的時間戳記。 如果時間戳記有效，KDC 可以確保預先驗證資料是以使用者的主要金鑰加密，因此用戶端為正版。

在 KDC 驗證使用者的身分識別之後，它會建立用戶端可以出示給 TGS 的認證，如下所示：

1.  KDC 會 invents 登入 [*工作階段金鑰*](/windows/desktop/SecGloss/s-gly) ，並使用使用者的主要金鑰來加密複本。
2.  KDC 會將登入工作階段金鑰的另一份複本和使用者的授權資料內嵌在票證授與票證 (TGT) ，並使用 KDC 本身的主要金鑰來加密 TGT。
3.  KDC 會以 KRB 類型的訊息來回複，將這些認證傳送回用戶端 \_ ， \_ (Kerberos 驗證服務回復) 。
4.  當用戶端收到回復時，會使用從使用者的密碼衍生的金鑰來解密新的登入工作階段金鑰。
5.  用戶端會將新的金鑰儲存在其票證快取中。
6.  用戶端也會從訊息中解壓縮 TGT，並將其儲存在其票證快取中。

 

 
