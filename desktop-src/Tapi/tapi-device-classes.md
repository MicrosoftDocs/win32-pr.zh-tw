---
description: 深入瞭解 TAPI 裝置類別。 裝置類別是應用程式用來傳送和接收呼叫資訊或資料的裝置或設備磁碟機群組。
ms.assetid: 859979a8-0d16-4b7b-b183-d6e30f3e034d
title: TAPI 裝置類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c16f5baf81bdc66d5110da2a1ac5127237738e
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011361"
---
# <a name="tapi-device-classes"></a>TAPI 裝置類別

裝置類別是一組相關實體裝置或設備磁碟機，應用程式會透過這些裝置或設備磁碟機來傳送和接收發出呼叫的資訊或資料。 每個裝置類別都有一個可唯一識別類別的 *裝置類別名稱* ，並提供可用來開啟和與類別中的裝置通訊之程式設計介面和命令的相關資訊。

電話語音應用程式開發介面 (TAPI) 將裝置從一或多個裝置類別關聯到每一行或電話裝置。 您可以使用 [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) 或 [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) 函式來取得裝置的裝置識別碼，以存取其中一個裝置。 您會提供裝置類別名稱，而函式會傳回您開啟及存取裝置所需的特定埠名稱、裝置名稱、裝置控制碼或裝置識別碼。 傳回的資訊格式取決於裝置類別，並將在本節的後續主題中說明。

您也可以使用裝置類別名稱搭配 [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) 和 [**phoneConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-phoneconfigdialog) 函式，讓使用者能夠設定指定裝置的設定選項，並使用 [**lineGetIcon**](/windows/desktop/api/Tapi/nf-tapi-linegeticon) 和 [**phoneGetIcon**](/windows/desktop/api/Tapi/nf-tapi-phonegeticon) 函式來抓取圖示來代表指定的裝置，以及使用 [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) 和 [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) 函式來直接取出並設定指定裝置的設定選項。

下列清單顯示裝置類別名稱。



| 裝置類別名稱                                      | Description                                       |
|--------------------------------------------------------|---------------------------------------------------|
| [通訊](comm.md)                                       | 通訊埠。                              |
| [通訊/datamodem](comm-datamodem.md)                   | 透過通訊埠的數據機。              |
| [通訊/datamodem/portname](comm-datamodem-portname.md) | 數據機所連接的裝置名稱。 |
| [wave/in](wave-in.md)                                 | Wave 音訊裝置 (只輸入) 。                   |
| [wave/out](wave-out.md)                               | Wave 音訊裝置 (只輸出) 。                  |
| [wave/in/out](wave-in-out.md)                         | Wave 音訊裝置，全雙工。                   |
| [midi/in](midi-in.md)                                 | MIDI sequencer (只輸入) 。                      |
| [midi/輸出](midi-out.md)                               | 只有)  (才會輸出 MIDI sequencer。                     |
| [tapi/行](tapi-line.md)                             | 線路裝置。                                      |
| [tapi/電話](tapi-phone.md)                           | 電話裝置。                                     |
| [Ndis](ndis.md)                                       | 網路裝置。                                   |
| [tapi/終端機](tapi-terminal.md)                     | 終端機裝置。                                  |



 

> [!Note]  
> 這些名稱不區分大小寫;您可以使用任何大小寫字母的組合。

 

給定的系統上可能會有其他裝置類別和裝置類別名稱。 一般情況下，如果裝置不屬於其中一個預設裝置類別，製造商通常會定義新的裝置類別，並指派唯一的裝置類別名稱。 檢查裝置的檔，以判斷有哪些其他裝置類別可供使用。 不過請注意，雖然裝置類別和媒體類型都是相關的，但它們並不相同。 媒體類型會描述呼叫資訊格式，而裝置類別會定義用來管理該資訊的程式設計介面。 因此，即使製造商定義了新的媒體類型，製造商也不一定需要定義新的裝置類別來支援模式。

搭配 [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) 和 [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) 函式使用的設定資料格式也取決於裝置類別。 一般而言，您會使用 **lineGetDevConfig** 來儲存目前裝置設定資料的複本，然後在稍後使用 **lineSetDevConfig** 搭配儲存的設定資料，將裝置設定還原為先前的狀態。 這是一種方便的方式，可暫時變更設定，而不需要使用者手動將其還原為先前的狀態。 由於裝置設定資料的確切格式可能與每個服務提供者不同，因此您不應該使用 **lineSetDevConfig** 和 **lineGetDevConfig** 來直接操作裝置設定資料。 部分格式僅提供資訊。

 

 



