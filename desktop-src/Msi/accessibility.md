---
description: 當設計其 UI 以符合 Active Accessibility 指導方針時，作者應留意下列清單中的資料表和欄位。
ms.assetid: 516e504e-7895-4388-a38e-fd2fc7dfd61d
title: '存取範圍 (Windows Installer) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46325c11337ef1e1db6f2da5728f06f9d4ee0649
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848996"
---
# <a name="accessibility-windows-installer"></a>存取範圍 (Windows Installer) 

當設計其 UI 以符合 Active Accessibility 指導方針時，作者應留意下列清單中的資料表和欄位。 安裝程式套件的使用者介面應該輔助應用程式或產品的協助工具給所有使用者。

-   工具提示文字會包含在 [控制資料表](control-table.md)的 [說明] 資料行中。 螢幕讀取器會針對包含圖片的控制項顯示此文字。
-   永遠不會顯示[VolumeCostList](volumecostlist-control.md)、 [ListView](listview-control.md)、 [DirectoryList](directorylist-control.md)和[SelectionTree](selectiontree-control.md)控制項之[控制資料表](control-table.md)的文字欄位。 相反地，螢幕審核公用程式會將它讀取為控制項的描述。 無法在螢幕上使用視覺資訊的人，可以使用螢幕評論公用程式的輔助工具來解讀資訊。 螢幕流覽公用程式 (也稱為螢幕瀏覽器程式或語音存取公用程式) 取得畫面上顯示的資訊，並透過替代媒體（例如合成語音或可重新整理的盲文顯示器）將它導向。
-   對話方塊中的控制項應使用 \_ [控制資料表](control-table.md)的 [下一步] 欄位來連結。 您必須撰寫這些控制項，才能使用 TAB 鍵來達成這些控制項。
-   應提供快速鍵以直接取得控制項的存取權。
-   使用者介面中顯示的文字色彩會設定在文字文字 [資料表](textstyle-table.md)中。 如果選擇的文字色彩太接近背景，則會忽略文字的色彩選擇。
-   文字大小和字型是在文字文字 [表格](textstyle-table.md)中設定。 適用于亞洲市場的套件應使用較大的字型大小。 例如，針對英文文字可辨認的10點字型大小，在中文中不一定是 true。
-   針對 [Edit](edit-control.md)、 [PathEdit](pathedit-control.md)、 [ListView](listview-control.md)、 [ComboBox](combobox-control.md) 或 [VolumeSelectCombo 控制項](volumeselectcombo-control.md)，螢幕讀取器會從 [文字控制項](text-control.md) 取得 accName 和 accKeyboardShortcut，而該控制項必須在控制項 \_ 下一個對話方塊順序的控制項之前。 螢幕讀取器會從文字控制項的文字欄位 accName，然後從文字欄位中的鍵盤快速鍵（如果有快速鍵的話） accKeyboardShortcut。
-   由於靜態文字無法取得焦點，因此必須將描述[編輯](edit-control.md)、 [PathEdit](pathedit-control.md)、 [ListView](listview-control.md)、 [ComboBox](combobox-control.md)或[VolumeSelectCombo 控制項](volumeselectcombo-control.md)的[文字控制項](text-control.md)設為對話方塊中的第一個控制項，以確保與螢幕讀取器的相容性。
-   如果是顯示圖示或點陣圖影像的 [按鈕控制項](pushbutton-control.md) ，AccName 和 accKeyboardShortcut 會指定于 [控制項資料表](control-table.md) 記錄的 [說明] 欄位中，位於分隔符號的左邊 \| 。
-   避免在白色點陣圖上使用文字控制項，因為在高對比黑色時，文字可能會變得不可見。
-   請勿在背景中放入全白色點陣圖影像的黑色文字控制項。 將 Windows 顯示變更為高對比黑色的使用者看不到這個文字。
-   請勿將白色文字控制項放在全部為黑色點陣圖影像的背景上。 將 Windows 顯示變更為高對比白色的使用者看不到這個文字。
-   請勿將透明 [文字控制項](text-control.md) 放在彩色點陣圖上方。 如果使用者變更顯示色彩配置，可能看不到文字。 例如，如果使用者設定協助工具的高對比參數，文字可能會變成隱藏。
-   請注意，在選取群組中的其中一個按鈕之前，不會將焦點放在對話方塊上的 [RadioButtonGroup 控制項](radiobuttongroup-control.md) 。 若要將 [焦點] 索引標籤設為這個按鈕群組，請將其中一個按鈕指定為控制項的預設設定。
-   為螢幕閱讀程式提供有關 [RadioButtonGroup 控制項](radiobuttongroup-control.md)的額外描述性文字。 遵循 [將額外文字新增至選項按鈕](adding-extra-text-to-radio-buttons.md)所提供的範例。
-   對話方塊的相對大小、控制項和字型可以根據所選的字型大小而變更。 如需詳細資訊，請參閱 [安裝程式單位](installer-units.md)。 為了確保在使用者介面中正確顯示文字和控制項，安裝程式開發人員應該一律使用可能使用的所有字型大小來測試其應用程式。

 

 



