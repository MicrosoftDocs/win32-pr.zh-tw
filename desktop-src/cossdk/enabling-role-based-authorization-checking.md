---
description: 若要在您的 COM + 應用程式中使用以角色為基礎的安全性，您必須先為應用程式啟用以角色為基礎的授權檢查。
ms.assetid: d391a0d4-fe5d-4587-b0b1-b3aa294b7ad7
title: 啟用 Role-Based 授權檢查
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c4268c35812af04ed8a0056900e821029274756
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025958"
---
# <a name="enabling-role-based-authorization-checking"></a>啟用 Role-Based 授權檢查

若要在您的 COM + 應用程式中使用以角色為基礎的安全性，您必須先為應用程式啟用以角色為基礎的授權檢查。 這可確保在授權使用者存取應用程式之前，會先檢查正在存取應用程式的使用者是否擁有所屬角色。 如果未啟用以角色為基礎的授權檢查，則不會使用應用程式的角色型安全性。

**啟用以角色為基礎的授權檢查**

1.  以滑鼠右鍵按一下您要啟用以角色為基礎之授權檢查的 COM + 應用程式，然後按一下 [ **屬性**]。

2.  在 [應用程式屬性] 對話方塊中，按一下 [ **安全性** ] 索引標籤。

3.  在 [ **授權**] 底下，選取 [ **強制執行此應用程式的存取檢查** ] 核取方塊。清除此核取方塊表示應用程式不會使用以角色為基礎的安全性。

4.  按一下 [確定]  。

選取的授權設定會在應用程式下次啟動時生效。

 

 



