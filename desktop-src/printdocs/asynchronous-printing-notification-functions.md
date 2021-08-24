---
description: 瞭解在列印多工緩衝處理器所裝載的應用程式和元件之間的非同步通訊中使用的函式。
ms.assetid: 7e98e63f-616c-4cd1-a8aa-482d27529b8c
title: 非同步列印通知函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d533ad1a3d1a8201e5a2d91946a66daee6cecd796e7bcc8e9c14d2c593542c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720238"
---
# <a name="asynchronous-printing-notification-functions"></a>非同步列印通知函式

下列函式用於在列印多工緩衝處理器（例如印表機驅動程式和埠監視器）所裝載的應用程式和元件之間的非同步通訊。

## <a name="in-this-section"></a>本節內容



| 函式                                                                                        | 描述                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreatePrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel)<br/>               | 在列印多工緩衝處理器裝載的列印元件（如列印驅動程式或埠監視器）與從元件接收通知的應用程式之間建立通道。<br/> |
| [**RegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications)<br/>     | 可讓應用程式從列印多工緩衝處理器裝載的列印元件（如印表機驅動程式、列印處理器和埠監視器）註冊通知。<br/>                              |
| [**UnRegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications)<br/> | 啟用已註冊的應用程式，以接收來自列印多工緩衝處理器之列印元件的通知，以取消註冊。<br/>                                                              |



 

 

 




