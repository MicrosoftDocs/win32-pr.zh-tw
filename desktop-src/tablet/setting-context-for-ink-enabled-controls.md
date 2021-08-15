---
description: 啟用筆墨之控制項的所有辨識都會透過 RecognizerCoNtext 物件進行。 Tablet PC 技術 Api 可讓您設定 RecognizerCoNtext 物件上的「模擬」屬性。
ms.assetid: 453993a7-f055-4d84-870c-256d1ec17731
title: 設定 Ink-Enabled 控制項的內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 306ae4c76ce5187c930c24a10631ec703f684cc8a3e4b0a94f46414bddbd058f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091295"
---
# <a name="setting-context-for-ink-enabled-controls"></a>設定 Ink-Enabled 控制項的內容

啟用筆墨之控制項的所有辨識都會透過 [**RecognizerCoNtext**](inkrecognizercontext-class.md) 物件進行。 Tablet PC 技術 Api 可讓您設定 **RecognizerCoNtext** 物件上的「[**模擬**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)」屬性。

如果您要建立啟用筆墨的應用程式，請使用 [**RecognizerCoNtext**](inkrecognizercontext-class.md) 物件的「 [**模擬**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) 」和「 [**單詞表**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) 」屬性來設定內容。

您可以將 [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) 列舉所定義之輸入範圍中的名稱字串值傳遞給 [**模擬**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) 程式屬性，並以開啟的 ( 來分隔！ 和結束 ) 。 例如，若要將 [**RecognizerCoNtext**](inkrecognizercontext-class.md) 物件的內容設定為對 URL 中使用的字元進行偏差，請使用下列 C 範例所示的語法 \# ：


```C++
theRecoContext.Factoid = "(!IS_URL)";
```



> [!Note]  
> [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope)列舉中所定義的輸入範圍會取代舊版 Windows XP Tablet PC Edition SDK 中所提供的 factoids，不過這些 factoids 將繼續運作，以提供回溯相容性。

 

下列 C \# 範例會設定郵遞區號的「 [**模擬**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) 」屬性：


```C++
theRecognizerContext.Factoid = "(!IS_ADDRESS_POSTALCODE)";
```



您可以使用手寫的正則運算式語法來合併輸入範圍。 如需使用正則運算式語法的詳細資訊，請參閱 [使用正則運算式的自訂輸入範圍](custom-input-scopes-with-regular-expressions.md)。

您可以設定 [**RecognizerCoNtext**](inkrecognizercontext-class.md) 物件上的辨識旗標，以影響辨識器的行為。 其中一個這類旗標是 **RecognizerCoNtext** 的 [**InkRecognitionModes**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionmodes)列舉中的 **強制** 旗標。 **強制** 辨識旗標會強制辨識器傳回符合所設定之模擬專案定義的結果。 例如，如果您的表單需要使用者輸入數值數量，則設定為 [是]，並將 [ [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) ] 屬性設定為 [**已 \_** **強制**]，可能會很有用。 在該實例中， **強制** 旗標可保證辨識器只會傳回數位。

下列 C \# 範例會將 [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) 屬性設定為 **強制** 轉換：


```C++
theRecognizerContext.RecognitionFlags = RecognitionModes.Coerce;
```



不過，在決定要設定 **強制** 執行旗標時，請特別小心。 旗標會強制辨識器僅符合模擬程式的定義。 例如，如果您設定的是 \_ 電話 \_ FULLTELEPHONENUMBER 輸入範圍和 **強制** 旗標，辨識器會傳回與的定義完全相符的結果，而 \_ \_ 只有電話 FULLTELEPHONENUMBER 輸入範圍。 如果使用者使用 \_ \_ FULLTELEPHONENUMBER 輸入範圍和 **強制** 旗標設定來寫入 "911"，辨識器可能會傳回空字串或格式為 (xxx) XXX (的隨機字串，其中 X 是數位) 。 XXX 的格式與的定義不相符 \_ \_ ，即使是有效的電話號碼也是一樣。

如需每個輸入範圍的支援格式清單，請參閱 [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) 參考。

若要將欄位傳回給辨識器的預設設定，請將 [模擬] 設定為 [ \_ 預設值]，如下列 C 範例所示 \# ：


```C++
theRecgonizerContext.Factoid = "(!IS_DEFAULT)";
```



針對使用 [InkEdit](inkedit-control-reference.md) 控制項的應用程式，藉由指定下列內容來設定控制項的模擬型別：


```C++
InkEdit1.Factoid = "(!IS_INPUTSCOPE)"
```



其中 `IS_INPUTSCOPE` 是您想要套用之輸入範圍的名稱。

[InkEdit](inkedit-control-reference.md)控制項不會公開 [**RecognizerCoNtext**](inkrecognizercontext-class.md)物件。 您仍然可以使用 InkEdit 控制項的 [ [**模擬**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid) ] 屬性指派內容，但是無法設定 **WORDMODE** 旗標。

 

 
