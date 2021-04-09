---
title: 轉散發 Windows Media Player 11
description: 轉散發 Windows Media Player 11
ms.assetid: 3348821f-6d72-40c2-954b-0046ce502401
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674da0298196f0749a549670bf9bd7c4095b6e7a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021222"
---
# <a name="redistributing-windows-media-player-11"></a><span data-ttu-id="3b671-103">轉散發 Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="3b671-103">Redistributing Windows Media Player 11</span></span>

<span data-ttu-id="3b671-104">您可以使用下列其中一個安裝程式，在 Windows XP 上安裝 Windows Media Player 11，其中 *localeId* 是地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="3b671-104">You can install Windows Media Player 11 on Windows XP by using one of the following setup programs, where *localeId* is a locale identifier.</span></span>

-   <span data-ttu-id="3b671-105">wmp11-windowsxp-x86-*localeId*.exe</span><span class="sxs-lookup"><span data-stu-id="3b671-105">wmp11-windowsxp-x86-*localeId*.exe</span></span>
-   <span data-ttu-id="3b671-106">wmp11-windowsxp-x64-*localeId*</span><span class="sxs-lookup"><span data-stu-id="3b671-106">wmp11-windowsxp-x64-*localeId*.exe</span></span>

<span data-ttu-id="3b671-107">以下是安裝時不含 UI 的命令列範例，且不會重新開機或重新開機提示。</span><span class="sxs-lookup"><span data-stu-id="3b671-107">Here is an example of a command line for installation with no UI and no restart or restart prompt.</span></span>


```
wmp11-windowsxp-x86-enu.exe /q:A /c:"setup_wm.exe /Q /R:N"
```



<span data-ttu-id="3b671-108">下表顯示您可以搭配 Windows Media Player 11 安裝程式使用的其他參數。</span><span class="sxs-lookup"><span data-stu-id="3b671-108">The following table shows additional parameters that you can use with the Windows Media Player 11 setup program.</span></span>



| <span data-ttu-id="3b671-109">參數</span><span class="sxs-lookup"><span data-stu-id="3b671-109">Parameter</span></span>              | <span data-ttu-id="3b671-110">Description</span><span class="sxs-lookup"><span data-stu-id="3b671-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b671-111">/NoMigrate</span><span class="sxs-lookup"><span data-stu-id="3b671-111">/NoMigrate</span></span>             | <span data-ttu-id="3b671-112">防止程式庫遷移。</span><span class="sxs-lookup"><span data-stu-id="3b671-112">Prevent library migration.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="3b671-113">/NestedRestore</span><span class="sxs-lookup"><span data-stu-id="3b671-113">/NestedRestore</span></span>         | <span data-ttu-id="3b671-114">建立嵌套的系統還原點。</span><span class="sxs-lookup"><span data-stu-id="3b671-114">Create a nested system restore point.</span></span> <span data-ttu-id="3b671-115">如果您的應用程式會建立系統還原點，以將 Windows Media Player 還原點嵌入應用程式還原點內，請使用此程式。</span><span class="sxs-lookup"><span data-stu-id="3b671-115">Use this if your application creates a system restore point to nest the Windows Media Player restore point within your application restore point.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="3b671-116">/DisallowSystemRestore</span><span class="sxs-lookup"><span data-stu-id="3b671-116">/DisallowSystemRestore</span></span> | <span data-ttu-id="3b671-117">不允許建立系統還原點。</span><span class="sxs-lookup"><span data-stu-id="3b671-117">Disallow the creation of a system restore point.</span></span> <span data-ttu-id="3b671-118">此旗標將會停用建立系統還原點。</span><span class="sxs-lookup"><span data-stu-id="3b671-118">This flag will disable the creation of a system restore point.</span></span> <span data-ttu-id="3b671-119">在大部分情況下，此旗標不應用於一般軟體轉散發。</span><span class="sxs-lookup"><span data-stu-id="3b671-119">Under most circumstances this flag should not be used for general software redistribution.</span></span> <span data-ttu-id="3b671-120">只有當您可以代表使用者明確選擇不支援將 Windows Media Player 檔案復原至舊版播放程式時，才應該使用此選項。</span><span class="sxs-lookup"><span data-stu-id="3b671-120">This should be used only when you can make an explicit choice on behalf of the end user not to support the rollback of the Windows Media Player files to an earlier version of the Player.</span></span> <span data-ttu-id="3b671-121">此旗標只能用於公司部署或原始設備製造商 (OEM) 安裝。</span><span class="sxs-lookup"><span data-stu-id="3b671-121">This flag should be used only for corporate deployment or original equipment manufacturer (OEM) installation.</span></span> |
| <span data-ttu-id="3b671-122">/DefaultService</span><span class="sxs-lookup"><span data-stu-id="3b671-122">/DefaultService</span></span>        | <span data-ttu-id="3b671-123">設定初始的線上商店。</span><span class="sxs-lookup"><span data-stu-id="3b671-123">Set the initial online store.</span></span> <span data-ttu-id="3b671-124">如需詳細資訊，請參閱 [安裝線上商店的命令列參數](setup-command-line-parameters-for-online-stores.md)。</span><span class="sxs-lookup"><span data-stu-id="3b671-124">For more information, see [Setup Command-line Parameters for Online Stores](setup-command-line-parameters-for-online-stores.md).</span></span>                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="3b671-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="3b671-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b671-126">**轉散發 Windows Media Player 軟體**</span><span class="sxs-lookup"><span data-stu-id="3b671-126">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




