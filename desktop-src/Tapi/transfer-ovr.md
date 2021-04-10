---
description: 傳送作業可讓應用程式將目前連線的通訊會話傳送至不同的位址。
ms.assetid: b1027f09-74e1-4da8-b718-bb55a56dda1d
title: 傳送
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724b9ade43e41ab95a5baa6dfe7d3269f4e4a174
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026795"
---
# <a name="transfer"></a>傳送

傳送作業可讓應用程式將目前連線的通訊會話傳送至不同的位址。

TAPI 提供兩種機制，可將目前的會話傳送至不同的位址。 *密件轉移* 可讓現有的會話在一個階段傳送至指定的目的地位址。 *諮詢轉移* 除了要設定傳送的目前會話之外，還需要存在諮詢會話，然後完成轉移。 這兩種類型的選擇通常是以服務提供者的功能為基礎，因為有些服務提供者不支援盲目轉移。 在某些情況下，應用程式的需求可能會讓諮詢轉移成為慣用的方法，即使在可能的情況下，也可以進行轉換。

在 TAPI 2 和 TAPI 3 下，轉傳送作業基本上是相同的，但諮詢轉移的模式會稍有不同。

**TAPI 2.x：** 諮詢轉移一開始會叫用 [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer)，這會將現有的呼叫放置在諮詢上，並將此呼叫識別為下一個傳輸完成要求的目標。 **LineSetupTransfer** 函式也會配置諮詢通話，以用來與將傳送通話的合作物件建立諮詢通話。 應用程式可以使用 [**lineDial**](/windows/win32/api/tapi/nf-tapi-linedial)) ，在諮詢 (電話上撥接目的地合作物件的延伸模組，或者可以卸載和解除配置諮詢通話，並改為使用 [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold)) 啟用現有的保留呼叫 (（如果交換器支援的話）。 當初始呼叫是在諮詢上，且諮詢通話為作用中時，應用程式可以使用 [**lineSwapHold**](/windows/win32/api/tapi/nf-tapi-lineswaphold)在這些呼叫之間切換。

**TAPI 2.x：** 應用程式使用 [**lineCompleteTransfer**](/windows/win32/api/tapi/nf-tapi-linecompletetransfer)完成諮詢轉移。 這兩個呼叫都會還原為 *閒置* 狀態。

應用程式可以使用多個 Pbx 的「單一步驟傳輸」功能 (按下按鈕來建立諮詢轉移) ，方法是在呼叫 [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer)時，將 *lpCallParams* 參數設定為 [LINECALLPARAMFLAGS \_ 常數](./linecallparamflags--constants.md)的 **LINECALLPARAMFLAGS \_ ONESTEPTRANSFER** 成員。

**TAPI 3.x：** 諮詢轉移一開始會使用 [**ITAddress：： CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) 來建立新目的地位址的諮詢通話。 接著，會使用新的諮詢呼叫物件的指標作為參數，對原始呼叫物件呼叫 [**ITBasicCallControl：： Transfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-transfer) 。 在諮詢呼叫物件上呼叫 [**ITBasicCallControl：： Finish**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish) ，然後完成轉移。

應用程式必須在成功完成傳送作業之後釋放會話資源。

並非所有服務提供者都支援使用這項作業。

**TAPI 2.x：** 請參閱 [**lineBlindTransfer**](/windows/win32/api/tapi/nf-tapi-lineblindtransfer)、 [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer)、 [**lineCompleteTransfer**](/windows/win32/api/tapi/nf-tapi-linecompletetransfer)。

**TAPI 3.x：** 請參閱 [**ITBasicCallControl：： BlindTransfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-blindtransfer)、 [**ITAddress：： CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall)、 [**ITBasicCallControl：： Transfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-transfer)、 [**ITBasicCallControl：： Finish**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish)。

 

 
