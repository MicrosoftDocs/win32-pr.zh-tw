---
title: Kerberos v5 通訊協定
description: Kerberos v5 通訊協定
ms.assetid: a53a1edf-f374-4cbf-8050-7cde45284157
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68d78c4bdc457007c04ad66163e2ebfd7f5397f9
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "106966844"
---
# <a name="kerberos-v5-protocol"></a>Kerberos v5 通訊協定

Kerberos v5 驗證通訊協定具有 RPC \_ C \_ 驗證 \_ GSS Kerberos 的驗證服務識別碼 \_ 。 Kerberos 通訊協定會定義用戶端與網路驗證服務的互動方式，並且是由網際網路工程任務推動小組在1993年9月的檔 [RFC 1510](https://www.ietf.org/rfc/rfc1510.txt)中 (IETF) 。 用戶端從 Kerberos 金鑰發佈中心 (KDC) 取得票證，並在建立連線時將這些票證呈交給伺服器。 Kerberos 票證代表用戶端的網路認證。

Kerberos 通訊協定與 NTLM 一樣，會使用功能變數名稱、使用者名稱和密碼來代表用戶端的身分識別。 當使用者登入時，從 KDC 取得的初始 Kerberos 票證是以使用者密碼的加密雜湊為基礎。 快取此初始票證。 當使用者嘗試連接到伺服器時，Kerberos 通訊協定會檢查票證快取是否有該伺服器的有效票證。 如果無法使用，則會將使用者的初始票證連同指定之伺服器的票證要求傳送給 KDC。 該會話票證會新增至快取，而且可以用來連接到相同的伺服器，直到票證到期為止。

當伺服器使用 Kerberos 通訊協定呼叫 [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket) 時，會傳回用戶端的功能變數名稱和使用者名稱。 當伺服器呼叫 [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)時，會傳回用戶端的權杖。 這些行為與使用 NTLM 時相同。

Kerberos 通訊協定可以跨電腦界限運作。 用戶端和伺服器電腦都必須位於網域中，而且這些網域必須具有信任關係。

Kerberos 通訊協定需要相互驗證並從遠端支援。 用戶端必須指定伺服器的主體名稱，且伺服器的身分識別必須完全符合該主體名稱。 如果用戶端為伺服器的主體名稱指定 **Null** ，或主體名稱與伺服器不符，則呼叫會失敗。

使用 Kerberos 通訊協定時，可使用模擬層級識別、模擬和委派。 當伺服器呼叫 [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)時，傳回的權杖會在5分鐘到8小時之間的一段時間內有效。 在這段時間之後，只能在伺服器電腦上使用。 如果伺服器是 "run as activator"，且啟用是使用 Kerberos 通訊協定完成，伺服器的權杖將會在啟用後的5分鐘到8小時之間到期。

Windows 所執行的 Kerberos v5 驗證通訊協定支援 [掩蓋](cloaking.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 和安全性封裝](com-and-security-packages.md)
</dt> </dl>

 

 




