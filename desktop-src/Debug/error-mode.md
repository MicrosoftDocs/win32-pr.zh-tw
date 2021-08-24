---
description: 錯誤模式向系統指出應用程式如何回應嚴重的錯誤。
ms.assetid: 288be838-6094-4824-9cae-99b7ff9eea74
title: 錯誤模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a1baa4c0bc4e1209586b630f2a58bfb06572131de8e7d2706614c78646d7e3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260928"
---
# <a name="error-mode"></a>錯誤模式

錯誤模式向系統指出應用程式如何回應嚴重的錯誤。 嚴重錯誤包括磁片故障、磁片磁碟機未就緒錯誤、資料對齊和未處理的例外狀況。 您可以透過每個執行緒或每個處理常式來管理此錯誤模式。 應用程式可讓系統顯示訊息方塊，通知使用者發生錯誤，或可處理錯誤。

若要在不需要使用者介入的情況下處理這些錯誤，請使用 [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) 或執行緒特定的 [**SetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode)。 呼叫其中一個函式並指定適當的旗標之後，系統將不會顯示對應的錯誤訊息方塊。

處理常式可以使用 [**GetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode) 或 [**GetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode)來取得其錯誤模式。

最佳做法是在啟動時，所有應用程式都會以 **SEM \_ FAILCRITICALERRORS** 的參數呼叫整個進程的 [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode)函式。 這是為了防止錯誤強制回應對話方塊讓應用程式停止回應。

相反地，呼叫端應該優先採用這些函式的執行緒特定版本，因為它們較不會干擾系統的正常行為。

 

 
