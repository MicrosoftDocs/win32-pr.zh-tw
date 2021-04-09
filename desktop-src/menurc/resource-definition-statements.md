---
title: Resource-Definition 語句
description: 資源定義語句會定義資源編譯器放入資源 ( 中的資源。Res) 檔。
ms.assetid: f96b8c1e-8188-40b7-8eda-c13b61b8fc41
keywords:
- 資源編譯器，資源定義語句
- TEXTINCLUDE 資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8887c002bc3564288eb99fdb373ac26c286d1bf7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933227"
---
# <a name="resource-definition-statements"></a>Resource-Definition 語句

資源定義語句會定義資源編譯器放入資源 ( 中的資源。Res) 檔。 之後。Res 檔案會連結到可執行檔，應用程式可以視需要在執行時間載入其資源。 所有資源語句都會將識別名稱或數位與指定的資源產生關聯。

資源定義語句可以分為下列類別：

-   資源
-   控制項
-   陳述式

下表描述資源定義語句。

## <a name="resources"></a>資源



| 資源                                      | 描述                                                                                                                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**加速器**](accelerators-resource.md) | 定義功能表快速鍵。                                                                                                                                                  |
| [**點陣圖**](bitmap-resource.md)             | 藉由為點陣圖命名並指定包含該點陣圖的檔案名，來定義點陣圖。  (使用特定的點陣圖時，應用程式會依名稱要求。 )                           |
| [**游標**](cursor-resource.md)             | 藉由命名資料指標或動態資料指標，並指定包含該資料指標的檔案名，來定義它。  (使用特定的資料指標時，應用程式會依名稱要求它。 )        |
| [**對話 框**](dialog-resource.md)             | 定義應用程式可用來建立對話方塊的範本。                                                                                                          |
| [**DIALOGEX**](dialogex-resource.md)         | 定義應用程式可用來建立對話方塊的範本。                                                                                                          |
| [**字體**](font-resource.md)                 | 指定包含字型的檔案名。                                                                                                                              |
| [**HTML**](html-resource.md)                 | 指定 HTML 檔。                                                                                                                                                         |
| [**圖示**](icon-resource.md)                 | 藉由命名圖示或動畫圖標來定義它，並指定包含該圖示的檔案名。  (使用特定的圖示時，應用程式會依名稱要求。 )             |
| [**功能表**](menu-resource.md)                 | 定義功能表的外觀和功能。                                                                                                                                  |
| [**MENUEX**](menuex-resource.md)             | 定義功能表的外觀和功能。                                                                                                                                  |
| [**MESSAGETABLE**](messagetable-resource.md) | 藉由命名訊息資料表並指定包含它的檔案名，來定義訊息資料表。 檔案是訊息編譯器所產生的二進位資源檔。                |
| [**彈出**](popup-resource.md)               | 定義可以包含功能表項目和子功能表的功能表項目。                                                                                                                   |
| **PLUGPLAY**                                  | 已過時。                                                                                                                                                                       |
| [**RCDATA**](rcdata-resource.md)             | 定義資料資源。 資料資源可讓您在可執行檔中包含二進位資料。                                                                                      |
| [**STRINGTABLE**](stringtable-resource.md)   | 定義字串資源。 字串資源是可以從可執行檔載入的 Unicode 或 ASCII 字串。                                                            |
| **TEXTINCLUDE**                               | Visual C++ 所解讀的特殊資源。 如需詳細資訊，請參閱 [TN035](/cpp/mfc/tn035-using-multiple-resource-files-and-header-files-with-visual-cpp?view=vs-2019)。                                        |
| **TYPELIB**                                   | 與 [/TLBID](/cpp/build/reference/tlbid-specify-resource-id-for-typelib?view=vs-2019) 和 [/TLBOUT](/cpp/build/reference/tlbout-name-dot-tlb-file?view=vs-2019) 連結器選項搭配使用的特殊資源。 |
| [**使用者定義**](user-defined-resource.md) | 定義包含應用程式特定資料的資源。                                                                                                                     |
| [**VERSIONINFO**](versioninfo-resource.md)   | 定義版本資訊資源。 包含版本號碼、預定作業系統等資訊。                                                  |
| **Vxd**                                       | 已過時。                                                                                                                                                                       |



 

如需預先定義之 MFC 資源的詳細資訊，請參閱 [TN023](/cpp/mfc/tn023-standard-mfc-resources?view=vs-2019) 和 [TN024](/cpp/mfc/tn024-mfc-defined-messages-and-resources?view=vs-2019)。

## <a name="controls"></a>控制項



| 控制                                            | 描述                                                                 |
|----------------------------------------------------|-----------------------------------------------------------------------------|
| [**AUTO3STATE**](auto3state-control.md)           | 建立自動的三狀態核取方塊控制項。                         |
| [**AUTOCHECKBOX**](autocheckbox-control.md)       | 建立自動核取方塊控制項。                                     |
| [**AUTORADIOBUTTON**](autoradiobutton-control.md) | 建立自動選項按鈕控制項。                                  |
| [**相應**](checkbox-control.md)               | 建立核取方塊控制項。                                                |
| [**組合**](combobox-control.md)               | 建立下拉式方塊控制項。                                                |
| [**控制**](control-control.md)                 | 建立應用程式定義的控制項。                                     |
| [**CTEXT**](ctext-control.md)                     | 建立中央文字控制項。                                            |
| [**DEFPUSHBUTTON**](defpushbutton-control.md)     | 建立預設的按鈕控制項。                                       |
| [**EDITTEXT**](edittext-control.md)               | 建立編輯控制項。                                                    |
| [**分組**](groupbox-control.md)               | 建立群組框控制項。                                                |
| [**圖示**](icon-control.md)                       | 建立圖示控制項。 此控制項是顯示在對話方塊中的圖示。 |
| [**LISTBOX**](listbox-control.md)                 | 建立清單方塊控制項。                                                 |
| [**LTEXT**](ltext-control.md)                     | 建立靠左對齊的文字控制項。                                        |
| [**PUSHBOX**](pushbox-control.md)                 | 建立推框控制項。                                                 |
| [**按鈕**](pushbutton-control.md)           | 建立推播按鈕控制項。                                              |
| [**RADIOBUTTON**](radiobutton-control.md)         | 建立選項按鈕控制項。                                             |
| [**RTEXT**](rtext-control.md)                     | 建立靠右對齊的控制項。                                            |
| [**狀態列**](scrollbar-control.md)             | 建立捲軸控制項。                                               |
| [**STATE3**](state3-control.md)                   | 建立三個狀態的核取方塊控制項。                                    |



 

## <a name="statements"></a>陳述式



| 陳述式                                            | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**標題**](caption-statement.md)                 | 設定對話方塊的標題。                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**特徵**](characteristics-statement.md) | 指定可讀取或寫入資源定義檔之工具可以使用之資源的相關資訊。                                                                                                                                                                                                                                                                                                                                                                           |
| [**類**](class-statement.md)                     | 設定對話方塊的類別。                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**EXSTYLE**](exstyle-statement.md)                 | 設定對話方塊的延伸視窗樣式。                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**字體**](font-statement.md)                       | 設定系統將用來繪製對話方塊文字的字型。                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**語言**](language-statement.md)               | 將所有資源的語言設定為下一個 [**語言**](language-statement.md) 語句或檔案結尾。 當 **語言** 語句出現在 [**加速器**](accelerators-resource.md)、 [**對話方塊**](dialog-resource.md)、 [**功能表**](menu-resource.md)、 [**RCDATA**](rcdata-resource.md)或 [**STRINGTABLE**](stringtable-resource.md) 資源定義的主體開頭之前，指定的語言只會套用至該資源。 |
| [**功能表**](menu-statement.md)                       | 設定對話方塊的功能表。                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**MENUITEM**](menuitem-statement.md)               | 定義功能表項目。                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**風格**](style-statement.md)                     | 設定對話方塊的視窗樣式。                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**版本**](version-statement.md)                 | 針對可讀取或寫入資源定義檔的工具，指定可使用之資源的版本資訊。                                                                                                                                                                                                                                                                                                                                                                     |



 

 

 