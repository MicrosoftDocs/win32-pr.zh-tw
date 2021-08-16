---
description: Wave/in 裝置類別包含適用于低層級 wave 音訊輸入的音訊裝置。
ms.assetid: b2f32019-088f-4805-af7e-559a8179b1e6
title: wave/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24cc80d41f402abf1886e063563f272abf7992768dd62f03e64b327a7e199360
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002526"
---
# <a name="wavein"></a>wave/in

Wave/in 裝置類別包含適用于低層級 wave 音訊輸入的音訊裝置。 您可以使用 (SDK) 平臺軟體發展工具組中所述的 wave 功能來存取這些裝置。 此類別中的裝置會與支援 LINEMEDIAMODE AUTOMATEDVOICE 媒體類型的線路裝置相關聯 \_ ，該媒體類型是線上路裝置之 [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)結構的 **dwMediaModes** 成員中指定的。

[**LineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)和 [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)函式會填滿 [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring)結構、將 **dwStringFormat** 成員設定為 STRINGFORMAT \_ 二進位值，並附加這個額外的成員：

``` syntax
DWORD DeviceId;  // identifier of audio device
```

**DeviceId** 成員是封閉式音訊裝置的識別碼。 在 [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) 函式的呼叫中，您可以使用此識別碼來開啟裝置以進行輸入。 您可以使用產生的裝置控制碼來記錄線路或電話裝置的數位化音訊資料。

雖然低層級 wave 音訊裝置也有「wave」裝置類別，但您應該一律針對低層級 wave 輸入使用 wave/in 裝置類別。

如需 wave 函數的詳細資訊，請參閱 [**多媒體功能**](../multimedia/multimedia-functions.md)。

 

 
