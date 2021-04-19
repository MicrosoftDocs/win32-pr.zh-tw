---
description: 有三個函數可產生對話方塊來處理錯誤： SetupCopyError、SetupDeleteError 和 SetupRenameError。
ms.assetid: fcb310e1-5db7-47f3-b3d6-d528eb17e19a
title: " (設定 API) 處理錯誤"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fb1347a3bec800200c2b6bda81e3f1eeeb866de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986379"
---
# <a name="error-handling-setup-api"></a><span data-ttu-id="fe792-103"> (設定 API) 處理錯誤</span><span class="sxs-lookup"><span data-stu-id="fe792-103">Error Handling (Setup API)</span></span>

<span data-ttu-id="fe792-104">有三個函數可產生對話方塊來處理錯誤： [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora)、 [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)和 [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)。</span><span class="sxs-lookup"><span data-stu-id="fe792-104">There are three functions that generate dialog boxes to handle errors: [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora), and [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora).</span></span>

<span data-ttu-id="fe792-105">回呼常式可以使用這些函數來產生使用者介面，以處理 [**SPFILENOTIFY \_ COPYERROR**](spfilenotify-copyerror.md)、 [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md)和 [**SPFILENOTIFY \_ RENAMEERROR**](spfilenotify-renameerror.md) 通知。</span><span class="sxs-lookup"><span data-stu-id="fe792-105">Callback routines can use these functions to generate a user interface to handle [**SPFILENOTIFY\_COPYERROR**](spfilenotify-copyerror.md), [**SPFILENOTIFY\_DELETEERROR**](spfilenotify-deleteerror.md), and [**SPFILENOTIFY\_RENAMEERROR**](spfilenotify-renameerror.md) notifications.</span></span>

<span data-ttu-id="fe792-106">這些錯誤處理函式都會產生對話方塊，詢問使用者如何繼續進行相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fe792-106">Each of these error-handling functions generates a dialog box that asks the user for information on how to proceed.</span></span> <span data-ttu-id="fe792-107">如同 [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)，您可以在函式呼叫期間指定旗標，以修改對話方塊的版面配置和行為。</span><span class="sxs-lookup"><span data-stu-id="fe792-107">As with [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska), you can modify the dialog box's layout and behavior by specifying flags during the function call.</span></span>

 

 



