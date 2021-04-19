---
description: RegOpenUserClassesRoot 函式會針對處理非互動式使用者用戶端的進程（例如服務）提供合併的視圖。
ms.assetid: 3815d487-2d58-4ba8-85d2-cae6a642a791
title: HKEY_CLASSES_ROOT 的合併視圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8597db976922db9ca348488b0092c41ba7c7489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984704"
---
# <a name="merged-view-of-hkey_classes_root"></a><span data-ttu-id="8c102-103">HKEY \_ 類別根目錄的合併 \_ 視圖</span><span class="sxs-lookup"><span data-stu-id="8c102-103">Merged View of HKEY\_CLASSES\_ROOT</span></span>

<span data-ttu-id="8c102-104">[**RegOpenUserClassesRoot**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot)函式會針對處理非互動式使用者用戶端的進程（例如服務）提供合併的視圖。</span><span class="sxs-lookup"><span data-stu-id="8c102-104">The [**RegOpenUserClassesRoot**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot) function provides a merged view for processes, such as services, that are dealing with clients other than the interactive user.</span></span> <span data-ttu-id="8c102-105">在此情況下， **HKEY \_ 類別 \_ 根金鑰** 會提供登錄的視圖，該登錄會將 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 中的資訊，與 **HKEY \_ 目前 \_ 使用者 \\ 軟體 \\ 類別** 的資訊合併。</span><span class="sxs-lookup"><span data-stu-id="8c102-105">In this case, the **HKEY\_CLASSES\_ROOT** key provides a view of the registry that merges the information from **HKEY\_LOCAL\_MACHINE\\Software\\Classes** with the information from **HKEY\_CURRENT\_USER\\Software\\Classes**.</span></span>

<span data-ttu-id="8c102-106">系統會使用下列規則來合併兩個來源中的資訊：</span><span class="sxs-lookup"><span data-stu-id="8c102-106">The system uses the following rules to merge information from the two sources:</span></span>

-   <span data-ttu-id="8c102-107">合併的視圖包含 **HKEY \_ 目前 \_ 使用者 \\ 軟體 \\ 類別** 金鑰的所有子機碼。</span><span class="sxs-lookup"><span data-stu-id="8c102-107">The merged view includes all subkeys of the **HKEY\_CURRENT\_USER\\Software\\Classes** key.</span></span>
-   <span data-ttu-id="8c102-108">合併的視圖包含 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 金鑰的所有立即子機碼，不會複製 HKEY 的 **\_ 目前 \_ 使用者 \\ 軟體 \\ 類別** 的子機碼。</span><span class="sxs-lookup"><span data-stu-id="8c102-108">The merged view includes all immediate subkeys of the **HKEY\_LOCAL\_MACHINE\\Software\\Classes** key that do not duplicate the subkeys of **HKEY\_CURRENT\_USER\\Software\\Classes**.</span></span>
-   <span data-ttu-id="8c102-109">本主題結尾處是在 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 和 **HKEY \_ 目前 \_ 使用者 \\ 軟體 \\ 類別** 中找到的子機碼清單。</span><span class="sxs-lookup"><span data-stu-id="8c102-109">At the end of this topic is a list of subkeys that are found in both **HKEY\_LOCAL\_MACHINE\\Software\\Classes** and **HKEY\_CURRENT\_USER\\Software\\Classes**.</span></span> <span data-ttu-id="8c102-110">**HKEY \_ 本機 \_ 電腦** 樹狀結構中這些機碼的立即子機碼，只會包含在合併的視圖中（如果它們不是 **HKEY \_ 目前 \_ 使用者** 樹狀結構中的立即子機碼的複本）。</span><span class="sxs-lookup"><span data-stu-id="8c102-110">The immediate subkeys of these keys from the **HKEY\_LOCAL\_MACHINE** tree are included in the merged view only if they are not duplicates of immediate subkeys from the **HKEY\_CURRENT\_USER** tree.</span></span> <span data-ttu-id="8c102-111">合併的視圖不包含重複子 **機碼的 HKEY \_ 本機 \_ 電腦** 內容。</span><span class="sxs-lookup"><span data-stu-id="8c102-111">The merged view does not include the **HKEY\_LOCAL\_MACHINE** contents of duplicate subkeys.</span></span>

<span data-ttu-id="8c102-112">如果使用系統管理員許可權來執行應用程式，且已停用 [使用者帳戶控制]，則 COM 執行時間會忽略個別使用者的 COM 設定，並只存取每一電腦的 COM 設定。</span><span class="sxs-lookup"><span data-stu-id="8c102-112">If an application is run with administrator rights and User Account Control is disabled, the COM runtime ignores per-user COM configuration and accesses only per-machine COM configuration.</span></span> <span data-ttu-id="8c102-113">需要系統管理員許可權的應用程式應該在安裝期間，將相依的 COM 物件註冊到個別電腦的 COM 設定存放區 (**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別**) 。</span><span class="sxs-lookup"><span data-stu-id="8c102-113">Applications that require administrator rights should register dependent COM objects during installation to the per-machine COM configuration store (**HKEY\_LOCAL\_MACHINE\\Software\\Classes**).</span></span> <span data-ttu-id="8c102-114">如需詳細資訊，請參閱 [AC： UAC： COM Per-User](/previous-versions/bb756926(v=msdn.10))設定。</span><span class="sxs-lookup"><span data-stu-id="8c102-114">For more information, see [AC: UAC: COM Per-User Configuration](/previous-versions/bb756926(v=msdn.10)).</span></span>

<span data-ttu-id="8c102-115">**Windows Server 2003 和 WINDOWS XP/2000：** 應用程式可以將相依的 COM 物件註冊到個別電腦或個別使用者的 COM 設定存放區 (**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 或 **HKEY 目前的 \_ \_ 使用者 \\ 軟體 \\ 類別**) 。</span><span class="sxs-lookup"><span data-stu-id="8c102-115">**Windows Server 2003 and Windows XP/2000:** Applications can register dependent COM objects to either the per-machine or per-user COM configuration store (**HKEY\_LOCAL\_MACHINE\\Software\\Classes** or **HKEY\_CURRENT\_USER\\Software\\Classes**).</span></span>

<span data-ttu-id="8c102-116">下列範例顯示 **HKEY \_ 本機 \_ 電腦** 底下的一組子機碼，並 **HKEY \_ 目前的 \_ 使用者** 金鑰，以及 **HKEY \_ 類別 \_ 根目錄** 的結果合併觀點。</span><span class="sxs-lookup"><span data-stu-id="8c102-116">The following example shows a set of subkeys under the **HKEY\_LOCAL\_MACHINE** and **HKEY\_CURRENT\_USER** keys and the resulting merged view of **HKEY\_CLASSES\_ROOT**.</span></span>

<span data-ttu-id="8c102-117">**HKEY \_本機 \_ 電腦 \\ 軟體 \\ 類別**    **CLSID**       *2*       *4*          **inprocserver32**          **localserver32**       *7*</span><span class="sxs-lookup"><span data-stu-id="8c102-117">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes**    **CLSID**       *2*       *4*          **inprocserver32**          **localserver32**       *7*</span></span>

<span data-ttu-id="8c102-118">**HKEY \_目前 \_ 的 \\ 使用者軟體 \\ 類別**    **CLSID**       *1*       *4*          **localserver**       *6*       *10*          **localserver**</span><span class="sxs-lookup"><span data-stu-id="8c102-118">**HKEY\_CURRENT\_USER\\Software\\Classes**    **CLSID**       *1*       *4*          **localserver**       *6*       *10*          **localserver**</span></span>

<span data-ttu-id="8c102-119">**HKEY \_類別 \_ 根目錄**    **CLSID**       *1*       *2*       *4*          **inprocserver32**          **localserver**          **localserver32**       *6*       *7*       *10*          **localserver**</span><span class="sxs-lookup"><span data-stu-id="8c102-119">**HKEY\_CLASSES\_ROOT**    **CLSID**       *1*       *2*       *4*          **inprocserver32**          **localserver**          **localserver32**       *6*       *7*       *10*          **localserver**</span></span>

<span data-ttu-id="8c102-120">下列子機碼可在 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 和 **HKEY 目前的 \_ \_ 使用者 \\ 軟體 \\ 類別** 中找到。</span><span class="sxs-lookup"><span data-stu-id="8c102-120">The following subkeys are found in both **HKEY\_LOCAL\_MACHINE\\Software\\Classes** and **HKEY\_CURRENT\_USER\\Software\\Classes**.</span></span> <span data-ttu-id="8c102-121">從 **HKEY \_ 本機 \_ 電腦** 樹狀目錄中，只有當這些金鑰與 **HKEY \_ 目前 \_ 使用者** 樹狀結構中的立即子機碼不重複時，才會將這些機碼的立即子機碼包含在合併的視圖中。</span><span class="sxs-lookup"><span data-stu-id="8c102-121">From the **HKEY\_LOCAL\_MACHINE** tree, the immediate subkeys of these keys are included in the merged view only if they are not duplicates of immediate subkeys from the **HKEY\_CURRENT\_USER** tree.</span></span> <span data-ttu-id="8c102-122">合併的視圖不包含重複子 **機碼的 HKEY \_ 本機 \_ 電腦** 內容。</span><span class="sxs-lookup"><span data-stu-id="8c102-122">The merged view does not include the **HKEY\_LOCAL\_MACHINE** contents of duplicate subkeys.</span></span>

<span data-ttu-id="8c102-123">**\**_ _*\*\\shellex**</span><span class="sxs-lookup"><span data-stu-id="8c102-123">**\**_ _*\*\\shellex**</span></span>  
<span data-ttu-id="8c102-124">**\*\\shellex \\ CoNtextMenuHandlers**</span><span class="sxs-lookup"><span data-stu-id="8c102-124">**\*\\shellex\\ContextMenuHandlers**</span></span>  
<span data-ttu-id="8c102-125">**\*\\shellex \\ PropertySheetHandlers**</span><span class="sxs-lookup"><span data-stu-id="8c102-125">**\*\\shellex\\PropertySheetHandlers**</span></span>  
<span data-ttu-id="8c102-126">**AppID**</span><span class="sxs-lookup"><span data-stu-id="8c102-126">**AppID**</span></span>  
<span data-ttu-id="8c102-127">**Clsid**</span><span class="sxs-lookup"><span data-stu-id="8c102-127">**ClsID**</span></span>  
<span data-ttu-id="8c102-128">**元件類別**</span><span class="sxs-lookup"><span data-stu-id="8c102-128">**Component Categories**</span></span>  
<span data-ttu-id="8c102-129">**磁碟機**</span><span class="sxs-lookup"><span data-stu-id="8c102-129">**Drive**</span></span>  
<span data-ttu-id="8c102-130">**磁片磁碟機 \\ shellex**</span><span class="sxs-lookup"><span data-stu-id="8c102-130">**Drive\\shellex**</span></span>  
<span data-ttu-id="8c102-131">**磁片磁碟機 \\ shellex \\ CoNtextMenuHandlers**</span><span class="sxs-lookup"><span data-stu-id="8c102-131">**Drive\\shellex\\ContextMenuHandlers**</span></span>  
<span data-ttu-id="8c102-132">**磁片磁碟機 \\ shellex \\ PropertySheetHandlers**</span><span class="sxs-lookup"><span data-stu-id="8c102-132">**Drive\\shellex\\PropertySheetHandlers**</span></span>  
<span data-ttu-id="8c102-133">**FileType**</span><span class="sxs-lookup"><span data-stu-id="8c102-133">**FileType**</span></span>  
<span data-ttu-id="8c102-134">**資料夾**</span><span class="sxs-lookup"><span data-stu-id="8c102-134">**Folder**</span></span>  
<span data-ttu-id="8c102-135">**資料夾 \\ shellex**</span><span class="sxs-lookup"><span data-stu-id="8c102-135">**Folder\\shellex**</span></span>  
<span data-ttu-id="8c102-136">**資料夾 \\ shellex \\ ColumnHandler**</span><span class="sxs-lookup"><span data-stu-id="8c102-136">**Folder\\shellex\\ColumnHandler**</span></span>  
<span data-ttu-id="8c102-137">**資料夾 \\ shellex \\ CoNtextMenuHandlers**</span><span class="sxs-lookup"><span data-stu-id="8c102-137">**Folder\\shellex\\ContextMenuHandlers**</span></span>  
<span data-ttu-id="8c102-138">**資料夾 \\ shellex \\ ExtShellFolderViews**</span><span class="sxs-lookup"><span data-stu-id="8c102-138">**Folder\\shellex\\ExtShellFolderViews**</span></span>  
<span data-ttu-id="8c102-139">**資料夾 \\ shellex \\ PropertySheetHandlers**</span><span class="sxs-lookup"><span data-stu-id="8c102-139">**Folder\\shellex\\PropertySheetHandlers**</span></span>  
<span data-ttu-id="8c102-140">**安裝程式 \\ 元件**</span><span class="sxs-lookup"><span data-stu-id="8c102-140">**Installer\\Components**</span></span>  
<span data-ttu-id="8c102-141">**安裝程式 \\ 功能**</span><span class="sxs-lookup"><span data-stu-id="8c102-141">**Installer\\Features**</span></span>  
<span data-ttu-id="8c102-142">**安裝程式 \\ 產品**</span><span class="sxs-lookup"><span data-stu-id="8c102-142">**Installer\\Products**</span></span>  
<span data-ttu-id="8c102-143">**介面**</span><span class="sxs-lookup"><span data-stu-id="8c102-143">**Interface**</span></span>  
<span data-ttu-id="8c102-144">**Mime**</span><span class="sxs-lookup"><span data-stu-id="8c102-144">**Mime**</span></span>  
<span data-ttu-id="8c102-145">**Mime \\ 資料庫**</span><span class="sxs-lookup"><span data-stu-id="8c102-145">**Mime\\Database**</span></span>  
<span data-ttu-id="8c102-146">**Mime \\ 資料庫 \\ 字元集**</span><span class="sxs-lookup"><span data-stu-id="8c102-146">**Mime\\Database\\Charset**</span></span>  
<span data-ttu-id="8c102-147">**Mime \\ 資料庫 \\ 字碼頁**</span><span class="sxs-lookup"><span data-stu-id="8c102-147">**Mime\\Database\\Codepage**</span></span>  
<span data-ttu-id="8c102-148">**Mime \\ 資料庫 \\ 內容類型**</span><span class="sxs-lookup"><span data-stu-id="8c102-148">**Mime\\Database\\Content Type**</span></span>  
<span data-ttu-id="8c102-149">**類型**</span><span class="sxs-lookup"><span data-stu-id="8c102-149">**Typelib**</span></span>  


 

 
