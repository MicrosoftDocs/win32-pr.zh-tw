---
description: 每個進程都有一個環境區塊，其中包含一組環境變數及其值。 環境變數有兩種類型：每個使用者的使用者環境變數 (設定) 和系統內容變數 (為每個人) 設定。
ms.assetid: 6732b12f-ced1-4769-b947-79da8fd2237a
title: 環境變數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647c685aac8ed6df36c0312d7eef49793fd4b2bbfca5576e0377e59da31dd777
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910318"
---
# <a name="environment-variables"></a>環境變數

每個進程都有一個環境區塊，其中包含一組環境變數及其值。 環境變數有兩種類型：每個使用者的使用者環境變數 (設定) 和系統內容變數 (為每個人) 設定。

根據預設，子進程會繼承其父進程的環境變數。 命令處理器啟動的程式會繼承命令處理器的環境變數。 若要為子進程指定不同的環境，請建立新的環境區塊，並將其指標作為參數傳遞給 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) 函數。

命令處理器提供 **set** 命令以顯示其環境區塊，或建立新的環境變數。 您也可以從 **主控台** 選取 [**系統**]、選取 [ **Advanced system settings**]，然後按一下 [**環境變數**]，以查看或修改環境變數。

每個環境區塊都包含下列格式的環境變數：<dl> *Var1* =*Value1* \\0  
*Var2* =*Value2* \\0  
*Var3* =*Value3* \\0  
...  
*VarN* =*值* \\0 \\ 0  
</dl>

環境變數的名稱不能包含等號 (=) 。

[**GetEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings)函式會傳回呼叫進程的環境區塊指標。 這應該被視為唯讀區塊;請勿直接修改它。 相反地，請使用 [**SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable) 函數來變更環境變數。 當您完成從 **GetEnvironmentStrings** 取得的環境區塊時，請呼叫 [**FreeEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-freeenvironmentstringsa) 函數來釋放區塊。

呼叫 [**SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable) 不會影響系統內容變數。 若要以程式設計方式新增或修改系統內容變數，請將它們新增至 **HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ Session Manager \\ 環境** 登錄機碼，然後將具有 *LParam* 設定的 [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange)訊息廣播至字串 "環境"。 這可讓應用程式（例如 shell）挑選您的更新。

使用者定義環境變數的大小上限為32767個字元。 環境區塊的大小不會有任何技術上的限制。 不過，視用來存取區塊的機制而定，有一些實際的限制。 例如，批次檔無法設定的變數長度超過命令列長度上限。

**Windows Server 2003 和 Windows XP：** 進程的環境區塊大小上限為32767個字元。 從 Windows Vista 和 Windows Server 2008 開始，環境區塊的大小不會有任何技術上的限制。

[**GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable)函式會判斷指定的變數是否定義在呼叫進程的環境中，如果是的話，則為其值。

若要取得指定使用者的環境區塊複本，請使用 [**CreateEnvironmentBlock**](/windows/win32/api/userenv/nf-userenv-createenvironmentblock) 函數。

若要展開環境變數字串，請使用 [**ExpandEnvironmentStrings**](/windows/desktop/api/processenv/nf-processenv-expandenvironmentstringsa) 函數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[變更環境變數](changing-environment-variables.md)
</dt> <dt>

[使用者環境變數](../shell/user-environment-variables.md)
</dt> </dl>

 

 
