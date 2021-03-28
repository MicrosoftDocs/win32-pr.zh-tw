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
# <a name="how-to-implement-custom-verbs-for-folders-through-desktopini"></a><span data-ttu-id="8f2e6-104">如何透過 Desktop.ini 為資料夾執行自訂動詞</span><span class="sxs-lookup"><span data-stu-id="8f2e6-104">How to Implement Custom Verbs for Folders through Desktop.ini</span></span>

<span data-ttu-id="8f2e6-105">在 Windows 7 和更新版本中，您可以使用 Desktop.ini 將動詞新增至資料夾。</span><span class="sxs-lookup"><span data-stu-id="8f2e6-105">In Windows 7 and later, you can add verbs to a folder by using Desktop.ini.</span></span> <span data-ttu-id="8f2e6-106">如需 Desktop.ini 檔案的詳細資訊，請參閱 [如何使用 Desktop.ini自訂資料夾 ](how-to-customize-folders-with-desktop-ini.md)。</span><span class="sxs-lookup"><span data-stu-id="8f2e6-106">For more information about Desktop.ini files, see [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span></span>

> [!Note]  
> <span data-ttu-id="8f2e6-107">Desktop.ini 的檔案應該一律標示為  +  **隱藏** 系統，使其不會顯示給使用者。</span><span class="sxs-lookup"><span data-stu-id="8f2e6-107">Desktop.ini files should always be marked **System** + **Hidden** so they won't be displayed to users.</span></span>

 

<span data-ttu-id="8f2e6-108">若要透過 Desktop.ini 檔新增資料夾的自訂動詞命令，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="8f2e6-108">To add custom verbs for folders through a Desktop.ini file, perform the following steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="8f2e6-109">指示</span><span class="sxs-lookup"><span data-stu-id="8f2e6-109">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="8f2e6-110">步驟 1:</span><span class="sxs-lookup"><span data-stu-id="8f2e6-110">Step 1:</span></span>

<span data-ttu-id="8f2e6-111">建立標示為 **唯讀** 或 **系統** 的資料夾。</span><span class="sxs-lookup"><span data-stu-id="8f2e6-111">Create a folder that is marked **Read-only** or **System**.</span></span>

### <a name="step-2"></a><span data-ttu-id="8f2e6-112">步驟 2:</span><span class="sxs-lookup"><span data-stu-id="8f2e6-112">Step 2:</span></span>

<span data-ttu-id="8f2e6-113">建立包含的 Desktop.ini 檔案 \[ 。ShellClassInfo \] DirectoryClass = Folder ProgID。</span><span class="sxs-lookup"><span data-stu-id="8f2e6-113">Create a Desktop.ini file that includes a \[.ShellClassInfo\] DirectoryClass=Folder ProgID.</span></span>

### <a name="step-3"></a><span data-ttu-id="8f2e6-114">步驟 3：</span><span class="sxs-lookup"><span data-stu-id="8f2e6-114">Step 3:</span></span>

<span data-ttu-id="8f2e6-115">在登錄中，使用 CanUseForDirectory 的值建立 **HKEY \_ 類別 \_ 根** \\ **資料夾 ProgID** 。</span><span class="sxs-lookup"><span data-stu-id="8f2e6-115">In the registry, create **HKEY\_CLASSES\_ROOT**\\**Folder ProgID** with a value of CanUseForDirectory.</span></span> <span data-ttu-id="8f2e6-116">CanUseForDirectory 值可避免誤用未設定為透過 Desktop.ini 為資料夾執行自訂動詞命令的 Progid。</span><span class="sxs-lookup"><span data-stu-id="8f2e6-116">The CanUseForDirectory value avoids the misuse of ProgIDs that are set not to participate in implementing custom verbs for folders through Desktop.ini.</span></span>

### <a name="step-4"></a><span data-ttu-id="8f2e6-117">步驟 4：</span><span class="sxs-lookup"><span data-stu-id="8f2e6-117">Step 4:</span></span>

<span data-ttu-id="8f2e6-118">在 **資料夾** ProgID 子機碼底下新增動詞，例如：</span><span class="sxs-lookup"><span data-stu-id="8f2e6-118">Add verbs under the **Folder** ProgID subkey, for example:</span></span>

```
HKEY_CLASSES_ROOT
   CustomFolderType
      Shell
         MyVerb
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
```

## <a name="remarks"></a><span data-ttu-id="8f2e6-119">備註</span><span class="sxs-lookup"><span data-stu-id="8f2e6-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8f2e6-120">這些動詞命令可以是預設動詞，在此情況下，按兩下資料夾會啟動動詞。</span><span class="sxs-lookup"><span data-stu-id="8f2e6-120">These verbs can be the default verbs, in which case double-clicking the folder activates the verb.</span></span>

 

 

 



