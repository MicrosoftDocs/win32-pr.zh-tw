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
# <a name="how-to-define-extended-verbs"></a><span data-ttu-id="3f4f1-104">如何定義擴充動詞</span><span class="sxs-lookup"><span data-stu-id="3f4f1-104">How to Define Extended Verbs</span></span>

<span data-ttu-id="3f4f1-105">您可以使用登錄來定義一個或多個擴充動詞。</span><span class="sxs-lookup"><span data-stu-id="3f4f1-105">You can use the registry to define one or more extended verbs.</span></span> <span data-ttu-id="3f4f1-106">只有當使用者在按下 SHIFT 鍵時，以滑鼠右鍵按一下物件時，才會顯示相關聯的命令。</span><span class="sxs-lookup"><span data-stu-id="3f4f1-106">The associated commands will be displayed only when the user right-clicks an object while pressing the SHIFT key.</span></span>

## <a name="instructions"></a><span data-ttu-id="3f4f1-107">指示</span><span class="sxs-lookup"><span data-stu-id="3f4f1-107">Instructions</span></span>


<span data-ttu-id="3f4f1-108">若要將動詞定義為擴充，只要將 "extended" **REG \_ SZ** 值新增至動詞的子機碼。</span><span class="sxs-lookup"><span data-stu-id="3f4f1-108">To define a verb as extended, simply add an "extended" **REG\_SZ** value to the verb's subkey.</span></span> <span data-ttu-id="3f4f1-109">此值不應該有任何與其相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="3f4f1-109">The value should not have any data associated with it.</span></span> <span data-ttu-id="3f4f1-110">下列範例登錄專案顯示上一節中的範例，並將 "doit r" 定義為擴充動詞。</span><span class="sxs-lookup"><span data-stu-id="3f4f1-110">The following sample registry entry shows the example from the previous section, with "doit" defined as an extended verb.</span></span>

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

 

 



