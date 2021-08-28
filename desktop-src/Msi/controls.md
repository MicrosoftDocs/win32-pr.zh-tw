---
description: 安裝套件的開發人員可以撰寫一個使用者介面，其中包含本主題所討論的控制項。
ms.assetid: ed9fa158-9dad-4d2d-8153-78122b19a34e
title: '控制 (Windows Installer) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47755cafc3d4d3d04ed443410571a9c4fc2cf215a3efb3584265dcbeb2f9d520
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143362"
---
# <a name="controls-windows-installer"></a>控制 (Windows Installer) 

安裝套件的開發人員可以撰寫一個使用者介面，其中包含本主題所討論的控制項。 如需有關如何將特定控制項新增至對話方塊的詳細資訊，請參閱該控制項的主題，並閱讀 [加入控制項和文字](adding-controls-and-text.md)的區段。

某些控制項（例如 CheckBox 和 ComboBox）會與 [控制資料表](control-table.md)的屬性資料行中指定的屬性相關聯。 使用者藉由與控制項互動來變更這個屬性的值。 被動式控制項（例如佈告欄和 bitmap）不會與這類屬性相關聯。

基於安全性，使用者無法與使用者介面互動來變更私用屬性。 對於要由使用者介面設定的屬性，它必須是公用屬性且為大寫。 另請參閱 [屬性](about-properties.md)。

在某些情況下，取消對話方塊時可能會不正確地重新繪製控制項。 這必須以控制項在 \_ 移除取消對話方塊之後收到 WM 油漆訊息的順序來進行。 若要修正此問題，請嘗試變更控制資料表中控制項的順序。



| 控制項名稱                                       | 相關聯的屬性 | 控制項的簡短描述                                                                                                                                                          |
|----------------------------------------------------|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [廣告 牌](billboard-control.md)                 | No                  | 根據進度訊息顯示公告欄。                                                                                                                                       |
| [點陣圖](bitmap-control.md)                       | No                  | 顯示點陣圖的靜態圖片。                                                                                                                                                |
| [CheckBox](checkbox-control.md)                   | Yes                 | 兩個狀態的核取方塊。                                                                                                                                                                |
| [ComboBox](combobox-control.md)                   | Yes                 | 具有編輯欄位的下拉式清單。                                                                                                                                                  |
| [DirectoryCombo](directorycombo-control.md)       | Yes                 | 除了路徑的最後一個區段之外，請選取 [全部]。                                                                                                                                       |
| [DirectoryList](directorylist-control.md)         | Yes                 | 顯示路徑主要部分底下的資料夾。                                                                                                                                         |
| [編輯](edit-control.md)                           | Yes                 | 任何字串或整數的一般編輯欄位。                                                                                                                                       |
| [GroupBox](groupbox-control.md)                   | No                  | 顯示將其他控制項群組在一起的矩形。                                                                                                                             |
| [超連結](hyperlink-control.md)                 | No                  | 顯示位址的 HTML 連結，此連結會在預設瀏覽器中開啟。**[Windows Installer 4.5 及更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。<br/> |
| [圖示](icon-control.md)                           | No                  | 顯示圖示的靜態圖片。                                                                                                                                                 |
| [線條](line-control.md)                           | No                  | 顯示水平線條。                                                                                                                                                           |
| [ListBox](listbox-control.md)                     | Yes                 | 沒有編輯欄位的下拉式清單。                                                                                                                                               |
| [ListView](listview-control.md)                   | Yes                 | 顯示值的資料行，其中包含選取的圖示。                                                                                                                                 |
| [MaskedEdit](maskededit-control.md)               | Yes                 | 文字欄位中包含遮罩的編輯欄位。                                                                                                                                          |
| [PathEdit](pathedit-control.md)                   | Yes                 | 顯示 [編輯] 欄位中的資料夾名稱或整個路徑。                                                                                                                                 |
| [ProgressBar 控制項](progressbar-control.md)     | No                  | 在接收進度訊息時變更長度的橫條圖。                                                                                                                       |
| [按鈕](pushbutton-control.md)               | No                  | 顯示基本的推播按鈕。                                                                                                                                                         |
| [RadioButtonGroup](radiobuttongroup-control.md)   | Yes                 | 一組選項按鈕。                                                                                                                                                             |
| [ScrollableText](scrollabletext-control.md)       | No                  | 顯示長字串的文字。                                                                                                                                                       |
| [SelectionTree](selectiontree-control.md)         | Yes                 | 顯示功能表中的資訊，並讓使用者變更其選取狀態。                                                                                     |
| [Text](text-control.md)                           | No                  | 顯示靜態文字。                                                                                                                                                                 |
| [VolumeCostList](volumecostlist-control.md)       | No                  | 顯示不同磁片區的成本資訊。                                                                                                                                    |
| [VolumeSelectCombo](volumeselectcombo-control.md) | Yes                 | 從按字母順序的清單中選取磁片區。                                                                                                                                             |



 

 

 




