---
description: 事件通知是應用程式從 TAPI 和服務提供者取得資訊的主要方式。
ms.assetid: 02160f10-dc3f-484c-9cd3-bcfb07ded822
title: 事件通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63aa232b0e712a76442c298ea04e24ec7671cb4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969353"
---
# <a name="event-notification"></a>事件通知

事件通知是應用程式從 TAPI 和服務提供者取得資訊的主要方式。 這項資訊可能是應用程式所啟動之非同步作業的狀態，或可能涉及在應用程式外部啟動的進程，例如新的連入呼叫的通知。

**TAPI 2.x：** 應用程式會以下列三種方式之一來處理通知：隱藏視窗、事件控制碼或完成埠。 如需這些通知機制的詳細資訊，請參閱 [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa)的備註一節。 應用程式會在呼叫 [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa)之前設定 [**LINEINITIALIZEEXPARAMS**](/windows/win32/api/tapi/ns-tapi-lineinitializeexparams)結構的 **>dwoptions** 成員，藉以指定機制。

[**LineSetStatusMessages**](/windows/win32/api/tapi/nf-tapi-linesetstatusmessages)函式可讓應用程式指定要接收的通知訊息，以取得與指定行或其任何位址的狀態變更相關的事件。

**TAPI 3.x：** 應用程式會使用 COM 標準可連接 [物件](../com/events-in-com-and-connectable-objects.md)來處理一般通知。 [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) 是必須向 tapi 的容器物件註冊的輸出介面，而 [**ITTAPIEventNotification：： Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) 是 TAPI 呼叫來判斷應用程式回應的方法。 [**ITTAPI：:p \_ >eventfilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter)方法會告知 TAPI 哪些事件對應用程式感興趣。 如果未輸入事件篩選器，應用程式將不會收到任何事件的通知。 [**ITTAPI：： RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications)方法會告知 TAPI 應用程式將處理傳入會話的媒體類型和位址。 如需 TAPI 3 事件處理的詳細資訊，請參閱 [事件](events.md) 總覽或 [註冊事件](register-events.md) 程式碼範例。

電話語音服務提供者會執行 [**TSPI \_ LineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) 和 [**TSPI \_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)。 TAPI 會呼叫這些函式，以指出應用程式所要求的所有線路、位址和媒體類型事件的集合。

 

 
