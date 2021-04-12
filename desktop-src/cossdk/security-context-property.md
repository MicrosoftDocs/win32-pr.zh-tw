---
description: 資訊安全內容屬性
ms.assetid: 7ffae145-be13-4a2c-beb1-eaa1d11ad9a7
title: 資訊安全內容屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b061ef7c0d0d0c146b626c11fd550c48ab488a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191023"
---
# <a name="security-context-property"></a>資訊安全內容屬性

如同 COM + 所提供的每個自動服務，自動角色檢查是以物件內容所包含的屬性為基礎。 決定是否必須在呼叫元件時執行安全性檢查，是根據設定的元件具現化時所建立物件內容上的安全性屬性。

您通常不需要擔心這個屬性;它直接由 COM + （而非您）使用。 不過，在某些情況下，您可能會想要嚴格控制物件的啟用。 在此情況下，安全性屬性可能會影響您的物件在哪個內容中啟用。 也就是說，如果物件的設定與其建立者的內容不相容，則會在其本身的內容中啟用。 安全性屬性可能會影響這一點，如同物件內容上的任何屬性。

如果您不想讓安全性設定影響啟用，則只能選擇處理層級的存取檢查。 這會隱藏物件內容上的安全性屬性，雖然它會有效停用以角色為基礎的檢查，並讓 [安全性呼叫內容資訊](security-call-context-information.md) 無法使用。

如需有關進程層級存取檢查的詳細資訊，請參閱 [安全性界限](security-boundaries.md)。 若要瞭解如何設定進程層級安全性，請參閱 [設定存取檢查的安全性層級](setting-a-security-level-for-access-checks.md)。

如需物件內容的詳細資訊， [請參閱內容](com--contexts.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[有效設計角色](designing-roles-effectively.md)
</dt> <dt>

[安全性界限](security-boundaries.md)
</dt> <dt>

[安全性呼叫內容資訊](security-call-context-information.md)
</dt> <dt>

[使用角色進行用戶端授權](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



