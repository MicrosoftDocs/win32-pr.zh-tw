---
description: Debug Output 函數
ms.assetid: dfe44c8c-43ec-461f-952f-b87256b82ee6
title: Debug Output 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 252e1020ca99bd5b4f2f46d7f2169fa6835dea83a25d599dba142f370bb794f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537738"
---
# <a name="debug-output-functions"></a>Debug Output 函數

[DirectShow 基類](directshow-base-classes.md)提供數個宏來顯示偵錯工具資訊。



| 函式                                               | 描述                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DbgCheckModuleLevel**](dbgcheckmodulelevel.md)     | 檢查是否已針對指定的訊息類型和層級啟用記錄。                             |
| [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) | 顯示作用中物件的相關資訊。                                                           |
| [**DbgInitialise**](dbginitialise.md)                 | 初始化 debug 程式庫。                                                                       |
| [**DbgLog**](dbglog.md)                               | 如果已啟用指定類型和層級的記錄，則會將字串傳送至偵錯工具輸出位置。 |
| [**DbgOutString**](dbgoutstring.md)                   | 將字串傳送至調試輸出位置。                                                         |
| [**DbgSetModuleLevel**](dbgsetmodulelevel.md)         | 設定一或多個訊息類型的記錄層級。                                                |
| [**DbgTerminate**](dbgterminate.md)                   | 清除 debug 程式庫。                                                                         |
| [**DisplayType**](displaytype.md)                     | 將媒體類型的相關資訊傳送至調試輸出位置。                                   |
| [**DumpGraph**](dumpgraph.md)                         | 將篩選圖形的相關資訊傳送至偵錯工具輸出位置。                                 |
| [**GuidNames**](guidnames.md)                         | 全域陣列，包含代表 Uuid 中定義之 Guid 的字串。                        |
| [**名字**](name.md)                                   | 產生僅限 debug 的字串。                                                                       |
| [**注意**](note.md)                                   | 將字串傳送至調試輸出位置。                                                         |
| [**提醒**](remind.md)                               | 在編譯時期產生提醒。                                                                |



 

**登錄機碼**

DirectShow 中的 debug output 函數會使用一組登錄機碼。 這些登錄機碼的位置取決於 Windows 的版本。

在 *Windows Vista 之前*，調試機碼位於下列路徑底下：

**HKEY \_本機 \_ 電腦** \\ **軟體** 的 \\ **調試** 程式

在 Windows Vista 或更新版本中，它們位於下列路徑：

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **DirectShow** 的 \\ **調試** 程式

若為協力廠商篩選，位置取決於用來建立篩選的[DirectShow 基類](directshow-base-classes.md)版本。 Windows Vista 的 Windows SDK 中包含的版本會使用較新的路徑。 先前的版本會使用較舊的路徑。

在接下來的備註中，標籤 *<DebugRoot>* 是用來表示這兩個路徑。 根據 Windows 版本或基類版本，取代正確的路徑。

**Debug 記錄**

DirectShow 定義數個訊息類型，如下表所示。



| 值                   | 描述                                             |
|-------------------------|---------------------------------------------------------|
| 記錄 \_ 錯誤              | 錯誤通知。                                     |
| 記錄 \_ 鎖定            | 鎖定和解除鎖定重要區段。             |
| 記錄檔 \_ 記憶體             | 記憶體配置，以及物件建立和終結。 |
| 記錄 \_ 時間             | 計時和效能度量。                    |
| 記錄 \_ 追蹤              | 一般呼叫追蹤。                                   |
| CUSTOM1 至 CUSTOM5 | 適用于自訂的偵錯工具訊息                     |



 

每一個 DirectShow 的 debug 記錄函數都會指定訊息類型和記錄層級。 只有當該訊息類型目前的調試層級等於或大於記錄函式中指定的層級時，才會顯示此偵錯工具訊息。 否則會忽略此訊息。

例如，如果記錄 \_ 追蹤層級為3或更高，則下列程式碼會輸出字串 "This a debug message"：

``` syntax
DbgLog((LOG_TRACE, 3, TEXT("This is a debug message")));
```

每個模組都可以針對每個訊息類型設定自己的調試層級。  (*模組* 是可使用 **LoadLibrary** 函式載入的 DLL 或可執行檔。 ) 模組的調試層級會出現在登錄的下列機碼底下：

**HKEY \_ 本機 \_ 電腦**\\**<DebugRoot>**\\**<ModuleName>**\\**<MessageType>**

其中 *<Message Type>* 是訊息類型減去初始 "LOG \_ "; 例如， **鎖定** 記錄 \_ 鎖定訊息。 載入模組時，debug 程式庫會在登錄中尋找模組的記錄層級。 如果登錄機碼不存在，則偵錯工具程式庫會建立它們。

模組也可以在執行時間使用 [**DbgSetModuleLevel**](dbgsetmodulelevel.md) 函式來設定它自己的層級。 若要將訊息傳送至調試輸出，請呼叫 [**DbgLog**](dbglog.md) 宏。 下列範例會建立類型記錄追蹤的層級3訊息 \_ ：

您也可以使用下列登錄機碼來指定全域記錄層級：


```C++
\HKEY_LOCAL_MACHINE\<DebugRoot>\GLOBAL\<Message Type>
```



Debug 程式庫會使用較大的層級，也就是全域層級或模組層級。

**調試輸出位置**

偵錯工具輸出位置取決於另一個登錄機碼：

**HKEY \_本機 \_ 電腦** \\ **<DebugRoot>** \\ **<Modile Name>** \\ **LogToFile**

如果此索引鍵的值為 `Console` ，則輸出會移至主控台視窗。 如果值為 `Deb` 、 `Debug` 、 `Debugger` 或空字串，則輸出會移至偵錯工具視窗。 否則，輸出會寫入登錄機碼所指定的檔案。

在可執行檔使用 DirectShow debug 程式庫之前，必須先呼叫 [**DbgInitialise**](dbginitialise.md)函數。 之後，它必須呼叫 [**DbgTerminate**](dbgterminate.md) 函數。 Dll 不需要呼叫這些函式，因為在基類庫中 (定義 DLL 進入點) 會自動呼叫這些函式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[偵錯工具](debugging-utilities.md)
</dt> </dl>

 

 



