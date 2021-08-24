---
description: 描述調試時，會使用下列詞彙。
ms.assetid: 580f2787-d944-4350-a2c2-c00816b3f515
title: 調試術語
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feb8de5035887f3d3c19cca1e8475ff17cb930b1142c712481e096e0e612ea81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692068"
---
# <a name="debugging-terminology"></a>調試術語

描述調試時，會使用下列詞彙。

<dl> <dt>

<span id="Blue_screen"></span><span id="blue_screen"></span><span id="BLUE_SCREEN"></span>藍色畫面
</dt> <dd>

當系統發生硬體問題、資料不一致或類似的錯誤時，可能會顯示藍色畫面，其中包含可用來判斷錯誤原因的資訊。 此資訊包含停止程式碼，以及是否已建立損毀傾印檔案。 它也可能包含已載入的驅動程式清單和堆疊追蹤。

</dd> <dt>

<span id="Crash_dump_file"></span><span id="crash_dump_file"></span><span id="CRASH_DUMP_FILE"></span>損毀傾印檔案
</dt> <dd>

您可以設定系統在每次產生停止程式碼時，將資訊寫入硬碟中的損毀傾印檔案。 檔案包含偵錯工具可以用來分析錯誤的資訊。 這個檔案可以與電腦中包含的實體記憶體一樣大。

</dd> <dt>

<span id="Debugger"></span><span id="debugger"></span><span id="DEBUGGER"></span>調試
</dt> <dd>

設計用來協助偵測、找出及修正另一個程式中錯誤的程式。 它可讓開發人員逐步執行進程及其執行緒、監視記憶體、變數，以及進程和執行緒內容的其他元素。

</dd> <dt>

<span id="Kernel_mode"></span><span id="kernel_mode"></span><span id="KERNEL_MODE"></span>核心模式
</dt> <dd>

執行系統服務和設備磁碟機的處理器模式。 所有介面和 CPU 指令都可供使用，而且可以存取所有的記憶體。

</dd> <dt>

<span id="Minidump_file"></span><span id="minidump_file"></span><span id="MINIDUMP_FILE"></span>小型傾印檔案
</dt> <dd>

應用程式可以產生使用者模式小型傾印檔案，其中包含損毀傾印檔案中包含的有用資訊子集。 如需詳細資訊，請參閱 [小型](minidump-files.md)傾印檔案。

</dd> <dt>

<span id="STOP_code"></span><span id="stop_code"></span><span id="STOP_CODE"></span>停止程式碼
</dt> <dd>

指出停止系統核心繼續執行的錯誤的錯誤碼。

</dd> <dt>

<span id="Symbol_files"></span><span id="symbol_files"></span><span id="SYMBOL_FILES"></span>符號檔
</dt> <dd>

系統會建立所有系統應用程式、驅動程式和 Dll，使其偵錯工具資訊位於稱為符號檔的個別檔案中。 因此，系統會變得更小且更快，但如果已安裝符號檔，仍然可以進行調試。 如需詳細資訊，請參閱 [符號](symbol-files.md)檔。

</dd> <dt>

<span id="User_mode"></span><span id="user_mode"></span><span id="USER_MODE"></span>使用者模式
</dt> <dd>

應用程式執行所在的處理器模式。 在此模式中有一組有限的介面可供使用，而且系統資料的存取會受到限制。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定自動調試](configuring-automatic-debugging.md)
</dt> </dl>

 

 



