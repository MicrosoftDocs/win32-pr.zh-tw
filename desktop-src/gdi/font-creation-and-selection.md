---
description: '[字型通用] 對話方塊可簡化建立和選取字型的流程。'
ms.assetid: 7183be25-a8e4-47a0-a34a-63eadf6ca10d
title: 字型建立和選取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 555293e78d5ddc60284f8cb36aa3da9cfcc84062e1954059af4ead1ad9e19c5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037936"
---
# <a name="font-creation-and-selection"></a>字型建立和選取

[ **字型** 通用] 對話方塊可簡化建立和選取字型的流程。 藉由初始化 [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) 結構並呼叫 [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) 函式，應用程式可以支援先前需要許多行自訂程式碼的相同字型選取介面。  (如需 [ **字型** 通用] 對話方塊的詳細資訊，請參閱 [通用對話方塊程式庫](../dlgbox/common-dialog-box-library.md)。 ) 

## <a name="selection-by-the-user"></a>使用者選取

大部分的字型建立和選取作業都牽涉到使用者。 例如，文字處理應用程式可讓使用者選取標題、註腳和內文文字的唯一字型。 當使用者使用 [ **字型** ] 對話方塊選取字型，並按下 [ **確定]** 按鈕之後， [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) 函式就會使用所要求字型的屬性，初始化 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) 結構的成員。 若要使用此字型進行文字輸出作業，應用程式必須先建立邏輯字型，然後在其裝置內容中選取該字型。 *邏輯字型* 是應用程式提供的理想字型描述。 開發人員可以藉由呼叫 [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta) 或 [**CreateFontIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirecta) 函數來建立邏輯字型。 在此情況下，應用程式會呼叫 [**CreateFontIndirect**](/windows/win32/api/wingdi/nf-wingdi-createfontindirecta) ，並提供 [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)所初始化之 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構的指標。 一般情況下，呼叫 **CreateFontIndirect** 會更有效率，因為 [**CreateFont**](/windows/win32/api/wingdi/nf-wingdi-createfonta) 需要數個參數，而 **CreateFontIndirect** 只需要一個 **LOGFONT** 指標。

在應用程式實際開始使用邏輯字型來繪製文字之前，它必須從儲存在裝置內部的字型，以及其資源已載入作業系統的字型中，找到最接近的相符項。 存放在裝置或作業系統中的字型稱為「 *實體字型」*。 尋找最符合指定邏輯字型之實體字型的程式稱為字型對應。 當應用程式呼叫 [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) 函式，並提供識別邏輯字型的控制碼時，就會發生此程式。 字型對應的執行方式是使用內部演算法，將所要求邏輯字型的屬性與可用實體字型的屬性進行比較。 當字型對應程式演算法完成其搜尋並判斷最接近的可能相符項時， [**SelectObject**](/windows/win32/api/wingdi/nf-wingdi-selectobject) 函式會傳回，而且應用程式可以開始使用新的字型來繪製文字。

[**SetMapperFlags**](/windows/desktop/api/Wingdi/nf-wingdi-setmapperflags)函式會指定字型對應程式演算法是否只搜尋外觀比例符合實體裝置的實體字型。 裝置的外觀比例是以該裝置上的圖元寬度和高度所形成的比例。

系統字型 (也稱為 shell 或預設字型) 是標題列、功能表和對話方塊中文字所使用的字型。

## <a name="special-font-selection-considerations"></a>特殊字型選擇考慮

雖然大部分的字型選取作業都牽涉到使用者，但在某些情況下並不會發生此情況。 例如，開發人員可能會想要在應用程式中使用唯一的字型，在控制項視窗中繪製文字。 若要選取適當的字型，應用程式必須能夠判斷可用的字型、建立描述其中一種可用字型的邏輯字型，然後在適當的裝置內容中選取該字型。

應用程式可以使用 [**EnumFonts**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) 或 [**>enumfontfamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) 函數來列舉可用的字型。 建議使用 [**>enumfontfamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) ，因為它會列舉與系列名稱相關聯的所有樣式。 如果字型具有許多或不尋常的樣式，以及跨國際框線的字型，這會很有用。

一旦應用程式列舉可用的字型，並找到適當的相符項，就應該使用字型列舉函數所傳回的值，初始化 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) 結構的成員。 然後，它可以呼叫 [**CreateFontIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirecta) 函式，並將指標傳遞至初始化的 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) 結構。 如果 [**CreateFontIndirect**](/windows/win32/api/wingdi/nf-wingdi-createfontindirecta) 函式成功，則應用程式可以藉由呼叫 [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) 函數來選取邏輯字型。 當初始化 **LOGFONT** 結構的成員時，請務必在 **lfCharSet** 成員中指定特定字元集。 這個成員在字型對應程式中很重要，如果這個成員未正確初始化，結果會不一致。 如果您在 **LOGFONT** 結構的 **lfFaceName** 成員中指定了字樣名稱，請確定 **lfCharSet** 值符合 **lfFaceName** 中指定的字樣字元集。 例如，如果您想要選取 MS Mincho 等字型， **lfCharSet** 必須設定為預先定義的 SHIFTJIS \_ 字元集值。

許多東亞語言的字型都有兩個字型名稱：英文名稱和當地語系化名稱。 [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta)、 [**CreateFontIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirecta)和 [**CreateFontIndirectEx**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirectexa) 會針對符合語言的系統地區設定採用當地語系化的字樣名稱，但會針對所有其他的系統地區設定採用英文的字樣名稱。 最佳方法是嘗試一個名稱，並在失敗時嘗試另一個名稱。 請注意，如果系統地區設定與字型的語言不符， [**EnumFonts**](/windows/win32/api/wingdi/nf-wingdi-enumfontsa)、 [**>enumfontfamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa)和 [**EnumFontFamiliesEx**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesexa) 會傳回英文字型名稱。 從 Windows 2000 開始，這不再是問題，因為 [**CreateFont**](/windows/win32/api/wingdi/nf-wingdi-createfonta)、 [**CreateFontIndirect**](/windows/win32/api/wingdi/nf-wingdi-createfontindirecta)和 [**CreateFontIndirectEx**](/windows/win32/api/wingdi/nf-wingdi-createfontindirectexa)的字型對應程式都會辨識字型名稱，不論地區設定為何。

 

 
