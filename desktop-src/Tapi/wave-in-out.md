---
description: Wave/in/out 裝置類別包含完整的雙工音訊裝置。
ms.assetid: 1b49c9ae-da64-4415-95ce-785ffedc65bc
title: wave/in/out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0e814cf2e8de1c3c5700a7570d2ed2b4c428572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985204"
---
# <a name="waveinout"></a>wave/in/out

Wave/in/out 裝置類別包含完整的雙工音訊裝置。 您可以使用 (SDK) 平臺軟體發展工具組中所述的 wave 功能來存取這些裝置。 此類別中的裝置會與支援 LINEMEDIAMODE AUTOMATEDVOICE 媒體類型的線路裝置相關聯 \_ ，該媒體類型是線上路裝置之 [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)結構的 **dwMediaModes** 成員中指定的。

[**LineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)和 [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)函數會填滿 [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring)結構、將 **dwStringFormat** 成員設定為 STRINGFORMAT \_ 二進位值，並附加兩個額外的成員：

``` syntax
DWORD DeviceInId;  // identifier of wave in audio device
DWORD DeviceOutId;  // identifier of wave out audio device
```

**DeviceInId** 和 **DeviceOutId** 成員是封閉式音訊裝置的識別碼。 在 [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) 函式的呼叫中，您可以使用這些識別碼來開啟裝置以進行輸出。 您可以使用產生的裝置控制碼，線上路或電話裝置上播放數位化的音訊資料。

如需 wave 函數的詳細資訊，請參閱 [**多媒體功能**](../multimedia/multimedia-functions.md)。

 

 
