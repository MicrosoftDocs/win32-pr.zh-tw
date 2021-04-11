---
description: 登入網路時，會使用 Kerberos 驗證套件;本機登入是由 MSV1 \_ 0 處理。
ms.assetid: 43970c99-53f1-43c1-9d9f-65573572f731
title: Kerberos SSP/AP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d14565c8c6526d9cab34d7b9ddec9a0a04ff8de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026871"
---
# <a name="kerberos-sspap"></a>Kerberos SSP/AP

登入網路時，會使用 [*Kerberos*](../secgloss/k-gly.md) 驗證套件;本機登入是由 MSV1 \_ 0 處理。

當使用者使用網路帳戶登入時，Kerberos 預設會嘗試連線到網域控制站上的 Kerberos [*金鑰發佈中心*](../secgloss/k-gly.md) (KDC) ，並使用使用者提供的登入資料， (TGT) 取得票證授權票證。

如果無法使用 Kerberos KDC，Windows 會使用 MSV1 \_ 0 和傳遞驗證，如 [MSV1 \_ 0 authentication 套件](msv1-0-authentication-package.md)中所述。

Kerberos 驗證套件支援 Kerberos 通訊協定的第5版（修訂版6）。 此通訊協定是以網際網路 [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt)為基礎。 如需詳細資訊，請參閱 IETF 網站：

[https://www.ietf.org](https://www.ietf.org/)

如需有關 Kerberos 的詳細資訊，請參閱 [Microsoft kerberos](microsoft-kerberos.md)。

## <a name="kerberos-credential-formats"></a>Kerberos 認證格式

Kerberos 驗證套件在成功登入之後所指派的使用者 [*認證*](../secgloss/c-gly.md) 是票證和暫時加密金鑰，通常稱為 [*工作階段金鑰*](../secgloss/s-gly.md)。 票證包含用戶端認證和工作階段金鑰的加密複本。

 

 
