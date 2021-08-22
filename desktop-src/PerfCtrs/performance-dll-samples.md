---
description: Windows SDK (WSDK) 包含三個完整的範例效能 dll。
ms.assetid: 862be53a-3d58-42b9-adf0-2f913dc6fb06
title: 效能 DLL 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94e77ed35b1c328879ad5f83dded45fe92bf4a62ae15c794e5d9d9b23daeda1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143881"
---
# <a name="performance-dll-samples"></a>效能 DLL 範例

Windows SDK (WSDK) 包含三個完整的範例效能 dll。 這些範例位於範例 \\ WinBase \\ WinNT \\ PerfTool \\ PerfDlls 目錄中。 此路徑的根目錄是 WSDK 的基礎安裝目錄。 您可以從[Microsoft Windows 軟體開發套件 (SDK) ](https://developer.microsoft.com/windows/downloads/windows-10-sdk/)下載 WSDK (搜尋 Windows SDK，然後針對最新發行的作業系統) 選取下載。

此目錄中包含的範例包括：

-   **AppMem**：提供 [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc)、 [**GlobalReAlloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc)和 [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) 函式的對應項，這些函數會報告效能資訊。 登錄中的效能計數器和效能工具可以讀取效能資訊。
-   **LeakyBin**：示範如何使用應用程式效能計數器。
-   **PerfGen**-在五個不同期間提供三個波形，以搭配效能工具使用，以已知的速率和值提供資料。 這有助於測試使用效能資料的應用程式，並需要可預測的值來進行測試。

 

 
