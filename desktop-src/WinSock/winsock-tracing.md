---
description: Winsock 追蹤
ms.assetid: 0c430fc2-28e7-4537-a887-4c36d24fedee
title: Winsock 追蹤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803be6220d4d2d440811033786b0f043fab0ff9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991997"
---
# <a name="winsock-tracing"></a>Winsock 追蹤

## <a name="introduction"></a>簡介

Winsock 追蹤是一項疑難排解功能，可以在零售二進位檔中啟用，以追蹤某些 Windows 通訊端事件的額外負荷。 將零售追蹤新增至 Windows 通訊端的目標是要讓開發人員和產品支援提供更佳的診斷功能。 Winsock 網路事件追蹤支援 IPv4 和 IPv6 應用程式的追蹤通訊端作業。 Winsock 目錄變更追蹤支援追蹤對 Winsock 類別目錄所做的變更， (Lsp) 的分層服務提供者。 Windows Vista 和更新版本支援 Winsock 追蹤。

> [!Note]  
> 已淘汰分層服務提供者。 從 Windows 8 和 Windows Server 2012 開始，請使用 [Windows 篩選平台](../fwp/windows-filtering-platform-start-page.md)。

 

當通訊端發生未預期的錯誤時，診斷問題的主要線索就是傳回的錯誤碼。 傳回的錯誤碼通常不會解釋發生錯誤的原因，特別是當基礎網路傳輸起始錯誤時。 Winsock 追蹤提供更詳細的追蹤層級，可記錄其他資訊來攔截緩衝區損毀和寫入不良的應用程式。

Winsock 追蹤會使用 Windows 的事件追蹤 (ETW) 是作業系統所提供的一般用途高速追蹤功能。 ETW 使用在核心中實作為緩衝和記錄機制，為使用者模式應用程式與核心模式設備磁碟機所引發的事件提供追蹤機制。 此外，ETW 還可讓您以動態方式啟用和停用記錄，讓您輕鬆地在生產環境中執行詳細追蹤，而不需要重新開機或重新開機應用程式。 記錄機制會使用由非同步寫入器執行緒寫入磁片的緩衝區。 這可讓大型伺服器應用程式以最少的干擾來寫入事件。 ETW 首次在 Windows 2000 上引進。 Windows Vista 和更新版本已新增使用 ETW 進行 Winsock 追蹤的支援。 如需 ETW 的一般資訊，請參閱 [使用 Etw 改善偵錯工具和效能微調](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)。

您只能針對在電腦上執行的所有進程和執行緒，在作業系統層級啟用 Winsock 追蹤。 目前只能針對單一進程或執行緒啟用 Winsock 追蹤。 啟用 Winsock 網路事件追蹤時，會追蹤電腦上 (IPv4 和 IPv6) 的所有通訊端應用程式。

下列主題會更詳細地說明 Winsock 追蹤：

-   [Winsock 追蹤層級](winsock-tracing-levels.md)
-   [Winsock 追蹤的控制權](control-of-winsock-tracing.md)
-   [Winsock 網路事件追蹤詳細資料](winsock-tracing-event-details.md)
-   [Winsock 目錄變更追蹤詳細資料](winsock-layered-service-provider-tracing-event-details.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 ETW 改善偵錯和效能調整](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> <dt>

[Debug 和 Trace 設備](debug-and-trace-facilities-2.md)
</dt> </dl>

 

 
