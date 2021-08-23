---
description: 裝置的媒體類型 (或模式) 描述可交換的資訊類型，例如互動式語音。 指定的裝置可能只能處理一種媒體類型，或者可以處理各種類型的類型。
ms.assetid: fccf85e9-3889-4ebc-b1bf-a60e27ab4586
title: 媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf79b97adb9df491aef1ff86be62fb838246c85a45b5ce251f5c0e88df5814f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002886"
---
# <a name="media-type"></a>媒體類型

裝置的 *媒體類型* (或模式) 描述可交換的資訊類型，例如互動式語音。 指定的裝置可能只能處理一種媒體類型，或者可以處理各種類型的類型。

服務提供者會公開所控制裝置所支援的媒體類型或類型。 應用程式會查詢媒體類型，然後使用此資訊來選取適當的位址以起始會話。 所提供之會話的應用程式回應可能也會在媒體類型上前提。

指定的通訊會話或呼叫可能牽涉到數種媒體類型。 如需詳細資訊，請參閱會話的媒體類型。

**TAPI 2.x：** 請參閱 *lpAddressCaps*、 [LINEMEDIAMODE \_ 常數](./linemediamode--constants.md)所指向之 [**LINEADDRESSCAPS**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps)結構的 **dwAvailableMediaModes** 成員 [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps)。

**TAPI 3.x：** 請參閱 [**ITTerminal：： get \_ 媒體**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype)， [TAPIMEDIATYPE \_ 常數](tapimediatype--constants.md)。
