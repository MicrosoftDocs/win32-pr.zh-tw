---
description: 為了協助支援應用程式中的筆跡，有兩個物件可以內嵌，而且任何 OLE 容器都支援這些物件。
ms.assetid: fbd7bdf0-63b4-48d1-be91-eabbbb3f1618
title: sInk 和 tInk 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8e25e1f258ac789382475666878c986f5053323a1b19bf8f4b6110c096f2fd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091294"
---
# <a name="sink-and-tink-objects"></a>sInk 和 tInk 物件

為了協助支援應用程式中的筆跡，有兩個物件可以內嵌，而且任何 OLE 容器都支援這些物件。 其產生方式是呼叫 **ClipboardCopy 方法 (矩形、InkClipboardFormats、InkClipboardModes) 或****方法 (筆觸、InkClipboardFormats、InkClipboardModes)** 方法，以及：

-   文字筆墨物件 (tInk) 。 這是代表預期會形成單字之筆墨的 OLE 物件。 TInk 物件可讓手寫筆跡轉換成文字，可作為辨識器傳回的文字，或是取自辨識替代項的清單中所做的選擇。 您可以透過程式設計方式設定筆墨的色彩和大小，而且可以根據物件周圍文字的屬性來設定。 TInk 物件的目的是要包含單一單字。TInk 物件是一個小型的輕量物件，可執行簡單的作業，例如轉譯 (提供裝置內容的控制碼 (HDC) 和 RECT) ，並在給定資料流程 (時保存本身) 。 使用 tInk 物件時，在使用手寫和文字輸入的應用程式中工作時，可提供順暢的使用者體驗。
-    (接收器) 草繪筆墨物件。 這是代表不需要形成單字之筆墨的 OLE 物件。 接收物件會被解釋為繪圖。 接收物件也適合用來表示多個單字。

這些物件可用於應用程式之間的互通性，方法是將它們放在剪貼簿上的 OLE 物件位置，或是以 Rtf)  (RTF 格式來內嵌它們。

您可以透過下列方式使用 tInk 和接收物件：

-   Microsoft Word 2002 都支援 tInk 和接收物件。 使用者可以使用 Word 2002 中提供的「書寫」和「繪製文字輸入面板」，將筆墨插入 Word 檔中。 這個筆墨會以具有接收器或 tInk 物件之 CLSID 的 OLE 物件形式內嵌至 Word 檔案。
-   Tablet PC [InkEdit](/previous-versions/ms552265(v=vs.100)) 控制項會使用 tInk 物件。 InkEdit 控制項是標準 [RichTextBox](/dotnet/api/system.windows.forms.richtextbox?view=netcore-3.1) 控制項的子類別。 筆墨會以 tInk 物件的形式插入 InkEdit 控制項的 RTF 資料流程中。
-   當應用程式將選取的 [筆墨](/previous-versions/aa515768(v=msdn.10)) 物件移到剪貼簿時，Ole 物件剪貼簿位置會包含 TInk 或接收 ole 物件。

例如，您的應用程式可以辨識手寫，並將任何 [筆墨](/previous-versions/aa515768(v=msdn.10)) 物件標示為 tInk 物件。 然後，如果您選取筆跡中的單字，並將其複製並貼到 Word 中，則會在 Word 2002 中顯示該單字的替代項。

> [!Note]  
> 當您將接收器或 tInk 物件放在剪貼簿上作為 OLE 物件時，Tablet PC 平臺的剪貼簿支援會自動為您選取增強的中繼檔 (EMF) 旗標。 物件本身會儲存在 [剪貼簿] 的 [剪貼簿] 和 [物件描述項位置] 中。

 

另一個範例是，藉由使用接收物件，您可以在應用程式中繪製筆墨草圖、將草圖複製並貼上至 Word 2002，然後使用 Word 中的 [Tablet PC 輸入面板] 編輯繪圖。

為了成功包含 tInk 物件，應用程式必須針對内嵌物件執行 OLE 容器支援。 然後，若要讓容器完全支援 tInk，您必須建立：

-   修改程式碼以進行尋找和取代。 這些物件的類型必須是查核，而不是略過搜尋中的內嵌物件。 如果它們是 tInk 物件，則必須將它們具現化，並針對其對應的文字進行查詢。
-   修改選取行為。 TInk 物件的選取範圍絕對不應該與調整大小控點一起出現。 它們的選取方式應該與檔中選取文字的方式相同。 物件的選取程式碼必須偵測型別是否為 tInk，並適當地顯示選取範圍。
-   環境屬性的使用。 字型大小、色彩和粗體格式等環境屬性必須傳送至 tInk 物件。 這些屬性的應用會變更手寫筆跡的寬度，因此需要透過呼叫 [**GetInkExtent 方法**](/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-getinkextent) 或 [IOleObject：： GetExtent](/windows/win32/api/oleidl/nf-oleidl-ioleobject-getextent) 方法來更新大小。
-   覆寫預設 [IOleObject：:D overb](/windows/win32/api/oleidl/nf-oleidl-ioleobject-doverb) 方法處理。 這可讓轉換成文字以將 tInk 物件的批次傳遞至辨識器，然後將這些文字分成辨識區段。

如需將字詞細分為辨識區段的詳細資訊，請參閱辨識 [區段](recognition-segments.md)。

 

 
