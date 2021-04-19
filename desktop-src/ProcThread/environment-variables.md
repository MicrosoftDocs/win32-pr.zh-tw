---
description: 每個進程都有一個環境區塊，其中包含一組環境變數及其值。 環境變數有兩種類型：每個使用者的使用者環境變數 (設定) 和系統內容變數 (為每個人) 設定。
ms.assetid: 6732b12f-ced1-4769-b947-79da8fd2237a
title: 環境變數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f50226d12286d01c77025d1cc38e33e2778392a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974274"
---
# <a name="environment-variables"></a><span data-ttu-id="2a682-104">環境變數</span><span class="sxs-lookup"><span data-stu-id="2a682-104">Environment Variables</span></span>

<span data-ttu-id="2a682-105">每個進程都有一個環境區塊，其中包含一組環境變數及其值。</span><span class="sxs-lookup"><span data-stu-id="2a682-105">Every process has an environment block that contains a set of environment variables and their values.</span></span> <span data-ttu-id="2a682-106">環境變數有兩種類型：每個使用者的使用者環境變數 (設定) 和系統內容變數 (為每個人) 設定。</span><span class="sxs-lookup"><span data-stu-id="2a682-106">There are two types of environment variables: user environment variables (set for each user) and system environment variables (set for everyone).</span></span>

<span data-ttu-id="2a682-107">根據預設，子進程會繼承其父進程的環境變數。</span><span class="sxs-lookup"><span data-stu-id="2a682-107">By default, a child process inherits the environment variables of its parent process.</span></span> <span data-ttu-id="2a682-108">命令處理器啟動的程式會繼承命令處理器的環境變數。</span><span class="sxs-lookup"><span data-stu-id="2a682-108">Programs started by the command processor inherit the command processor's environment variables.</span></span> <span data-ttu-id="2a682-109">若要為子進程指定不同的環境，請建立新的環境區塊，並將其指標作為參數傳遞給 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) 函數。</span><span class="sxs-lookup"><span data-stu-id="2a682-109">To specify a different environment for a child process, create a new environment block and pass a pointer to it as a parameter to the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span>

<span data-ttu-id="2a682-110">命令處理器提供 **set** 命令以顯示其環境區塊，或建立新的環境變數。</span><span class="sxs-lookup"><span data-stu-id="2a682-110">The command processor provides the **set** command to display its environment block or to create new environment variables.</span></span> <span data-ttu-id="2a682-111">您也可以從 **主控台** 選取 [**系統**]、選取 [ **Advanced system settings**]，然後按一下 [**環境變數**]，以查看或修改環境變數。</span><span class="sxs-lookup"><span data-stu-id="2a682-111">You can also view or modify the environment variables by selecting **System** from the **Control Panel**, selecting **Advanced system settings**, and clicking **Environment Variables**.</span></span>

<span data-ttu-id="2a682-112">每個環境區塊都包含下列格式的環境變數：</span><span class="sxs-lookup"><span data-stu-id="2a682-112">Each environment block contains the environment variables in the following format:</span></span><dl> <span data-ttu-id="2a682-113">*Var1* =*Value1* \\0</span><span class="sxs-lookup"><span data-stu-id="2a682-113">*Var1*=*Value1*\\0</span></span>  
<span data-ttu-id="2a682-114">*Var2* =*Value2* \\0</span><span class="sxs-lookup"><span data-stu-id="2a682-114">*Var2*=*Value2*\\0</span></span>  
<span data-ttu-id="2a682-115">*Var3* =*Value3* \\0</span><span class="sxs-lookup"><span data-stu-id="2a682-115">*Var3*=*Value3*\\0</span></span>  
<span data-ttu-id="2a682-116">...</span><span class="sxs-lookup"><span data-stu-id="2a682-116">...</span></span>  
<span data-ttu-id="2a682-117">*VarN* =*值* \\0 \\ 0</span><span class="sxs-lookup"><span data-stu-id="2a682-117">*VarN*=*ValueN*\\0\\0</span></span>  
</dl>

<span data-ttu-id="2a682-118">環境變數的名稱不能包含等號 (=) 。</span><span class="sxs-lookup"><span data-stu-id="2a682-118">The name of an environment variable cannot include an equal sign (=).</span></span>

<span data-ttu-id="2a682-119">[**GetEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings)函式會傳回呼叫進程的環境區塊指標。</span><span class="sxs-lookup"><span data-stu-id="2a682-119">The [**GetEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings) function returns a pointer to the environment block of the calling process.</span></span> <span data-ttu-id="2a682-120">這應該被視為唯讀區塊;請勿直接修改它。</span><span class="sxs-lookup"><span data-stu-id="2a682-120">This should be treated as a read-only block; do not modify it directly.</span></span> <span data-ttu-id="2a682-121">相反地，請使用 [**SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable) 函數來變更環境變數。</span><span class="sxs-lookup"><span data-stu-id="2a682-121">Instead, use the [**SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable) function to change an environment variable.</span></span> <span data-ttu-id="2a682-122">當您完成從 **GetEnvironmentStrings** 取得的環境區塊時，請呼叫 [**FreeEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-freeenvironmentstringsa) 函數來釋放區塊。</span><span class="sxs-lookup"><span data-stu-id="2a682-122">When you are finished with the environment block obtained from **GetEnvironmentStrings**, call the [**FreeEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-freeenvironmentstringsa) function to free the block.</span></span>

<span data-ttu-id="2a682-123">呼叫 [**SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable) 不會影響系統內容變數。</span><span class="sxs-lookup"><span data-stu-id="2a682-123">Calling [**SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable) has no effect on the system environment variables.</span></span> <span data-ttu-id="2a682-124">若要以程式設計方式新增或修改系統內容變數，請將它們新增至 **HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ Session Manager \\ 環境** 登錄機碼，然後將具有 *LParam* 設定的 [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange)訊息廣播至字串 "環境"。</span><span class="sxs-lookup"><span data-stu-id="2a682-124">To programmatically add or modify system environment variables, add them to the **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Session Manager\\Environment** registry key, then broadcast a [**WM\_SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) message with *lParam* set to the string "Environment".</span></span> <span data-ttu-id="2a682-125">這可讓應用程式（例如 shell）挑選您的更新。</span><span class="sxs-lookup"><span data-stu-id="2a682-125">This allows applications, such as the shell, to pick up your updates.</span></span>

<span data-ttu-id="2a682-126">使用者定義環境變數的大小上限為32767個字元。</span><span class="sxs-lookup"><span data-stu-id="2a682-126">The maximum size of a user-defined environment variable is 32,767 characters.</span></span> <span data-ttu-id="2a682-127">環境區塊的大小不會有任何技術上的限制。</span><span class="sxs-lookup"><span data-stu-id="2a682-127">There is no technical limitation on the size of the environment block.</span></span> <span data-ttu-id="2a682-128">不過，視用來存取區塊的機制而定，有一些實際的限制。</span><span class="sxs-lookup"><span data-stu-id="2a682-128">However, there are practical limits depending on the mechanism used to access the block.</span></span> <span data-ttu-id="2a682-129">例如，批次檔無法設定的變數長度超過命令列長度上限。</span><span class="sxs-lookup"><span data-stu-id="2a682-129">For example, a batch file cannot set a variable that is longer than the maximum command line length.</span></span>

<span data-ttu-id="2a682-130">**Windows Server 2003 和 WINDOWS XP：** 進程的環境區塊大小上限為32767個字元。</span><span class="sxs-lookup"><span data-stu-id="2a682-130">**Windows Server 2003 and Windows XP:** The maximum size of the environment block for the process is 32,767 characters.</span></span> <span data-ttu-id="2a682-131">從 Windows Vista 和 Windows Server 2008 開始，環境區塊的大小不會有任何技術上的限制。</span><span class="sxs-lookup"><span data-stu-id="2a682-131">Starting with Windows Vista and Windows Server 2008, there is no technical limitation on the size of the environment block.</span></span>

<span data-ttu-id="2a682-132">[**GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable)函式會判斷指定的變數是否定義在呼叫進程的環境中，如果是的話，則為其值。</span><span class="sxs-lookup"><span data-stu-id="2a682-132">The [**GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable) function determines whether a specified variable is defined in the environment of the calling process, and, if so, what its value is.</span></span>

<span data-ttu-id="2a682-133">若要取得指定使用者的環境區塊複本，請使用 [**CreateEnvironmentBlock**](/windows/win32/api/userenv/nf-userenv-createenvironmentblock) 函數。</span><span class="sxs-lookup"><span data-stu-id="2a682-133">To retrieve a copy of the environment block for a given user, use the [**CreateEnvironmentBlock**](/windows/win32/api/userenv/nf-userenv-createenvironmentblock) function.</span></span>

<span data-ttu-id="2a682-134">若要展開環境變數字串，請使用 [**ExpandEnvironmentStrings**](/windows/desktop/api/processenv/nf-processenv-expandenvironmentstringsa) 函數。</span><span class="sxs-lookup"><span data-stu-id="2a682-134">To expand environment-variable strings, use the [**ExpandEnvironmentStrings**](/windows/desktop/api/processenv/nf-processenv-expandenvironmentstringsa) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a682-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="2a682-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a682-136">變更環境變數</span><span class="sxs-lookup"><span data-stu-id="2a682-136">Changing Environment Variables</span></span>](changing-environment-variables.md)
</dt> <dt>

[<span data-ttu-id="2a682-137">使用者環境變數</span><span class="sxs-lookup"><span data-stu-id="2a682-137">User Environment Variables</span></span>](../shell/user-environment-variables.md)
</dt> </dl>

 

 
