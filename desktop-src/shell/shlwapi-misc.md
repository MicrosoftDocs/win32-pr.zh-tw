---
description: 本節描述 Shlwapi.dll 所匯出的 Windows Shell 函式，並在不屬於其他公用程式函式類別的 Shlwapi 和 Shlwapi 中定義。
title: Shell 其他公用程式函式
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 11787717-6370-408d-9a86-e208b33521c7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 87c4d7c585ce9a6cbae1702d4c49da3dcea5a0a465d32d8a6221d6c5783114ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709398"
---
# <a name="shell-miscellaneous-utility-functions"></a>Shell 其他公用程式函式

本節描述 Shlwapi.dll 所匯出的 Windows Shell 函式，並在不屬於其他公用程式函式類別的 Shlwapi 和 Shlwapi 中定義。

## <a name="in-this-section"></a>本節內容



| 主題                                                                   | 描述                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DllInstall**](/windows/desktop/api/Shlwapi/nf-shlwapi-dllinstall)<br/>                             | 處理 DLL 的安裝和設定。<br/>                                                                                                                                                                                                                             |
| [**GetProcessReference**](/windows/desktop/api/Shlwapi/nf-shlwapi-getprocessreference)<br/>           | 抓取 [**SetProcessReference**](/windows/desktop/api/Shlwapi/nf-shlwapi-setprocessreference)所提供的進程特定物件，遞增參考計數以使進程保持運作。<br/>                                                                                                     |
| [**HashData**](/windows/desktop/api/Shlwapi/nf-shlwapi-hashdata)<br/>                                 | 雜湊資料的陣列。<br/>                                                                                                                                                                                                                                              |
| [**IsInternetESCEnabled**](/windows/desktop/api/Shlwapi/nf-shlwapi-isinternetescenabled)<br/>         | 判斷 Windows Internet Explorer 是否位於增強式安全性設定中。<br/>                                                                                                                                                                               |
| [**Iso**](/windows/desktop/api/Shlwapi/nf-shlwapi-isos)<br/>                                         | 檢查指定的作業系統和作業系統功能。<br/>                                                                                                                                                                                                 |
| [**IStream \_ 複製**](/windows/desktop/api/Shlwapi/nf-shlwapi-istream_copy)<br/>                        | 將資料流程複製到另一個資料流程。<br/>                                                                                                                                                                                                                                    |
| [**IStream \_ 讀取**](/windows/desktop/api/Shlwapi/nf-shlwapi-istream_read)<br/>                        | 從指定的資料流程讀取位元組，並傳回值，這個值表示是否已成功讀取所有的位元組。<br/>                                                                                                                                                      |
| [**IStream \_ ReadPidl**](/windows/desktop/api/Shlwapi/nf-shlwapi-istream_readpidl)<br/>                | 讀取專案識別碼清單的指標， (從 [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) 物件將) PIDL 至 PIDLIST 的 \_ 相對物件。<br/>                                                                                                                                          |
| [**IStream \_ ReadStr**](/windows/desktop/api/Shlwapi/nf-shlwapi-istream_readstr)<br/>                  | 從資料流程讀取並寫入字串。<br/>                                                                                                                                                                                                                         |
| [**IStream \_ 重設**](/windows/desktop/api/Shlwapi/nf-shlwapi-istream_reset)<br/>                      | 將指定資料流程中的搜尋位置移至資料流程的開頭。<br/>                                                                                                                                                                                         |
| [**IStream \_ 大小**](/windows/desktop/api/Shlwapi/nf-shlwapi-istream_size)<br/>                        | 抓取指定資料流程的大小（以位元組為單位）。<br/>                                                                                                                                                                                                                  |
| [**IStream \_ 寫入**](/windows/desktop/api/Shlwapi/nf-shlwapi-istream_write)<br/>                      | 將未知格式的資料從緩衝區寫入至指定的資料流程。<br/>                                                                                                                                                                                                    |
| [**IStream \_ WritePidl**](/windows/desktop/api/Shlwapi/nf-shlwapi-istream_writepidl)<br/>              | 將 PIDL 從 PCUIDLIST 的 \_ 相對物件寫入 [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) 物件中。<br/>                                                                                                                                                                            |
| [**IStream \_ WriteStr**](/windows/desktop/api/Shlwapi/nf-shlwapi-istream_writestr)<br/>                | 從字串讀取並寫入資料流程。<br/>                                                                                                                                                                                                                         |
| [**IUnknown \_ AtomicRelease**](/windows/desktop/api/Shlwapi/nf-shlwapi-iunknown_atomicrelease)<br/>    | 釋放元件物件模型 (COM) 指標，並將它設定為 **Null**。<br/>                                                                                                                                                                                              |
| [**IUnknown \_ GetSite**](/windows/desktop/api/Shlwapi/nf-shlwapi-iunknown_getsite)<br/>                | 呼叫指定之物件的 [**IObjectWithSite：： GetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-getsite) 方法。<br/>                                                                                                                                                                      |
| [**IUnknown \_ GetWindow**](/windows/desktop/api/Shlwapi/nf-shlwapi-iunknown_getwindow)<br/>            | 藉由查詢具有 **GetWindow** 方法的各種介面，嘗試從 COM 物件中取出視窗控制碼。<br/>                                                                                                                                           |
| [**IUnknown \_ QueryService**](/windows/desktop/api/Shlwapi/nf-shlwapi-iunknown_queryservice)<br/>      | 從指定的物件中，抓取服務的介面。<br/>                                                                                                                                                                                                         |
| [**IUnknown \_ 設定**](/windows/desktop/api/Shlwapi/nf-shlwapi-iunknown_set)<br/>                        | 變更 COM 介面指標的值，並釋放先前的介面。<br/>                                                                                                                                                                                     |
| [**IUnknown \_ SetSite**](/windows/desktop/api/Shlwapi/nf-shlwapi-iunknown_setsite)<br/>                | 藉由呼叫 [**IObjectWithSite：： SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) 方法來設定指定物件的網站。<br/>                                                                                                                                                   |
| [**ParseURL**](/windows/desktop/api/Shlwapi/nf-shlwapi-parseurla)<br/>                                 | 執行 URL 的基本剖析。<br/>                                                                                                                                                                                                                                |
| [**QISearch**](/windows/desktop/api/Shlwapi/nf-shlwapi-qisearch)<br/>                                 | [**IUnknown：： QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))方法的資料表驅動實作為。<br/>                                                                                                                                                              |
| [**SetProcessReference**](/windows/desktop/api/Shlwapi/nf-shlwapi-setprocessreference)<br/>           | 提供 COM 物件，可允許裝載的 Shell 擴充和其他元件，以防止其主機進程提前關閉。 主機進程通常是 Windows 檔案總管或 Internet Explorer，但其他應用程式也可以使用此函數。<br/> |
| [**SHAutoComplete**](/windows/win32/api/shlwapi/nf-shlwapi-shautocomplete)<br/>                   | 指示系統編輯控制項使用自動完成功能，以協助完成 Url 或檔案系統路徑。<br/>                                                                                                                                                                        |
| [**SHCreateMemStream**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatememstream)<br/>               | 使用與 [**CreateStreamOnHGlobal**](/windows/win32/api/combaseapi/nf-combaseapi-createstreamonhglobal)類似的進程來建立記憶體資料流程。<br/>                                                                                                                                                            |
| [**SHCreateStreamOnFileEx**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatestreamonfileex)<br/>     | 開啟或建立檔案，並抓取資料流程以讀取或寫入該檔案。<br/>                                                                                                                                                                                         |
| [**SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread)<br/>                     | 建立執行緒。<br/>                                                                                                                                                                                                                                                     |
| [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref)<br/>               | 建立 COM 物件的每個執行緒參考。<br/>                                                                                                                                                                                                                       |
| [**SHCreateThreadWithHandle**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadwithhandle)<br/> | 建立新的執行緒，並抓取其控制碼。<br/>                                                                                                                                                                                                                        |
| [**SHGetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref)<br/>                     | 抓取 [**SHSetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetthreadref)所設定的每個執行緒物件參考。<br/>                                                                                                                                                                            |
| [**SHGlobalCounterDecrement**](/windows/desktop/api/Shlwapi/nf-shlwapi-shglobalcounterdecrement)<br/> | 遞減全域計數器。<br/>                                                                                                                                                                                                                                          |
| [**SHGlobalCounterGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shglobalcountergetvalue)<br/>   | 取得全域計數器的目前值。<br/>                                                                                                                                                                                                                           |
| [**SHGlobalCounterIncrement**](/windows/desktop/api/Shlwapi/nf-shlwapi-shglobalcounterincrement)<br/> | 遞增全域計數器。<br/>                                                                                                                                                                                                                                          |
| [**SHIsLowMemoryMachine**](/windows/desktop/api/shlwapi/nf-shlwapi-shislowmemorymachine)<br/>         |                                                                                                                                                                                                                                                                                  |
| [**SHReleaseThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreleasethreadref)<br/>             | 線上程程式傳回之前釋放執行緒參考。<br/>                                                                                                                                                                                                      |
| [**SHSetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetthreadref)<br/>                     | 將每個執行緒的參考儲存至 COM 物件。 這可讓呼叫者控制執行緒的存留期，以確保在呼叫端就緒之前，Windows 不會關閉執行緒。<br/>                                                                      |



 

 

 
