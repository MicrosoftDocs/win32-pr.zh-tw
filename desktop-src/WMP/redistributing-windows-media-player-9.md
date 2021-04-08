---
title: 轉散發 Windows Media Player 9 系列
description: 轉散發 Windows Media Player 9 系列
ms.assetid: 812e3fc7-e23d-489c-a486-62c7602cf46e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f48da20123255ae08a0993d361a95deb8ed335
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021991"
---
# <a name="redistributing-windows-media-player-9-series"></a><span data-ttu-id="11800-103">轉散發 Windows Media Player 9 系列</span><span class="sxs-lookup"><span data-stu-id="11800-103">Redistributing Windows Media Player 9 Series</span></span>

<span data-ttu-id="11800-104">您可以使用下列其中一個安裝程式，在 Windows XP 上安裝 Windows Media Player 9 系列。</span><span class="sxs-lookup"><span data-stu-id="11800-104">You can install Windows Media Player 9 Series on Windows XP by using one of the following setup programs.</span></span>

-   <span data-ttu-id="11800-105">MPSetupXP.exe</span><span class="sxs-lookup"><span data-stu-id="11800-105">MPSetupXP.exe</span></span>
-   <span data-ttu-id="11800-106">MPSetup.exe</span><span class="sxs-lookup"><span data-stu-id="11800-106">MPSetup.exe</span></span>

> [!Note]  
> <span data-ttu-id="11800-107">MPSetup.exe 是 MPSetupXP.exe 安裝程式的超集合。</span><span class="sxs-lookup"><span data-stu-id="11800-107">MPSetup.exe is a superset of the MPSetupXP.exe setup program.</span></span> <span data-ttu-id="11800-108">它包含 Windows XP 之前發行的作業系統所需的檔案。</span><span class="sxs-lookup"><span data-stu-id="11800-108">It contains files that are needed by operating systems released before Windows XP.</span></span> <span data-ttu-id="11800-109">在 Windows XP 上執行時，MPSetup.exe 的功能相當於 MPSetupXP.exe，但安裝程式檔案大小卻較大，因為它尚未針對安裝在 Windows XP 作業系統上進行優化。</span><span class="sxs-lookup"><span data-stu-id="11800-109">MPSetup.exe is functionally equivalent to MPSetupXP.exe when run on Windows XP, but the setup program file size is larger because it has not been optimized for installation on Windows XP operating systems.</span></span>

 

<span data-ttu-id="11800-110">您可以使用下列安裝程式，在 Windows 98 Second Edition、Windows Millennium Edition 或 Windows 2000 上安裝 Windows Media Player 9 系列。</span><span class="sxs-lookup"><span data-stu-id="11800-110">You can install Windows Media Player 9 Series on Windows 98 Second Edition, Windows Millennium Edition or Windows 2000 by using the following setup program.</span></span>

-   <span data-ttu-id="11800-111">MPSetup.exe</span><span class="sxs-lookup"><span data-stu-id="11800-111">MPSetup.exe</span></span>

<span data-ttu-id="11800-112">以下是安裝時不含 UI 的命令列範例，且不會重新開機或重新開機提示。</span><span class="sxs-lookup"><span data-stu-id="11800-112">Here is an example of a command line for installation with no UI and no restart or restart prompt.</span></span>


```
MPSetup.exe /q:A /c:"setup_wm.exe /Q /R:N /P:#e"
```



> [!Note]  
> <span data-ttu-id="11800-113">/P： \# e 參數會指定在 Windows Media Player 安裝期間應該快取 Windows Media Player 安裝套件。</span><span class="sxs-lookup"><span data-stu-id="11800-113">The /P:\#e parameter specifies that the Windows Media Player installation package should be cached during Windows Media Player setup.</span></span> <span data-ttu-id="11800-114">此命令可用來處理未來的作業系統升級。</span><span class="sxs-lookup"><span data-stu-id="11800-114">This command is used to handle future upgrades of the operating system.</span></span> <span data-ttu-id="11800-115">只有公司 IT 系統管理員才能省略這個命令。</span><span class="sxs-lookup"><span data-stu-id="11800-115">This command should be omitted only by corporate IT administrators.</span></span> <span data-ttu-id="11800-116">在 \# 命令列中不應包含/p： e 的唯一情況是當您擁有目標系統，並知道目標系統永遠不會升級至較新的作業系統時。</span><span class="sxs-lookup"><span data-stu-id="11800-116">The only case where /P:\#e should not be included on the command line is when you own the target system and know that the target system will never be upgraded to a later operating system.</span></span> <span data-ttu-id="11800-117">例如，如果您要在 Windows 2000 上安裝 Windows Media Player 9 系列，而且電腦可能會在未來升級為 Windows XP，則必須 \# 在命令列上使用/p： e。</span><span class="sxs-lookup"><span data-stu-id="11800-117">For example, if you are installing Windows Media Player 9 Series on Windows 2000 and the computer may someday be upgraded to Windows XP, you must use /P:\#e on the command line.</span></span> <span data-ttu-id="11800-118">否則，在 Windows XP 安裝之後，將會以 Windows XP 的 Windows Media Player 檔案覆寫 Windows Media Player 的檔案。</span><span class="sxs-lookup"><span data-stu-id="11800-118">Otherwise, after the Windows XP installation, the Windows Media Player files will be overwritten with the files for Windows Media Player for Windows XP.</span></span>

 

<span data-ttu-id="11800-119">下表顯示您可以搭配 Windows Media Player 9 系列安裝程式使用的其他參數。</span><span class="sxs-lookup"><span data-stu-id="11800-119">The following table shows additional parameters that you can use with the Windows Media Player 9 Series setup program.</span></span>



| <span data-ttu-id="11800-120">參數</span><span class="sxs-lookup"><span data-stu-id="11800-120">Parameter</span></span>              | <span data-ttu-id="11800-121">Description</span><span class="sxs-lookup"><span data-stu-id="11800-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11800-122">/NoMigrate</span><span class="sxs-lookup"><span data-stu-id="11800-122">/NoMigrate</span></span>             | <span data-ttu-id="11800-123">防止程式庫遷移。</span><span class="sxs-lookup"><span data-stu-id="11800-123">Prevent library migration.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="11800-124">/NestedRestore</span><span class="sxs-lookup"><span data-stu-id="11800-124">/NestedRestore</span></span>         | <span data-ttu-id="11800-125">建立嵌套的系統還原點。</span><span class="sxs-lookup"><span data-stu-id="11800-125">Create a nested system restore point.</span></span> <span data-ttu-id="11800-126">如果您的應用程式會建立系統還原點，以將 Windows Media Player 還原點嵌入應用程式還原點內，請使用此程式。</span><span class="sxs-lookup"><span data-stu-id="11800-126">Use this if your application creates a system restore point to nest the Windows Media Player restore point within your application restore point.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="11800-127">/DisallowSystemRestore</span><span class="sxs-lookup"><span data-stu-id="11800-127">/DisallowSystemRestore</span></span> | <span data-ttu-id="11800-128">不允許建立系統還原點。</span><span class="sxs-lookup"><span data-stu-id="11800-128">Disallow the creation of a system restore point.</span></span> <span data-ttu-id="11800-129">此旗標將會停用建立系統還原點。</span><span class="sxs-lookup"><span data-stu-id="11800-129">This flag will disable the creation of a system restore point.</span></span> <span data-ttu-id="11800-130">在大部分情況下，此旗標不應用於一般軟體轉散發。</span><span class="sxs-lookup"><span data-stu-id="11800-130">Under most circumstances this flag should not be used for general software redistribution.</span></span> <span data-ttu-id="11800-131">只有當您可以代表使用者明確選擇不支援將 Windows Media Player 檔案復原至舊版播放程式時，才應該使用此選項。</span><span class="sxs-lookup"><span data-stu-id="11800-131">This should be used only when you can make an explicit choice on behalf of the end user not to support the rollback of the Windows Media Player files to an earlier version of the Player.</span></span> <span data-ttu-id="11800-132">此旗標只能用於公司部署或原始設備製造商 (OEM) 安裝。</span><span class="sxs-lookup"><span data-stu-id="11800-132">This flag should be used only for corporate deployment or original equipment manufacturer (OEM) installation.</span></span> |



 

## <a name="notes"></a><span data-ttu-id="11800-133">備註</span><span class="sxs-lookup"><span data-stu-id="11800-133">Notes</span></span>

-   <span data-ttu-id="11800-134">命令列參數會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="11800-134">The command-line parameters are case-sensitive.</span></span>
-   <span data-ttu-id="11800-135">當您隱藏重新開機提示時，必須檢查 InstallResult 登錄機碼，並處理呼叫安裝程式中的重新開機通知。</span><span class="sxs-lookup"><span data-stu-id="11800-135">When suppressing the restart prompt, you must check the InstallResult registry key and handle restart notification in the calling setup application.</span></span>
-   <span data-ttu-id="11800-136">Windows Media Player 9 系列也會安裝 Windows Media 格式執行時間，因此不需要在相同的軟體轉散發套件中同時包含 Windows Media Player 散發套件和 Windows Media Format runtime 散發套件。</span><span class="sxs-lookup"><span data-stu-id="11800-136">Windows Media Player 9 Series also installs the Windows Media Format runtime, so there is no need to include both the Windows Media Player distribution package and the Windows Media Format runtime distribution package in the same software redistribution package.</span></span> <span data-ttu-id="11800-137">因此，如果您在安裝中包含 MPSetup.exe 或 MPSetupXP.exe，就不需要包含 WMFdist.exe。</span><span class="sxs-lookup"><span data-stu-id="11800-137">Therefore, if you include MPSetup.exe or MPSetupXP.exe in your installation, you do not need to include WMFdist.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11800-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="11800-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11800-139">**轉散發 Windows Media Player 軟體**</span><span class="sxs-lookup"><span data-stu-id="11800-139">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




