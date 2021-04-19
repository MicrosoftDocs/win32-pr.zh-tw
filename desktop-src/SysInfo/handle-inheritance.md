---
description: 子進程可以繼承其父進程的控制碼。 繼承的控制碼只在子進程的內容中有效。 若要讓子進程繼承其父進程的開啟控制碼，請使用下列步驟。
ms.assetid: 957cd369-bebf-4e04-9f7e-a936e2e97887
title: 處理繼承
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd684308503a8747f6730e9d0daf4aa3de760186
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000322"
---
# <a name="handle-inheritance"></a>處理繼承

子進程可以繼承其父進程的控制碼。 繼承的控制碼只在子進程的內容中有效。 若要讓子進程繼承其父進程的開啟控制碼，請使用下列步驟。

1.  使用設定為 **TRUE** 的 [**安全性 \_ 屬性**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85))結構的 **bInheritHandle** 成員建立控制碼。
2.  使用 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) 函數建立子進程，並將 *bInheritHandles* 參數設定為 **TRUE**。

[**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)函式會複製要在目前進程或另一個進程中使用的控制碼。 如果應用程式為另一個進程複製其中一個控制碼，則重複的控制碼只在其他進程的內容中有效。

重複或繼承的控制碼是唯一值，但它是指與原始控制碼相同的物件。 進程可以繼承或複製下列物件類型的控制碼：

-   存取權杖
-   通訊裝置
-   主控台輸入
-   主控台畫面緩衝區
-   桌面
-   目錄
-   事件
-   檔案
-   檔案對應
-   工作 (Job)
-   郵箱
-   Mutex
-   Pipe
-   處理序
-   登錄機碼
-   Semaphore
-   插座
-   Thread
-   計時器
-   視窗站

所有其他物件都是建立它們的進程的私用;無法複製或繼承其物件控制碼。

如需詳細資訊，請參閱[繼承](/windows/desktop/ProcThread/inheritance)。

 

 
