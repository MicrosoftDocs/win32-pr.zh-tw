---
description: 有三個函數可產生對話方塊來處理錯誤： SetupCopyError、SetupDeleteError 和 SetupRenameError。
ms.assetid: fcb310e1-5db7-47f3-b3d6-d528eb17e19a
title: " (設定 API) 處理錯誤"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59f3c69a4ab4943589d00354c401b1f35aa984b04552ecd03a1c4863fcf9134a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665988"
---
# <a name="error-handling-setup-api"></a> (設定 API) 處理錯誤

有三個函數可產生對話方塊來處理錯誤： [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora)、 [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)和 [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)。

回呼常式可以使用這些函數來產生使用者介面，以處理 [**SPFILENOTIFY \_ COPYERROR**](spfilenotify-copyerror.md)、 [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md)和 [**SPFILENOTIFY \_ RENAMEERROR**](spfilenotify-renameerror.md) 通知。

這些錯誤處理函式都會產生對話方塊，詢問使用者如何繼續進行相關資訊。 如同 [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)，您可以在函式呼叫期間指定旗標，以修改對話方塊的版面配置和行為。

 

 



