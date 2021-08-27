---
description: Kerberos 票證原則是在網域層級定義，並由網域的金鑰發佈中心 (KDC) 所執行。
ms.assetid: 4774218b-7cbd-4e8d-a064-44ebdc37e534
title: Kerberos 原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743d1dd394c42028c70f560fcb7f83b42bab506fbd222f877857be362a450041
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127308"
---
# <a name="kerberos-policy"></a>Kerberos 原則

Kerberos 票證原則是在網域層級定義，並由網域的 [*金鑰發佈中心*](../secgloss/k-gly.md) (KDC) 所執行。 Kerberos 原則會以網域安全性原則的屬性子集的形式儲存在 Active Directory 中。 根據預設，原則選項只能由 Domain Administrators 群組的成員設定。 網域原則包含下列選項：

-   支援遠期票證
-   僅支援限制委派 (Windows Server 2003) 
-   可以轉寄的支援票證
-   支援可再生票證
-   設定票證最長使用期限
-   設定最大續約期限
-   設定最大 proxy 票證存留期
-   當票證到期時強制登出使用者

使用 [*限制委派*](../secgloss/c-gly.md)時，可以將電腦設定為只允許將認證轉送到特定的服務清單。 這些服務必須位於與轉送認證的電腦相同的網域中。 在 *限制委派* 下，票證不再從用戶端傳送到伺服器。 伺服器電腦會根據所需的資訊，從用來驗證用戶端的資訊建立服務票證。

雖然網域的 Kerberos 原則可能會允許轉送票證來允許委派的驗證，但該原則的部分不需要套用至所有使用者或所有電腦。 您可以將個別使用者帳戶的屬性設定為停用任何伺服器轉送該使用者的 [*認證*](../secgloss/c-gly.md) 。 個別電腦帳戶的屬性可以設定為停用從任何使用者轉送認證。 在這兩種情況下，都可以藉由建立群組原則來停用委派，以套用至 Active Directory 組織單位中的所有使用者或所有電腦。

**Windows XP/2000：** 不支援限制委派。

 

 
