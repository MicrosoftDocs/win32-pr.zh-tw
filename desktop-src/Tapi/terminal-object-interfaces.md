---
description: 終端物件介面會提供應用程式存取權，以操作用來建立或接收媒體資料流程的裝置。
ms.assetid: 08320d1c-1400-4746-b526-74b0789c5fc0
title: 終端物件介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed3286d9a2bf3c247f813d3a1f942b0490de0154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695835"
---
# <a name="terminal-object-interfaces"></a>終端物件介面

[終端物件](terminal-object.md)介面會提供應用程式存取權，以操作用來建立或接收媒體資料流程的裝置。

這些介面是由 MSP 所執行，如果媒體服務提供者不支援位址，將無法使用這些介面。 如果有相關聯的 MSP 存在，則會在 [位址物件](address-object.md)上公開 [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)介面。

[**IEnumTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminal)和 [**IEnumTerminalClass**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass)介面不會直接在終端機物件上公開，但與其緊密相關，並在此處列出以供參考便利性。



| 介面                                                                  | 描述                                                                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)                                           | 終端物件的基底介面。 它會提供方法來取得資訊，例如支援終端機類別和媒體。 |
| [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat)                                 | 設定和取得 DirectShow 媒體格式。                                                                                            |
| [**ITBasicAudioTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasicaudioterminal)                       | 提供可設定及取得標準音頻終端機特性（例如 volume）的方法。                                          |
| [**IEnumTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminal)                                     | 列舉 [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)。                                                                                      |
| [**IEnumTerminalClass**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass)                           | 列舉 [**終端機類別**](terminal-class.md)。                                                                              |
| [**IEnumPluggableSuperclassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggablesuperclassinfo)       | 列舉 [**ITPluggableTerminalSuperclassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalsuperclassinfo)。                                        |
| [**IEnumPluggableTerminalClassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggableterminalclassinfo) | 列舉 [**ITPluggableTerminalClassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo)。                                                  |
| [**ITFileTrack**](/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack)                                         | 抓取和設定有關檔案終端機追蹤的資訊。                                                                   |
| [**ITASRTerminalEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itasrterminalevent)                           | 抓取自動語音辨識終端機事件的描述。                                                        |
| [**ITFileTerminalEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itfileterminalevent)                         | 抓取檔終端機事件的描述。                                                                                |
| [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal)                       | 列舉、建立或移除 multitrack 終端機上的追蹤。                                                                   |



 



| 介面                                                                                      | 描述                                                                                                                  |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**ITPluggableTerminalClassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo)                           | 抓取可插入終端機的相關資訊。                                                                       |
| [**ITPluggableTerminalClassRegistration**](/windows/desktop/api/Termmgr/nn-termmgr-itpluggableterminalclassregistration)           | 建立、修改或刪除插入式終端機的登錄專案。                                                   |
| [**ITPluggableTerminalInitialization**](/windows/desktop/api/Termmgr/nn-termmgr-itpluggableterminalinitialization)                 | 執行插入式終端機的主要終端物件建立，讓終端機管理員可以初始化終端機。 |
| [**ITPluggableTerminalSuperclassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalsuperclassinfo)                 | 抓取插入式終端機類別的名稱和 CLSID。                                                                  |
| [**ITPluggableTerminalSuperclassRegistration**](/windows/desktop/api/Termmgr/nn-termmgr-itpluggableterminalsuperclassregistration) | 抓取和設定終端超級類別 (名稱和 CLSID) 的相關資訊。                                                 |
| [**ITPluggableTerminalEventSink**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink)                           | 通知用戶端應用程式有關插入式終端機中的變更。                                                          |
| [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration)   | 註冊和取消註冊用戶端應用程式，以取得可插入終端機事件的通知。                             |



 



| 介面                                            | 描述                                                        |
|------------------------------------------------------|--------------------------------------------------------------------|
| [**ITTTSTerminalEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itttsterminalevent)     | 抓取文字轉換語音 (TTS) 終端機事件的描述。 |
| [**ITToneDetectionEvent**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittonedetectionevent) | 抓取語氣偵測事件的相關資訊。                |
| [**ITToneTerminalEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittoneterminalevent)   | 抓取語氣終端機事件的描述。                 |



 

 

 
