---
description: 類似于命令列參數。 不過，您不需要在 \# 每次編譯 MOF 檔案時重新輸入 pragma 命令。
ms.assetid: 3cf22686-dd56-43a3-9584-3d707a20a3a0
ms.tgt_platform: multiple
title: '#pragma'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ae13d5f960e0b415f34dce97a40cff6cba8056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991915"
---
# <a name="pragma"></a><span data-ttu-id="43dc2-104">\#pragma</span><span class="sxs-lookup"><span data-stu-id="43dc2-104">\#pragma</span></span>

<span data-ttu-id="43dc2-105">**\# Pragma** 預處理器命令類似于命令列參數。</span><span class="sxs-lookup"><span data-stu-id="43dc2-105">The **\#pragma** preprocessor command is similar to a command-line switch.</span></span> <span data-ttu-id="43dc2-106">不過，您不需要在每次編譯 MOF 檔案時重新輸入 **\# pragma** 命令。</span><span class="sxs-lookup"><span data-stu-id="43dc2-106">However, you do not need to reenter a **\#pragma** command each time you compile a MOF file.</span></span> <span data-ttu-id="43dc2-107">下列範例說明 **\# pragma** 命令語法：</span><span class="sxs-lookup"><span data-stu-id="43dc2-107">The following example illustrates **\#pragma** command syntax:</span></span>


```mof
#pragma [command]
```



<span data-ttu-id="43dc2-108">您通常會在 MOF 檔案的開頭放置 **\# pragma** 命令。</span><span class="sxs-lookup"><span data-stu-id="43dc2-108">You usually place a **\#pragma** command at the beginning of a MOF file.</span></span> <span data-ttu-id="43dc2-109">不過，您可以將一些命令（例如 **\# pragma** 命令）放在您的 MOF 程式碼主體中。</span><span class="sxs-lookup"><span data-stu-id="43dc2-109">However, you can place some commands, such as the **\#pragma** command, in the body of your MOF code.</span></span> <span data-ttu-id="43dc2-110">下列範例會顯示 **\# pragma** 命令，指出 MOF 編譯器必須將類別和實例放在根 \\ cimv2 命名空間中，並且編譯儲存機制復原期間包含命令的檔案：</span><span class="sxs-lookup"><span data-stu-id="43dc2-110">The following example shows **\#pragma** commands that indicate to the MOF compiler that it must place classes and instances in the root\\cimv2 namespace and compile the file in which the commands are included during repository recovery:</span></span>


```mof
#pragma autorecover
#pragma namespace ("\\\\.\\root\\cimv2")
```



<span data-ttu-id="43dc2-111">以下列出可用的 **\# pragma** 命令。</span><span class="sxs-lookup"><span data-stu-id="43dc2-111">The following lists the available **\#pragma** commands.</span></span>



| <span data-ttu-id="43dc2-112">命令</span><span class="sxs-lookup"><span data-stu-id="43dc2-112">Command</span></span>                                         | <span data-ttu-id="43dc2-113">描述</span><span class="sxs-lookup"><span data-stu-id="43dc2-113">Description</span></span>                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43dc2-114">**修訂**</span><span class="sxs-lookup"><span data-stu-id="43dc2-114">**amendment**</span></span>](pragma-amendment.md)           | <span data-ttu-id="43dc2-115">指示 MOF 編譯器將 MOF 檔案分隔成非語言相關和語言特定版本。</span><span class="sxs-lookup"><span data-stu-id="43dc2-115">Directs the MOF compiler to separate a MOF file into language-neutral and language-specific versions.</span></span> |
| [<span data-ttu-id="43dc2-116">**自動**</span><span class="sxs-lookup"><span data-stu-id="43dc2-116">**autorecover**</span></span>](pragma-autorecover.md)       | <span data-ttu-id="43dc2-117">將 MOF 檔案新增至儲存機制復原期間所編譯的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="43dc2-117">Adds a MOF file to the list of files compiled during repository recovery.</span></span>                             |
| [<span data-ttu-id="43dc2-118">**classflags**</span><span class="sxs-lookup"><span data-stu-id="43dc2-118">**classflags**</span></span>](pragma-classflags.md)         | <span data-ttu-id="43dc2-119">根據指定的旗標，控制建立或更新類別的方式。</span><span class="sxs-lookup"><span data-stu-id="43dc2-119">Controls the way classes are created or updated depending on the flags specified.</span></span>                     |
| [<span data-ttu-id="43dc2-120">**deleteclass**</span><span class="sxs-lookup"><span data-stu-id="43dc2-120">**deleteclass**</span></span>](pragma-deleteclass.md)       | <span data-ttu-id="43dc2-121">從存放庫中刪除現有的類別及其實例。</span><span class="sxs-lookup"><span data-stu-id="43dc2-121">Deletes an existing class and its instances from the repository.</span></span>                                      |
| [<span data-ttu-id="43dc2-122">**路經**</span><span class="sxs-lookup"><span data-stu-id="43dc2-122">**deleteinstance**</span></span>](pragma-deleteinstance.md) | <span data-ttu-id="43dc2-123">從存放庫中刪除類別的現有實例。</span><span class="sxs-lookup"><span data-stu-id="43dc2-123">Deletes an existing instance of a class from the repository.</span></span>                                          |
| [<span data-ttu-id="43dc2-124">**instanceflags**</span><span class="sxs-lookup"><span data-stu-id="43dc2-124">**instanceflags**</span></span>](pragma-instanceflags.md)   | <span data-ttu-id="43dc2-125">根據指定的旗標，控制建立或更新實例的方式。</span><span class="sxs-lookup"><span data-stu-id="43dc2-125">Controls the way instances are created or updated depending on the flags specified.</span></span>                   |
| [<span data-ttu-id="43dc2-126">**命名 空間**</span><span class="sxs-lookup"><span data-stu-id="43dc2-126">**namespace**</span></span>](pragma-namespace.md)           | <span data-ttu-id="43dc2-127">要求編譯器將 MOF 檔案載入至指定為 *namespacepath* 的命名空間。</span><span class="sxs-lookup"><span data-stu-id="43dc2-127">Requests that the compiler load the MOF file into the namespace specified as *namespacepath*.</span></span>         |



 

## <a name="related-topics"></a><span data-ttu-id="43dc2-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="43dc2-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43dc2-129">預處理器命令</span><span class="sxs-lookup"><span data-stu-id="43dc2-129">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



