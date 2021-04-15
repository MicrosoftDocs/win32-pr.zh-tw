---
description: 擴充行服務 (或裝置專屬的線路服務) 包含 API 的所有服務提供者定義延伸模組。
ms.assetid: 0f01509e-caa5-4f79-be78-36bd5f23c5d7
title: 擴充行函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3531a63357276e6b2ea37365b5d5078d5c1de324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511537"
---
# <a name="extended-line-functions"></a>擴充行函式

擴充行服務 (或裝置專屬的線路服務) 包含 API 的所有服務提供者定義延伸模組。 此 API 定義了一種機制，可讓服務提供者廠商使用裝置專屬的延伸模組來擴充 TAPI。 API 只會定義擴充機制，藉由這樣做可存取裝置專屬的延伸模組，但 API 不會定義其行為。 行為完全由服務提供者定義。

TAPI 包含純量和位旗標常數定義、資料結構、函數和訊息。 定義的程式可讓廠商擴充大部分的程式，如下所示。

針對可延伸的純量資料常數，服務提供者廠商可以在指定的範圍內定義新值。 因為大部分的資料常數都是 **DWORD**，所以通常會將0X00000000 到0x7fffffff 的範圍保留給一般未來的延伸模組，而透過0xffffffff 的0x80000000 則適用于供應商專屬的延伸模組。 假設廠商會定義值，這些值是 API 所定義之資料類型的自然延伸。

針對可延伸位旗標資料常數，服務提供者廠商可以定義指定位的新值。 因為大部分的位旗標常數都是 **DWORD**，所以一般的延伸模組通常會保留較低的特定數目，而剩餘的較高位則適用于廠商專屬的延伸模組。 一般位旗標是從位零向上指派;廠商專屬的延伸模組應從位31下指派。 這可提供最大的彈性，可將位位置指派給一般擴充功能與特定廠商的延伸模組。 廠商預期會定義新的值，這些值是 API 所定義之位旗標的自然延伸。

可擴充的資料結構具有大小可變大小的欄位，保留給裝置特定用途。 在大小可變調整大小的情況下，服務提供者會決定資訊數量和轉譯。 定義裝置特定欄位的廠商預期會讓 API 所定義的原始資料結構自然擴充。

[**LineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific)和 [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature)這兩個函式，以及兩個相關訊息（[**行 \_ DEVSPECIFIC**](line-devspecific.md)和 [**行 \_ DEVSPECIFICFEATURE**](line-devspecificfeature.md)）提供廠商專屬的擴充機制。 **LineDevSpecific** 函式和相關行 \_ DEVSPECIFIC 訊息可讓應用程式存取基本或補充電話語音服務無法使用的裝置專屬行、位址或呼叫功能。 **LineDevSpecific** 函式的參數設定檔是泛型，因為這些參數的小部分解釋是由 API 所組成。 參數的解讀是由服務提供者所定義，而且必須由使用這些參數的應用程式加以瞭解。 這些參數只會透過 TAPI 從應用程式傳遞至服務提供者。 依賴裝置專屬延伸模組的應用程式通常不會與其他服務提供者搭配使用;不過，寫入基本和補充電話語音服務的應用程式將會與擴充的服務提供者合作。

為了方便起見，也提供更特製化的 escape 函數。 它類似于 [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific)，但會對某些參數進行轉譯。 這個更特製化的函式是 [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature)，這是裝置特定的 escape 函式，可讓您將交換器功能傳送至交換器。 訊息 [**行 \_ DEVSPECIFICFEATURE**](line-devspecificfeature.md) 是傳送至應用程式的裝置特定訊息，以指出傳送至交換器的功能。 此函式及其相關聯的訊息可讓應用程式在行的功能電話上模擬按鈕按下。 隨著功能電話和其按鈕的意義是廠商專屬的，使用 [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) 的功能叫用也是廠商特定的。

如先前所述，製造商識別碼沒有中央登錄。 相反地， (EXTIDGEN) 的唯一識別碼產生器可供使用。

 

 



