---
description: 終端使用者或伺服器應用層級的裝置控制需要一組相當小的基本資訊。
ms.assetid: 9c787656-93ef-4e0b-9516-8822ae49a83a
title: '裝置控制 (電話語音 API) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f67b33cb03b5a4ac84309bd9c463a9d73e1ebfb8bf51deb4189585f9e1ec3752
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118867400"
---
# <a name="device-control-telephony-api"></a>裝置控制 (電話語音 API) 

終端使用者或伺服器應用層級的裝置控制需要一組相當小的基本資訊。 服務提供者抽象層會執行詳細的裝置控制項。 服務提供者會透過 TAPI 向應用程式報告所需的裝置資訊。

主要裝置類別包括：

-   [網路](network-ovr.md)：通訊的傳輸層。 從應用程式的觀點來看，網路的相關資訊通常內嵌于網址類別型，例如 LINEADDRESSTYPE \_ PHONENUMBER。
-   [Line](line-ovr.md)：與網路的連接。 此概念大量用於 TAPI 2.2 (TAPI/C) 內。
-   [Channel](channel-ovr.md)：線條的細分。 應用程式通常不需要使用通道的知識，因為服務提供者會設定其顯示為位址的方式。
-   [位址](address-ovr.md)：網路上的網路位置。 每一行或通道都有一個或多個相關聯的位址。 此位址是 TAPI 3.1 (TAPI/COM) 和 TAPI 2.2 (TAPI/C) 的主要概念。
-   [終端](terminal-ovr.md)機：特定位址和媒體類型的來源或轉譯器。

服務提供者會將裝置特性回報給 TAPI，以回應應用程式查詢。 服務提供者也會起始裝置狀態變更的報告。 然後，系統會根據初始化期間要求的通知，將這些變更回報給應用程式。

基本裝置特性為：

-   [Device 類別](device-class-ovr.md)
-   [裝置識別碼](device-identifier-ovr.md)
-   [網址類別型](address-type-ovr.md)
-   [位址識別碼](address-identifier-ovr.md)
-   [裝置事件](device-events-ovr.md)
-   [媒體類型](media-type-ovr.md)
-   [終端機類型](terminal-type-ovr.md)

此外，服務提供者會提供有關特定位址的容量資訊，以執行各種會話作業。

如果服務提供者支援，補充特性可能會與特定裝置產生關聯。 TAPI 2.x 應用程式會使用 [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) 和 [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) 功能來探索功能。 TAPI 3.x 應用程式會針對此用途使用 [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) 介面。

TAPI 2.x 提供一組特殊的補充作業，服務提供者可能會執行這些作業，以與手機裝置搭配使用。 請參閱[電話裝置](./opening-and-closing-phone-devices.md)。

擴充功能是提供者專屬的，而且不會直接由 Microsoft 電話語音 API 所涵蓋。 請參閱[擴充的行](./extended-line-functions.md)函式、擴充的[電話語音電話](./extended-telephony-phone-functions.md)函[式或提供者特定的介面](provider-specific-interfaces.md)。

以下是 TAPI 作業的摘要，可查詢裝置特性上的服務提供者，並提供目前狀態的資料。



| TAPI 2.x 函數                                                  | 描述                                                                                                    |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)                   | 查詢指定的線路裝置，以判斷相關位址的電話語音功能。               |
| [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps)           | 查詢指定的線路裝置，以判斷特定位址的電話語音功能。                   |
| [**lineGetDevConfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig)               | 傳回「不透明」的資料結構，此結構會儲存裝置目前的設定。                          |
| [**lineSetDevConfig**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig)               | 還原裝置設定。                                                                                 |
| [**lineConfigDialog**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog)               | 顯示對話方塊，讓使用者能夠設定與裝置相關的參數。                       |
| [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid)                             | 抓取可用於進一步 TAPI 函式呼叫或使用不同 API 的穩定裝置識別碼。 |
| [**lineGetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus)       | 查詢裝置的目前狀態，例如使用中通話的數目。                                             |
| [**lineSetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linesetlinedevstatus)       | 設定裝置狀態，例如將裝置設定為不在服務中。                                                |
| [**lineGetIcon**](/windows/win32/api/tapi/nf-tapi-linegeticon)                         | 抓取要顯示給使用者的提供者特定圖示。                                                      |
| [**lineNegotiateExtVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateextversion) | 允許應用程式與指定的線路裝置協調使用延伸模組版本。                 |
| [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific)                 | 提供裝置特定功能的存取權。                                                                      |
| [**lineDevSpecificFeature**](/windows/win32/api/tapi/nf-tapi-linedevspecificfeature)   | 將裝置特有的功能傳送給服務提供者。                                                        |



 



| TAPI 3.x 介面或方法                                   | 描述                                                                                             |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities)           | 取得位址功能的相關資訊。                                                  |
| [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat)                       | 設定並取得 DirectShow™媒體格式。                                                                 |
| [**ITBasicAudioTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasicaudioterminal)             | 設定並取得標準音頻終端機特性，例如 volume。                                  |
| [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)                         | 取得位址媒體支援功能的相關資訊。                                    |
| [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)                                 | 終端物件的基底介面。 取得支援終端機類別和媒體等資訊。 |
| [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)                   | 取得可用終端機的相關資訊，並建立額外的終端機。                               |
| [提供者特定的介面](provider-specific-interfaces.md) | 服務提供者相依。                                                                             |



 

 

 
