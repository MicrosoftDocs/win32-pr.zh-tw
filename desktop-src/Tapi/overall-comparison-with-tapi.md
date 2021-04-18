---
description: TSPI 規格與 TAPI 2.2 (TAPI/C) 的規格密切相關。
ms.assetid: 2c51f7e3-c741-4736-9611-2327d65b427e
title: 與 TAPI 的整體比較
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce81d569d042cdd3eeb87088b1b7027858ca806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989434"
---
# <a name="overall-comparison-with-tapi"></a>與 TAPI 的整體比較

TSPI 規格與 TAPI 2.2 (TAPI/C) 的規格密切相關。 其中一個函式中的大部分函式都有相對應的函式。 一般的對應如下所示：

-   TSPI 函式與 TAPI 函式的名稱相同，不同之處在于它們前面加上 "**TSPI \_**"。 例如，TAPI 函式 [**lineAccept**](/windows/win32/api/tapi/nf-tapi-lineaccept) 對應至 TSPI 函數 [**TSPI \_ lineAccept**](/windows/win32/api/tspi/nf-tspi-tspi_lineaccept)。
-   允許非同步作業的程式會將類型 [Winspool.drv \_ REQUESTID](drv-requestid.md)的 *dwRequestID* 參數插入其第一個參數。 此參數會指定要傳回的值以表示非同步作業，並報告非同步完成。
-   HCALL 類型的 *hCall* 參數會取代為類型 [HDRVCALL](hdrvline.md)的 *hdCall* 參數，表示服務提供者的呼叫控制碼。
-   HLINE 類型的 *hLine* 參數會以-類型 [HDRVLINE](hdrvline.md)的 *hdLine* 參數取代，表示服務提供者的行控制碼。
-   HPHONE 類型的 *hPhone* 參數會取代為類型 [HDRVPHONE](hdrvphone.md)的 *hdPhone* 參數，表示服務提供者的電話控點。
-   建立新呼叫的程式（例如 [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)）會使用兩個參數來取代單一 *lphCall* 參數： [HTAPICALL](htapicall.md)參數的 *HTCALL* ，它會傳入用於呼叫的 TAPI 控制碼，以及 lphdCall 類型 *的 LPHDRVCALL* ，指出服務提供者必須為其撰寫其新控制碼的位置。 [**TSPI \_ LineOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)和 [**TSPI \_ phoneOpen**](/windows/win32/api/tspi/nf-tspi-tspi_phoneopen)中會出現類似的參數分割。
-   在 TSPI 層級中，不會有與裝置控制碼相關聯的「許可權」概念。 此外，在 API 層級，具有裝置或呼叫控制碼的每個應用程式都有不同的控制碼，但 TAPI 會將這些應用程式合併到服務提供者端的單一控制碼中。 因此，與許可權相關的錯誤碼和狀態訊息以及使用裝置的用戶端數目，都不會出現在 TSPI 層級。

這組 TAPI 函式不會在一組 TSPI 函式上對應到一個。 尤其是，與許可權、電話號碼轉譯和應用程式間通訊相關的函式是由 TAPI 處理，而且在 TSPI 中沒有對應的功能。 其他功能（例如用於服務提供者設定和初始化的函式）在 TAPI 中沒有對應的函式。

 

 
