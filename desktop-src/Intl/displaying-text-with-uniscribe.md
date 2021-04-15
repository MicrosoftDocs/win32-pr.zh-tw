---
description: 您的應用程式可以使用 Uniscribe API 函式來支援印刷樣式以及國際文字的顯示和編輯。 Uniscribe 使用段落作為文字顯示的單位，而 Uniscribe 功能則必須用於整個段落。
ms.assetid: e1adc567-0445-4deb-8634-25653f82127c
title: 使用 Uniscribe 顯示文字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baeb9a2be4d00efaa2681097ddefe3a6de4c576b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320240"
---
# <a name="displaying-text-with-uniscribe"></a>使用 Uniscribe 顯示文字

您的應用程式可以使用 Uniscribe API 函式來支援印刷樣式以及國際文字的顯示和編輯。 Uniscribe 使用段落作為文字顯示的單位，而 Uniscribe 功能則必須用於整個段落。

使用 Uniscribe 來顯示文字時，應用程式必須經過格式化 ( 「版面配置」 ) 進程，通常是使用 Uniscribe。 應用程式會將文欄位落分割為具有相同樣式的字元字串，稱為「執行」。 樣式取決於特定的執行，但通常會包含字型、大小和色彩這類屬性。 在定義回合中，應用程式也可以套用其他資訊，例如為了搭配使用詞法工具而維護的語言和地區設定資料。 例如，應用程式可能會被視為個別的執行以法文轉譯的英文文字。

一旦決定所有段落的回合之後，應用程式就會將每個段落分割成具有相同腳本和方向 ( 「專案」 ) 的字串。 應用程式會套用專案資訊，以產生在腳本和方向中是唯一的執行，並且完全落在單一專案內 ( 「範圍」 ) 。

雖然範圍應包含一或多個連續的腳本定義不可分割字元群組（稱為「叢集」），但專案的明細也有點任意。 若是歐洲語言，叢集通常會對應 [至單一代碼](uniscribe-glossary.md)頁字元或 Unicode 程式碼點，並由單一字元組成。 不過，在泰文之類的語言中，叢集是一組字元，並且對應至多個連續的字元或程式碼點。 例如，泰文叢集可能包含輔音、母音和音調標記。 因此，它不會中斷叢集，應用程式通常應該使用它所能使用的最長範圍，或使用自己的詞法資訊，在不在叢集中間的位置之間中斷。

當它識別出每個範圍中的叢集時，應用程式必須決定每個叢集的大小。 它會使用 Uniscribe 來加總群集，以決定每個範圍的大小。 然後，應用程式會加總範圍的大小，直到行溢位為止，也就是到達邊界。 溢位的範圍會在目前的行和下一行之間分割。 應用程式會針對每一行，從視覺位置建立對應到每個範圍的邏輯位置。 然後，應用程式會將每個範圍的程式碼指向字元，以供之後定位和轉譯。

應用程式只會執行一次文字版面配置。 之後，它會儲存字元和位置以供顯示之用，或在每次顯示文字時產生它們，而且會有速度與記憶體的取捨。 一般的應用程式會實作為配置程式一次，然後在每次顯示文字時產生圖像和位置。

使用 [複雜字集](uniscribe-glossary.md) 的應用程式對於版面配置和顯示的簡單方法有下列問題。

-   複雜字集字元的寬度取決於其內容。 不可能將寬度儲存在簡單資料表中。
-   在泰文等腳本中的單字之間中斷需要字典支援。 例如，在泰文單字之間不會使用任何分隔字元。
-   阿拉伯文、希伯來文、波斯文、烏爾型別的和其他 [雙向文字](uniscribe-glossary.md) 語言都需要重新排列才能顯示。
-   通常需要某種形式的字型關聯，才能輕鬆地使用複雜的腳本。

Uniscribe 使用段落作為顯示單元，可協助應用程式適當地處理這些複雜的腳本問題。

> [!Note]  
> Uniscribe 必須用於整個段落，即使段落的區段不是複雜的腳本。

 

如下表所示，Uniscribe 1.6 版或更高版本支援數個可利用 OpenType 標記的函式。 它們可以替代對應的一般 Uniscribe 函式。 一般來說，您的應用程式應該會完全與一個集合中的函式搭配運作，而且不應該嘗試「混合和比對」函數。



| 一般 Uniscribe 函式             | 相等的 OpenType 函數                           |
|----------------------------------------|--------------------------------------------------------|
| [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) | [**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype) |
| [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)     | [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)     |
| [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)     | [**ScriptPlaceOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)     |



 

## <a name="lay-out-text-using-uniscribe"></a>使用 Uniscribe 配置文字

您的應用程式可以使用下列步驟，透過 Uniscribe 配置文欄位落。 此程式假設應用程式已將段落劃分為執行。

1.  只有在啟動或收到 [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md)訊息時，才呼叫 [**ScriptRecordDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptrecorddigitsubstitution) 。
2.   (選擇性的) 呼叫 [**ScriptIsComplex**](/windows/desktop/api/Usp10/nf-usp10-scriptiscomplex) ，以判斷段落是否需要複雜的處理。
3.   (選擇性) 如果使用 Uniscribe 來處理雙向文字及/或數位替代，請呼叫 [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) 來準備 [**腳本 \_ 控制項**](/windows/win32/api/usp10/ns-usp10-script_control) ，並以 [**腳本 \_ 狀態**](/windows/win32/api/usp10/ns-usp10-script_state) 結構作為 [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize)的輸入。 如果略過此步驟，但仍需要數位替換，請將 Unicode U + 0030 的國家/地區數位替換成 U + 0039 (歐洲數位) 。 如需數位替換的詳細資訊，請參閱 [數位圖形](digit-shapes.md)。
4.  呼叫 [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) 將段落分割成專案。 如果未使用 Uniscribe 進行數位替換，且雙向順序是已知的，例如，由於用來輸入字元的鍵盤配置，請呼叫 **ScriptItemize**。 在呼叫中，提供 [**腳本 \_ 控制項**](/windows/win32/api/usp10/ns-usp10-script_control) 和 [**腳本 \_ 狀態**](/windows/win32/api/usp10/ns-usp10-script_state) 結構的 null 指標。 這項技術只會透過使用成形引擎來產生專案，而且可以使用引擎資訊將專案重新排序。
    > [!Note]  
    > 一般來說，只使用由左至右腳本且沒有任何數位替代的應用程式，應該傳遞 [**腳本 \_ 控制項**](/windows/win32/api/usp10/ns-usp10-script_control) 和 [**腳本 \_ 狀態**](/windows/win32/api/usp10/ns-usp10-script_state) 結構的 null 指標。

     

5.  將專案資訊與執行資訊合併，以產生範圍。
6.  呼叫 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) 來識別叢集並產生字元。
7.  如果 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) 傳回 \_ 不在字型中的程式碼 USP E \_ 腳本 \_ \_ \_ \_ ，或有輸出包含遺漏圖像的輸出，請選取不同字型中的字元。 請將傳遞給 **ScriptShape** 的 [**腳本 \_ 分析**](/windows/win32/api/usp10/ns-usp10-script_analysis)結構的 **eScript** 成員設定為未定義的腳本，以替代另一個字型或停用成形 \_ 。 如需詳細資訊，請參閱 [使用字型](using-font-fallback.md)回復。
8.  呼叫 [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) 以產生每個後續範圍中圖像的 [前進寬度](uniscribe-glossary.md) 和 x 和 y 位置。 這是文字大小變成考慮的第一個步驟。
9.  將範圍大小加總，直到行溢位為止。
10. 使用邏輯屬性中的 **fSoftBreak** 和 **fWhiteSpace** 成員，來中斷單字界限的範圍。 若要在執行時中斷單一字元叢集，請使用呼叫 [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)傳回的資訊。
    > [!Note]  
    > 決定範圍的第一個程式碼點是否應為斷字點，因為前一個範圍中的最後一個字元需要它。 例如，如果一個範圍以逗號結束，請將下一個範圍中的第一個字元視為單字分隔點。

     

11. 針對段落中的每一行，重複步驟6到10。 但是，如果中斷最後一次執行的程式程式碼，請呼叫 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) ，將執行的其餘部分重新調整為下一行的第一次執行。

## <a name="display-text-using-uniscribe"></a>使用 Uniscribe 顯示文字

您的應用程式可以使用下列步驟來顯示文欄位落。 此程式假設應用程式已配置文字，而且尚未從配置進程儲存字元和位置。 如果速度是個問題，應用程式可以從配置程式儲存字元和位置，並在顯示程式的步驟2開始。

> [!Note]  
> 如果文字不包含由右至左的腳本提供任何字元、不包含雙向控制字元，而且使用由左至右的基底內嵌層級，則應用程式可以省略步驟2。

 

1.  針對每個執行，執行下列步驟：
    1.  如果樣式自上一次執行之後已變更，請釋放並重新取得裝置內容的控制碼。
    2.  呼叫 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) 以產生執行的字元。
    3.  呼叫 [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) 以產生每個字元的前進寬度和 x、y 位移。
2.  執行下列動作，以在行中建立執行的正確視覺效果順序：
    1.  將雙向內嵌 [層級](uniscribe-glossary.md)的陣列（每個範圍一個）解壓縮。 內嵌層級是由 (腳本 \_ 專案) si 提供。 (腳本 \_ 分析) 。  (腳本 \_ 狀態) s. uBidiLevel。
    2.  將此陣列傳遞至 [**ScriptLayout**](/windows/desktop/api/Usp10/nf-usp10-scriptlayout) ，以產生邏輯位置的視覺位置對應。
3.   (選擇性的) 來證明文字，請呼叫 [**ScriptJustify**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify) 或使用文字的特定知識。
4.  使用視覺效果對邏輯地圖以視覺化順序顯示執行。 從該行的左邊端開始，呼叫 [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) ，以顯示對應中第一個專案所指定的執行。 針對對應中的每個後續專案，呼叫 **ScriptTextOut** ，以顯示先前顯示之執行右邊的指定回合。

    如果省略步驟2，請從該行的左邊開始，然後呼叫 [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) 來顯示第一個邏輯執行，然後在上一次執行的右側顯示每個邏輯執行。

5.  針對段落中的所有行重複上述步驟。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 
