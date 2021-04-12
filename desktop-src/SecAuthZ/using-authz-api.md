---
description: Authz API 可讓應用程式使用較低層級的存取控制，以更佳的效能和更簡化的開發執行可自訂的存取檢查。
ms.assetid: 83df96ff-f3d6-43f8-88b2-6387914b3503
title: 使用 Authz API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d86394c0df408307ae4c49377af4a1ae8cc1f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320859"
---
# <a name="using-authz-api"></a>使用 Authz API

Authz API 可讓應用程式使用 [較低層級的存取控制](low-level-access-control.md)，以更佳的效能和更簡化的開發執行可自訂的存取檢查。

Authz API 可讓應用程式快取存取檢查以改善效能、查詢和修改用戶端內容，以及定義可用來動態評估存取權限的商務規則。

## <a name="in-this-section"></a>本節內容



| 主題                                                                             | 描述                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [初始化用戶端內容](initializing-a-client-context.md)<br/>     | 應用程式必須先建立用戶端內容，才能使用 Authz API 來執行存取檢查或審核。<br/>                                                                                                                                            |
| [查詢用戶端內容](querying-a-client-context.md)<br/>             | 應用程式可以呼叫 [**AuthzGetInformationFromCoNtext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) 函數來查詢現有用戶端內容的相關資訊。<br/>                                                                                       |
| [將 Sid 新增至用戶端內容](adding-sids-to-a-client-context.md)<br/> | 應用程式可以藉由呼叫 [**AuthzAddSidsToCoNtext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext)函式，將 [*安全識別碼*](/windows/desktop/SecGloss/s-gly) (sid) 新增至現有的用戶端內容。<br/> |
| [使用 Authz API 檢查存取權](checking-access-with-authz-api.md)<br/>   | 應用程式會藉由呼叫 [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) 函式來判斷是否要授與安全物件的存取權。<br/>                                                                                                                |
| [快取存取檢查](caching-access-checks.md)<br/>                     | 當應用程式藉由呼叫 [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) 函數來執行存取檢查時，可以快取該存取檢查的結果。<br/>                                                                                       |



 

 

