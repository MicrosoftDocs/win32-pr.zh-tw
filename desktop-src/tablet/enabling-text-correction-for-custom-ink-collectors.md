---
description: Microsoft Tablet PC 輸入面板是一種功能強大的工具，可使用畫筆來輸入手寫文字，並在不使用鍵盤的情況下更正文字。
ms.assetid: c45ac1b5-7713-4bcb-a130-4692cff99aa2
title: 啟用自訂筆墨收集器的文字更正
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: accb0bf2129a4e93e543e3ec5cc73d3e65383dc57b581114f30e812b1ac88b8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940823"
---
# <a name="enabling-text-correction-for-custom-ink-collectors"></a>啟用自訂筆墨收集器的文字更正

Microsoft Tablet PC 輸入面板是一種功能強大的工具，可使用畫筆來輸入手寫文字，並在不使用鍵盤的情況下更正文字。 使用 [輸入面板] 時，使用者會在輸入面板的筆墨表面上以手寫方式輸入文字，這會導致輸入面板將使用者的手寫辨識為文字。 辨識文字之後，使用者可以在 [輸入面板] 上按 [插入]，將文字插入應用程式或檔中。 在插入文字之前，使用者可以存取 [輸入面板] 中的一組更正工具。 這些包括選取替代辨識結果、重寫單一字元的能力，或甚至是將整個單字重寫。 這些更正工具可讓使用者更正辨識錯誤和人為錯誤。

在檔中使用 [輸入面板] 輸入的文字之後，使用者就可以在插入 Windows[文字服務架構](/windows/desktop/TSF/text-services-framework)型和啟用文字服務的應用程式之前，存取同樣可用的更正功能。 從 Microsoft Windows XP Service Pack 2 Tablet PC Edition 開始，所有豐富的編輯應用程式都是文字服務-預設為啟用，而且從 Windows Vista 開始，HTML 應用程式預設為啟用文字服務。 檔內更正僅適用于以文字服務為基礎且已啟用的應用程式;這是因為輸入面板相依于文字服務的功能來儲存相關聯的文字屬性（包括筆墨物件和辨識替代項），以提供檔內的更正。

![具有文字更正的 tablet pc 輸入面板](images/a0dced5e-16de-410b-965f-5d97d297cee5.jpg)

不過，在許多情況下，您可以使用輸入面板來修正語音辨識或更正輸入的文字，而不是以使用輸入面板的文字輸入來啟動，但在這種情況下，檔內更正可能對 Tablet PC 使用者非常有用。 其中的一個主要範例是在應用程式中提供使用畫筆輸入文字的自訂筆跡表面。 自訂筆跡介面是一個很好的方式，可讓應用程式針對每個應用程式的文字輸入工作提供唯一量身打造的功能。 此外，自訂的筆墨表面也提供完全整合的 Tablet PC 使用者體驗，讓它清楚地看畫筆是包含它們之應用程式中的第一個類別輸入裝置。 不過，提供自訂筆跡表面的應用程式可能不允許或可能無法提供來自輸入面板檔內更正的相同等級的更正支援。

![自訂筆墨收集器](images/b6797b12-dda6-44c4-87f4-570fe0c23f3a.jpg)

以文字服務為基礎或已啟用的應用程式，在其中使用 [輸入面板] 來更正未輸入的文字時，可使用 [輸入面板] 中的 [IHandWrittenTextInsertion API]，在 managed 程式) 代碼中使用輸入面板的[](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) API ([>textinput HandwrittenTextInsertion](/previous-versions/ms573516(v=vs.100))類別，以啟用以其他方式輸入之文字的檔內校正。 如此一來，應用程式就可以低廉價格將強大的修正支援新增至自訂的筆墨表面或其他文字輸入案例，並將其 Tablet PC 文字輸入的故事。 輸入面板 IHandWrittenTextInsertion API 隨附于 Windows Vista 作業系統的一部分，而且是平板電腦平臺 SDK 1.9 版或更新版本的一部分。 同時包含 .NET 和 COM 型的 API 版本。 Windows Vista 和更新版本支援使用 [輸入面板] 來啟用未輸入文字的檔內校正。 檔內更正僅適用于拉丁語言，而且無法顯示拉丁字元集以外的任何字元。

## <a name="how-to-use-the-handwrittentextinsertion-api-in-an-application"></a>如何在應用程式中使用 HandwrittenTextInsertion API

為了針對未使用輸入面板和使用 [**IHandWrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) API 所輸入的文字，將輸入面板的輸入面板檔內更正，以整合輸入面板的必要變更很簡單。 除了最後一個步驟之外，所有應用程式的自訂文字專案程式碼都會保持不變。 在使用自訂筆跡介面、語音辨識或其他方法所輸入文字的位置，會在文字服務 **啟用的文字** 欄位中顯示，而不是直接將文字傳送到文字欄位。 輸入面板的可程式性元件接著會處理將文字插入文字欄位和文字服務備份存放區的程式。 將文字新增至文字服務備份儲存區時，輸入面板的可程式性元件會處理設定輸入面板所需的文字屬性，以便針對該文字啟用檔內更正。

下一節將逐步說明使用 [**IHandWrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) API COM 版本之 c + + 應用程式的程式。 在 c \# + + 中使用 COM 版本的 c # 中使用 .NET Framework 版 API 的步驟有很大的不同。 Managed **HandwrittenTextInsertion** API 包含單一 COM 介面 **IHandwrittenTextInsertion**。 此介面的定義位於 PenInputPanel .h 和 PenInputPanel \_ i.c。

首先，應用程式應該使用 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)函數來產生具有類別識別碼 **CLSID \_ HandwrittenTextInsertion** 的 [**IHandWrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion)實例。 請注意，只有在建立視窗並獲得焦點之後，才會成功建立 **CLSID \_ HandwrittenTextInsertion** 物件，因為在此之前，不會啟動文字服務支援存放區。 此外，如果系統上沒有 tiptsf.dll， **CoCreateInstance** 函式會失敗並傳回 **REGDB \_ E \_ CLASSNOTREG**，表示系統上不支援輸入面板的檔內更正。 此時應用程式應該繼續進行，而不嘗試啟用輸入面板的檔內校正。 您必須可從應用程式的程式碼存取 **HandwrittenTextInsertion** 實例，以處理將文字插入文字欄位的程式碼。

> [!Note]  
> 使用 .NET Framework 版的 API 時，應用程式應該加入 using 語句以允許存取[>textinput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90))命名空間，然後直接建立物件。

 

其次，必須改變應用程式的程式碼，以將文字插入文字欄位中，如此一來，它就不會再直接將文字插入文字欄位中，而會改為呼叫 [**IHandwrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion)的兩個插入方法的其中一個。 應用程式是否應該選擇呼叫 [**InsertRecognitionResultsArray**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ihandwrittentextinsertion-insertrecognitionresultsarray) 或 [**InsertRecognitionResults**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ihandwrittentextinsertion-insertinkrecognitionresult) ，取決於應用程式是否針對儲存為數組或 [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) 物件的文字進行辨識替代。

> [!Note]  
> 在 managed 程式碼中工作時，InsertRecognitionResultsArray 所使用的對應辨識物件為 [RecognitionResult](/previous-versions/ms552537(v=vs.100))。 這兩種方法都會使用下列三個參數：

 

-   *替代* 這是兩個維度的字串集合，儲存為數組的陣列或 [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) (或 [RecognitionResult](/previous-versions/ms552537(v=vs.100))) 物件。 如果替代項儲存為數組的陣列，則應該以安全陣列指標的形式傳遞。 最上層陣列中的每個專案都是插入中單一單字的替代清單。 替代項的子陣列中位置零的專案是插入文字欄位中的文字。 每個子陣列中的額外替代 (索引1到 n) 都會儲存在文字服務備份儲存區中，並提供給使用者作為檔內更正的一部分選項。 如果未包含替代項，則使用者會看到「沒有建議」取代替代清單。 如果插入包含多個單字之間有空格，則每個空格都必須包含在最上層陣列中做為專案。
-   *語言* 對應至 *替代* 參數中所包含之文字的輸入語言 [LCID](/previous-versions/ms221397(v=vs.71)) 。 在手寫或語音辨識器產生 *替代* 項內容的情況下，這也是與所用辨識器相關聯的 [ [**語言**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) ] 屬性。
-   *fLatticeContainsAutoSpacingInformation* 旗標，指出 *替代* 參數中包含的文字是否由已啟用自動間距的辨識器產生。 如果已啟用自動間距，則旗標應設定為 **TRUE**。 如果已停用自動間距，則旗標應設定為 **FALSE**。 如果 *替代* 項的內容是由不支援自動間距的辨識器所產生，或者完全不是由辨識器產生，則旗標應設為 **FALSE**。

輸入面板的可程式性模型可以從系統插入號的位置，插入檔或應用程式中的文字。

如果插入成功，這兩種方法都會傳回 **S \_ OK** 。 如果應用程式不是以文字服務為基礎或未啟用，則會傳回 **e \_ NOINTERFACE** ，而如果 *替代* 功能格式不正確或無法存取，則會傳回 **e \_ INVALIDARG** 。 如果系統上沒有足夠的記憶體可用，它們也可能會傳回 **e \_ OUTOFMEMORY** ，或在發生嚴重失敗（例如文字服務架構未啟用）之後 **\_ 發生** 錯誤。

### <a name="conclusion"></a>結論

使用 [輸入面板] 針對未輸入的文字啟用輸入面板的檔內更正，對於以文字服務為基礎或啟用的應用程式，使用功能強大的畫筆修正功能來補充自訂筆跡或輸入方法，是一種便宜且簡單的方式。 在 Windows Vista 中，所有豐富的編輯和 Trident 應用程式都已啟用文字服務。 雖然整合式筆墨表面是將自訂 Tablet PC 使用者體驗新增到應用程式的絕佳選項，但是如果不包含更正功能，則只支援一半的文字專案。 檔內更正可為使用者提供另一半的案例，方法是新增交換辨識選項的功能，或重寫部分或全部的選取專案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式設計文字輸入面板](programming-the-text-input-panel.md)
</dt> </dl>

 

 
