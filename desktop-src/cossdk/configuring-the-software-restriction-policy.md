---
description: 設定軟體限制原則
ms.assetid: 22c1897a-abb5-4ce9-9d09-21b6aed4f1d8
title: 設定軟體限制原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30aa7de81769288e5cdcee6a7612fa0439a0e9f41d8c384b0855b7bd7ae06d41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128950"
---
# <a name="configuring-the-software-restriction-policy"></a>設定軟體限制原則

當您明確設定 COM + 應用程式的軟體限制原則信任層級時，會覆寫預設的全系統設定。 這通常是 COM + 伺服器應用程式的必要項，因為所有伺服器應用程式都有相同的全系統信任層級設定， (因為它們都是在相同的檔案中執行，dllhost.exe) 。 但是，當您設定 COM + 程式庫應用程式的軟體限制原則信任層級時，會影響該應用程式的全系統設定。 如需如何在 COM + 中使用軟體限制原則的討論，請參閱 [在 COM + 中使用軟體限制原則](using-the-software-restriction-policy-in-com-.md)。

**設定軟體限制原則**

1.  在您要設定軟體限制原則的 COM + 應用程式 **上按一下滑鼠** 右鍵，然後按一下 [內容]。

2.  在 [應用程式屬性] 對話方塊中，按一下 [ **安全性** ] 索引標籤。

3.  在 [ **軟體限制原則**] 底下，選取 [套用 **軟體限制原則** ] 核取方塊。這可讓您設定信任層級。 清除此核取方塊會導致 COM + 針對應用程式使用軟體限制原則的全系統設定。 這個核取方塊會對應到 [**應用程式**](applications.md) 集合的 SRPEnabled 屬性。

4.  在 [ **限制等級** ] 方塊中，選取適當的層級。 這個下拉式清單方塊對應至 [**應用程式**](applications.md) 集合的 SRPTrustLevel 屬性。 層級如下所示，從最高到最受信任的順序：

    -   不 **允許**。 不允許應用程式使用使用者的完整許可權。 具有任何信任層級的元件可以載入到其中。
    -   不 **受限制**。 應用程式可不受限制地存取使用者的許可權。 只有具有不受限制之信任層級的元件可以載入到其中。

5.  按一下 [確定]。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定 Role-Based 安全性](configuring-role-based-security.md)
</dt> <dt>

[啟用程式庫應用程式的驗證](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[設定伺服器應用程式的驗證層級](setting-an-authentication-level-for-a-server-application.md)
</dt> <dt>

[設定模擬等級](setting-an-impersonation-level.md)
</dt> </dl>

 

 



