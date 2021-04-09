---
description: 大部分的 get 和 set 作業只會處理某一元件的資訊。 PhoneGetStatus 函式會將電話裝置的完整狀態資訊傳回給應用程式。
ms.assetid: ca38396c-6f97-4c1c-99fb-2bd64c74c626
title: " (電話語音 API) 的狀態"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a9a93fdd97d32b477545ba0fb9f73f10b45021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849231"
---
# <a name="status-telephony-api"></a> (電話語音 API) 的狀態

大部分的 get 和 set 作業只會處理某一元件的資訊。 [**PhoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)函式會將電話裝置的完整狀態資訊傳回給應用程式。

如先前所述，每當手機裝置上的狀態專案變更時，就會將 [**電話 \_ 狀態**](phone-state.md) 消息傳送至應用程式功能。 此訊息的參數包括電話裝置的控制碼，以及已變更狀態專案的指示。

應用程式可以使用 [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) 來選取要通知的特定狀態變更。 同樣地， [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) 會傳回應用程式想要收到通知的狀態變更。

 

 



