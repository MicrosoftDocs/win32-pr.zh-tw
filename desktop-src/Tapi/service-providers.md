---
description: 服務提供者會執行詳細的電話語音裝置控制項。 電話語音服務提供者 (TSP) 提供呼叫控制和媒體服務提供者（如果有的話）提供媒體資料流程的控制權。
ms.assetid: eb63d55e-4a2b-4bc0-8001-99772f418d72
title: 服務提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba0bc427b79daadc8dc89e49a29e18ebbd9797bed74da7f890dc851d6ee97b13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773118"
---
# <a name="service-providers"></a>服務提供者

服務提供者會執行詳細的電話語音裝置控制項。 電話語音服務提供者 (TSP) 提供呼叫控制和媒體服務提供者（如果有的話）提供媒體資料流程的控制權。

所有電話語音服務提供者會在 TAPISRV 程式中執行。 服務提供者可以視需要在 TAPISRV 內容中建立執行緒，以執行其工作，並確信任何個別應用程式的結束都不會終結其所建立的任何資源。 TAPI 伺服器會視需要將應用程式命令轉譯為一組一致的命令，稱為電話語音服務提供者介面 (TSPI) 。

媒體服務提供者會在應用程式的進程空間中執行，讓媒體控制項有時候需要快速回應。 TAPI DLL 提供一致的遵循媒體服務提供者介面 (MSPI) 。

如需服務提供者的詳細資訊，請參閱 [TAPI 服務提供者總覽](./tapi-service-provider-overview.md)。

在電話語音服務提供者 DLL 底下，服務提供者可以使用任何系統函數或其他必要元件。 這些函式包含 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 和 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)，可搭配獨立硬體廠商設計的核心模式元件和服務，以及標準裝置（例如串列和平行埠）來控制外部、本機連接的裝置。 它們也可以存取 (的網路服務，例如 RPC、Windows 通訊端，以及用戶端/伺服器電話語音) 的具名管道。

TAPI 會將電話語音服務提供者的使用者介面 DLL 載入至應用程式的程式，此應用程式會叫用可顯示對話方塊 (的任何服務提供者函式，例如 [**TSPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog)) 。 如果服務提供者需要在非預期的時間顯示 UI，服務提供者也會在應用程式的進程中載入和執行其相關聯的 UI DLL。例如，若要顯示通用數據機驅動程式所顯示的 [ **交談]/[掛斷** ] 對話方塊 (UNIMODEM) 當使用 [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) 來撥打互動式語音通話時， (通常不會被視為 UI 產生的函數) 。

Proxy 要求處理常式是一種完整的電話語音應用程式，通常會在電話語音伺服器上執行， (與電話語音服務提供者針對相關線路裝置) 執行的同一部伺服器。 此架構（而不是 WOSA 服務提供者架構）是在應用程式中比伺服器上的驅動程式更適當地執行特定服務時使用。 例如，ACD 代理程式管理函數是在 proxy 要求處理常式中執行，而不是在服務提供者中。

數據機的 UNIMODEM 驅動程式服務提供者可在 Windows Server 2003 作業系統、Windows XP、Windows 2000 和 Windows NT 上取得。 Windows電話語音也包含一般核心模式的電話語音服務提供者介面 (TSPI) 對應程式（KMDDSP），可讓服務提供者實作為核心模式設備磁碟機。

 

 
