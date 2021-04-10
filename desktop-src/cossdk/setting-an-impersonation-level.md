---
description: 當您為應用程式設定模擬層級時，您會決定應用程式在呼叫這些應用程式時，要授與其他應用程式使用其身分識別的許可權等級。
ms.assetid: 5b5b2c2d-dc3d-4edd-9e13-e6cb13022ceb
title: 設定模擬等級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1075ac3b10380892cdfdf770543a2dcbb32d56c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110897"
---
# <a name="setting-an-impersonation-level"></a>設定模擬等級

當您為應用程式設定模擬層級時，您會決定應用程式在呼叫這些應用程式時，要授與其他應用程式使用其身分識別的許可權等級。 您只能針對 COM + 伺服器應用程式進行這項作業：程式庫應用程式是在裝載進程的身分識別下執行，並使用其指定的模擬等級。 如需詳細資訊，請參閱模擬 [層級](/windows/desktop/com/impersonation-levels)。

**選取模擬等級**

1.  以滑鼠右鍵按一下您要設定模擬的 COM + 應用程式，然後按一下 [ **屬性**]。

2.  在 [應用程式屬性] 對話方塊中，按一下 [ **安全性** ] 索引標籤。

3.  在 [模擬 **等級** ] 方塊中，選取適當的層級。 層級如下所示，從授與的最小授權單位：

    -   **匿名**。 用戶端對伺服器而言是匿名。 伺服器可以模擬用戶端，但是模擬權杖 (本機認證) 不包含用戶端的任何相關資訊。
    -   **識別**。 伺服器可以取得用戶端的身分識別，並可模擬用戶端來進行 ACL 檢查。
    -   模擬。 伺服器可以模擬用戶端，並代表它執行動作 (但仍會有部份限制)。 伺服器可以存取與用戶端所在之同一部電腦上的資源。 如果伺服器與用戶端位於同一部電腦上，則可以做為用戶端來存取網路資源。 如果伺服器位於與用戶端不同的電腦上，則只能存取與伺服器位於同一部電腦上的資源。 這是 COM+ 伺服器應用程式的預設值。
    -   **委派**。 伺服器可以模擬用戶端，而不是在與用戶端相同的電腦上代表它。 在模擬期間，用戶端的認證 (具有本機的憑證，以及具有網路有效) 的憑證可傳遞至任意數目的電腦。

4.  按一下 [確定]  。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定 Role-Based 安全性](configuring-role-based-security.md)
</dt> <dt>

[設定軟體限制原則](configuring-the-software-restriction-policy.md)
</dt> <dt>

[啟用程式庫應用程式的驗證](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[設定伺服器應用程式的驗證層級](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 
