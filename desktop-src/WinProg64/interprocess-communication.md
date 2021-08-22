---
title: 處理序間通訊
description: 下列技巧可用於32位和64位應用程式之間的通訊。
ms.assetid: 9a60ccfe-4ccf-44d7-9522-42609d95217b
keywords:
- 處理序間通訊 64-位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5089440caf6ac537a314e7e920796fadeac5817220ba91f283c297bd0451b705
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734118"
---
# <a name="interprocess-communication-between-32-bit-and-64-bit-applications"></a>32位和64位應用程式之間的處理序間通訊

下列技術可用於32位和64位應用程式之間的通訊：

-   64位版本的 Windows 使用32位控制碼來進行互通性。 當共用32位和64位應用程式之間的控制碼時，只有較低的32位是很重要的，因此在將控制碼從64位傳遞到32位時，可以安全地截斷控制碼 () 或將控制碼從32位傳遞到64位) 時，將它進行正負號擴充 (。 可以共用的控制碼包括使用者物件的控制碼（例如 windows (**HWND**) ）、GDI 物件的控制碼（例如畫筆和筆刷） (**HBRUSH** 和 **HPEN**) ，以及命名物件（例如 mutex、信號和檔案控制代碼）的控制碼。
-   您可以使用 (RPC) 的遠端程序呼叫。
-   如果已針對所有使用的介面註冊32位和64位 proxy/stub Dll，則可以使用 COM LocalServers。
-   如果指標相依類型已正確轉換 (或避免) ，則可以使用共用記憶體。
-   [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)和 [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)函式可以從32位或64位進程啟動32位和64位進程，但有某些限制。

位於% windir% System32 下的64位可執行檔 \\ 無法從32位進程啟動，因為檔案系統重新導向程式會重新導向路徑。 請勿停用重新導向來完成此動作;請改用% windir% \\ Sysnative。 如需詳細資訊，請參閱 [檔案系統重定向](file-system-redirector.md)程式。

 

 