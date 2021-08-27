---
description: 在 Windows 7 和更新版本中，您可以使用此主題中提供的程式，在登錄中使用子命令專案來建立串聯功能表。
title: 使用子命令登錄專案建立串聯功能表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f12eb473d45a3d3aef1b7cf8e7f6cc51a0d97aa5b9e60ee39681c80af459988
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111798"
---
# <a name="how-to-create-cascading-menus-with-the-subcommands-registry-entry"></a>如何使用子命令登錄專案建立串聯功能表

在 Windows 7 和更新版本中，您可以使用此主題中提供的程式，在登錄中使用子命令專案來建立串聯功能表。

## <a name="instructions"></a>指示

### <a name="step-1"></a>步驟 1:

在 **HKEY \_ 類別 \_ 根目錄** ProgID shell 下建立新的子機碼 \\  \\ ****，其中 *ProgID* 是您要新增串聯功能表的檔案類型。 您可以將這個新的子機碼命名為任何您想要的名稱。 在本主題的其餘部分，我們會將它稱為 *CascadeMenu*，如下列範例所示。

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
```

### <a name="step-2"></a>步驟 2:

將名為 "MUIVerb" 的專案（其類型為 **REG \_ Sz** 或 **reg \_ EXPAND \_**）新增至 *CascadeMenu* 子機碼。 將此專案指派為字串值，例如「測試 Cascade 功能表」。 一般來說，此字串是以 "，resource" 格式的資源參考形式提供 @file 。 不應設定 *CascadeMenu* 子機碼的 (預設) 值。

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
            (Default)
            MUIVerb = Test Cascade Menu
```

### <a name="step-3"></a>步驟 3：

將名為 "entry" 的專案（其類型為 **REG \_ Sz** 或 **reg \_ EXPAND \_**）新增至 *CascadeMenu* 子機碼。 以分號分隔的動詞清單，指派應出現在功能表上的動詞清單（以其所需的外觀順序表示）。

```
HKEY_CLASSES_ROOT
   ProgID
      Shell
         CascadeMenu
            SubCommands = Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
```

### <a name="step-4"></a>步驟 4：

針對您在子命令專案中使用的任何自訂靜態動詞方法，使用動詞執行來填入 **CommandStore** 子機碼;例如：

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  CommandStore
                     Shell
                        VerbName
                           command
                              (Default) = notepad.exe %1
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立靜態串聯功能表](creating-static-cascading-menus.md)
</dt> </dl>

 

 



