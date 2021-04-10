---
title: WOW64 執行詳細資料
description: WOW64 模擬器會以使用者模式執行。
ms.assetid: 93daf9d0-dfdb-42c3-8c3d-397b21991e83
keywords:
- WOW64 64 位 Windows 程式設計，環境變數
- WOW64 64 位 Windows 程式設計，執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c7d095369b883171e39bffd4dc629b7f80a7f39
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092825"
---
# <a name="wow64-implementation-details"></a>WOW64 執行詳細資料

WOW64 模擬器會以使用者模式執行。 它會提供32位版本的 Ntdll.dll 和處理器核心之間的介面，並攔截核心呼叫。 WOW64 模擬器包含下列 Dll：

-   Wow64.dll 提供核心模擬基礎結構，以及 Ntoskrnl.exe 進入點函數的 Thunk。
-   Wow64Win.dll 為 Win32k.sys 的進入點函數提供 Thunk。
-    (x64 僅) Wow64Cpu.dll 提供在 x64 上執行 x86 程式的支援。
-    (僅限 Intel Itanium) IA32Exec 包含 x86 軟體模擬器。
-    (Intel Itanium 僅) Wowia32x.dll 提供 IA32Exec 和 WOW64 之間的介面。
-    (僅限 ARM64) xtajit.dll 包含 x86 軟體模擬器。
-    (僅限 ARM64) wowarmw.dll 提供在 ARM64 上執行 ARM32 程式的支援。

這些 Dll 以及64位版本的 Ntdll.dll 是唯一可以載入至32位進程的64位二進位檔。 在 ARM 上的 Windows 10 上，CHPE (編譯的混合式可執行檔) 二進位檔也可能載入至 x86 32 位進程。

在啟動時，Wow64.dll 會載入 x86 版本的 Ntdll.dll (或 CHPE 版本（若已啟用) ）並執行其初始化程式碼，以載入所有必要的32位 Dll。 幾乎所有的32位 Dll 都是32位 Windows 二進位檔的未修改複本，但基於效能考慮，部分會載入為 CHPE。 其中某些 Dll 的寫入方式與在32位的 Windows 上的 WOW64 不同，通常是因為它們與64位系統元件共用記憶體。 所有超過32位限制的使用者模式位址空間都是由系統所保留。 如需詳細資訊，請參閱 [WOW64 下的效能和記憶體耗用量](performance-and-memory-consumption.md)。

我們不會使用 x86 系統服務呼叫順序，而是會重建進行系統呼叫的32位二進位檔，以使用自訂的呼叫序列。 此呼叫順序的成本較低，因為 WOW64 會維持在使用者模式中，所以無法攔截。 當偵測到自訂呼叫順序時，WOW64 CPU 會轉換回原生64位模式並呼叫 Wow64.dll。 Thunking 是在使用者模式中完成，以降低對64位核心的影響，並降低 Thunk 中可能造成核心模式損毀、資料損毀或安全性漏洞的錯誤風險。 Thunk 會從32位堆疊解壓縮引數，並將它們延伸至64位，然後進行原生系統呼叫。

## <a name="environment-variables"></a>環境變數

當64位進程建立32位進程，或當32位進程建立64位進程時，WOW64 會為建立的進程設定環境變數，如下表所示。



| 處理序                   | 環境變數                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 64位進程<br/> | 處理器 \_ 架構 = AMD64 或處理器 \_ 架構 = IA64 或處理器 \_ 架構 = ARM64<br/> ProgramFiles =% ProgramFiles%<br/> ProgramW6432 =% ProgramFiles%<br/> CommonProgramFiles =% CommonProgramFiles%<br/> CommonProgramW6432 =% CommonProgramFiles%<br/> **Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 從 Windows 7 和 Windows Server 2008 R2 開始，已新增 ProgramW6432 和 CommonProgramW6432 環境變數。 <br/> |
| 32位進程<br/> | 處理器 \_ 架構 = x86<br/> 處理器 \_ ARCHITEW6432 =% 處理器 \_ 架構%<br/> ProgramFiles =% ProgramFiles (x86) %<br/> ProgramW6432 =% ProgramFiles%<br/> CommonProgramFiles =% CommonProgramFiles (x86) %<br/> CommonProgramW6432 =% CommonProgramFiles%<br/>                                                                                                                                                                                                                  |



 

## <a name="global-hooks"></a>全域攔截

如果符合下列條件，則可以使用 [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) 函數將 DLL 插入另一個進程：

-   32位 DLL 只能插入32位的進程中，而64位 DLL 只能插入至64位進程。 您無法將32位 DLL 插入64位進程，反之亦然。
-   32位和64位 Dll 必須有不同的名稱。
-   DLL 和進程的架構必須相符。 例如，您不能將32位 x86 DLL 插入32位 ARM 進程中。

如需詳細資訊，請參閱 [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)。

請注意，您可以在安裝攔截的執行緒上呼叫 **WH \_ 滑鼠**、 **WH \_ 鍵盤**、 **WH \_ 日誌 \***、 **WH \_ SHELL** 和低層級的勾點，而不是在處理攔截的執行緒上呼叫。 針對這些攔截器，如果32位攔截器早于攔截鏈中的64位攔截器，則可能會呼叫32位和64位的勾點。 如需詳細資訊，請參閱 [使用](../winmsg/using-hooks.md)勾點。

 

