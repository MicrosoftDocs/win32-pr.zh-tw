---
description: TAPI 3.1 新增了詳細的電話裝置控制項和一些專門的終端介面。 下表列出新的介面。
ms.assetid: 71f87258-f8e1-466b-802e-a5ae22b38974
title: " (電話語音 API) 的新功能"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3abbc758d9fdf1560a9187a4a258b15801794b0d2917dcd84e6a03f1e510719a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011838"
---
# <a name="whats-new-telephony-api"></a> (電話語音 API) 的新功能

TAPI 3.1 新增了詳細的電話裝置控制項和一些專門的終端介面。 下表列出新的介面。



| nbbnInterface                                                                                  | 描述                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone)                                                               | 提供 [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone) 介面的列舉方法。                                                                                                                                       |
| [**IEnumPluggableSuperclassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggablesuperclassinfo)                           | 提供 [**ITPluggableTerminalSuperclassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalsuperclassinfo) 介面的列舉方法。                                                                                   |
| [**IEnumPluggableTerminalClassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggableterminalclassinfo)                     | 提供 [**ITPluggableTerminalClassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo) 介面的列舉方法。                                                                                             |
| [**ITASRTerminalEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itasrterminalevent)                                               | 抓取自動語音辨識終端機事件的描述。                                                                                                                                       |
| [**ITAddress2**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress2)                                                               | 提供支援電話裝置之 Address 物件的其他方法;衍生自 [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress) 介面。                                                                         |
| [**ITAutomatedPhoneControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol)                                     | 執行數個高階電話相關功能，包括啟用和設定電話語音和環形的自動控制，以及根據手機 hookswitch 狀態的自動通話處理。          |
| [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2)                                             | 藉由提供方法，讓您在呼叫上選取終端機，以擴充 [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) 介面。                                                                                    |
| [**ITCallInfo2**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo2)                                                             | 藉由提供方法，以每個呼叫為基礎來設定事件篩選，來擴充 [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) 介面。                                                                                          |
| [**ITCollection2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itcollection2)                                                         | 藉由提供修改集合的其他方法來擴充 [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) 介面。                                                                                         |
| [**ITCustomTone**](/windows/desktop/api/Tapi3if/nn-tapi3if-itcustomtone)                                                           | 提供的方法可讓您更深入地控制某些電話組可能的自訂音調。                                                                                                                |
| [**ITDetectTone**](/windows/desktop/api/Tapi3if/nn-tapi3if-itdetecttone)                                                           | 提供的方法可讓應用程式指定給 TAPI 伺服器的語音和語氣特性，使伺服器產生語氣事件。                                                      |
| [**ITDigitsGatheredEvent**](/windows/desktop/api/Tapi3if/nn-tapi3if-itdigitsgatheredevent)                                         | 提供方法來取得與應用程式之數位收集要求相關的資料。                                                                                                                           |
| [**ITFileTerminalEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itfileterminalevent)                                             | 抓取檔終端機事件的描述。                                                                                                                                                               |
| [**ITFileTrack**](/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack)                                                             | 抓取和設定有關檔案終端機追蹤的資訊。                                                                                                                                                  |
| [**ITLegacyAddressMediaControl2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itlegacyaddressmediacontrol2)                           | 藉由提供其他方法來擴充 [**ITLegacyAddressMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol) 介面，以允許設定與線路裝置相關的參數。                     |
| [**ITLegacyCallMediaControl2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itlegacycallmediacontrol2)                                 | 藉由提供用於語氣偵測和產生的額外方法，擴充 [**ITLegacyCallMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol) 介面。                                                            |
| [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol)                                                       | 啟動、停止和暫停目前的動作，例如播放。                                                                                                                                                   |
| [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback)                                                     | 提供播放特定的方法，讓應用程式能夠設定和取得要播放的檔案清單。                                                                                                           |
| [**ITMediaRecord**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord)                                                         | 提供記錄特有的方法，可讓應用程式設定和取得要記錄之檔案的名稱。                                                                                                       |
| [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal)                                           | 列舉、建立或移除 multitrack 終端機上的追蹤。                                                                                                                                                  |
| [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone)                                                                     | 允許存取電話裝置，其層級可與 TAPI 2 所提供的相同。*x* C API。                                                                                                             |
| [**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent)                                                           | 抓取電話事件的描述。                                                                                                                                                                       |
| [**ITPluggableTerminalClassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo)                           | 抓取可插入終端機的相關資訊。                                                                                                                                                           |
| [**ITPluggableTerminalClassRegistration**](/windows/desktop/api/Termmgr/nn-termmgr-itpluggableterminalclassregistration)           | 建立、修改或刪除插入式終端機的登錄專案。                                                                                                                                       |
| [**ITPluggableTerminalEventSink**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink)                           | 通知用戶端應用程式有關插入式終端機中的變更。                                                                                                                                              |
| [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration)   | 註冊和取消註冊用戶端應用程式，以取得可插入終端機事件的通知。                                                                                                                 |
| [**ITPluggableTerminalInitialization**](/windows/desktop/api/Termmgr/nn-termmgr-itpluggableterminalinitialization)                 | 執行插入式終端機的主要終端物件建立，讓終端機管理員可以初始化終端機。                                                                                     |
| [**ITPluggableTerminalSuperclassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalsuperclassinfo)                 | 抓取插入式終端機類別的名稱和 CLSID。                                                                                                                                                      |
| [**ITPluggableTerminalSuperclassRegistration**](/windows/desktop/api/Termmgr/nn-termmgr-itpluggableterminalsuperclassregistration) | 抓取和設定終端超級類別 (名稱和 CLSID) 的相關資訊。                                                                                                                                     |
| [**ITScriptableAudioFormat**](/windows/desktop/api/tapi3if/nn-tapi3if-itscriptableaudioformat)                                     | 從取出音訊格式，或設定播放軌的音訊格式。                                                                                                                                          |
| [**ITStaticAudioTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itstaticaudioterminal)                                         | 提供支援電話裝置所需之靜態音訊終端機物件的方法。 TAPI 3.1 Msp 必須在所有靜態音訊終端機上公開這個介面。                                              |
| [**ITTAPI2**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi2)                                                                     | 提供 TAPI 物件上的其他方法來支援電話裝置;衍生自 [**ITTAPI**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi) 介面。                                                                                    |
| [**ITTAPIObjectEvent2**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent2)                                               | 擴充 [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent) 介面;提供方法，此方法會傳回造成 TAPI 物件事件之 phone 物件上 [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone) 介面的指標。 |
| [**ITTTSTerminalEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itttsterminalevent)                                               | 抓取文字轉換語音 (TTS) 終端機事件的描述。                                                                                                                                               |
| [**ITTerminalManager2**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalmanager2)                                               | 抓取目前系統中已註冊之插入式終端機類別的相關資訊;衍生自 [**ITTerminalManager**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalmanager) 介面。                                              |
| [**ITTerminalSupport2**](/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport2)                                               | 抓取可插入的終端機類別和超類的相關資訊;衍生自 [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) 介面。                                                              |
| [**ITToneDetectionEvent**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittonedetectionevent)                                           | 抓取語氣偵測事件的相關資訊。                                                                                                                                                              |
| [**ITToneTerminalEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittoneterminalevent)                                             | 抓取語氣終端機事件的描述。                                                                                                                                                               |



 

 

 
