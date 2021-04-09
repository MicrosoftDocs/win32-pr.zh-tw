---
description: 主要升級可以套用至應用程式，方法是從命令列或使用可執行檔來修補應用程式的本機安裝。
ms.assetid: be651457-5c66-478b-89d5-3d7607702b8e
title: 藉由修補產品的本機安裝來套用主要升級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043d106ed9f8d6455ab4412959b70854a526a4e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848973"
---
# <a name="applying-major-upgrades-by-patching-the-local-installation-of-the-product"></a><span data-ttu-id="5ace0-103">藉由修補產品的本機安裝來套用主要升級</span><span class="sxs-lookup"><span data-stu-id="5ace0-103">Applying Major Upgrades by Patching the Local Installation of the Product</span></span>

<span data-ttu-id="5ace0-104">主要升級可以套用至應用程式，方法是從命令列或使用可執行檔來修補應用程式的本機安裝。</span><span class="sxs-lookup"><span data-stu-id="5ace0-104">A major upgrade can be applied to an application by patching the local installation of the application from the command line or by using an executable.</span></span>

> [!Note]  
> <span data-ttu-id="5ace0-105">不建議將主要升級提供為修補程式套件，因為主要升級修補程式套件無法與其他更新一起排序，且修補程式不是 [可卸載修補](uninstallable-patches.md)程式。</span><span class="sxs-lookup"><span data-stu-id="5ace0-105">Providing a major upgrade as a patch package is not recommended because a major upgrade patch package cannot be sequenced with other updates and because the patch is not an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="5ace0-106">[Msimsp.exe](msimsp-exe.md)公用程式無法用來產生套用主要升級的修補程式套件。</span><span class="sxs-lookup"><span data-stu-id="5ace0-106">The [Msimsp.exe](msimsp-exe.md) utility cannot be used to generate a patch package that applies a major upgrade.</span></span> <span data-ttu-id="5ace0-107">相反地，請依照 [安裝產品的主要升級](applying-major-upgrades-by-installing-the-product.md)所述，套用主要升級。</span><span class="sxs-lookup"><span data-stu-id="5ace0-107">Instead, apply major upgrades as described in [Applying Major Upgrades by Installing the Product](applying-major-upgrades-by-installing-the-product.md).</span></span>

 

<span data-ttu-id="5ace0-108">**將主要升級修補程式套用至產品的本機安裝**</span><span class="sxs-lookup"><span data-stu-id="5ace0-108">**To apply a major upgrade patch to a local installation of the product**</span></span>

1.  <span data-ttu-id="5ace0-109">從命令列或使用可執行檔啟動修補程式的安裝。</span><span class="sxs-lookup"><span data-stu-id="5ace0-109">Launch the installation of the patch from the command line or by using an executable.</span></span> <span data-ttu-id="5ace0-110">若要從命令列啟動，請使用 msiexec/p patch .msp。</span><span class="sxs-lookup"><span data-stu-id="5ace0-110">To launch from the command line, use msiexec /p patch.msp.</span></span> <span data-ttu-id="5ace0-111">若要從可執行檔啟動，請呼叫 [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) 或 [**ApplyPatch 方法**](installer-applypatch.md) ，並提供相同的命令列引數。</span><span class="sxs-lookup"><span data-stu-id="5ace0-111">To launch from an executable, call [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or the [**ApplyPatch Method**](installer-applypatch.md) and provide the same command line arguments.</span></span>
2.  <span data-ttu-id="5ace0-112">修補用戶端安裝時，安裝程式會忽略安裝來源，並繼續修補使用者電腦上已安裝的檔案。</span><span class="sxs-lookup"><span data-stu-id="5ace0-112">When patching a client installation, the installer ignores the installation source and proceeds to patch the files that are already installed on the user's computer.</span></span>
3.  <span data-ttu-id="5ace0-113">安裝程式會將標示為執行來源的任何已修補元件，變更為在本機執行。</span><span class="sxs-lookup"><span data-stu-id="5ace0-113">The installer changes any patched components marked as run-from-source to run-locally.</span></span> <span data-ttu-id="5ace0-114">只要修補程式保留在電腦上，使用者就無法從來源執行這些元件。</span><span class="sxs-lookup"><span data-stu-id="5ace0-114">Users are unable to run these components from the source as long as the patch remains on the computer.</span></span>
4.  <span data-ttu-id="5ace0-115">安裝程式會新增任何用來更新 .msi 檔案的轉換，或將修補程式特定的資訊新增至使用者的設定檔。</span><span class="sxs-lookup"><span data-stu-id="5ace0-115">The installer adds any transforms used to update the .msi file or adds patch-specific information to the user's profile.</span></span>
5.  <span data-ttu-id="5ace0-116">安裝程式會將 .msi 檔案快取在使用者的電腦上，讓它可以執行隨選安裝、重新安裝及修復應用程式。</span><span class="sxs-lookup"><span data-stu-id="5ace0-116">The installer caches the .msi file on the user's computer so that it can perform installation-on-demand, reinstall, and repair of the application.</span></span> <span data-ttu-id="5ace0-117">將修補程式套用至獨立安裝之後，安裝程式會參考兩個或多個來源清單至外部檔案：一個適用于原始來源，另一個則用於已套用的每個修補程式。</span><span class="sxs-lookup"><span data-stu-id="5ace0-117">After a patch is applied to a stand alone installation, the installer references two or more source lists to external files: one for the original source and one for each patch that has been applied.</span></span>

 

 



