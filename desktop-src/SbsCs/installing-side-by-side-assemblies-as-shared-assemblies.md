---
description: 下列程式描述如何安裝並存元件作為共用元件。
ms.assetid: 272ad1b8-9ea2-4af8-ba0d-c59f4db027e6
title: 將並存元件安裝為共用元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b4e796fb371a299f508945371fea926c5d56a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468908"
---
# <a name="installing-side-by-side-assemblies-as-shared-assemblies"></a><span data-ttu-id="d96f8-103">將並存元件安裝為共用元件</span><span class="sxs-lookup"><span data-stu-id="d96f8-103">Installing Side-by-side Assemblies as Shared Assemblies</span></span>

<span data-ttu-id="d96f8-104">下列程式描述如何安裝 [並存元件](about-side-by-side-assemblies-.md) 作為 [共用元件](/windows/desktop/Msi/shared-assemblies)。</span><span class="sxs-lookup"><span data-stu-id="d96f8-104">The following procedure describes how to install [side-by-side assemblies](about-side-by-side-assemblies-.md) as [shared assemblies](/windows/desktop/Msi/shared-assemblies).</span></span>

<span data-ttu-id="d96f8-105">**安裝並存元件作為共用元件**</span><span class="sxs-lookup"><span data-stu-id="d96f8-105">**To install a side-by-side assembly as a shared assembly**</span></span>

1.  <span data-ttu-id="d96f8-106">簽署並建立元件中檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="d96f8-106">Sign and create a catalog for the files in the assembly.</span></span>

    <span data-ttu-id="d96f8-107">檔案必須經過簽署，才能以並存元件的形式安裝檔案。</span><span class="sxs-lookup"><span data-stu-id="d96f8-107">Files must be signed to install them as side-by-side assemblies.</span></span> <span data-ttu-id="d96f8-108">如需詳細資訊，請參閱 [建立簽署的檔案和目錄](creating-signed-files-and-catalogs.md)。</span><span class="sxs-lookup"><span data-stu-id="d96f8-108">For more information, see [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).</span></span>

2.  <span data-ttu-id="d96f8-109">您應將共用並存元件安裝為 Windows Installer 套件的元件。</span><span class="sxs-lookup"><span data-stu-id="d96f8-109">You should install shared side-by-side assemblies as components of a Windows Installer package.</span></span> <span data-ttu-id="d96f8-110">這可以是用來安裝或更新應用程式的相同安裝套件。</span><span class="sxs-lookup"><span data-stu-id="d96f8-110">This can be the same installation package used to install or update your application.</span></span> <span data-ttu-id="d96f8-111">如果共用的元件隨附為多個應用程式的一部分，您應該提供合併模組，該模組可以併入這些應用程式的安裝套件，並為元件中的檔案建立目錄。</span><span class="sxs-lookup"><span data-stu-id="d96f8-111">If the shared assembly is shipped as part of multiple applications, you should provide a merge module that can be incorporated into these applications' installation packages and create a catalog for the files in the assembly.</span></span>

    <span data-ttu-id="d96f8-112">安裝元件需要 Windows Installer 2.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="d96f8-112">Windows Installer version 2.0 or later is required to install assemblies.</span></span> <span data-ttu-id="d96f8-113">如需詳細資訊，請參閱 [Windows Installer](../msi/windows-installer-portal.md) SDK 和 [Win32 元件安裝](../msi/installation-of-win32-assemblies.md)中的章節。</span><span class="sxs-lookup"><span data-stu-id="d96f8-113">For more information, see the [Windows Installer](../msi/windows-installer-portal.md) SDK and the sections under [Installation of Win32 Assemblies](../msi/installation-of-win32-assemblies.md).</span></span>

 

 
