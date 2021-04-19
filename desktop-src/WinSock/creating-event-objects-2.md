---
description: Ws2 \_32.dll 會為應用程式和服務提供者提供事件物件建立的功能，不過在大部分的情況下，應用程式會建立事件物件。
ms.assetid: 86da30ad-80bc-4982-9306-bbe29b1bab19
title: 建立事件物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bec202f8f17790ed85979a8287005aa65374a244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970170"
---
# <a name="creating-event-objects"></a>建立事件物件

Ws2 \_32.dll 會為應用程式和服務提供者提供事件物件建立的功能，不過在大部分的情況下，應用程式會建立事件物件。 事件物件服務可透過 [**WPUCreateEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreateevent) 提供給 Windows 通訊端服務提供者，就像是任何可能受益于任何內部處理的便利機制。 請注意，事件物件控制碼只在呼叫進程的內容中有效。 在 Windows 環境中，事件物件的實現是透過作業系統所提供的原生事件服務。

 

 



