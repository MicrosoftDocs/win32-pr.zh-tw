---
title: 服務主要名稱
description: 服務主體名稱 (SPN) 是服務實例的唯一識別碼。
ms.assetid: 54b02853-4097-4e37-b7a2-6b5cfd168ece
ms.tgt_platform: multiple
keywords:
- 服務主要名稱
- SPN 請參閱服務主體名稱
- 服務主體名稱 AD
- 服務主體名稱 AD、關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6639ade82f029a89cb378de20bb279348962c4a991899f95e7f1b06157cd7ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024816"
---
# <a name="service-principal-names"></a>服務主要名稱

服務主體名稱 (SPN) 是服務實例的唯一識別碼。 [Kerberos 驗證](mutual-authentication-using-kerberos.md)會使用 spn，將服務實例與服務登入帳戶建立關聯。 這可讓用戶端應用程式要求服務驗證帳戶，即使用戶端沒有帳戶名稱也一樣。

若您透過樹系在電腦上安裝多個服務執行個體，則每個執行個體都須有自己的 SPN。 若用戶端需使用多個名稱進行驗證，則指定的服務執行個體可擁有多個 SPN。 例如，SPN 一律會包含執行服務實例之主機電腦的名稱，因此服務實例可能會為其主機的每個名稱或別名註冊 SPN。 如需 SPN 格式和撰寫唯一 SPN 的詳細資訊，請參閱 [唯一 spn 的名稱格式](name-formats-for-unique-spns.md)。

在 Kerberos 驗證服務可以使用 SPN 來驗證服務之前，必須先在服務實例用來登入的帳戶物件上註冊 SPN。 指定的 SPN 只能在一個帳戶上註冊。 針對 Win32 服務，服務安裝程式會在安裝服務的實例時，指定登入帳戶。 然後，安裝程式會撰寫 Spn，並在 Active Directory Domain Services 中將其寫入為 account 物件的屬性。 如果服務實例的登入帳戶變更，必須在新帳戶下重新註冊 Spn。 如需詳細資訊，請參閱 [服務如何註冊其 spn](how-a-service-registers-its-spns.md)。

當用戶端想要連接到服務時，它會尋找服務的執行個體、撰寫該執行個體的 SPN、連接到服務，然後呈現服務的 SPN 以進行驗證。 如需詳細資訊，請參閱 [用戶端如何撰寫服務的 SPN](how-clients-compose-a-serviceampaposs-spn.md)。

## <a name="in-this-section"></a>本章節內容

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[唯一 Spn 的名稱格式](name-formats-for-unique-spns.md)
</dt> <dt>

[服務如何撰寫其 Spn](how-a-service-composes-its-spns.md)
</dt> <dt>

[服務如何註冊其 Spn](how-a-service-registers-its-spns.md)
</dt> <dt>

[用戶端如何撰寫服務的 SPN](how-clients-compose-a-serviceampaposs-spn.md)
</dt> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[什麼是 SPN，為什麼您應該在意？](/archive/blogs/autz_auth_stuff/what-is-a-spn-and-why-should-you-care)
</dt> <dt>

[使用 Kerberos 進行相互驗證](mutual-authentication-using-kerberos.md)
</dt> </dl>

 

 