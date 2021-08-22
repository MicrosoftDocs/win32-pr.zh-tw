---
description: 本節說明 IMM 功能。
ms.assetid: 833c07eb-0ecf-41e2-9e01-8d83e51ffcef
title: 輸入方法管理員函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c0f03c2e6d29b262bd97729b92f9eea5fbf99d09f52ea3fe2b3579646a6fa8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948723"
---
# <a name="input-method-manager-functions"></a>輸入方法管理員函數

本節說明 IMM 功能。



| 函式                                                           | 描述                                                                                                                |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**CreateIFECommonInstance**](/windows/desktop/api/msime/nf-msime-createifecommoninstance)         | 傳回 [**IFECommon**](/windows/desktop/api/Msime/nn-msime-ifecommon) 介面的指標。                                                          |
| [**CreateIFEDictionaryInstance**](/windows/desktop/api/msime/nf-msime-createifedictionaryinstance) | 傳回 [**IFEDictionary**](/windows/desktop/api/Msime/nn-msime-ifedictionary) 介面的指標。                                                  |
| [**CreateIFELanguageInstance**](/windows/desktop/api/msime/nf-msime-createifelanguageinstance)     | 傳回 [**IFELanguage**](/windows/desktop/api/Msime/nn-msime-ifelanguage) 介面的指標。                                                      |
| [**EnumInputCoNtext**](/windows/desktop/api/Imm/nc-imm-imcenumproc)                       | 應用程式定義的回呼函式，可處理 **ImmEnumInputCoNtext** 函數所提供的輸入內容。   |
| [**EnumRegisterWordProc**](/windows/desktop/api/Imm/nc-imm-registerwordenumproca)               | 搭配 **ImmEnumRegisterWord** 函式使用的應用程式定義回呼函數。                                   |
| [**ImmAssociateCoNtext**](/windows/desktop/api/Imm/nf-imm-immassociatecontext)                 | 將指定的輸入內容與指定的視窗產生關聯。                                                          |
| [**ImmAssociateCoNtextEx**](/windows/desktop/api/Imm/nf-imm-immassociatecontextex)             | 變更輸入方法內容與指定視窗或其子系之間的關聯。                         |
| [**ImmConfigureIME**](/windows/desktop/api/Imm/nf-imm-immconfigureimea)                         | 顯示指定輸入地區設定識別碼之 IME 的設定對話方塊。                                |
| [**ImmCreateCoNtext**](/windows/desktop/api/Imm/nf-imm-immcreatecontext)                       | 建立新的輸入內容、為內容配置記憶體，並將其初始化。                                        |
| [**ImmDestroyCoNtext**](/windows/desktop/api/Imm/nf-imm-immdestroycontext)                     | 釋放輸入內容並釋出相關聯的記憶體。                                                                    |
| [**ImmDisableIME**](/windows/desktop/api/Imm/nf-imm-immdisableime)                             | 停用執行緒或進程中所有線程的 IME。                                                             |
| [**ImmDisableLegacyIME**](/windows/desktop/api/Imm/nf-imm-immdisablelegacyime)                 | 指出這個執行緒是 Windows 存放區應用程式 UI 執行緒。                                                               |
| [**ImmDisableTextFrameService**](/windows/desktop/api/Imm/nf-imm-immdisabletextframeservice)   | 已取代。 停用指定之執行緒的文字服務。                                                            |
| [**ImmEnumInputCoNtext**](/windows/desktop/api/Imm/nf-imm-immenuminputcontext)                 | 抓取指定之執行緒的輸入內容。                                                                      |
| [**ImmEnumRegisterWord**](/windows/desktop/api/Imm/nf-imm-immenumregisterworda)                 | 列舉具有指定的讀取字串、樣式和暫存器字串的暫存器字串。                           |
| [**ImmEscape**](/windows/desktop/api/Imm/nf-imm-immescapea)                                     | 存取特定 Ime 的功能，這些功能無法透過其他輸入法 API 函式使用。                           |
| [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)                 | 抓取候選清單。                                                                                                |
| [**ImmGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta)       | 捕獲候選清單的大小。                                                                                 |
| [**ImmGetCandidateWindow**](/windows/desktop/api/Imm/nf-imm-immgetcandidatewindow)             | 抓取候選視窗的相關資訊。                                                                         |
| [**ImmGetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta)             | 抓取目前用來顯示組合視窗字元的邏輯字型相關資訊。               |
| [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa)         | 抓取組合字元串的相關資訊。                                                                        |
| [**ImmGetCompositionWindow**](/windows/desktop/api/Imm/nf-imm-immgetcompositionwindow)         | 抓取組合視窗的相關資訊。                                                                        |
| [**ImmGetCoNtext**](/windows/desktop/api/Imm/nf-imm-immgetcontext)                             | 抓取與指定視窗相關聯的輸入內容。                                                          |
| [**ImmGetConversionList**](/windows/desktop/api/Imm/nf-imm-immgetconversionlista)               | 抓取字元或單字的轉換結果清單，而不產生任何輸入法相關的訊息。                   |
| [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)           | 抓取目前的轉換狀態。                                                                                   |
| [**ImmGetDefaultIMEWnd**](/windows/desktop/api/Imm/nf-imm-immgetdefaultimewnd)                 | 抓取 IME 類別的預設視窗控制碼。                                                                      |
| [**ImmGetDescription**](/windows/desktop/api/Imm/nf-imm-immgetdescriptiona)                     | 將 IME 的描述複製到指定的緩衝區。                                                                 |
| [**ImmGetGuideLine**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea)                         | 捕獲錯誤的相關資訊。                                                                                        |
| [**ImmGetIMEFileName**](/windows/desktop/api/Imm/nf-imm-immgetimefilenamea)                     | 抓取與指定之輸入地區設定相關聯的輸入法檔案名。                                             |
| [**ImmGetImeMenuItems**](/windows/desktop/api/Imm/nf-imm-immgetimemenuitemsa)                   | 抓取在指定輸入內容的 IME 功能表中註冊的功能表項目。                                 |
| [**ImmGetOpenStatus**](/windows/desktop/api/Imm/nf-imm-immgetopenstatus)                       | 判斷 IME 是否為開啟或關閉。                                                                              |
| [**ImmGetProperty**](/windows/desktop/api/Imm/nf-imm-immgetproperty)                           | 抓取與指定輸入地區設定相關聯之 IME 的屬性和功能。                             |
| [**ImmGetRegisterWordStyle**](/windows/desktop/api/Imm/nf-imm-immgetregisterwordstylea)         | 抓取與指定之輸入地區設定相關聯的 IME 所支援的樣式清單。                            |
| [**ImmGetStatusWindowPos**](/windows/desktop/api/Imm/nf-imm-immgetstatuswindowpos)             | 抓取狀態視窗的位置。                                                                               |
| [**ImmGetVirtualKey**](/windows/desktop/api/Imm/nf-imm-immgetvirtualkey)                       | 抓取與 IME 已處理之索引鍵輸入訊息相關聯的原始虛擬機器碼值。           |
| [**ImmInstallIME**](/windows/desktop/api/Imm/nf-imm-imminstallimea)                             | 安裝 IME。                                                                                                           |
| [**ImmIsIME**](/windows/desktop/api/Imm/nf-imm-immisime)                                       | 判斷指定的輸入地區設定是否具有 IME。                                                                       |
| [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)                           | 檢查是否有適用于 IME 視窗的訊息，並將這些訊息傳送至指定的視窗。                          |
| [**ImmNotifyIME**](/windows/desktop/api/Imm/nf-imm-immnotifyime)                               | 通知輸入輸入內容的狀態變更。                                                         |
| [**ImmRegisterWord**](/windows/desktop/api/Imm/nf-imm-immregisterworda)                         | 使用與指定之輸入地區設定相關聯的 IME 字典來註冊字串。                              |
| [**ImmReleaseCoNtext**](/windows/desktop/api/Imm/nf-imm-immreleasecontext)                     | 釋放輸入內容，並解除鎖定輸入內容中相關聯的記憶體。                                         |
| [**ImmRequestMessage**](/windows/desktop/api/Immdev/nf-immdev-immrequestmessagea)                     | 從應用程式要求訊息。                                                                                   |
| [**ImmSetCandidateWindow**](/windows/desktop/api/Imm/nf-imm-immsetcandidatewindow)             | 設定候選視窗的相關資訊。                                                                              |
| [**ImmSetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immsetcompositionfonta)             | 設定要用來顯示撰寫視窗字元的邏輯字型。                                              |
| [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa)         | 設定撰寫和讀取字串的字元、屬性和子句。                                       |
| [**ImmSetCompositionWindow**](/windows/desktop/api/Imm/nf-imm-immsetcompositionwindow)         | 設定組合視窗的位置。                                                                               |
| [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus)           | 設定目前的轉換狀態。                                                                                        |
| [**ImmSetOpenStatus**](/windows/desktop/api/Imm/nf-imm-immsetopenstatus)                       | 開啟或關閉 IME。                                                                                                   |
| [**ImmSetStatusWindowPos**](/windows/desktop/api/Imm/nf-imm-immsetstatuswindowpos)             | 設定狀態視窗的位置。                                                                                    |
| [**ImmSimulateHotKey**](/windows/desktop/api/Imm/nf-imm-immsimulatehotkey)                     | 模擬指定的輸入法熱鍵，使與使用者按下指定視窗中的熱鍵時相同的回應。 |
| [**ImmUnregisterWord**](/windows/desktop/api/Imm/nf-imm-immunregisterworda)                     | 從與指定輸入地區設定相關聯的 IME 字典中移除暫存器字串。                       |



 

 

 



