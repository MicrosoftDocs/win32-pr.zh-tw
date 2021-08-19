---
description: 只會在應用程式界限檢查安全性。
ms.assetid: 32a05150-a68a-4302-9983-b9c1269b368c
title: 安全性界限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050be064c8a2fe3dc8eb81e2297e1699504f92ae7b8b4352d9b875dfc50e91a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047266"
---
# <a name="security-boundaries"></a>安全性界限

只會在應用程式界限檢查安全性。 也就是說，在同一個應用程式的兩個元件中，當某個元件呼叫另一個元件時，不會執行任何安全性檢查。 不過，如果兩個應用程式共用相同的進程，而其中一個元件呼叫另一個元件，則會進行安全性檢查，因為已超過應用程式界限。 同樣地，如果有兩個應用程式位於不同的伺服器進程，而第一個應用程式中的元件呼叫第二個應用程式中的元件，則會完成安全性檢查。

因此，如果您有兩個元件，而且您想要在一個呼叫另一個元件時完成安全性檢查，您必須將元件放在不同的 COM + 應用程式中。

由於 COM + 程式庫應用程式是由其他進程所裝載，因此程式庫應用程式和裝載進程之間會有一個安全性界限。 此外，程式庫應用程式不會控制進程層級的安全性，這會影響您需要為其設定安全性的方式。 如需詳細資訊，請參閱連結 [庫應用程式安全性](library-application-security.md)。

決定是否必須在呼叫元件時執行安全性檢查，是根據設定的元件具現化時所建立物件內容上的安全性屬性。 如需詳細資訊，請參閱 [資訊安全內容屬性](security-context-property.md)。

## <a name="component-level-access-checks"></a>Component-Level 存取檢查

若是 COM + 伺服器應用程式，您可以選擇在元件層級或在進程層級強制執行存取檢查。

當您選取元件層級存取檢查時，您會啟用更細緻的角色指派。 您可以將角色指派給元件、介面和方法，並達成有明確的授權原則。 這會是使用以角色為基礎的安全性之應用程式的標準設定。

若是 COM + 程式庫應用程式，如果您想要使用角色，則必須選取元件層級安全性。 程式庫應用程式無法使用進程層級安全性。

如果您使用以程式設計的角色為基礎的安全性，則應該選取元件層級的存取檢查。 只有在啟用元件層級安全性時，才可使用安全性呼叫內容資訊。 如需詳細資訊，請參閱 [安全性呼叫內容資訊](security-call-context-information.md)。

此外，當您選取元件層級存取檢查時，安全性屬性將會包含在物件內容中。 這表示安全性設定可以在物件啟動的方式中扮演角色。 如需詳細資訊，請參閱 [資訊安全內容屬性](security-context-property.md)。

## <a name="process-level-access-checks"></a>Process-Level 存取檢查

進程層級檢查只適用于應用程式界限。 也就是說，您針對整個 COM + 應用程式所定義的角色，將會決定誰被授與應用程式內任何資源的存取權。 不會套用更細緻的角色指派。 基本上，角色是用來建立安全描述項，以針對應用程式元件的任何呼叫進行驗證。 在此情況下，您不會想要建立具有多個角色的詳細授權原則。 應用程式會使用單一安全描述項。

若是 COM + 程式庫應用程式，則不會選取進程層級的存取檢查。 程式庫應用程式將會在用戶端的進程中執行，因此不會控制進程層級安全性。 如需詳細資訊，請參閱連結 [庫應用程式安全性](library-application-security.md)。

啟用進程層級的存取檢查後，就無法使用安全性呼叫內容資訊。 這表示，當您只使用進程層級安全性時，不能以程式設計的方式進行安全性。 如需詳細資訊，請參閱 [安全性呼叫內容資訊](security-call-context-information.md)。

此外，安全性屬性不會包含在物件內容中。 這表示，在只使用進程層級的存取檢查時，安全性設定永遠不會在物件的啟用方式中扮演角色。 如需詳細資訊，請參閱 [資訊安全內容屬性](security-context-property.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[有效設計角色](designing-roles-effectively.md)
</dt> <dt>

[安全性呼叫內容資訊](security-call-context-information.md)
</dt> <dt>

[資訊安全內容屬性](security-context-property.md)
</dt> <dt>

[使用角色進行用戶端授權](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



