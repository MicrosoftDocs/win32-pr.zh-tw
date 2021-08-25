---
title: 將資料流程寫入檔案
description: 將資料流程寫入檔案
ms.assetid: a3766f8c-aaa6-4fc5-a306-54aee71018f1
keywords:
- AVIFileCreateStream 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baaedd4103d2141ecaccde78462b2290cf5d5d37813b224c20101eacbe580d70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891758"
---
# <a name="writing-streams-to-a-file"></a>將資料流程寫入檔案

您也可以藉由將新的資料流程寫入檔案，來建立包含資料流程的檔案。

您可以使用 [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream) 函數，在新的或現有的檔案中建立新的資料流程。 此函式會根據 [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) 結構中所述的特性來定義新的資料流程、建立新資料流程的資料流程介面、遞增資料流程的參考計數，以及傳回資料流程介面指標的位址。

寫入資料流程的內容之前，您必須指定資料流程格式。 您可以使用 [**AVIStreamSetFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat) 函數來設定資料流程格式。 設定影片資料流程的格式時，您必須以包含適當資訊的 [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) 結構提供此函數。 設定音訊資料流程的格式時，您必須提供 [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) 或 [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) 結構，其中包含適當的資訊。 您需要提供給其他資料流程類型之函式的資訊取決於資料流程類型和資料流程處理常式。

您可以使用 [**AVIStreamWrite**](/windows/desktop/api/Vfw/nf-vfw-avistreamwrite) 函式來寫入資料流程中的多媒體內容。 此函數會將原始資料從應用程式提供的緩衝區複製到指定的資料流程。 預設的 AVI 檔處理常式會將資訊附加到資料流程的結尾。 預設 WAVE 處理常式可以在資料流程中以及在資料流程的結尾寫入波形音訊資料。

您可以使用 [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata)和 [**AVIStreamWriteData**](/windows/desktop/api/Vfw/nf-vfw-avistreamwritedata)函式，來寫入未包含在 [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream)或 [**AVIStreamSetFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat)函式中之檔案或資料流程的補充資訊。 您可以使用 **AVIFileWriteData** 來記錄適用于整個檔案的資料，例如著作權資訊和修改歷程記錄。 您可以使用 **AVIStreamWriteData** 來記錄資料流程特定的資訊，例如壓縮和解壓縮設定。 補充資訊儲存在檔案中的不同區塊。

當您使用 [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) 函式完成寫入至新的資料流程之後，就可以關閉資料流程。 此函式會清除用來記錄資料流程資料的緩衝區，並在檔案中完成並關閉任何不完整的資料區塊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[資料流作業](stream-operations.md)
</dt> </dl>

 

 