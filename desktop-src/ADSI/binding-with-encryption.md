---
title: 使用加密的系結
description: 透過網路交換的機密資料應該加密。
ms.assetid: 51fe2131-5f7d-41b1-ad88-d965cbb4d630
ms.tgt_platform: multiple
keywords:
- ADSI ADSI、using、encryption 和 encryption
- 使用加密的系結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cf19747a8356459f4ab50c0aa409f69b58eb224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931854"
---
# <a name="binding-with-encryption"></a>使用加密的系結

透過網路交換的機密資料應該加密。 為了允許這種情況，ADSI 支援兩種類型的加密、Kerberos 和安全通訊端層 (SSL) 。 這兩種加密類型都需要使用 [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) 或 [**IADsOpenDSObject：： objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) 進行系結。

在此情況下，無法使用 **GetObject** 和 [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject)進行系結，因為這些函式會導致 ADSI 所使用的 LDAP 要求和目錄伺服器所傳回的資料，以純文字格式在網路上傳輸。 基於偵錯工具的目的，關閉加密很有説明，網路監視器可以用來在用戶端與目錄伺服器之間查看 LDAP 要求和資料。

## <a name="kerberos-based-encryption"></a>以 Kerberos 為基礎的加密

若要使用以 Kerberos 為基礎的加密，請在呼叫 [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)或 [**IADsOpenDSObject：： objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)時，指定 **ADS \_ 使用 \_ 密封** 旗標。 ADS 也可以 **\_ 使用 \_ 密封** 旗標來確認資料完整性，也就是確保收到的資料與傳送的資料相同。 如果指定 **ads \_ 使用 \_ 密封** 旗標，則也會自動指定 **ads \_ 使用 \_ 簽署** 旗標。 這兩個旗標都需要 Kerberos 驗證，這只適用于下列條件：

-   用戶端電腦必須登入 Windows 網域或 Windows 網域所信任的網域。
-   必須以 null 認證呼叫 [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)或 [**IADsOpenDSObject：： objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) ;也就是說，無法指定替代認證。

## <a name="ssl-based-encryption"></a>以 SSL 為基礎的加密

若要使用以 SSL 為基礎的加密，請在呼叫 [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)或 [**IADsOpenDSObject：： objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)時，指定 **ADS \_ 使用 \_ ssl** 旗標。 如果只指定 **ADS \_ 使用 \_ ssl** 旗標，ADSI 會開啟 ssl 埠636，然後透過該 ssl 通道執行簡單的系結。 如果同時指定 **ads \_ 安全 \_ 驗證** 和 **ads \_ 使用 \_ SSL** 旗標，系結行為將取決於發出呼叫的用戶端。 在不支援的 Windows 版本上，ADSI 先開啟 SSL 通道，並使用指定的使用者名稱和密碼來執行簡單的系結，如果使用者名稱和密碼都是 null，則會使用目前的使用者內容來執行簡單的系結。 在支援的 Windows 版本上，ADSI 會執行安全驗證，而不是簡單的系結。

若要使用以 SSL 為基礎的加密來與 Active Directory 通訊，Active Directory 必須啟用公開金鑰基礎結構 (PKI) 。 您可以在 Active Directory 的其中一部伺服器上設定企業憑證授權單位單位來啟用 PKI，包括其中一部 Active Directory 伺服器本身。 設定企業憑證授權單位單位，會使 Active Directory 的伺服器取得伺服器憑證，然後用來進行以 SSL 為基礎的加密。

 

 




