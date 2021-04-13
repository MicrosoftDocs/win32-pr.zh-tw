---
description: 在 TAPI 架構中，所有 Tsp 都是在 TAPISRV 的內容中執行，這會在 SVCHOST 中實作為服務進程。
ms.assetid: f47662f9-2fca-4044-ab26-617e5b1f9eae
title: MSP 架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8c1229ddce90f79c122c47572b4567d230b0b4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386062"
---
# <a name="msp-architecture"></a>MSP 架構

在 TAPI 架構中，所有 Tsp 都是在 TAPISRV 的內容中執行，這會在 SVCHOST 中實作為服務進程。 TAPI 應用程式會在自己的進程中存留。 TAPI 應用程式會將 Tapi3.dll 以及任何所需的 Msp 載入其本身的進程，而 TAPI DLL 會透過私用 RPC 介面與 TAPISRV 通訊。 下圖說明這些元件的互動。

![tapisrv、tapi 應用程式與 msp 之間的互動](images/tsp-msp1.png)

 (MSP 的媒體服務提供者) 使用終端機、串流和子串流的抽象概念來提供媒體串流處理。

終端機是媒體串流的接收或來源。 它可能是實體物件，例如喇叭或麥克風，也可能是裝置的抽象類別，例如影片視窗。 [Terminal 物件](terminal-object.md)會公開 [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)介面。 終端機 [**類別**](terminal-class.md) GUID 描述終端機類別。 MSP 可能會定義自己的終端機類別。

資料流程會根據媒體 [**類型**](tapimediatype--constants.md) 或類型、資料流程的 [**方向**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction)和媒體的目的地位址來分割通話的媒體。 例如，來自數據機的連入音訊串流是串流物件、連至 IP 位址的輸出影片串流，以及埠是資料流程物件，來自 IP 多播群組的影片串流也會被視為一個資料流程物件。 資料流程物件是以 [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) 介面表示。

子串流可讓您更精確地控制媒體。 例如，在 IP 多播案例中，內送的影片資料流程物件可能代表數個人員。 應用程式很可能會希望每個參與者都有個別的轉譯器。 傳入的影片串流可以分成數個子串流，每個人一個。 一個子串流會對應到一個人，並且可以個別設定和控制。 子流物件是以 [**ITSubStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol) 介面表示。

當應用程式呼叫 [**ITAddress：： CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) 來設定呼叫時，必須指定所需的媒體類型。 在撥打電話時，它只會在呼叫建立時告訴 TAPI。 例如：

``` syntax
HRESULT hr = pAddress->CreateCall( 
       pszDestAddress, 
       lAddressType, 
       TAPIMEDIATYPE_AUDIO | TAPIMEDIATYPE_VIDEO, 
       &pCall 
       ); 
// If (hr != S_OK ) process the error here
```

在此情況下，應用程式會建立外寄音訊視頻通話。

傳入的媒體類型表示應用程式在呼叫的存留期內有興趣的媒體。 例如，應用程式可能會在建立通話時指定音訊和影片，但一開始只選取音訊端子。 MSP 只會開始串流音訊，但不會拒絕稍後在呼叫的存留期內進行的本機或遠端影片要求。

當應用程式接著呼叫 [**ITBasicCallControl：： Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect)時，TAPI 3 會呼叫 TSP 中的 [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) 。 在建立通話之後，MSP 和 TSP 可以視需要進行通訊。

當通話中斷時，就會由 MSP 和 TSP 來傳達中斷通話的相關資訊。 如果應用程式呼叫 [**中斷連接**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect)，Tapi3.dll 會呼叫 [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) 。

 

 
