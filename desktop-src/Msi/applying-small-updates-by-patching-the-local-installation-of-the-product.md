---
description: 您可以藉由修補應用程式的本機安裝，將小型更新套用至應用程式。
ms.assetid: 2a04ffd0-d5b6-44f3-bef2-73f59179aed1
title: 藉由修補產品的本機安裝來套用小型更新
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bced3e7f69761ff3e270046718eedb9032cab8a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944029"
---
# <a name="applying-small-updates-by-patching-the-local-installation-of-the-product"></a><span data-ttu-id="36633-103">藉由修補產品的本機安裝來套用小型更新</span><span class="sxs-lookup"><span data-stu-id="36633-103">Applying Small Updates by Patching the Local Installation of the Product</span></span>

<span data-ttu-id="36633-104">您可以藉由修補應用程式的本機安裝，將小型更新套用至應用程式。</span><span class="sxs-lookup"><span data-stu-id="36633-104">A small update can be applied to an application by patching the local installation of the application.</span></span>

<span data-ttu-id="36633-105">**將小型更新修補程式套用至產品的本機安裝**</span><span class="sxs-lookup"><span data-stu-id="36633-105">**To apply a small update patch to a local installation of the product**</span></span>

1.  <span data-ttu-id="36633-106">從命令列或使用可執行檔啟動修補程式的安裝。</span><span class="sxs-lookup"><span data-stu-id="36633-106">Launch the installation of the patch from the command line or by using an executable.</span></span> <span data-ttu-id="36633-107">若要從命令列啟動，請使用 **msiexec/p patch。 msp 重新 \[ 安裝 =**_Feature list_ *_\] REINSTALLMODE = omus reinstall_*。</span><span class="sxs-lookup"><span data-stu-id="36633-107">To launch from the command line, use **msiexec /p patch.msp REINSTALL=\[**_Feature list_*_\] REINSTALLMODE=omus_*.</span></span> <span data-ttu-id="36633-108">若要從可執行檔啟動，請呼叫 [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) 或 [**ApplyPatch 方法**](installer-applypatch.md) ，並提供相同的命令列引數。</span><span class="sxs-lookup"><span data-stu-id="36633-108">To launch from an executable, call [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or the [**ApplyPatch Method**](installer-applypatch.md) and provide the same command line arguments.</span></span>
2.  <span data-ttu-id="36633-109">修補用戶端安裝時，安裝程式會忽略安裝來源，並繼續修補使用者電腦上已安裝的檔案。</span><span class="sxs-lookup"><span data-stu-id="36633-109">When patching a client installation, the installer ignores the installation source and proceeds to patch the files that are already installed on the user's computer.</span></span>
3.  <span data-ttu-id="36633-110">安裝程式會將標示為執行來源的任何已修補元件，變更為在本機執行。</span><span class="sxs-lookup"><span data-stu-id="36633-110">The installer changes any patched components marked as run-from-source to run-locally.</span></span> <span data-ttu-id="36633-111">只要修補程式保留在電腦上，使用者就無法從來源執行這些元件。</span><span class="sxs-lookup"><span data-stu-id="36633-111">Users are unable to run these components from the source as long as the patch remains on the computer.</span></span>
4.  <span data-ttu-id="36633-112">安裝程式會新增任何用來更新 .msi 檔案的轉換，或將修補程式特定的資訊新增至使用者的設定檔。</span><span class="sxs-lookup"><span data-stu-id="36633-112">The installer adds any transforms used to update the .msi file or adds patch-specific information to the user's profile.</span></span>
5.  <span data-ttu-id="36633-113">安裝程式會將 .msi 檔案快取在使用者的電腦上，讓它可以執行隨選安裝、重新安裝及修復應用程式。</span><span class="sxs-lookup"><span data-stu-id="36633-113">The installer caches the .msi file on the user's computer so that it can perform installation-on-demand, reinstall, and repair of the application.</span></span> <span data-ttu-id="36633-114">將修補程式套用至獨立安裝之後，安裝程式會參考兩個或多個來源清單至外部檔案：一個適用于原始來源，另一個則用於已套用的每個修補程式。</span><span class="sxs-lookup"><span data-stu-id="36633-114">After a patch is applied to a standalone installation, the installer references two or more source lists to external files: one for the original source and one for each patch that has been applied.</span></span>

 

 



