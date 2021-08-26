---
description: 除了先前章節討論的資訊之外，uisample.msi 也包含範例使用者介面的資料。
ms.assetid: 7e4ae4b8-e7b2-49b3-97b7-374b69006a2f
title: 匯入消費者介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2678eb2c6fb1c53f0d052c6bb1553af0f3d773b75d057969c66d74a39e499f35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043638"
---
# <a name="importing-the-user-interface"></a>匯入消費者介面

除了先前章節討論的資訊之外，uisample.msi 也包含範例使用者介面的資料。 如果您將 uisample.msi 合併到匯 [入空白資料庫](importing-a-blank-database.md)區段中的 MNP2000.msi，則這項資訊也會出現在 MNP2000.msi 中。 範例使用者介面的資訊如下表所示。

-   [ActionText 資料表](actiontext-table.md)
-   [二進位資料表](binary-table.md)
-   [控制資料表](control-table.md)
-   [ControlEvent 資料表](controlevent-table.md)
-   [對話方塊資料表](dialog-table.md)
-   [錯誤資料表](error-table.md)
-   [EventMapping 資料表](eventmapping-table.md)
-   [選項按鈕資料表](radiobutton-table.md)
-   [樣式表單](textstyle-table.md)
-   [UIText 資料表](uitext-table.md)

安裝程式隨附的資料庫編輯器 Orca 包含對話方塊預覽選項，可讓您用來預覽上表中的資料所指定之使用者介面的對話方塊。

MNP2000.msi 安裝套件範例現在已準備好進行封裝驗證。 在第一次嘗試安裝封裝之前，請一律在新的封裝上執行驗證。 這會在驗證安裝範例中討論。

如果您不想要在範例封裝中包含使用者介面，請省略或移除上述表格中的所有資訊，但不包括用來定義 [**DefaultUIFont**](defaultuifont.md)屬性) 所需的 [[樣式表單] 表格](textstyle-table.md) (。 您也應該從 [屬性資料表](property-table.md)中移除使用者介面屬性。 沒有 UI 的記事本範例屬性工作表如下所示。 如果您複製此範例，請不要重複使用表格中顯示的 Guid。

[屬性工作表](property-table.md)



| 屬性                                   | 值                                  |
|--------------------------------------------|----------------------------------------|
| [**DefaultUIFont**](defaultuifont.md)     | DlgFont8                               |
| [**INSTALLLEVEL**](installlevel.md)       | 3                                      |
| [**LIMITUI**](limitui.md)                 | 1                                      |
| [**製造商**](manufacturer.md)       | Microsoft                              |
| [**ProductCode**](productcode.md)         | {18A9233C-0B34-4127-A966-C257386270BC} |
| [**ProductLanguage**](productlanguage.md) | 1033                                   |
| [**ProductName**](productname.md)         | MNP2000                                |
| [**ProductVersion**](productversion.md)   | 01.40.0000                             |
| [**UpgradeCode**](upgradecode.md)         | {908E378A-9551-4772-BF1D-5CFAF6FD9CB4} |



 

您可以從命令列或從程式安裝沒有使用者介面的封裝。 若要從命令列安裝封裝，請使用 [命令列選項](command-line-options.md)中所述的方法。 若要從程式安裝套件，請使用 [使用安裝程式函數](using-installer-functions.md)中所述的方法。 在第一次嘗試安裝新套件之前，請一律在新的封裝上執行驗證。

[繼續](validating-an-installation-database.md)

 

 



