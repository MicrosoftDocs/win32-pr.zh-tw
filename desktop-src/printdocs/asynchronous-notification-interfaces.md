---
description: 下列介面可用於在列印多工緩衝處理器所裝載的應用程式和元件之間的非同步通訊，例如印表機驅動程式和埠監視器。
ms.assetid: e96c957f-3972-4afc-9d76-a4725b8688f8
title: 非同步列印通知介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7da8d320b33224e81852542e39f435b45b6dab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695012"
---
# <a name="asynchronous-printing-notification-interfaces"></a>非同步列印通知介面

下列介面可用於在列印多工緩衝處理器所裝載的應用程式和元件之間的非同步通訊，例如印表機驅動程式和埠監視器。

## <a name="in-this-section"></a>本節內容



| 介面                                                                     | 描述                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPrintAsyncNotifyCallback**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback)<br/>     | 建立及管理由列印多工緩衝處理器所裝載的應用程式和元件所使用的通道。<br/>                                                                                                                              |
| [**IPrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifychannel)<br/>       | 代表由「列印多工緩衝處理器」所裝載之元件用來將通知傳送至應用程式的通道。 如果通道是雙向的，應用程式可以使用相同的通道，將回應傳回至元件。<br/> |
| [**IPrintAsyncNotifyDataObject**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject)<br/> | 封裝通知通道中傳送的資料。 <br/>                                                                                                                                                                                             |



 

 

 




