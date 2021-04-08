---
title: 轉散發 Windows Media Player 10
description: 轉散發 Windows Media Player 10
ms.assetid: 58d601d4-e3d4-4a29-969c-799b2819f92c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4515317e0a6714d53c147671bbb83c06c172ef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671472"
---
# <a name="redistributing-windows-media-player-10"></a><span data-ttu-id="265cf-103">轉散發 Windows Media Player 10</span><span class="sxs-lookup"><span data-stu-id="265cf-103">Redistributing Windows Media Player 10</span></span>

<span data-ttu-id="265cf-104">您可以使用下列安裝程式，在 Windows XP 上安裝 Windows Media Player 10。</span><span class="sxs-lookup"><span data-stu-id="265cf-104">You can install Windows Media Player 10 on Windows XP by using the following setup program.</span></span>

-   <span data-ttu-id="265cf-105">MP10Setup.exe</span><span class="sxs-lookup"><span data-stu-id="265cf-105">MP10Setup.exe</span></span>

<span data-ttu-id="265cf-106">以下是安裝時不含 UI 的命令列範例，且不會重新開機或重新開機提示。</span><span class="sxs-lookup"><span data-stu-id="265cf-106">Here is an example of a command line for installation with no UI and no restart or restart prompt.</span></span>


```
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N"
```



<span data-ttu-id="265cf-107">下表顯示您可以搭配 Windows Media Player 10 安裝程式使用的其他參數。</span><span class="sxs-lookup"><span data-stu-id="265cf-107">The following table shows additional parameters that you can use with the Windows Media Player 10 setup program.</span></span>



| <span data-ttu-id="265cf-108">參數</span><span class="sxs-lookup"><span data-stu-id="265cf-108">Parameter</span></span>              | <span data-ttu-id="265cf-109">Description</span><span class="sxs-lookup"><span data-stu-id="265cf-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="265cf-110">/NoMigrate</span><span class="sxs-lookup"><span data-stu-id="265cf-110">/NoMigrate</span></span>             | <span data-ttu-id="265cf-111">防止程式庫遷移。</span><span class="sxs-lookup"><span data-stu-id="265cf-111">Prevent library migration.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="265cf-112">/NestedRestore</span><span class="sxs-lookup"><span data-stu-id="265cf-112">/NestedRestore</span></span>         | <span data-ttu-id="265cf-113">建立嵌套的系統還原點。</span><span class="sxs-lookup"><span data-stu-id="265cf-113">Create a nested system restore point.</span></span> <span data-ttu-id="265cf-114">如果您的應用程式會建立系統還原點，以將 Windows Media Player 還原點嵌入應用程式還原點內，請使用此程式。</span><span class="sxs-lookup"><span data-stu-id="265cf-114">Use this if your application creates a system restore point to nest the Windows Media Player restore point within your application restore point.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="265cf-115">/DisallowSystemRestore</span><span class="sxs-lookup"><span data-stu-id="265cf-115">/DisallowSystemRestore</span></span> | <span data-ttu-id="265cf-116">不允許建立系統還原點。</span><span class="sxs-lookup"><span data-stu-id="265cf-116">Disallow the creation of a system restore point.</span></span> <span data-ttu-id="265cf-117">此旗標將會停用建立系統還原點。</span><span class="sxs-lookup"><span data-stu-id="265cf-117">This flag will disable the creation of a system restore point.</span></span> <span data-ttu-id="265cf-118">在大部分情況下，此旗標不應用於一般軟體轉散發。</span><span class="sxs-lookup"><span data-stu-id="265cf-118">Under most circumstances this flag should not be used for general software redistribution.</span></span> <span data-ttu-id="265cf-119">只有當您可以代表使用者明確選擇不支援將 Windows Media Player 檔案復原至舊版播放程式時，才應該使用此選項。</span><span class="sxs-lookup"><span data-stu-id="265cf-119">This should be used only when you can make an explicit choice on behalf of the end user not to support the rollback of the Windows Media Player files to an earlier version of the Player.</span></span> <span data-ttu-id="265cf-120">此旗標只能用於公司部署或原始設備製造商 (OEM) 安裝。</span><span class="sxs-lookup"><span data-stu-id="265cf-120">This flag should be used only for corporate deployment or original equipment manufacturer (OEM) installation.</span></span> |
| <span data-ttu-id="265cf-121">/DefaultService</span><span class="sxs-lookup"><span data-stu-id="265cf-121">/DefaultService</span></span>        | <span data-ttu-id="265cf-122">設定初始的線上商店。</span><span class="sxs-lookup"><span data-stu-id="265cf-122">Set the initial online store.</span></span> <span data-ttu-id="265cf-123">如需詳細資訊，請參閱 [安裝線上商店的命令列參數](setup-command-line-parameters-for-online-stores.md)。</span><span class="sxs-lookup"><span data-stu-id="265cf-123">For more information, see [Setup Command-line Parameters for Online Stores](setup-command-line-parameters-for-online-stores.md).</span></span>                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="265cf-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="265cf-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="265cf-125">**轉散發 Windows Media Player 軟體**</span><span class="sxs-lookup"><span data-stu-id="265cf-125">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> <dt>

[<span data-ttu-id="265cf-126">**ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="265cf-126">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 




