---
description: 新服務提供者的安裝是高度裝置和作業系統專用的，因此詳細資料不在此 SDK 範圍內。
ms.assetid: 5b48e144-5092-4462-b74c-d3295d23afe1
title: 安裝和初始化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b15dc5d9d93ce33ac13a04aec3abd7d49fec3ed2ece3cce691d47c0d617bacd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003536"
---
# <a name="installation-and-initialization"></a>安裝和初始化

新服務提供者的安裝是高度裝置和作業系統專用的，因此詳細資料不在此 SDK 範圍內。 一般來說，安裝的目標是針對目前的通訊環境設定服務提供者。 這通常牽涉到登錄專案和服務相依性的設定。

電話語音服務提供者的初始化是從版本協商開始。 如需版本協商和目前版本的討論，請參閱 [TSPI 版本控制](tspi-versioning.md) 。

然後，TAPI 會呼叫 [**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)，它會將指標傳遞至用來報告非同步函式進度的回呼函數。 TSP 會傳回與目前裝置識別碼相關聯的線路與電話裝置計數。

一般而言，下一個步驟將是由 TAPI 叫用 [**TSPI \_ LineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) 和 [**TSPI \_ lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)所進行的資源清查。 服務提供者預期會填入相關的資料結構元素，這些元素與它所支援的裝置和會話功能有關。

TAPI 會從各種應用程式收集有關事件通知需求的資訊，並使用 [**TSPI \_ LINESETDEFAULTMEDIADETECTION**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) 指示 TSP 來指出要偵測哪些媒體類型和 [**TSPI \_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages) ，以指出應該報告哪個行和位址事件。

 

 
