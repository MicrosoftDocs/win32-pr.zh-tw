---
description: 啟用存取檢查之後，您必須為您的 COM + 應用程式選取您要執行存取檢查的層級。
ms.assetid: 9c044add-7761-4378-b7eb-bf4e84e913b3
title: 設定存取檢查的安全性等級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e912f671a27d35b51939376fa14af3b693c368e3375680913693d364ddf638
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120368"
---
# <a name="setting-a-security-level-for-access-checks"></a>設定存取檢查的安全性等級

啟用 [存取檢查](enabling-access-checks-for-an-application.md)之後，您必須為您的 com + 應用程式選取您要執行存取檢查的層級。

**若要選取安全性等級**

1.  在 [元件服務] 系統管理工具的主控台樹中，以滑鼠 **按右鍵您** 要啟用存取檢查的 com + 應用程式，然後按一下 [內容]。

2.  在 [應用程式屬性] 對話方塊中，按一下 [ **安全性** ] 索引標籤。

3.  在 [ **安全性等級**] 底下，選取下列其中一項：

    -   **只有在處理層級執行存取檢查**，此設定表示指派給應用程式的角色中的使用者將會新增至流程安全描述項。 這有下列效果和含意：

        在元件、方法和介面層級關閉更細緻的角色檢查。 安全性檢查只會在應用層級執行。

        安全性屬性不會包含在應用程式中執行之任何物件的內容上。 這可能會影響物件的啟用方式。 請參閱 [資訊安全內容屬性](security-context-property.md)。

        安全性呼叫內容將無法使用。 依賴安全性呼叫內容資訊的程式設計安全性將無法運作。 請參閱 [安全性呼叫內容資訊](security-call-context-information.md)。

    -   **在程式和元件層級執行存取檢查**，此設定表示將會執行進程層級的安全性描述項檢查和以角色為基礎的完整安全性檢查。 這有下列效果和含意：

        若要啟用特定元件的角色檢查，您必須 [在元件層級啟用存取檢查](enabling-access-checks-at-the-component-level.md)。

        安全性屬性包含在應用程式內執行之任何物件的內容中。 這可能會影響物件的啟用方式。 請參閱 [資訊安全內容屬性](security-context-property.md)。

        可以使用安全性呼叫內容。 啟用以程式設計的角色為基礎的安全性。 請參閱 [安全性呼叫內容資訊](security-call-context-information.md)。

        > [!Note]  
        > 針對 COM + 程式庫應用程式，您必須選擇在進程和元件層級檢查，以確定任何有意義的存取檢查可運作。 程式庫應用程式依賴進程層級安全性的主機進程。 您可以藉由 [設定驗證](enabling-authentication-for-a-library-application.md)，判斷程式庫應用程式如何與主機進程所執行的驗證互動。 如需詳細資訊，請參閱連結 [庫應用程式安全性](library-application-security.md)。

         

4.  按一下 [確定]。

下次啟動應用程式時，系統會在指定的層級自動檢查安全性。 只有指派給指派給應用程式角色的使用者才會獲得應用程式的存取權。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將角色指派給元件、介面或方法](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[設定 Role-Based 安全性](configuring-role-based-security.md)
</dt> <dt>

[定義應用程式的角色](defining-roles-for-an-application.md)
</dt> <dt>

[啟用應用程式的存取檢查](enabling-access-checks-for-an-application.md)
</dt> <dt>

[在元件層級啟用存取檢查](enabling-access-checks-at-the-component-level.md)
</dt> </dl>

 

 



