---
description: 在 Windows 7 （含）以後版本中，您可以使用本主題中提供的程式，在登錄中使用子命令專案來建立串聯功能表。
title: 使用子命令登錄專案建立串聯功能表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8b1168daae5ea927f079c66eb436c099f8b3d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991570"
---
# <a name="how-to-create-cascading-menus-with-the-subcommands-registry-entry"></a><span data-ttu-id="94e7a-103">如何使用子命令登錄專案建立串聯功能表</span><span class="sxs-lookup"><span data-stu-id="94e7a-103">How to Create Cascading Menus with the SubCommands Registry Entry</span></span>

<span data-ttu-id="94e7a-104">在 Windows 7 （含）以後版本中，您可以使用本主題中提供的程式，在登錄中使用子命令專案來建立串聯功能表。</span><span class="sxs-lookup"><span data-stu-id="94e7a-104">In Windows 7 and later, you can use the SubCommands entry in the registry to create cascading menus by using the procedure given in this topic.</span></span>

## <a name="instructions"></a><span data-ttu-id="94e7a-105">指示</span><span class="sxs-lookup"><span data-stu-id="94e7a-105">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="94e7a-106">步驟 1:</span><span class="sxs-lookup"><span data-stu-id="94e7a-106">Step 1:</span></span>

<span data-ttu-id="94e7a-107">在 **HKEY \_ 類別 \_ 根目錄** ProgID shell 下建立新的子機碼 \\  \\ \*\*\*\*，其中 *ProgID* 是您要新增串聯功能表的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="94e7a-107">Create a new subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell**, where *ProgID* is the file type for which you want to add a cascading menu.</span></span> <span data-ttu-id="94e7a-108">您可以將這個新的子機碼命名為任何您想要的名稱。</span><span class="sxs-lookup"><span data-stu-id="94e7a-108">You can name this new subkey anything you'd like.</span></span> <span data-ttu-id="94e7a-109">在本主題的其餘部分，我們會將它稱為 *CascadeMenu*，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="94e7a-109">For the remainder of this topic, we'll call it *CascadeMenu*, as shown in the following example.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
```

### <a name="step-2"></a><span data-ttu-id="94e7a-110">步驟 2:</span><span class="sxs-lookup"><span data-stu-id="94e7a-110">Step 2:</span></span>

<span data-ttu-id="94e7a-111">將名為 "MUIVerb" 的專案（其類型為 **REG \_ Sz** 或 **reg \_ EXPAND \_**）新增至 *CascadeMenu* 子機碼。</span><span class="sxs-lookup"><span data-stu-id="94e7a-111">Add an entry named "MUIVerb", of type **REG\_SZ** or **REG\_EXPAND\_SZ**, to the *CascadeMenu* subkey.</span></span> <span data-ttu-id="94e7a-112">將此專案指派為字串值，例如「測試 Cascade 功能表」。</span><span class="sxs-lookup"><span data-stu-id="94e7a-112">Assign this entry a string value such as "Test Cascade Menu".</span></span> <span data-ttu-id="94e7a-113">一般來說，此字串是以 "，resource" 格式的資源參考形式提供 @file 。</span><span class="sxs-lookup"><span data-stu-id="94e7a-113">Normally, this string is provided as a resource reference in the form "@file, resource".</span></span> <span data-ttu-id="94e7a-114">不應設定 *CascadeMenu* 子機碼的 (預設) 值。</span><span class="sxs-lookup"><span data-stu-id="94e7a-114">The (Default) value for the *CascadeMenu* subkey should not be set.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
            (Default)
            MUIVerb = Test Cascade Menu
```

### <a name="step-3"></a><span data-ttu-id="94e7a-115">步驟 3：</span><span class="sxs-lookup"><span data-stu-id="94e7a-115">Step 3:</span></span>

<span data-ttu-id="94e7a-116">將名為 "entry" 的專案（其類型為 **REG \_ Sz** 或 **reg \_ EXPAND \_**）新增至 *CascadeMenu* 子機碼。</span><span class="sxs-lookup"><span data-stu-id="94e7a-116">Add an entry named "SubCommands", of type **REG\_SZ** or **REG\_EXPAND\_SZ**, to the *CascadeMenu* subkey.</span></span> <span data-ttu-id="94e7a-117">以分號分隔的動詞清單，指派應出現在功能表上的動詞清單（以其所需的外觀順序表示）。</span><span class="sxs-lookup"><span data-stu-id="94e7a-117">Assign this entry a semicolon-delimited list of the verbs that should appear on the menu, in their desired order of appearance.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      Shell
         CascadeMenu
            SubCommands = Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
```

### <a name="step-4"></a><span data-ttu-id="94e7a-118">步驟 4：</span><span class="sxs-lookup"><span data-stu-id="94e7a-118">Step 4:</span></span>

<span data-ttu-id="94e7a-119">針對您在子命令專案中使用的任何自訂靜態動詞方法，使用動詞執行來填入 **CommandStore** 子機碼;例如：</span><span class="sxs-lookup"><span data-stu-id="94e7a-119">Populate the **CommandStore** subkey with verb implementations for any custom static verb implementation methods that you've used in your SubCommands entry; for example:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="94e7a-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="94e7a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94e7a-121">建立靜態串聯功能表</span><span class="sxs-lookup"><span data-stu-id="94e7a-121">Creating Static Cascading Menus</span></span>](creating-static-cascading-menus.md)
</dt> </dl>

 

 



