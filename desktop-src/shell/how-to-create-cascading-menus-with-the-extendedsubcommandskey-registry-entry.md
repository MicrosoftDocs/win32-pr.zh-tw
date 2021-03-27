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
# <a name="how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a><span data-ttu-id="16890-103">如何使用 ExtendedSubCommandsKey 登錄專案建立串聯功能表</span><span class="sxs-lookup"><span data-stu-id="16890-103">How to Create Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>

<span data-ttu-id="16890-104">在 Windows 7 和更新版本中，您可以使用 **ExtendedSubCommandsKey** 子機碼來建立擴充的串聯功能表。</span><span class="sxs-lookup"><span data-stu-id="16890-104">In Windows 7 and later, you can use the **ExtendedSubCommandsKey** subkey to create extended cascading menus.</span></span>

<span data-ttu-id="16890-105">下列螢幕擷取畫面是延伸串聯功能表的範例。</span><span class="sxs-lookup"><span data-stu-id="16890-105">The following screen shot is an example of an extended cascading menu.</span></span>

![顯示裝置的擴充串聯功能表的螢幕擷取畫面](images/file-assoc/extendedsubcommandskey.png)

<span data-ttu-id="16890-107">由於 **HKEY \_ 類別 \_ 根目錄** 是 **HKEY \_ 目前 \_ 使用者** 和 **HKEY \_ 本機 \_ 電腦** 的組合，因此您可以在 [ **HKEY \_ 目前 \_ 使用者** \\ **軟體** \\ **類別**] 子機碼下註冊該 subverbs。</span><span class="sxs-lookup"><span data-stu-id="16890-107">Because **HKEY\_CLASSES\_ROOT** is a combination of **HKEY\_CURRENT\_USER** and **HKEY\_LOCAL\_MACHINE**, you can register the subverbs under the **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** subkey.</span></span> <span data-ttu-id="16890-108">這樣做的優點是不需要提高許可權。</span><span class="sxs-lookup"><span data-stu-id="16890-108">The advantage of doing so is that elevated permission is not required.</span></span> <span data-ttu-id="16890-109">其他檔案關聯可以藉由指定相同的 **ExtendedSubCommandsKey** 子機碼，重複使用這整組動詞。</span><span class="sxs-lookup"><span data-stu-id="16890-109">Other file associations can reuse this entire set of verbs by specifying the same **ExtendedSubCommandsKey** subkey.</span></span> <span data-ttu-id="16890-110">如果您不需要重複使用這組動詞，可以列出父系下的動詞。</span><span class="sxs-lookup"><span data-stu-id="16890-110">If you do not need to reuse this set of verbs, you can list the verbs under the parent.</span></span> <span data-ttu-id="16890-111">在此情況下，請確定父系的預設值是空的，如本節的登錄專案範例中所述。</span><span class="sxs-lookup"><span data-stu-id="16890-111">In this case, make sure the default value of the parent is empty, as illustrated in the registry entry example in this section.</span></span>

## <a name="instructions"></a><span data-ttu-id="16890-112">指示</span><span class="sxs-lookup"><span data-stu-id="16890-112">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="16890-113">步驟 1:</span><span class="sxs-lookup"><span data-stu-id="16890-113">Step 1:</span></span>

<span data-ttu-id="16890-114">在 **HKEY \_ 類別的 \_ 根目錄** ProgID shell CascadeMenuKey 底下建立子機碼， \\  \\  \\ 並指定 CascadeMenuKey 的名稱（例如 *CascadeTest*）。</span><span class="sxs-lookup"><span data-stu-id="16890-114">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell**\\*CascadeMenuKey* and give the CascadeMenuKey a name such as *CascadeTest*, for example.</span></span> <span data-ttu-id="16890-115">然後加入 **REG \_ SZ** 型別的 MUIVerb 專案，並為它命名，例如「測試 Cascade」功能表2，如下列登錄範例所示。</span><span class="sxs-lookup"><span data-stu-id="16890-115">Then add a MUIVerb entry of **REG\_SZ** type and give it a name such as Test Cascade Menu 2, as illustrated in the following registry example.</span></span>

```
HKEY_CLASSES_ROOT
   txtfile
      shell
         CascadeTest
            MUIVerb = Test Cascade Menu 2
```

### <a name="step-2"></a><span data-ttu-id="16890-116">步驟 2:</span><span class="sxs-lookup"><span data-stu-id="16890-116">Step 2:</span></span>

<span data-ttu-id="16890-117">在您所建立的 *CascadeTest* 子機碼底下，新增 **ExtendedSubCommandsKey** 子機碼，然後將檔子命令 (的類型為 **REG \_ SZ**) ; 例如：</span><span class="sxs-lookup"><span data-stu-id="16890-117">Under the *CascadeTest* subkey that you created, add an **ExtendedSubCommandsKey** subkey, and then add the document subcommands (of type **REG\_SZ**); for example:</span></span>

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

<span data-ttu-id="16890-118">確定 [ *測試串聯功能表 2* ] 子機碼的預設值是空的，而且顯示為 [ **未設定) 的 (值**]。</span><span class="sxs-lookup"><span data-stu-id="16890-118">Ensure that the default value of the *Test Cascade Menu 2* subkey is empty, and shown as **(value not set)**.</span></span>

### <a name="step-3"></a><span data-ttu-id="16890-119">步驟 3：</span><span class="sxs-lookup"><span data-stu-id="16890-119">Step 3:</span></span>

<span data-ttu-id="16890-120">使用下列任何靜態動詞命令來填入 subverbs。</span><span class="sxs-lookup"><span data-stu-id="16890-120">Populate the subverbs using any of the following static verb implementations.</span></span> <span data-ttu-id="16890-121">請注意，CommandFlags 子機碼代表 EXPCMDFLAGS 值。</span><span class="sxs-lookup"><span data-stu-id="16890-121">Note that the CommandFlags subkey represents EXPCMDFLAGS values.</span></span> <span data-ttu-id="16890-122">如果您想要在 cascade 功能表項目之前或之後加入分隔符號，請使用 ECF \_ SEPARATORBEFORE (0x20) 或 ECF \_ SEPARATORAFTER (0x40) 。</span><span class="sxs-lookup"><span data-stu-id="16890-122">If you want to add a separator before or after the cascade menu item, use ECF\_SEPARATORBEFORE (0x20) or ECF\_SEPARATORAFTER (0x40).</span></span> <span data-ttu-id="16890-123">如需這些 Windows 7 及更新版本旗標的說明，請參閱 [**IExplorerCommand：： GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags)。</span><span class="sxs-lookup"><span data-stu-id="16890-123">For a description of these Windows 7 and later flags, see [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span></span> <span data-ttu-id="16890-124">ECF \_ SEPARATORBEFORE 僅適用于最上層的功能表項目。</span><span class="sxs-lookup"><span data-stu-id="16890-124">ECF\_SEPARATORBEFORE works only for the top level menu items.</span></span> <span data-ttu-id="16890-125">MUIVerb 的類型為 **reg \_ SZ**，而 CommandFlags 的類型為 **reg \_ DWORD**。</span><span class="sxs-lookup"><span data-stu-id="16890-125">MUIVerb is of type **REG\_SZ**, and CommandFlags is of type **REG\_DWORD**.</span></span>

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

## <a name="remarks"></a><span data-ttu-id="16890-126">備註</span><span class="sxs-lookup"><span data-stu-id="16890-126">Remarks</span></span>

<span data-ttu-id="16890-127">下列螢幕擷取畫面是先前的登錄機碼專案範例的圖例。</span><span class="sxs-lookup"><span data-stu-id="16890-127">The following screen shot is an illustration of the previous registry key entry examples.</span></span>

![顯示顯示 [記事本] 和 [wordpad] 選項之級聯功能表範例的螢幕擷取畫面](images/file-assoc/testcascademenu2.png)

 

 



