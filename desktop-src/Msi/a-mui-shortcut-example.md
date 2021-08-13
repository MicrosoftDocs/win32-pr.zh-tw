---
description: 本節說明如何將資源字串加入 Windows Installer 的快捷方式資料表中，以供 (MUI) 的多語系使用者介面使用。
ms.assetid: f521cfb8-32a8-4b62-b258-5b99cc3e0416
title: MUI 快捷方式範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b38f674a63e854fbcd4439229c5aded5b0efe6cfc17d3e475f8a52f30db949
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640285"
---
# <a name="a-mui-shortcut-example"></a>MUI 快捷方式範例

本節說明如何將資源字串加入 Windows Installer 的[快捷方式](shortcut-table.md)資料表中，以供 (MUI) 的多語系使用者介面使用。

**Windows Installer 2.0 和 Windows Installer 3.0：** 不支援。 此範例需要 Windows Installer 4.0。

如需如何開發具備 MUI 功能的應用程式的相關資訊，請參閱[多語系消費者介面 (MUI) ](/windows/desktop/Intl/multilingual-user-interface)檔。

將 Windows Vista 多語系使用者介面所使用的資源字串新增至 Windows Installer 封裝：

1.  將所有語言中性和語言檔案的資訊新增至檔案 [資料表](file-table.md)。 例如，檔案可能包含語言中性檔案 (msimsg.dll) 和英文的語言檔案（英文） (msimsgen.dll mui) 、日文 (msimsgja.dll mui) 和中文 (msimsgcs.dll mui) 。 每個檔案都可以屬於不同的元件。 每個檔案都可以同時具有完整和簡短的檔案名。 在此範例中，您可以將下列資訊新增至檔案 [資料表](file-table.md)。

    [檔資料表](file-table.md) (部分) 

    

    | 檔案        | 元件\_     | FileName                     |
    |-------------|-----------------|------------------------------|
    | msimsgmuija | MSIMSG \_ MUI \_ JA-JP | msimsgja.dll\|msimsg.dll mui |
    | msimsgmuics | MSIMSG \_ MUI \_ CS | msimsgcs.dll\|msimsg.dll mui |
    | msimsgmuien | MSIMSG \_ MUI \_ EN | msimsgen.dll\|msimsg.dll mui |
    | msimsgdll   | MSIMSG          | msimsg.dll                   |

    

     

2.  將資訊新增至這些元件的 [元件資料表](component-table.md) 中。 每個元件都有唯一的 GUID 識別碼，應該輸入至元件資料表的 [元件識別碼] 欄位。 屬於元件的檔案可作為該元件的 KeyPath。 您可以在 [目錄] 欄位中指定包含每個元件的目錄 \_ 。 您可以將下列資訊加入元件資料表中。

    [元件資料表](component-table.md) (部分) 

    

    | 元件       | 目錄\_   | KeyPath     |
    |-----------------|---------------|-------------|
    | MSIMSG \_ MUI \_ JA-JP | MUIFolder \_ ja-jp | msimsgmuija |
    | MSIMSG \_ MUI \_ CS | MUIFolder \_ CS | msimsgmuics |
    | MSIMSG \_ MUI \_ EN | MUIFolder \_ EN | msimsgmuien |
    | MSIMSG          | MUIFolder     | msimsgdll   |

    

     

3.  編輯 [目錄](directory-table.md) 資料表，讓元件安裝在正確的目錄中。 請務必包含要安裝快捷方式之目錄的相關資訊。 例如，下列資訊可能會新增至封裝的目錄資料表，以安裝元件和位於 DesktopFolder 目錄中的快捷方式。

    [目錄資料表](directory-table.md) (部分) 

    

    | 目錄     | 目錄 \_ 父系 | DefaultDir |
    |---------------|-------------------|------------|
    | TARGETDIR     |                   | SourceDir  |
    | MsiTest       | TARGETDIR         | MsiTest:.  |
    | MUIFolder     | MsiTest           | 梅        |
    | MUIFolder \_ CS | MUIFolder         | cs-CZ      |
    | MUIFolder \_ EN | MUIFolder         | en-US      |
    | MUIFolder \_ ja-jp | MUIFolder         | ja-JP      |
    | DesktopFolder | TARGETDIR         | .          |

    

     

4.  將資料列新增至每個快捷方式的 [快速鍵](shortcut-table.md) 對應表。 例如，此 [快捷方式](shortcut-table.md) 表可以針對安裝在 DirectoryFolder 目錄中的兩個快捷方式（Quick1 和 Quick2），包含下列資訊。 每個快捷方式都屬於目標欄位中指定的功能。 與快捷方式相關聯的圖示可以在圖示 \_ 欄位和 [圖示](icon-table.md) 表格中指定。

     (部分) 的[快捷方式資料表](shortcut-table.md)

    

    | 快速鍵 | 目錄\_   | 元件\_ | 目標               | 圖示             |
    |----------|---------------|-------------|----------------------|------------------|
    | Quick1   | DesktopFolder | MSIMSG      | FeatureChild1 \_ 本機 | HelpFileIcon.exe |
    | Quick2   | DesktopFolder | MSIMSG      | FeatureChild1 \_ 本機 | HelpFileIcon.exe |

    

     

5.  將資訊加入功能 [資料表](feature-table.md) 資料表中，該功能擁有的快捷方式屬於。 當快捷方式啟動時，安裝程式會先確認所有屬於這項功能的元件都已安裝，然後才會啟動 \_ [快速鍵](shortcut-table.md) 表格之 component 資料行中所指定元件的金鑰檔。 在此範例中，您可以將下列資訊加入至 FeatureParent1 本機功能的功能資料表資料表中 \_ 。

    [功能表](feature-table.md) (部分) 

    

    | 功能               | 功能 \_ 父系       | Title                 | 屬性 |
    |-----------------------|-----------------------|-----------------------|------------|
    | FeatureParent1 \_ 本機 |                       | FeatureParent1 \_ 本機 | 16         |
    | FeatureChild1 \_ 本機  | FeatureParent1 \_ 本機 | FeatureParent1 \_ 本機 | 0          |

    

     

6.  針對每個新的快捷方式，將資源字串資訊加入至 [快捷方式資料表](shortcut-table.md)的 DisplayResourceDLL、DisplayResourceId、DescriptionResourceDLL 和 DescriptionResourceId 欄位中。 DisplayResourceDLL 和 DescriptionResourceDLL 欄位包含 [格式化](formatted.md) 字串格式的資源字串。 格式化的字串可以使用 \[ \#  \] [格式化](formatted.md)格式的 filekey 慣例。 在 [DisplayResourceId] 和 [DescriptionResourceId] 欄位中，加入資源字串的顯示和描述索引。

     (部分) 的[快捷方式資料表](shortcut-table.md)

    

    | 快速鍵 | DisplayResourceDLL | DisplayResourceId | DescriptionResourceDLL | DescriptionResourceId |
    |----------|--------------------|-------------------|------------------------|-----------------------|
    | Quick1   | \[\#msimsgdll\]    | 36                | \[\#msimsgdll\]        | 37                    |
    | Quick2   | \[\#msimsgdll\]    | 38                | \[\#msimsgdll\]        | 39                    |

    

     

7.  安裝封裝之後，請進行測試以確保多語系消費者介面如預期般運作。

 

 
