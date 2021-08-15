---
description: 不再建議使用屬於 WMI 提供者架構一部分的 WMI c + + 類別。
ms.assetid: d2414a72-3435-4035-bcd9-b3ec87f5709c
ms.tgt_platform: multiple
title: 提供者架構公用程式類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 254a1321ab835c86e7b4bf0e5cb14048be0352290707a61aaf993a9a6cc6e8dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130980"
---
# <a name="provider-framework-utility-classes"></a>提供者架構公用程式類別

\[WMI c + + 類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會有任何進一步的開發、增強功能或更新可用於影響這些程式庫的非安全性相關問題。 [MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]

提供者 framework 程式庫 Framedyd.dll (debug 版本) 和 Framedyn.dll (發行版本) 實施數個提供者協助程式類別。 某些 Framedyn.dll 中的函式已從標頭檔中移除。 若要繼續使用這些函式，請 `#define FRAMEWORK_ALLOW_DEPRECATED` 先加入至您的程式碼，再加入 Fwcommon .h。

您可以卸載不再需要的個別提供者。

若要使用此功能，您必須對 MainDll 中的提供者進行下列三項變更：

-   在您呼叫 [**CWbemProviderGlue：： FrameworkLoginDLL**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogindll(lpcwstr_plong))的函數 **DllMain** 中，您必須新增第二個參數，也就是 long 的指標。
-   在呼叫 [**CWbemProviderGlue：： FrameworkLogoffDLL**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogoffdll(lpcwstr_plong))的函式 **DllCanUnloadNow** 中，您必須新增第二個參數，也就是 long 的指標。
-   在您建立 **CWbemGlueFactory** 實例的函式 **DllGetClassObject** 中，您必須加入一個指向 long 指標的參數。

在這三種情況下，long 的指標必須是相同的指標。

> [!Note]  
> 在 Maindll .cpp 中， **DllGetClassObject**、 **DllCanUnloadNow**、 **DllRegisterServer**、 **DllUnregisterServer** 和 **DllMain** 常式必須包裝在 try/catch 區塊中。

 

> [!Caution]  
> Framedyd.dll 的提供者 debug 與 Framedyd 程式庫連結。 Framedyd.dll 位於 \\ 不包含在系統路徑中的 Microsoft Windows 軟體開發套件 (SDK) bin 目錄。 當提供者的偵錯工具使用 Windows 管理服務進行測試時，架構提供者將無法載入，因為找不到 Framedyd.dll 或其中一個相依性。 因此，您必須將 Framedyd.dll 從 Windows SDK \\ bin 目錄複寫到 \\ system32 \\ wbem 目錄，或將 Windows SDK \\ bin 目錄新增至系統搜尋路徑。

 

下表列出提供者 framework 公用程式類別。



| 公用程式類別                                          | Description                                                                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**CHString**](chstring.md)                           | 提供 WMI 的字串比較和操作函數。                                                                  |
| [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray)                 | 包含用於建立及操作 CHString 的陣列。                                                                      |
| [**TRefPointerCollection**](/windows/desktop/api/RefPtrCo/nl-refptrco-trefpointercollection) | 針對指標授與容器類別的存取權。                                                                                |
| [**WBEMTime**](wbemtime.md)                           | 促進各種 Windows 和 ANSI C 執行時間時間格式之間的轉換。                                               |
| [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan)                   | 包含 helper 函式，用來計算和保存兩個 [**WBEMTime**](wbemtime.md) 物件之間的時間範圍差異。 |



 

> [!Note]  
> [**CHString**](chstring.md)和 [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray)類別類似于 (MFC) **CString** 和 **CStringArray** 的 Microsoft Foundation 類別。 WMI 版本存在，讓開發人員可以存取字串操作和比較方法，而不需要存取 MFC。 [**WBEMTime**](wbemtime.md)和 [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan)類別也類似于 MFC **CTime** 和 **CTimeSpan** 類別。 WMI 版本能夠儲存時間到毫微秒的精確度，也可以在 **BSTR** 之間轉換。 如需 CString、CStringArray、CTime 和 CTimeSpan 類別的詳細資訊，請參閱 MSDN 上的 [Microsoft Foundation 類別](https://msdn.microsoft.com/library/d06h2x6e(VS.71).aspx) 。

 

[**WBEMTime**](wbemtime.md)方法所傳回的 **BSTR** 值為 [日期和時間格式](date-and-time-format.md)： "yyyymmddhhmmss.ffffff. mmmmmmsUUU"

[**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan)方法所傳回的 **BSTR** 值採用 [間隔格式](interval-format.md)： "ddddddddHHMMSS. mmmmmm： 000"

雖然時間和時間範圍會在內部儲存為毫微秒，但不一定會以毫微秒精確度進行儲存。 這是因為 [**WBEMTime**](wbemtime.md) 物件可以使用精確至第二個 (**結構 tm** 和 **時間 \_ t**) 的時間格式來建立。 新增人工小數位數不會提高精確度。

 

 
