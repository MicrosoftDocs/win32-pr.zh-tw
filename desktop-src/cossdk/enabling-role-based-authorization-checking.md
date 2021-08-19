---
description: 若要在您的 COM + 應用程式中使用以角色為基礎的安全性，您必須先為應用程式啟用以角色為基礎的授權檢查。
ms.assetid: d391a0d4-fe5d-4587-b0b1-b3aa294b7ad7
title: 啟用 Role-Based 授權檢查
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd46a0b09b981a3dd7731f5839458550379dad5619f22d1caaaddb24e87deaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118813856"
---
# <a name="enabling-role-based-authorization-checking"></a>啟用 Role-Based 授權檢查

若要在您的 COM + 應用程式中使用以角色為基礎的安全性，您必須先為應用程式啟用以角色為基礎的授權檢查。 這可確保在授權使用者存取應用程式之前，會先檢查正在存取應用程式的使用者是否擁有所屬角色。 如果未啟用以角色為基礎的授權檢查，則不會使用應用程式的角色型安全性。

**啟用以角色為基礎的授權檢查**

1.  以滑鼠右鍵按一下您要啟用以角色為基礎之授權檢查的 COM + 應用程式，然後按一下 [ **屬性**]。

2.  在 [應用程式屬性] 對話方塊中，按一下 [ **安全性** ] 索引標籤。

3.  在 [ **授權**] 底下，選取 [ **強制執行此應用程式的存取檢查** ] 核取方塊。清除此核取方塊表示應用程式不會使用以角色為基礎的安全性。

4.  按一下 [確定]。

選取的授權設定會在應用程式下次啟動時生效。

 

 



