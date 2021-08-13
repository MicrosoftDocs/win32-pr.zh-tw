---
title: 使用 LDAP 提供者來設定和變更使用者密碼
description: 若要設定使用者密碼，請使用 IADsUser. SetPassword 方法。
ms.assetid: da3d9861-dd04-406c-9356-db1e4ff0eebc
ms.tgt_platform: multiple
keywords:
- LDAP 提供者 ADSI、使用者物件、設定密碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbbd0439a011575fbc9278dbe506d46db2210ce03d807ea74097499cb764b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690523"
---
# <a name="setting-and-changing-user-passwords-with-the-ldap-provider"></a>使用 LDAP 提供者來設定和變更使用者密碼

若要設定使用者密碼，請使用 [**IADsUser. SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) 方法。

Active Directory 的 LDAP 提供者會使用三個處理常式的其中一個來設定密碼 (協力廠商 LDAP 目錄，例如 iPlanet 不使用此密碼驗證程式) 。 此方法可能會根據網路設定而有所不同。 設定密碼方法會依下列順序發生：

-   首先，LDAP 提供者會嘗試在128位 SSL 連線上使用 LDAP。 Ldap 伺服器必須已安裝適當的伺服器驗證憑證，而且執行 ADSI 程式碼的用戶端必須信任發行這些憑證的授權單位，ldap SSL 才能順利運作。 伺服器和用戶端都必須支援128位加密。
-   其次，如果 SSL 連線失敗，LDAP 提供者會嘗試使用 Kerberos。 在 Windows 2000 上，Kerberos 可能不支援跨樹系驗證。 Kerberos 的後續增強功能支援跨樹系驗證。
-   第三，如果 Kerberos 失敗，LDAP 提供者會嘗試 [**NetUserSetInfo**](/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo) API 呼叫。 在舊版中，ADSI 會在執行執行緒的安全性內容中呼叫 **NetUserSetInfo** ，而不是在 [**IADsOpenDSObject. objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) 或 [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)的呼叫中指定的安全性內容。 在之後的版本中，這已變更，讓 ADSI LDAP 提供者在呼叫 **NetUserSetInfo** 時模擬 **objdso.opendsobject** 呼叫中指定的使用者。

若要變更使用者密碼，請使用 [**IADsUser**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) 方法。 如同 [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword)，此方法可以使用多個進程來變更密碼。 變更密碼方法會以下列順序發生：

-   首先，LDAP 提供者會嘗試在128位 SSL 連線上使用 LDAP。
-   其次，如果 128-SSL 連線失敗，LDAP 提供者會嘗試 [**NetUserChangePassword**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserchangepassword) API 呼叫。 如同 [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword)，在舊版中，ADSI LDAP 提供者會模擬使用 [**IADsOpenDSObject. Objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) 方法或 [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) 函數傳遞的使用者認證。

 

 