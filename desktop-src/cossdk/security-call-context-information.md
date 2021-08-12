---
description: 安全性呼叫內容資訊
ms.assetid: 8b170c17-f095-4c25-9ee2-480681b7e5f6
title: 安全性呼叫內容資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0aed07f79fdba16f0ea6139a58cc50871d795e1eacbf94737b04dbf5f1fe900
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546865"
---
# <a name="security-call-context-information"></a>安全性呼叫內容資訊

以角色為基礎的安全性建基於一般機制，可讓您在對您的元件發出呼叫的鏈中，取得有關所有上游呼叫端的安全性資訊。 只有當您啟用元件層級角色檢查時，才能使用這項資訊。 如需有關如何設定元件層級安全性的詳細資訊，請參閱 [設定存取檢查的安全性層級](setting-a-security-level-for-access-checks.md)。

您可以使用 [**ISecurityCallCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) 介面，以程式設計方式存取安全性呼叫內容資訊。 如需描述，請參閱程式 [設計元件安全性](programmatic-component-security.md)。

每次超過安全性界限時，都會傳遞安全性呼叫內容。 針對位於相同安全性界限內的應用程式中元件之間的呼叫，不會傳遞任何呼叫內容資訊。 對於進程之間或進程內的應用程式之間的呼叫，呼叫內容資訊流程。

如果您想要進行詳細的審核和記錄，這項功能特別有用。 您可以取得並記錄每個上游呼叫端的安全性資訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[有效設計角色](designing-roles-effectively.md)
</dt> <dt>

[安全性界限](security-boundaries.md)
</dt> <dt>

[資訊安全內容屬性](security-context-property.md)
</dt> <dt>

[使用角色進行用戶端授權](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



