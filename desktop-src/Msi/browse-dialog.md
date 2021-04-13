---
description: '[流覽] 對話方塊可讓使用者選取目錄。 目錄不一定要存在，而且可以使用此控制項來建立。'
ms.assetid: 35b991b8-d291-44ef-b1c0-8128bed3c3c8
title: 流覽對話方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f6d3c3d95caec7e9a439621f6741b0dceb0c83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386199"
---
# <a name="browse-dialog"></a>流覽對話方塊

[流覽] 對話方塊可讓使用者選取目錄。 目錄不一定要存在，而且可以使用此控制項來建立。

這種類型的對話方塊通常包含下列三個控制項。 這些控制項會連接至相同的屬性。 該屬性是要選取的路徑。

-   [PathEdit 控制項](pathedit-control.md)，可選取路徑的 tail 區段。 如果輸入的尾在目前磁片區上無效，則此控制項不會遺失焦點。
-   [DirectoryCombo 控制項](directorycombo-control.md)，可顯示 PathEdit 控制項所顯示之目前選取的路徑。 此控制項不會顯示路徑的最後一個區段。
-   [DirectoryList 控制項](directorylist-control.md)，可顯示 DirectoryCombo 目前所顯示之目錄底下的資料夾。 這也可能會顯示尚未建立的資料夾。

[流覽] 對話方塊通常也包含 [DirectoryCombo 控制項](directorycombo-control.md) ，可指定要顯示的磁片區類型。 在 [流覽] 對話方塊上顯示的所有磁片區類型都很常見。

流覽對話方塊通常包含三個 [按鈕控制項](pushbutton-control.md)。 這些按鈕會連結至 [ControlEvent 資料表](controlevent-table.md)中各自的事件。 這些按鈕可用來啟用下列控制項選項。



| Control 選項 | ControlEvent                                            |
|----------------|---------------------------------------------------------|
| 移到上一層   | [DirectoryListUp](directorylistup-controlevent.md)     |
| 新增資料夾     | [DirectoryListNew](directorylistnew-controlevent.md)   |
| 開啟           | [DirectoryListOpen](directorylistopen-controlevent.md) |



 

若要讓 [新增資料夾] 選項使用非預設的資料夾名稱，必須在 [UIText 資料表](uitext-table.md)中指定新資料夾的路徑。 路徑字串應該使用「簡短檔案名 \| 長檔名」形式的檔案名。 例如，使用 "MyProd ~ 1 \| My Fabulous Product" 之類的檔案名。 如需檔案名格式的詳細資訊，請參閱 [Filename](filename.md) 資料行資料類型。 如果路徑不存在於 UIText 資料表中，或設定為無效值，則預設會將它設定為 "Fldr \| New Folder" 值。 如果對話方塊只需要搜尋現有的資料夾，就可以省略 [ **新增資料夾** ] 按鈕。

 

 



