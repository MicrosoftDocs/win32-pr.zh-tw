---
description: 使用者可以設定自動偵測，以協助他們判斷其系統或應用程式停止回應的原因。
ms.assetid: c3c7aa98-c298-452c-b8d0-10a08b4d82a3
title: 設定自動調試
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990f2f52e6227e4b1a2cf92656794c90fb5d465915a5d888025d0f3b2c438630
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076502"
---
# <a name="configuring-automatic-debugging"></a>設定自動調試

使用者可以設定自動偵測，以協助他們判斷其系統或應用程式停止回應的原因。

## <a name="configuring-automatic-debugging-for-system-crashes"></a>設定系統損毀的自動偵測

若要設定目的電腦在系統停止回應時產生損毀傾印檔案，請使用主控台中的 **系統** 應用程式。 按一下 [ **Advanced system settings**]，這會顯示 [ **系統** 內容] 對話方塊。 在該方塊的 [ **Advanced （Advanced** ）] 索引標籤上，按一下 [**啟動和** 復原] 下的 **設定**，然後使用適當的修復選項。 或者，您可以使用下列登錄機碼來設定損毀傾印選項：

**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制項** \\ **CrashControl**

您可以指定的檔案是損毀傾印檔案。 其預設名稱為 Memory。 您可以使用核心模式的偵錯工具（例如 WinDbg 或 KD）來進行損毀傾印的偵錯工具。 如需詳細資訊，請參閱偵錯工具隨附的檔。

## <a name="configuring-automatic-debugging-for-application-crashes"></a>設定應用程式損毀的自動偵測

當應用程式停止回應時 (例如，在存取違規) 之後，系統會自動叫用登錄中指定的偵錯工具進行事後的偵錯工具，如果已正確設定命令列，則會將處理序識別碼和事件控制碼傳遞至偵錯工具。 下列程式描述如何在登錄中指定偵錯工具。

**將偵錯工具設定為事後偵錯工具**

1.  移至下列登錄機碼：

    **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AeDebug**

2.  使用指定偵錯工具命令列的 REG SZ 字串，來新增或編輯 **偵錯工具** 值 \_ 。

    字串應包含偵錯工具可執行檔的完整路徑。 以 "% ld" 參數表示偵錯工具命令列的處理序識別碼和事件控制碼。 不同的偵錯工具可能會有自己的參數語法來指出這些值。 叫用偵錯工具時，會以處理序識別碼取代第一個 "% ld"，然後將第二個 "% ld" 取代成事件控制碼。

    下列文字是如何將 WinDbg 設定為偵錯工具的範例。

    ``` syntax
    "C:\debuggers\windbg.exe" -p %ld -e %ld -g
    ```

3.  如果您想要在沒有使用者互動的情況下叫用偵錯工具， 請在叫用 \_ 偵錯工具之前，使用指定系統是否應該對使用者顯示對話方塊的 REG SZ 字串，來新增或編輯自動值。 字串 "1" 停用此對話方塊;字串 "0" 會啟用對話方塊。

## <a name="excluding-an-application-from-automatic-debugging"></a>從自動偵測排除應用程式

下列程式描述如何在 **AeDebug** 索引鍵的 **自動** 值設定為1之後，從自動偵測排除應用程式。

**若要將應用程式從自動偵錯工具中排除**

1.  移至下列登錄機碼：

    **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AeDebug**

2.  將 REG \_ DWORD 值新增至 **AutoExclusionList** 子機碼，其中名稱是可執行檔的名稱，而值為1。 根據預設，桌面視窗管理員 (Dwm.exe) 會從自動偵錯工具中排除，否則如果 Dwm.exe 停止回應，則會發生系統鎖死 (使用者無法看到偵錯工具所顯示的介面，因為 Dwm.exe 沒有回應，而且 Dwm.exe 因為偵錯工具) 而無法終止。

    **Windows Server 2003 和 Windows XP：****AutoExclusionList** 子機碼無法使用;因此，您無法從自動偵測中排除任何應用程式（包括 Dwm.exe）。

預設的 **AeDebug** 登錄專案可以如下所示：

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows NT
            CurrentVersion
               AeDebug
                  Auto = 1
                  AutoExclusionList
                     DWM.exe = 1
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 WinDbg 啟用事後的調試](/windows-hardware/drivers/debugger/enabling-postmortem-debugging)
</dt> </dl>

 

 
