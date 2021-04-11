---
description: 下列函式會搭配多語系消費者介面 (MUI) 使用。
ms.assetid: 918d1f04-78fe-4b60-bee7-08d2f131437e
title: 多語系消費者介面函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f082115b0b12bdf6d26923ed8fc941b89887723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114189"
---
# <a name="multilingual-user-interface-functions"></a>多語系消費者介面函式

下列函式會搭配多語系消費者介面 (MUI) 使用。



| 函式                                                                 | 描述                                                                                                             |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**EnumUILanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa)                               | 列舉作業系統上可用的使用者介面語言。                                     |
| [**EnumUILanguagesProc**](/windows/win32/api/winnls/nc-winnls-uilanguage_enumproca)                       | 搭配 [**EnumUILanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa) 函數使用的應用程式定義函數。                      |
| [**FreeMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary)                                 | 減少 LoadMUILibrary 所載入之資源模組的參考計數[ ](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya)                  |
| [**GetFileMUIInfo**](/windows/desktop/api/Winnls/nf-winnls-getfilemuiinfo)                                 | 抓取與檔案相關的資源相關資訊。                                                                    |
| [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)                                 | 抓取與所提供之 LN 檔案相關聯之特定語言資源檔的路徑。                           |
| [**GetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getprocesspreferreduilanguages) | 抓取處理常式慣用的 UI 語言。                                                                           |
| [**GetSystemDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultuilanguage)         | 抓取系統預設 UI 語言的語言識別項，在 Windows Vista 上稱為「安裝語言」。 |
| [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages)   | 捕獲系統慣用的 UI 語言。                                                                            |
| [**GetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getthreadpreferreduilanguages)   | 抓取目前線程的執行緒慣用 UI 語言。                                                     |
| [**GetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getthreaduilanguage)                       | 傳回目前線程之第一個使用者介面語言的語言識別項。                            |
| [**GetUILanguageFallbackList**](/windows/desktop/api/Muiload/nf-muiload-getuilanguagefallbacklist)           | 取得以語言名稱表示的使用者介面語言的 fallback 清單。                                         |
| [**GetUILanguageInfo**](/windows/desktop/api/Winnls/nf-winnls-getuilanguageinfo)                           | 抓取有關使用者介面語言的各種資訊。                                                     |
| [**GetUserDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultuilanguage)             | 傳回目前使用者之使用者 UI 語言的語言識別項。                                          |
| [**GetUserPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages)       | 抓取使用者慣用的 UI 語言。                                                                              |
| [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya)                                 | 傳回與特定語言中性 (LN) 檔相關聯之語言特定資源的控制碼。            |
| [**SetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages) | 設定應用程式處理常式慣用的 UI 語言。                                                    |
| [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)   | 設定執行緒慣用的 UI 語言。                                                                                 |
| [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage)                       | 設定目前線程的慣用使用者介面語言。                                                      |



 

 

 
