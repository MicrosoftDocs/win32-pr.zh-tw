---
description: 媒體服務提供者介面 (MSPI) 是一組由 MSP 所執行的介面和方法，可在通訊會話期間，讓 TAPI 3 應用程式能控制媒體傳輸。
ms.assetid: 53b7bcbd-571a-44da-a6db-10d4c3e5d30a
title: '媒體服務提供者介面 (MSPI) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b99f78d62c0784e38ede7a4019eef40cf8a48cf9480a4326c5d7b7129ca971
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073008"
---
# <a name="media-service-provider-interface-mspi"></a>媒體服務提供者介面 (MSPI) 

媒體服務提供者介面 (MSPI) 是一組由 MSP 所執行的介面和方法，可在通訊會話期間，讓 TAPI 3 應用程式能控制媒體傳輸。 MSP 會處理制定這些控制項所需的裝置特定和通訊協定特定機制，並透過使用 MSPI 中提供的方法，與其配對的 TSP 或應用程式進行通訊。

下一節 ( [媒體服務提供者介面 (MSPI) 參考](media-service-provider-interface-mspi-reference.md)) 詳述 MSP 公開的介面，以便與 Microsoft 電話語音環境互動。

此外，MSP 可能會公開提供者專屬的私用介面和方法，以進一步協助媒體控制項。 例如， [IP 會議 MSP](ipconf-msp.md) 會公開提供參與者控制項的介面。 請參閱 [提供者特定介面](provider-specific-interfaces.md) ，以取得私用物件如何運作的資訊，以及 [IPConf MSP 介面](ipconf-msp-interfaces.md) 以取得 IPConf 的參考清單。

建立 MSP 的大部分程式設計工作，對指定的平臺、裝置和傳輸通訊協定而言都是高度專屬的，而且不在本檔的範圍內。 不過，Microsoft 會提供一組 MSP 基類，這對大多數 MSP 作者很有用。 如需使用這些類別的詳細資訊，請參閱 [TAPI 3 MSP 基類](tapi-3-msp-base-classes.md) 。

[**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)介面代表 TAPI DLL 的媒體服務提供者。 此介面不會由或公開給使用者應用程式。 TAPI 3 DLL 會呼叫此介面上的 **CoCreateInstance** 來建立主要 MSP 物件。 此物件上的方法可讓應用程式載入和卸載 MSP、接收 TSP 的資訊，以及建立 [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) 介面，此介面會在呼叫物件上公開。

[**ITSubStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol)和 [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)介面提供與子串流相關的平行方法。 子流支援是選擇性的。 所有其他介面都必須由 MSP 來執行。

> [!Note]  
> TSP/MSP 組所實行的作業必須位於一個 DLL 中，才能讓使用者更新服務提供者，而不需要重新開機其系統。

 

 

 
