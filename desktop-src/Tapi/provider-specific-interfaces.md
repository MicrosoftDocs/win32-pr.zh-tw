---
description: TAPI 3 支援將服務提供者專屬的介面整合至標準物件，讓應用程式能夠利用提供者特有的功能。
ms.assetid: 8077c9a7-3235-41a7-97dc-ca5f3c291ee6
title: Provider-Specific 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f95499f005c8c3b3e854f33835b9c9b183416d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027276"
---
# <a name="provider-specific-interfaces"></a>Provider-Specific 介面

TAPI 3 支援將服務提供者專屬的介面整合至標準物件，讓應用程式能夠利用提供者特有的功能。 此外，TAPI 3 還可讓服務提供者將廠商專屬的事件傳遞至應用程式，使其成為應用程式接收標準事件的相同介面上的 COM 物件。

TAPI 藉由使用標準物件（TAPI、位址、終端機、呼叫和 CallHub）來匯總提供者特定物件，並將未知的方法分派或委派給這些提供者特定的物件，以達成這項整合。

例如，服務提供者可能會允許應用程式取得除了 [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) 介面所公開之呼叫的相關資訊。 廠商必須定義介面，讓應用程式能夠進行這些額外的查詢，並在物件上執行該介面。 此物件也會執行廠商資訊查詢介面，讓應用程式可以探索哪些提供者特定的函式可供使用。

當應用程式取得呼叫物件的參考時，應用程式可以使用新的提供者特定介面和其方法，就像它們是由呼叫物件本身來執行一樣。

請參閱 [媒體服務提供者介面 (MSPI) 參考](media-service-provider-interface-mspi-reference.md) ，取得所有標準 MSP 介面的清單。

如需 IPConf MSP 專屬的所有介面清單，請參閱 [IPCONF Msp 介面](ipconf-msp-interfaces.md) 。

 

 



