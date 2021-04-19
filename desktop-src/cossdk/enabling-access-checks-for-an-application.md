---
description: 執行此步驟會根據您選取的安全性層級以及是否啟用個別元件的存取檢查，來啟用程式存取檢查或完整的角色型安全性。
ms.assetid: 266bdac1-41be-45a5-a8c7-f9c6fe08445c
title: 啟用應用程式的存取檢查
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3d64a32b23467f85c368e088a870ebe5e4d683e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972333"
---
# <a name="enabling-access-checks-for-an-application"></a>啟用應用程式的存取檢查

執行此步驟會根據您選取的安全性層級以及是否啟用個別元件的存取檢查，來啟用程式存取檢查或完整的角色型安全性。

**若要啟用應用程式的存取檢查**

1.  在 [元件服務] 系統管理工具的主控台樹中，以滑鼠 **按右鍵您** 要啟用存取檢查的 com + 應用程式，然後按一下 [內容]。

2.  在 [應用程式屬性] 對話方塊中，按一下 [ **安全性** ] 索引標籤。

3.  選取 [ **強制執行此應用程式的存取檢查** ] 核取方塊。

4.  按一下 [確定]  。

> [!Note]  
> 從 Windows Server 2003，建立 COM + 應用程式時，預設會啟用存取檢查。 預設會在應用層級啟用存取檢查，並且在元件層級預設為停用。 先前，在應用層級依預設會停用存取檢查，而且在元件層級預設為啟用。

 

啟用存取檢查之後，您應該選取適當的安全性層級。 請參閱 [設定存取檢查的安全性層級](setting-a-security-level-for-access-checks.md)。 此外，您必須務必定義角色，並將它們新增至應用程式。 如果啟用存取檢查但未新增任何角色，對應用程式的所有呼叫都將會失敗。 請參閱 [定義應用程式的角色](defining-roles-for-an-application.md)。

> [!Note]  
> 當您對應用程式進行偵錯工具時，停用安全性可能會很有説明，讓您能夠專注于程式列為和設計的其他層面。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將角色指派給元件、介面或方法](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[設定 Role-Based 安全性](configuring-role-based-security.md)
</dt> <dt>

[定義應用程式的角色](defining-roles-for-an-application.md)
</dt> <dt>

[在元件層級啟用存取檢查](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[設定存取檢查的安全性等級](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



