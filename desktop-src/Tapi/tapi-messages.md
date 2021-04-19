---
description: 訊息是用來通知應用程式非同步事件。 所有這些訊息都會透過應用程式在 lineInitializeEx 中指定的訊息通知機制傳送至應用程式。
ms.assetid: d302819e-c522-470a-be5e-52625c9223a4
title: TAPI 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58307a0230b76c6ad98c57f4590098f0dcf6b236
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980588"
---
# <a name="tapi-messages"></a>TAPI 訊息

訊息是用來通知應用程式非同步事件。 所有這些訊息都會透過應用程式在 [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)中指定的訊息通知機制傳送至應用程式。

訊息一律包含相關物件的控制碼 (phone、line 或 call) ，應用程式可以使用此控制碼來判斷訊息類型。

某些訊息是用來通知應用程式有關物件狀態的變更。 這些訊息會提供物件控制碼，並指出已變更的狀態專案。 應用程式可以呼叫物件的適當「取得狀態」功能，以取得物件的完整狀態。

當事件發生時，可以將訊息傳送至零個、一個或多個應用程式。 訊息的目標應用程式取決於許多不同的因素，包括訊息的意義、應用程式對物件的許可權、應用程式是否起始訊息為直接結果的要求，以及已由應用程式設定的訊息遮罩。 請注意下列有關訊息的要點：

-   非同步回復訊息只會傳送到發出要求的應用程式，而且無法遮罩。
-   發出數位或語氣產生或數位收集的訊息，只會傳送到要求數位或語氣產生的應用程式。
-   指出行或位址狀態變更的訊息會傳送至已開啟該行的所有應用程式，只要訊息已透過 [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)啟用即可。
-   指出撥號狀態和呼叫資訊變更的訊息會傳送至所有具有呼叫控制碼的應用程式。
-   表示數位偵測、語氣偵測或媒體類型偵測的訊息會傳送給要求監視該事件的應用程式。

本節包含下列 TAPI 訊息的參考資訊：

-   [輔助電話語音訊息](assisted-telephony-messages.md)
-   [撥打電話中心訊息](call-center-messages.md)
-   [格式化的錯誤訊息](formatted-error-messages.md)
-   [線路裝置訊息](line-device-messages.md)
-   [手機裝置訊息](phone-device-messages.md)

 

 



