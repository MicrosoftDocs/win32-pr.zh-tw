---
description: 在 Windows 7 和更新版本中，您可以使用 Desktop.ini 將動詞新增至資料夾。 如需 Desktop.ini 檔案的詳細資訊，請參閱如何使用 Desktop.ini 自訂資料夾。
ms.assetid: F03AB35D-FBFE-46C2-A37F-F70C18219B9A
title: 如何透過 Desktop.ini 為資料夾執行自訂動詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133726133abe884863a0b4d2abc0cc76aab1310a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973145"
---
# <a name="how-to-implement-custom-verbs-for-folders-through-desktopini"></a>如何透過 Desktop.ini 為資料夾執行自訂動詞

在 Windows 7 和更新版本中，您可以使用 Desktop.ini 將動詞新增至資料夾。 如需 Desktop.ini 檔案的詳細資訊，請參閱 [如何使用 Desktop.ini自訂資料夾 ](how-to-customize-folders-with-desktop-ini.md)。

> [!Note]  
> Desktop.ini 的檔案應該一律標示為  +  **隱藏** 系統，使其不會顯示給使用者。

 

若要透過 Desktop.ini 檔新增資料夾的自訂動詞命令，請執行下列步驟。

## <a name="instructions"></a>指示

### <a name="step-1"></a>步驟 1:

建立標示為 **唯讀** 或 **系統** 的資料夾。

### <a name="step-2"></a>步驟 2:

建立包含的 Desktop.ini 檔案 \[ 。ShellClassInfo \] DirectoryClass = Folder ProgID。

### <a name="step-3"></a>步驟 3：

在登錄中，使用 CanUseForDirectory 的值建立 **HKEY \_ 類別 \_ 根** \\ **資料夾 ProgID** 。 CanUseForDirectory 值可避免誤用未設定為透過 Desktop.ini 為資料夾執行自訂動詞命令的 Progid。

### <a name="step-4"></a>步驟 4：

在 **資料夾** ProgID 子機碼底下新增動詞，例如：

```
HKEY_CLASSES_ROOT
   CustomFolderType
      Shell
         MyVerb
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
```

## <a name="remarks"></a>備註

> [!Note]  
> 這些動詞命令可以是預設動詞，在此情況下，按兩下資料夾會啟動動詞。

 

 

 



