---
title: AccChecker 主控台
description: AccChecker 主控台 (AccCheckConsole.exe) 是一種命令列工具，可用於驗證應用程式 UI 的協助工具執行。
ms.assetid: 9E80BFDD-FB5D-45C5-BE69-7036AD29D863
keywords:
- AccChecker 主控台
- AccChecker 命令列工具
- 命令列、AccChecker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d370f1b4ba5c3d9752015425e12f48311c66dfd8928c6b9fe0f011c48ee6c8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994030"
---
# <a name="the-accchecker-console"></a>AccChecker 主控台

AccChecker 主控台 (AccCheckConsole.exe) 是一種命令列工具，可用於驗證應用程式 UI 的協助工具執行。 命令列接受各種輸入 (例如 HWND、視窗標題和驗證常式) ，並提供對應至錯誤記錄計數的結束代碼。

-   [命令列語法](#command-line-syntax)
-   [命令列錯誤碼](#command-line-error-codes)
-   [命令列範例](#command-line-examples)
-   [相關主題](#related-topics)

![accchecker 主控台命令列工具](images/accchecker-console.png)

## <a name="command-line-syntax"></a>命令列語法

AccChecker 主控台具有下列命令列語法。

**AccCheckConsole \[ 選項 \] (-hwnd <hwnd> \| -進程 <name>) \[<dlls>\]**

命令列選項如下所示。



| 選項。                                                                                                                                                         | 描述                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span id="-hwnd__hwnd_"></span><span id="-HWND__HWND_"></span>-hwnd <hwnd><br/>                                                                     | 驗證具有指定之控制碼 (HWND) 的視窗。 控制碼可以用十六進位或十進位來指定。<br/> |
| <span id="-window__title_"></span><span id="-WINDOW__TITLE_"></span>-視窗 <title><br/>                                                            | 驗證具有指定之標題的視窗。<br/>                                                                |
| <span id="__________________-process__name_"></span><span id="__________________-PROCESS__NAME_"></span> -進程 <name><br/>                       | 驗證具有指定名稱之進程的主視窗。<br/>                                             |
| <span id="____________________________-list"></span><span id="____________________________-LIST"></span> -list<br/>                                       | 列出所有可用的驗證常式。<br/>                                                                 |
| <span id="__________________-enable__name_"></span><span id="__________________-ENABLE__NAME_"></span> -啟用 <name><br/>                          | 執行指定的驗證常式。 此選項可指定一次以上。<br/>                             |
| <span id="_____________________________-disable__name_"></span><span id="_____________________________-DISABLE__NAME_"></span> -停用 <name><br/> | 除了指定的驗證常式之外，全部執行。 此選項可指定一次以上。<br/>                     |
| <span id="___________-log__info_warn_err_"></span><span id="___________-LOG__INFO_WARN_ERR_"></span> -log (info \| 警告 \| err) <br/>                          | 將記錄的最低事件評等。<br/>                                                                      |
| <span id="__________________-logfile__file_"></span><span id="__________________-LOGFILE__FILE_"></span> -logfile <file><br/>                       | 將輸出寫入指定的記錄檔。 此選項可指定一次以上。<br/>                          |
| <span id="-suppress__file_"></span><span id="-SUPPRESS__FILE_"></span>-隱藏 <file><br/>                                                         | 使用指定的 XML 檔案來抑制錯誤。 <br/>                                                                   |
| <span id="-quiet"></span><span id="-QUIET"></span>-quiet<br/>                                                                                             | 請勿將記錄輸出寫入至 stdout。<br/>                                                                            |
| <span id="-help__________________________________"></span><span id="-HELP__________________________________"></span>-help <br/>                           | 顯示快速協助。 <br/>                                                                                             |



 

## <a name="command-line-error-codes"></a>命令列錯誤碼

以下是使用 "echo% errorlevel%" 時，從 AccCheckConsole 傳回的錯誤碼。



| 錯誤碼                       | 描述                                 |
|----------------------------------|---------------------------------------------|
| <span id="0"></span>0<br/> | 沒有錯誤和警告。<br/>       |
| <span id="1"></span>1<br/> | 已要求使用方式語句。 <br/> |
| <span id="2"></span>2<br/> | 錯誤與警告。<br/>          |
| <span id="3"></span>3<br/> | 錯誤和警告。<br/>             |
| <span id="4"></span>4<br/> | 警告但沒有錯誤。<br/>          |
| <span id="5"></span>.5<br/> | 不正確命令列。 <br/>           |



 

## <a name="command-line-examples"></a>命令列範例

以下是數個 AccChecker 主控台命令列範例。

-   在具有指定名稱的視窗上執行所有驗證。

    **AccCheckConsole-視窗「未命名-記事本」**

-   針對 HWND 執行驗證的子集，並指定隱藏專案檔。

    **AccCheckConsole-hwnd 0x00382f00-enable CheckTabbing-enable CheckName-抑制 suppress.xml**

-   從新的驗證 DLL 執行所有驗證。

    **AccCheckConsole-視窗「未命名-記事本」 VerificationRoutine1.dll**

## <a name="related-topics"></a>相關主題

<dl> <dt>

[UI 協助工具檢查程式](ui-accessibility-checker.md)
</dt> </dl>

 

 





