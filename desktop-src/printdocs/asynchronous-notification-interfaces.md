---
description: 瞭解在列印多工緩衝處理器所裝載的應用程式和元件之間的非同步通訊中所使用的介面。
ms.assetid: e96c957f-3972-4afc-9d76-a4725b8688f8
title: 非同步列印通知介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfe0de2cf8510b1bb039907067b62fce08a4145
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396093"
---
# <a name="asynchronous-printing-notification-interfaces"></a>非同步列印通知介面

下列介面可用於在列印多工緩衝處理器所裝載的應用程式和元件之間的非同步通訊，例如印表機驅動程式和埠監視器。

## <a name="in-this-section"></a>本節內容



| 介面                                                                     | 描述                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPrintAsyncNotifyCallback**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback)<br/>     | 建立及管理由列印多工緩衝處理器所裝載的應用程式和元件所使用的通道。<br/>                                                                                                                              |
| [**IPrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifychannel)<br/>       | 代表由「列印多工緩衝處理器」所裝載之元件用來將通知傳送至應用程式的通道。 如果通道是雙向的，應用程式可以使用相同的通道，將回應傳回至元件。<br/> |
| [**IPrintAsyncNotifyDataObject**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject)<br/> | 封裝通知通道中傳送的資料。 <br/>                                                                                                                                                                                             |



 

 

 




