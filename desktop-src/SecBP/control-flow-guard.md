---
description: 控制流程防護 (CFG) 是一種高度優化的平臺安全性功能，其建立是為了對抗記憶體損毀弱點。
ms.assetid: 116EAD64-7CAE-455C-BA43-9492F78DE873
title: 控制流程防護
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91cf97a648443135e7fee666ea4c259b1c32104e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115908"
---
# <a name="control-flow-guard"></a>控制流程防護

## <a name="what-is-control-flow-guard"></a>什麼是控制流程防護？

控制流程防護 (CFG) 是一種高度優化的平臺安全性功能，其建立是為了對抗記憶體損毀弱點。 藉由對應用程式可從中執行程式碼的位置進行嚴格的限制，就能讓惡意探索更難利用緩衝區溢位等弱點來執行任意程式碼。 CFG 擴充了先前的惡意探索緩和技術，例如 [/gs](/cpp/build/reference/gs-buffer-security-check?view=vs-2019)、 [DEP](../memory/data-execution-prevention.md)和 [ASLR](/archive/blogs/michael_howard/address-space-layout-randomization-in-windows-vista)。

這項功能可在 Microsoft Visual Studio 2015 中取得，並可在「CFG 感知」版本的 Windows 上執行，也就是適用于桌上型電腦和伺服器的 x86 和 x64 版本，Windows 10 和 Windows 8.1 更新版 (KB3000850) 。

我們強烈建議開發人員為其應用程式啟用 CFG。 您不需要為程式碼的每個部分啟用 CFG，因為已啟用混合的 CFG 和非 CFG 啟用的程式碼將會正常執行。 但是無法針對所有程式碼啟用 CFG，可以在保護中開啟間距。 此外，CFG 啟用的程式碼可在「CFG 感知」版本的 Windows 上正常運作，因此完全與其相容。

## <a name="how-can-i-enable-cfg"></a>如何啟用 CFG？

在大部分情況下，不需要變更原始程式碼。 您只需要在 Visual Studio 2015 專案中新增一個選項，編譯器和連結器就會啟用 CFG。

最簡單的方法是流覽至 **專案 \| 屬性設定 \| 屬性 \| C/c + + 程式 \| 代碼產生** ，然後選擇 **[是] (/Guard： cf)** 用於控制流程防護。

![visual studio 中的 cfg 屬性](images/cfg-vs.png)

或者，將 **/guard： cf** 新增至 **專案 \| 屬性設定 \| 屬性 \| C/c + + \| 命令列 \| 額外選項** (針對編譯器) 和 **/Guard： cf** 至 **專案屬性設定 \| \| 屬性 \| 連結器 \| 命令列 \| 額外選項** (的連結器) 。

![編譯器的 cfg 屬性](images/cfg-compiler.png)![連結器的 cfg 屬性](images/cfg-linker.png)

如需其他資訊，請參閱 [/guard (啟用控制流程防護) ](/cpp/build/reference/guard-enable-control-flow-guard?view=vs-2019) 。

如果您是從命令列建立您的專案，您可以新增相同的選項。 例如，如果您要編譯稱為 test .cpp 的專案，請使用 **cl/guard： cf test .cpp/guard： cf**。

您也可以選擇使用記憶體管理 API 中的 [**SetProcessValidCallTargets**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessvalidcalltargets) ，以動態方式控制由 CFG 視為有效的一組 icall 目標位址。 您可以使用相同的 API 來指定頁面是否為 CFG 的無效或有效的目標。 [**VirtualProtect**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualprotect)和 [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc)函數預設會將可執行檔和認可頁面的指定區域視為有效的間接呼叫目標。 您可以覆寫此行為，例如在實作為時間的編譯器時，在呼叫 **VirtualAlloc** 時指定不正確頁面目標，或在呼叫 **VirtualProtect** 時指定 **\_ \_ 無效** 的頁面目標，如 [**記憶體保護常數**](/windows/desktop/Memory/memory-protection-constants)中所述。 **\_ \_ \_**

## <a name="how-do-i-tell-that-a-binary-is-under-control-flow-guard"></a>如何判斷二進位檔位於控制流程防護下？

使用 */headers* 和 */loadconfig* 選項，從 Visual Studio 命令提示字元執行 [dumpbin 工具](/cpp/build/reference/dumpbin-reference) (包含在 Visual Studio 2015 安裝) 中： **dumpbin/headers/loadconfig test.exe**。 在 CFG 下，二進位檔的輸出應該會顯示標頭值包含 "Guard"，且載入設定值包含「CF 檢測」和「存在 FID 資料表」。

![dumpbin/headers 的輸出](images/cfg-dumpbin-headers.png)

![dumpbin/loadconfig 的輸出](images/cfg-dumpbin-loadconfig.png)

## <a name="how-does-cfg-really-work"></a>CFG 真正的運作方式為何？

軟體弱點通常是藉由將不太可能、不尋常或極端的資料提供給執行中的程式而遭到惡意探索。 例如，攻擊者可以藉由提供比預期更多的程式輸入，來利用緩衝區溢位弱點，藉此將程式所保留的區域保留以保留回應。 這可能會損毀可能保存函式指標的相鄰記憶體。 當程式呼叫這個函式時，它可能會跳到攻擊者指定的非預期位置。

不過，強大的編譯和執行時間支援組合，可實現控制流程完整性，以嚴格限制間接呼叫指示的執行位置。

編譯器會執行下列動作：

1.  將輕量安全性檢查新增至已編譯的程式碼。
2.  識別應用程式中的函式集合，這些函數是間接呼叫的有效目標。

Windows 核心提供的執行時間支援：

1.  有效率地維護識別有效間接呼叫目標的狀態。
2.  執行驗證間接呼叫目標是否有效的邏輯。

說明：

![cfg 虛擬虛擬](images/cfg-pseudocode.jpg)

當 CFG 檢查在執行時間失敗時，Windows 會立即終止程式，進而中斷任何嘗試間接呼叫無效位址的惡意探索。

 

 
