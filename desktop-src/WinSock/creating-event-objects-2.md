---
description: Ws2 \_32.dll 會為應用程式和服務提供者提供事件物件建立的功能，不過在大部分的情況下，應用程式會建立事件物件。
ms.assetid: 86da30ad-80bc-4982-9306-bbe29b1bab19
title: 建立事件物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab867e6398db4b5c97303c8739431d7baaca311daf8d103f4375721e96a864b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051696"
---
# <a name="creating-event-objects"></a>建立事件物件

Ws2 \_32.dll 會為應用程式和服務提供者提供事件物件建立的功能，不過在大部分的情況下，應用程式會建立事件物件。 事件物件服務可透過 [**WPUCreateEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreateevent)提供給 Windows 通訊端服務提供者，就像是任何可能受益于任何內部處理的便利機制。 請注意，事件物件控制碼只在呼叫進程的內容中有效。 在 Windows 環境中，事件物件的實現是透過作業系統所提供的原生事件服務。

 

 



