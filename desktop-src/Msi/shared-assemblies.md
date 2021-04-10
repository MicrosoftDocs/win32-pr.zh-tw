---
description: Win32 元件可以安裝為共用的元件，並且可供電腦上的多個應用程式使用。 共用的元件應該由用來安裝或更新應用程式的 Windows Installer 套件進行安裝。
ms.assetid: d408b0a9-8dc5-4cd0-93b3-429de7d12b17
title: 共用組件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e99d805614c05838abe9f5c869fc9c072b1fa8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693848"
---
# <a name="shared-assemblies"></a><span data-ttu-id="6a27e-104">共用組件</span><span class="sxs-lookup"><span data-stu-id="6a27e-104">Shared Assemblies</span></span>

<span data-ttu-id="6a27e-105">Win32 元件可以安裝為共用的元件，並且可供電腦上的多個應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="6a27e-105">A Win32 assembly can be installed as a shared assembly and be available for use by multiple applications on the computer.</span></span> <span data-ttu-id="6a27e-106">共用的元件應該由用來安裝或更新應用程式的 Windows Installer 套件進行安裝。</span><span class="sxs-lookup"><span data-stu-id="6a27e-106">Shared assemblies should be installed by a Windows Installer package used to install or update an application.</span></span>

<span data-ttu-id="6a27e-107">共用的元件會以 [並存元件](side-by-side-assemblies.md)的形式安裝。</span><span class="sxs-lookup"><span data-stu-id="6a27e-107">Shared assemblies are installed as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="6a27e-108">Windows Installer 會將共用的並存元件安裝到 Winsxs 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="6a27e-108">The Windows Installer installs shared side-by-side assemblies into the Winsxs folder.</span></span> <span data-ttu-id="6a27e-109">元件不會在系統上全域註冊，但是在資訊清單檔中指定元件相依性的任何應用程式都可以全域使用這些元件。</span><span class="sxs-lookup"><span data-stu-id="6a27e-109">The assemblies are not registered globally on the system, but they are globally available to any application that specifies a dependency on the assembly in a manifest file.</span></span> <span data-ttu-id="6a27e-110">如需詳細資訊，請參閱 [隔離的應用程式和並存元件](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)。</span><span class="sxs-lookup"><span data-stu-id="6a27e-110">For more information, see [Isolated Applications and Side-by-side Assemblies](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span></span>

<span data-ttu-id="6a27e-111">在 Windows XP 之前的作業系統上，共用的元件通常會安裝在 Windows system 資料夾中，並在全域註冊。</span><span class="sxs-lookup"><span data-stu-id="6a27e-111">On operating systems earlier than Windows XP, shared assemblies are usually installed in the Windows system folder and registered globally.</span></span> <span data-ttu-id="6a27e-112">已安裝的最新版本可供任何系結至該版本的應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="6a27e-112">The latest installed version is available to any application that binds to it.</span></span>

<span data-ttu-id="6a27e-113">如需如何撰寫 Windows Installer 套件以安裝共用元件的詳細資訊，請參閱下列內容：</span><span class="sxs-lookup"><span data-stu-id="6a27e-113">For information on how to author a Windows Installer package to install a shared assembly, see the following:</span></span>

-   [<span data-ttu-id="6a27e-114">在 Windows XP 上安裝適用于並存共用的 Win32 元件</span><span class="sxs-lookup"><span data-stu-id="6a27e-114">Installing Win32 Assemblies for Side-by-Side Sharing on Windows XP</span></span>](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [<span data-ttu-id="6a27e-115">在 Windows XP 上安裝 Win32 元件以私用應用程式</span><span class="sxs-lookup"><span data-stu-id="6a27e-115">Installing Win32 Assemblies for the Private Use of an Application on Windows XP</span></span>](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 
