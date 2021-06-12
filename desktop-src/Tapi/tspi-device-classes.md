---
description: 瞭解 TSPI 裝置類別。 裝置類別是應用程式用來傳送和接收呼叫資訊或資料的裝置或設備磁碟機群組。
ms.assetid: b29ea789-d017-4e35-b77a-c0d54ac54c66
title: TSPI 裝置類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6775e73df3914339edbdf791659de821855864dd
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011341"
---
# <a name="tspi-device-classes"></a>TSPI 裝置類別

*裝置類別* 是一組相關實體裝置或設備磁碟機，應用程式會透過這些裝置或設備磁碟機來傳送和接收發出呼叫的資訊或資料。 每個裝置類別都有一個可唯一識別類別的 *裝置類別名稱* ，並提供可用來開啟和與類別中的裝置通訊之程式設計介面和命令的相關資訊。

電話語音應用程式開發介面 (TAPI) 將裝置從一或多個裝置類別關聯到每一行或電話裝置。 您可以使用 [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid) 或 [**phoneGetID**](/windows/win32/api/tapi/nf-tapi-phonegetid) 函式來取得裝置的裝置識別碼，以存取其中一個裝置。 您會提供裝置類別名稱，而函式會傳回您開啟及存取裝置所需的特定埠名稱、裝置名稱、裝置控制碼或裝置識別碼。 傳回的資訊格式取決於裝置類別，如本節所述。

您也可以使用裝置類別名稱搭配 [**lineConfigDialog**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog) 和 [**phoneConfigDialog**](/windows/win32/api/tapi/nf-tapi-phoneconfigdialog) 函式，讓使用者能夠設定指定裝置的設定選項;使用 [**lineGetIcon**](/windows/win32/api/tapi/nf-tapi-linegeticon) 和 [**phoneGetIcon**](/windows/win32/api/tapi/nf-tapi-phonegeticon) 函式來取出圖示以代表指定的裝置;以及使用 [**lineGetDevConfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig) 和 [**lineSetDevConfig**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig) 函式，直接取得並設定指定裝置的設定選項。

以下是預設的裝置類別名稱。



| 裝置類別名稱                                       | Description                                      |
|---------------------------------------------------------|--------------------------------------------------|
| [通訊](/previous-versions/windows/desktop/legacy/ms725177(v=vs.85))                                       | 通訊埠                              |
| [通訊/datamodem](/previous-versions/windows/desktop/legacy/ms725178(v=vs.85))                   | 透過通訊埠的數據機              |
| [通訊/datamodem/portname](/previous-versions/windows/desktop/legacy/ms725179(v=vs.85)) | 數據機所連線的裝置名稱 |
| [wave/in](/previous-versions/windows/desktop/legacy/ms725990(v=vs.85))                                 | Wave 音訊裝置 (只輸入)                    |
| [wave/out](/previous-versions/windows/desktop/legacy/ms725992(v=vs.85))                               | Wave 音訊裝置 (只輸出)                   |
| [wave/in/out](/previous-versions/windows/desktop/legacy/ms725991(v=vs.85))                         | Wave 音訊裝置，全雙工                   |
| [midi/in](/previous-versions/windows/desktop/legacy/ms725244(v=vs.85))                                 | MIDI sequencer (僅輸入)                       |
| [midi/輸出](/previous-versions/windows/desktop/legacy/ms725245(v=vs.85))                               | 僅) 的 MIDI sequencer (輸出                     |
| [tapi/行](/previous-versions/windows/desktop/legacy/ms725511(v=vs.85))                             | 線路裝置                                      |
| [tapi/電話](/previous-versions/windows/desktop/legacy/ms725512(v=vs.85))                           | 手機裝置                                     |
| [Ndis](/previous-versions/windows/desktop/legacy/ms725247(v=vs.85))                                       | 網路裝置                                   |
| [tapi/終端機](/previous-versions/windows/desktop/legacy/ms725515(v=vs.85))                     | 終端機裝置                                  |



 

這些名稱不區分大小寫，因此您可以使用任何大小寫字母的組合。

給定的系統上可能會有其他裝置類別和裝置類別名稱。 一般情況下，如果裝置不屬於其中一個預設裝置類別，製造商通常會定義新的裝置類別，並指派唯一的裝置類別名稱。 您必須檢查裝置的檔，以判斷有哪些其他裝置類別可供使用。 不過請注意，雖然裝置類別和媒體類型都是相關的，但它們並不相同。 *媒體類型* 描述呼叫上的資訊格式，而 *裝置類別* 會定義用來管理該資訊的程式設計介面。 因此，即使製造商定義了新的媒體類型，製造商也必須定義新的裝置類別來支援模式。

搭配 [**lineSetDevConfig**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig) 和 [**lineGetDevConfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig) 函式使用的設定資料格式也取決於裝置類別。 一般而言，您會使用 **lineGetDevConfig** 來儲存目前裝置設定資料的複本，然後在稍後使用 **lineSetDevConfig** 搭配儲存的設定資料，將裝置設定還原為先前的狀態。 這是一種方便的方式，可暫時變更設定，而不需要使用者手動將其還原為先前的狀態。 由於裝置設定資料的確切格式可能與每個服務提供者不同，因此請勿使用 **lineSetDevConfig** 和 **lineGetDevConfig** 來直接操作裝置設定資料。 部分格式僅提供資訊。

 

 
