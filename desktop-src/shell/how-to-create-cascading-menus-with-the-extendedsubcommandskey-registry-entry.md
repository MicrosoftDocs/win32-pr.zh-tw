---
description: 在 Windows 7 和更新版本中，您可以使用 ExtendedSubCommandsKey 子機碼來建立擴充的串聯功能表。
ms.assetid: 6E8B4FB7-D4DB-4DBC-AF6F-59D02CB6AB13
title: 使用 ExtendedSubCommandsKey 登錄專案建立串聯功能表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 220a38825ae250a0d58d30bc7de93f290f819eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692984"
---
# <a name="how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a>如何使用 ExtendedSubCommandsKey 登錄專案建立串聯功能表

在 Windows 7 和更新版本中，您可以使用 **ExtendedSubCommandsKey** 子機碼來建立擴充的串聯功能表。

下列螢幕擷取畫面是延伸串聯功能表的範例。

![顯示裝置的擴充串聯功能表的螢幕擷取畫面](images/file-assoc/extendedsubcommandskey.png)

由於 **HKEY \_ 類別 \_ 根目錄** 是 **HKEY \_ 目前 \_ 使用者** 和 **HKEY \_ 本機 \_ 電腦** 的組合，因此您可以在 [ **HKEY \_ 目前 \_ 使用者** \\ **軟體** \\ **類別**] 子機碼下註冊該 subverbs。 這樣做的優點是不需要提高許可權。 其他檔案關聯可以藉由指定相同的 **ExtendedSubCommandsKey** 子機碼，重複使用這整組動詞。 如果您不需要重複使用這組動詞，可以列出父系下的動詞。 在此情況下，請確定父系的預設值是空的，如本節的登錄專案範例中所述。

## <a name="instructions"></a>指示

### <a name="step-1"></a>步驟 1:

在 **HKEY \_ 類別的 \_ 根目錄** ProgID shell CascadeMenuKey 底下建立子機碼， \\  \\  \\ 並指定 CascadeMenuKey 的名稱（例如 *CascadeTest*）。 然後加入 **REG \_ SZ** 型別的 MUIVerb 專案，並為它命名，例如「測試 Cascade」功能表2，如下列登錄範例所示。

```
HKEY_CLASSES_ROOT
   txtfile
      shell
         CascadeTest
            MUIVerb = Test Cascade Menu 2
```

### <a name="step-2"></a>步驟 2:

在您所建立的 *CascadeTest* 子機碼底下，新增 **ExtendedSubCommandsKey** 子機碼，然後將檔子命令 (的類型為 **REG \_ SZ**) ; 例如：

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         Test Cascade Menu 2
            (Default)
            ExtendedSubCommandsKey
               Layout
               Properties
               Select all
```

確定 [ *測試串聯功能表 2* ] 子機碼的預設值是空的，而且顯示為 [ **未設定) 的 (值**]。

### <a name="step-3"></a>步驟 3：

使用下列任何靜態動詞命令來填入 subverbs。 請注意，CommandFlags 子機碼代表 EXPCMDFLAGS 值。 如果您想要在 cascade 功能表項目之前或之後加入分隔符號，請使用 ECF \_ SEPARATORBEFORE (0x20) 或 ECF \_ SEPARATORAFTER (0x40) 。 如需這些 Windows 7 及更新版本旗標的說明，請參閱 [**IExplorerCommand：： GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags)。 ECF \_ SEPARATORBEFORE 僅適用于最上層的功能表項目。 MUIVerb 的類型為 **reg \_ SZ**，而 CommandFlags 的類型為 **reg \_ DWORD**。

```
HKEY_CLASSES_ROOT
   txtile
      Shell
         Test Cascade Menu 2
            (Default)
            ExtendedSubCommandsKey
               Shell
                  cmd1
                     MUIVerb = Notepad
                     command
                        (Default) = %SystemRoot%\system32\notepad.exe %1
                  cmd2
                     MUIVerb = Wordpad
                     CommandFlags = 0x20
                     command
                        (Default) = C:\Program Files\Windows NT\Accessories\wordpad.exe %1
```

## <a name="remarks"></a>備註

下列螢幕擷取畫面是先前的登錄機碼專案範例的圖例。

![顯示顯示 [記事本] 和 [wordpad] 選項之級聯功能表範例的螢幕擷取畫面](images/file-assoc/testcascademenu2.png)

 

 



