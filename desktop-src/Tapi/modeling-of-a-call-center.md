---
description: 服務提供者可以將 PBX 上的每個資源公開為線路裝置，以及可能的關聯電話裝置。
ms.assetid: 25394b19-bf75-4adc-b07d-41bc781931b6
title: 撥打電話中心的模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2763a1baafa41cf2d9b3b9b3c9d13be675a02d83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386064"
---
# <a name="modeling-of-a-call-center"></a>撥打電話中心的模型

服務提供者可以將 PBX 上的每個資源公開為線路裝置，以及可能的關聯電話裝置。 支援多個呼叫外觀的終端機會透過多個位址來執行，就像第一方的呼叫控制一樣。 事實上，裝置的協力廠商觀點等同于第一方的觀點;伺服器上的應用程式可以查看及控制所有第一方的裝置，而連接到伺服器的個別用戶端電腦只能透過伺服器上的 TAPISRV 所管理的存取控制，來查看可看見的裝置。 終端機以外的資源也可以模型化為線路裝置。 例如，ACD 佇列或路由點會模型化為可能具有許多使用中呼叫的線路裝置;IVR 伺服器、語音郵件伺服器或一組預測撥號埠也可以模型化為支援多個呼叫的線路裝置。

在此模型中，您可以透過現有的 TAPI 訊息（例如 [**行 \_ LINEDEVSTATE**](line-linedevstate.md)、 [**行 \_ ADDRESSSTATE**](line-addressstate.md)、 [**行 \_ CALLSTATE**](line-callstate.md)和 [**行 \_ CALLINFO**](line-callinfo.md)），以及透過 [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)、 [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)、 [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)和 [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)等函式取得的詳細資料，來監視定址裝置的狀態和與其相關聯的呼叫。 只要透過伺服器上執行的協力廠商應用程式來操作 TAPI 物件，結果就會與該裝置相關聯的用戶端電腦上執行的第一方應用程式同樣操作時，所發生的結果相同。 由伺服器服務提供者所傳送的狀態指標，可控制切換網狀架構 (或切換) 會傳遞給在伺服器上執行的應用程式，以及在相關聯的授權用戶端上執行的應用程式。

 

 



