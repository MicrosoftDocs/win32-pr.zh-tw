---
description: 環境變數會指定檔案的搜尋路徑、暫存檔的目錄、應用程式特定的選項，以及其他類似的資訊。
ms.assetid: 6180e54e-4bd9-4692-83fd-f3f7f1d8f8d7
title: 使用者環境變數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf4f898c7a9135c0421fdd67a7bed1d97655556f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991614"
---
# <a name="user-environment-variables"></a><span data-ttu-id="b5253-103">使用者環境變數</span><span class="sxs-lookup"><span data-stu-id="b5253-103">User Environment Variables</span></span>

<span data-ttu-id="b5253-104">環境變數會指定檔案的搜尋路徑、暫存檔的目錄、應用程式特定的選項，以及其他類似的資訊。</span><span class="sxs-lookup"><span data-stu-id="b5253-104">Environment variables specify search paths for files, directories for temporary files, application-specific options, and other similar information.</span></span> <span data-ttu-id="b5253-105">系統會維護每個使用者的環境區塊，以及一部電腦的環境區塊。</span><span class="sxs-lookup"><span data-stu-id="b5253-105">The system maintains an environment block for each user and one for the computer.</span></span> <span data-ttu-id="b5253-106">系統內容區塊代表特定電腦上所有使用者的環境變數。</span><span class="sxs-lookup"><span data-stu-id="b5253-106">The system environment block represents environment variables for all users of the particular computer.</span></span> <span data-ttu-id="b5253-107">使用者的環境區塊代表系統為該特定使用者維護的環境變數，包括系統內容變數集。</span><span class="sxs-lookup"><span data-stu-id="b5253-107">A user's environment block represents the environment variables the system maintains for that particular user, including the set of system environment variables.</span></span>

<span data-ttu-id="b5253-108">根據預設，每個進程都會收到其父進程的環境區塊複本。</span><span class="sxs-lookup"><span data-stu-id="b5253-108">By default, each process receives a copy of the environment block for its parent process.</span></span> <span data-ttu-id="b5253-109">一般來說，這是登入之使用者的環境區塊。</span><span class="sxs-lookup"><span data-stu-id="b5253-109">Typically, this is the environment block for the user who is logged on.</span></span> <span data-ttu-id="b5253-110">處理常式可以使用 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) 或 [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 函式，為其子進程指定不同的環境區塊。</span><span class="sxs-lookup"><span data-stu-id="b5253-110">A process can specify different environment blocks for its child processes using the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) or [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function.</span></span>

<span data-ttu-id="b5253-111">若要新增或修改環境變數，使用者可從 **主控台** 中選取 [**系統**]，然後選取 [**環境**] 索引標籤。使用者也可以在命令提示字元中使用 **set** 命令來新增或修改環境變數。</span><span class="sxs-lookup"><span data-stu-id="b5253-111">To add or modify environment variables, the user selects **System** from the **Control Panel**, then selects the **Environment** tab. The user can also add or modify environment variables at a command prompt using the **set** command.</span></span> <span data-ttu-id="b5253-112">使用 **set** 命令建立的環境變數只會套用至其所設定的命令視窗以及其子進程。</span><span class="sxs-lookup"><span data-stu-id="b5253-112">Environment variables created with the **set** command apply only to the command window in which they are set, and to its child processes.</span></span> <span data-ttu-id="b5253-113">如需詳細資訊，請輸入 **set/？**</span><span class="sxs-lookup"><span data-stu-id="b5253-113">For more information, type **set /?**</span></span> <span data-ttu-id="b5253-114">。</span><span class="sxs-lookup"><span data-stu-id="b5253-114">at a command prompt.</span></span>

<span data-ttu-id="b5253-115">若要取得指定使用者的環境區塊複本，請使用 [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) 函數。</span><span class="sxs-lookup"><span data-stu-id="b5253-115">To retrieve a copy of the environment block for a given user, use the [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) function.</span></span> <span data-ttu-id="b5253-116">若要釋放 **CreateEnvironmentBlock** 所建立的環境區塊，請使用 [**DestroyEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock) 函數。</span><span class="sxs-lookup"><span data-stu-id="b5253-116">To free an environment block created by **CreateEnvironmentBlock**, use the [**DestroyEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock) function.</span></span> <span data-ttu-id="b5253-117">這些函數會參考環境區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="b5253-117">These functions reference a pointer to an environment block.</span></span> <span data-ttu-id="b5253-118">環境區塊是以 null 結束之 Unicode 字串的陣列。</span><span class="sxs-lookup"><span data-stu-id="b5253-118">The environment block is an array of null-terminated Unicode strings.</span></span> <span data-ttu-id="b5253-119">此清單以兩個 null 結尾 (\\ 0 \\ 0) 。</span><span class="sxs-lookup"><span data-stu-id="b5253-119">The list ends with two nulls (\\0\\0).</span></span>

<span data-ttu-id="b5253-120">若要使用指定使用者的環境區塊來展開包含環境變數的字串，請使用 [**ExpandEnvironmentStringsForUser**](/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera) 函數。</span><span class="sxs-lookup"><span data-stu-id="b5253-120">To expand a string that contains environment variables by using the environment block for a specified user, use the [**ExpandEnvironmentStringsForUser**](/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera) function.</span></span>

 

 
