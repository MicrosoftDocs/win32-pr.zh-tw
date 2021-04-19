---
description: 放在對話方塊和公告欄上的控制項和文字，可讓使用者與安裝程式互動。
ms.assetid: 2c6204c7-535d-4dda-8394-723ddbf46b96
title: 加入控制項和文字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706d071741d742205d0df2b19c4416acf355fd7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979107"
---
# <a name="adding-controls-and-text"></a>加入控制項和文字

放在對話方塊和公告欄上的控制項和文字，可讓使用者與安裝程式互動。 將對話方塊加入至 [對話方塊資料表](dialog-table.md) 中，將它加入至使用者介面，如 [使用消費者介面](using-the-user-interface.md)所述。 填入 [控制項資料表](control-table.md) 和 [BBControl 資料表](bbcontrol-table.md)，以填滿對話方塊並公告欄控制項。

控制項的初始屬性可以在 [控制資料表](control-table.md)的 [屬性] 資料行中指定。 請參閱 [控制項屬性](control-attributes.md)。

若要讓控制項屬性相依于條件，請使用 [ControlCondition 資料表](controlcondition-table.md) 來根據屬性或條件陳述式的值來停用、啟用、隱藏或顯示控制項。 您也可以使用此資料表來覆寫在 [對話方塊資料表](dialog-table.md)中輸入之預設控制項的規格。

若要讓事件變更控制項屬性，請將控制項訂閱至 [EventMapping 資料表](eventmapping-table.md)中的 ControlEvent。 ControlEvent 指定安裝程式所要採取的動作，或對話方塊中一或多個控制項的屬性變更。 請參閱 [ControlEvent 總覽](controlevent-overview.md)。 在 [屬性] 資料行中輸入屬性的識別碼，並在 [EventMapping 資料表](eventmapping-table.md)的事件資料行中輸入 ControlEvent 的識別碼。

某些控制項有助於收集使用者的資訊。 例如，核取方塊可讓使用者設定屬性的值。 請參閱 [核取方塊](checkbox-table.md)資料表、 [ComboBox](combobox-table.md)資料表、 [ListBox 資料表](listbox-table.md)、 [選項按鈕資料表](radiobutton-table.md)和 [ListView 資料表](listview-table.md)。

請注意，基於安全性考慮，使用者與使用者介面互動時，無法變更私用屬性。 如果屬性是由使用者介面設定，它就必須是公用屬性，而且在全部大寫的情況下都必須有名稱。 請參閱 [關於屬性](about-properties.md)。

您可以藉由填入 [ActionText 資料表](actiontext-table.md)，讓對話方塊顯示資訊給使用者，或將其寫入至記錄以回應安裝動作。

控制項可以有預先定義的字型樣式。 若要設定文字字串的字型與字型樣式，請在顯示的字元字串前面加上 { \\ style} 或 {&*style*}。 其中 style 是在 [資料行] 資料表的 [樣式 [表單](textstyle-table.md)] 資料行中所列的識別碼。 如果這兩個都不存在，但 [**DefaultUIFont**](defaultuifont.md) 屬性定義為有效的文字樣式，則會使用該字型。

建議您在 [屬性工作表](property-table.md)中，將每個安裝封裝的 [**DefaultUIFont**](defaultuifont.md)屬性設定為 [[樣式](textstyle-table.md)表單] 中所列的其中一個預先定義樣式。 如果未指定這個屬性，安裝程式會使用系統字型。 如果封裝的字碼頁與使用者的預設 UI 字碼頁不同，這可能會導致安裝程式不正確地顯示文字字串。

對於大部分的控制項而言，會使用資料庫字碼頁所指定的字元集來顯示文字。 這可確保使用正確的字元集搭配資料庫中包含的資訊。 例外狀況是 [編輯](edit-control.md)、 [DirectoryList](directorylist-control.md)、 [PathEdit](pathedit-control.md)和 [DirectoryCombo](directorycombo-control.md) 控制項，一律會使用使用者的預設 UI 字元集來顯示文字。 如果已設定[UsersLanguage 控制項屬性](userslanguage-control-attribute.md)，則[文字](text-control.md)、 [ListBox](listbox-control.md)和[COMBOBOX](combobox-control.md)控制項會使用使用者的預設 UI 字元集。

在某些情況下，取消對話方塊時可能會不正確地重新繪製控制項。 這必須以控制項 \_ 在移除 [ **取消** ] 對話方塊之後收到 WM 油漆訊息的順序來進行。 若要修正此問題，請嘗試變更控制資料表中控制項的順序。

控制項的大小應該夠大，足以容納整個在所有字型大小設定中看到的文字。 如果 UI 中的文字可能會當地語系化，則控制項的大小應該夠大，足以容納整個當地語系化文字。 較大的字型大小或當地語系化的文字可能需要比原始文字更多的空間，而且可能會被變得太小的控制項截斷。 如需當地語系化 UI 文字的詳細資訊，請參閱一節： [當地語系化範例](a-localization-example.md)。

 

 



