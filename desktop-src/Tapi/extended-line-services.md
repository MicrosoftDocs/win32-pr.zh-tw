---
description: 擴充行服務 (或裝置專屬的行服務) 包含 TSPI 的所有服務提供者定義延伸模組。
ms.assetid: 23519d23-27bd-422e-b3c4-00e0d0d93f9e
title: 擴充行服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc1ce08d25633d33fd518d8686271c198ca5034
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981571"
---
# <a name="extended-line-services"></a>擴充行服務

擴充行服務 (或裝置專屬的行服務) 包含 TSPI 的所有服務提供者定義延伸模組。 TSPI 定義了一種機制，可讓服務提供者廠商使用裝置特定的擴充功能來擴充電話語音 SPI。 TSPI 只會定義擴充機制，藉由這樣做，可存取裝置專屬的延伸模組，但是 TSPI 不會定義其行為。 行為完全由服務提供者定義。

電話語音 SPI 包含純量和位旗標常數定義、資料結構、函數和回呼訊息。 定義的程式可讓廠商擴充大部分的程式，如下所示。

針對可延伸的純量資料常數，服務提供者廠商可以在指定的範圍內定義新值。 因為大部分的資料常數都是 **DWORD**，所以通常會將0X00000000 到0x7fffffff 的範圍保留給一般未來的延伸模組，而透過0xffffffff 的0x80000000 則適用于供應商專屬的延伸模組。 假設廠商會定義值，這些值是 TSPI 所定義之資料類型的自然延伸。

針對可延伸位旗標資料常數，服務提供者廠商可以定義指定位的新值。 因為大部分的位旗標常數都是 **DWORD**，所以通常會保留較低的特定數目給通用副檔名，而其餘的位則適用于供應商專屬的延伸模組。 一般位旗標是從位零向上指派;廠商專屬的延伸模組應從位31下指派。 這可提供最大的彈性，可將位位置指派給一般擴充功能與特定廠商的延伸模組。 廠商預期會定義新的值，這些值是 TSPI 所定義之位旗標的自然延伸。

可擴充的資料結構具有大小可變大小的欄位，保留給裝置特定用途。 在大小可變調整大小的情況下，服務提供者會決定資訊數量和轉譯。 定義裝置特定欄位的廠商預期會讓 TSPI 所定義之原始資料結構的自然延伸。

有兩個函式 [**TSPI \_ LineDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific) 和 [**TSPI \_ lineDevSpecificFeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)，以及四個相關的訊息、 [**行 \_ DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85))、 [**行 \_ CALLDEVSPECIFIC**](line-calldevspecific.md)、 [**行 \_ DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85))和 [**行 \_ CALLDEVSPECIFICFEATURE**](line-calldevspecificfeature.md)，提供廠商專屬的擴充機制。 **TSPI \_ lineDevSpecific** 作業和相關行 \_ DEVSPECIFIC 和行 \_ CALLDEVSPECIFIC 訊息可讓 Tapi32.dll 用戶端應用程式存取基本或補充電話語音服務中無法使用的裝置專屬行、位址或呼叫功能。 [**TSPI \_ lineDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)函式的參數設定檔是泛型，因為參數的微小解釋是由 TSPI 所建立。 裝置控制碼參數具有 TSPI 定義的意義，並會在應用程式與服務提供者之間妥善轉譯。 泛型參數只會透過未修改的傳遞。 泛型參數的解讀是由服務提供者所定義，而且必須由使用這些參數的任何應用程式加以瞭解。 依賴裝置專屬延伸模組的應用程式通常不會與其他服務提供者一起使用。 不過，完全寫入基本和補充的電話語音服務的應用程式，應該與延伸的服務提供者一起使用。

裝置特定函式和訊息的 TAPI 實作為「傳遞」。 TAPI 不會檢查或修改一般裝置特定的參數和緩衝區，但它會將應用層級的不透明控制碼值對應 (用於 TAPI 層級的) 服務提供者層級的不透明控制碼值 (用於 TSPI 層級) 。

關於控制碼轉譯，裝置專屬延伸模組的一般部分的傳遞本質有很大的結果。 服務提供者無法將 TSPI 層級所使用的控制碼與 TAPI 層級的控制碼建立關聯，除了透過預先定義的控制碼參數和欄位傳遞它們之外。 因為 TAPI 會在應用程式與服務提供者之間傳遞，所以任何放入泛型延伸區域的控制碼都會由 TAPI 轉譯。 服務提供者延伸模組的設計工具通常應該不會定義以這種方式傳遞控制碼的延伸模組。

在定義裝置專屬的延伸模組時，若未使用控制碼而必須參考特定裝置，則適當的方法是使用其絕對裝置識別來參考這些裝置。 例如，用來在 TAPI 層級開啟線路的裝置識別碼，與 TSPI 層級上用來開啟該行的值完全相同。 同樣地， (行裝置識別碼、位址識別碼) 可唯一識別 TAPI 層級位址的元組，會使用相同的值來識別 TSPI 層級的相同內容。

為了方便起見，也提供更特製化的 escape 函數。 它類似于 [**TSPI \_ lineDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)，但會對某些參數進行轉譯。 [**TSPI \_ lineDevSpecificFeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)函式和相關 [**行 \_ DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85))和 [**行 \_ CALLDEVSPECIFICFEATURE**](line-calldevspecificfeature.md)訊息可讓 TAPI 在行的功能電話上模擬按鈕按下。 因為功能電話和其按鈕的意義是廠商專屬的，使用 **TSPI \_ lineDevSpecificFeature** 的功能叫用也是特定廠商。

總而言之， [**TSPI \_ lineDevSpecificFeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature) 函式是裝置專屬的 escape 函式，可讓您將交換器功能傳送至交換器。 [**\_ CALLDEVSPECIFICFEATURE**](line-calldevspecificfeature.md)訊息是傳送至應用程式回呼的裝置特定訊息，以指出傳送至交換器的呼叫相關功能。 [**行 \_DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85)) 是傳送至應用程式回呼的裝置特定訊息，表示傳送至參數的行相關功能。

沒有適用于製造商識別碼的中央登錄。 相反地，稱為 Extidgen.exe 的唯一識別碼產生器會在 TSPI 中提供。 設計一組裝置專屬延伸模組的廠商會使用此公用程式來取得這些擴充功能的唯一識別碼。

 

 
