---
description: 您可以使用登錄來定義一個或多個擴充動詞。 只有當使用者在按下 SHIFT 鍵時，以滑鼠右鍵按一下物件時，才會顯示相關聯的命令。
ms.assetid: C6E51716-1D4F-454F-9AF4-8D0E486CB885
title: 如何定義擴充動詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4bd8cca04b40bb0b0b77bab5fd7546fd5bff45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973161"
---
# <a name="how-to-define-extended-verbs"></a>如何定義擴充動詞

您可以使用登錄來定義一個或多個擴充動詞。 只有當使用者在按下 SHIFT 鍵時，以滑鼠右鍵按一下物件時，才會顯示相關聯的命令。

## <a name="instructions"></a>指示


若要將動詞定義為擴充，只要將 "extended" **REG \_ SZ** 值新增至動詞的子機碼。 此值不應該有任何與其相關聯的資料。 下列範例登錄專案顯示上一節中的範例，並將 "doit r" 定義為擴充動詞。

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
         doit
            (Default) = &Do It
            extended
            command
               (Default) = C:\MyDir\MyProgram.exe /d "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1" "%2" %3 %4
```

 

 



