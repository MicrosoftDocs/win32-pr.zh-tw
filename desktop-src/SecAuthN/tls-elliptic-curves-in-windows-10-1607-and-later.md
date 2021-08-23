---
description: 在 Windows 10 1607 版和更新版本中啟用的橢圓曲線。
title: Windows 10 1607 版和更新版本中的 TLS 橢圓曲線
ms.topic: article
ms.keywords: ecc curves, elliptic curves, tls elliptic curves, ECC curves, schannel, ECC, EC, Elliptic Curve Cryptography
ms.date: 06/10/2020
ms.openlocfilehash: 237d0f7a7b4b2a7fecb99a91f21c55349e7d435b221e1b3297afd1ba614cc92c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915843"
---
# <a name="tls-elliptic-curves-in-windows-10-version-1607-and-later"></a>Windows 10 1607 版和更新版本中的 TLS 橢圓曲線

針對 Windows 10 （1607和更新版本），下列的橢圓曲線預設會啟用，並依預設使用 Microsoft Schannel 提供者：

| 橢圓曲線字串 | 可在 FIPS 模式中使用 |
|-------------|--------------|
| curve25519 | No |
| NistP256 | Yes |
| NistP384 | Yes |


Microsoft Schannel 提供者支援下列橢圓曲線，但預設不會啟用：

| 橢圓曲線字串 | 可在 FIPS 模式中使用 |
|-------------|--------------|
| brainpoolP256r1 | No |
| brainpoolP384r1 | No |
| brainpoolP512r1 | No |
| nistP192 | No |
| nistP224 | No |
| nistP521 | Yes |
| secP160k1 | No |
| secP160r1 | No |
| secP160r2 | No |
| secP192k1 | No |
| secP192r1 | No |
| secP224k1 | No |
| secP224r1 | No |
| secP256k1 | No |
| secP256r1 | No |
| secP384r1 | No |
| secP521r1 | No |



## <a name="enabling-elliptic-curves"></a>啟用橢圓曲線

若要新增橢圓曲線，可以部署群組原則或使用 TLS Cmdlet：
- 若要使用群組原則，請在 [電腦設定] 下[設定 ECC 曲線順序](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order)> 系統管理範本 > 網路 > SSL 設定] 設定，以及您想要啟用之所有橢圓曲線的優先順序清單。

- 若要使用 PowerShell，請參閱 [tls](/powershell/module/tls) Cmdlet 以取得 tls Cmdlet 語法和描述的完整清單。


> [!NOTE]
> 在 Windows 10 之前，會使用橢圓曲線附加加密套件字串來決定曲線的優先順序。 Windows 10 支援橢圓曲線優先順序設定，因此不需要橢圓曲線尾碼，而是在提供時由新的橢圓曲線優先順序順序覆寫，以便讓組織使用群組原則，以相同的加密套件來設定不同版本的 Windows。


## <a name="see-also"></a>另請參閱

[設定 TLS ECC 曲線順序](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order)

[管理 TLS ECC 順序](/windows-server/security/tls/manage-tls#managing-tls-ecc-order)

[使用群組原則管理 Windows ECC 曲線](/windows-server/security/tls/manage-tls#managing-windows-ecc-curves-using-group-policy)

[TLS Cmdlet](/powershell/module/tls)
